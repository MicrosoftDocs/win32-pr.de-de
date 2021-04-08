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
# <a name="object"></a><span data-ttu-id="41341-103">OBJECT</span><span class="sxs-lookup"><span data-stu-id="41341-103">OBJECT</span></span>

<span data-ttu-id="41341-104">Der Objekt Datentyp ist ein WMI-Klassenobjekt, das zum Deklarieren von schwach typisierten Zuordnungen und eingebetteten Objekten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="41341-104">The OBJECT data type is a WMI class object use to declare weakly typed associations and embedded objects.</span></span> <span data-ttu-id="41341-105">Die spezifische Klasse für ein schwach typisiertes Objekt wird erst definiert, wenn Sie eine Instanz der Klasse erstellen.</span><span class="sxs-lookup"><span data-stu-id="41341-105">You do not define the specific class for a weakly typed object until you create an instance of the class.</span></span> <span data-ttu-id="41341-106">Eingebettete Objekte, die mit dem Object-Datentyp definiert sind, können Instanzen einer beliebigen WMI-Klasse enthalten.</span><span class="sxs-lookup"><span data-stu-id="41341-106">Embedded objects defined with the OBJECT data type can contain instances of any WMI class.</span></span> <span data-ttu-id="41341-107">Weitere Informationen finden Sie unter [eingebettete Objekte](embedded-objects.md).</span><span class="sxs-lookup"><span data-stu-id="41341-107">For more information, see [Embedded Objects](embedded-objects.md).</span></span>

<span data-ttu-id="41341-108">Im folgenden Beispiel werden Instanzen von zwei Klassen definiert und erstellt, von denen eine ein eingebettetes Objekt vom Typ "Object" enthält:</span><span class="sxs-lookup"><span data-stu-id="41341-108">The following example defines and creates instances of two classes, one of which contains an embedded object of type OBJECT:</span></span>

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

 

 



