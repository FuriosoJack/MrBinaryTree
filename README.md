# MrBinaryTree
Arbol binario para ordenamiento o busqueda de cualquier tipo de dato que sea comparable con > y < | Binary tree to sort or search

# License

  El codigo de licencia debe seguirse al pie de la letra, si usted utiliza esta libreria los derechos de autor deben estar incluidos en todas la copias.
  
  Para mas informacion la puede encontra en el archivo LICENSE.txt.

  
## Installation 

```bash
$ composer require furiosojack/mr-binary-tree
```

OR 

add to your `composer.json`

```json
{
    "require": {
        "furiosojack/mr-binary-tree": "^0.2"
    }
}
```

## Examples

 ```php
$ips = [
          '255.168.0.1',
            '172.6.0.1',
            '172.0.0.1',
            '201.0.0.0'
        ];
$i=0;
$tree = new MrBinaryTree();
foreach ($ips as $address){
            $keyAdress = $i;
            $tree->addNode($keyAdress, $address);
			$i++;
        }
		
$tree->inAsc($tree->getRoot());
//Deprecated
echo $tree->getLisOrderedList();

var_dump($tree->getNodesOrdered());
```

result 
```json
array:4 [▼
  0 => "201.0.0.0"
  1 => "172.0.0.1"
  2 => "172.6.0.1"
  3 => "255.168.0.1"
]
```