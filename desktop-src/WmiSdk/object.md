---
description: Der Objekt Datentyp ist ein WMI-Klassenobjekt, das zum Deklarieren von schwach typisierten Zuordnungen und eingebetteten Objekten verwendet wird.
ms.assetid: 1ad99b92-dfd4-4147-abf5-045edceaa97d
ms.tgt_platform: multiple
title: OBJECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c257b45833204a873292da467d484fab97b22b0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749513"
---
# <a name="object"></a>OBJECT

Der Objekt Datentyp ist ein WMI-Klassenobjekt, das zum Deklarieren von schwach typisierten Zuordnungen und eingebetteten Objekten verwendet wird. Die spezifische Klasse für ein schwach typisiertes Objekt wird erst definiert, wenn Sie eine Instanz der Klasse erstellen. Eingebettete Objekte, die mit dem Object-Datentyp definiert sind, können Instanzen einer beliebigen WMI-Klasse enthalten. Weitere Informationen finden Sie unter [eingebettete Objekte](embedded-objects.md).

Im folgenden Beispiel werden Instanzen von zwei Klassen definiert und erstellt, von denen eine ein eingebettetes Objekt vom Typ "Object" enthält:

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

 

 



