---
description: Der OBJECT-Datentyp ist ein WMI-Klassenobjekt, das verwendet wird, um schwach typierte Zuordnungen und eingebettete Objekte zu deklarieren.
ms.assetid: 1ad99b92-dfd4-4147-abf5-045edceaa97d
ms.tgt_platform: multiple
title: OBJECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c26b8b6ff77f788aeed607057541d19d80fea4c105b53d492c1f1e8468b319
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554929"
---
# <a name="object"></a>OBJECT

Der OBJECT-Datentyp ist ein WMI-Klassenobjekt, das verwendet wird, um schwach typierte Zuordnungen und eingebettete Objekte zu deklarieren. Sie definieren die spezifische Klasse für ein schwach typiertes Objekt erst, wenn Sie eine Instanz der -Klasse erstellen. Eingebettete Objekte, die mit dem OBJECT-Datentyp definiert sind, können Instanzen einer beliebigen WMI-Klasse enthalten. Weitere Informationen finden Sie unter [Eingebettete Objekte.](embedded-objects.md)

Im folgenden Beispiel werden Instanzen von zwei Klassen definiert und erstellt, von denen eine ein eingebettetes Objekt vom Typ OBJECT enthält:

``` syntax
#pragma namespace("\\\\.\\root")

instance of __Namespace
{
    Name = "WMI" ;
} ;

#pragma namespace("\\\\.\\root\\WMI")

class CompositeClass
{
    [key] string aKey;   
    object EmbObj;       // Weakly typed
};

class EmbClass

{
  [key] string aKey;
};

instance of CompositeClass
{
    aKey = "CompositeClass Key";
    EmbObj = 
        instance of EmbClass
        {
           aKey = "key for embedded object";
        };
};
```

 

 



