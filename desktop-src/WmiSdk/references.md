---
description: Das MOF-ref-Schlüsselwort beschreibt einen Objekt Pfad und ist einem VT \_ BSTR-Automatisierungstyp zugeordnet.
ms.assetid: 9da25435-4ccc-4251-a4be-37239156e320
ms.tgt_platform: multiple
title: Verweise (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d30722910de761f3d2111a3218cf364f49ccb3c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866587"
---
# <a name="references-wmi"></a>Verweise (WMI)

Das MOF- **ref** -Schlüsselwort beschreibt einen Objekt Pfad und ist einem VT \_ BSTR-Automatisierungstyp zugeordnet. Der Objekt Pfad kann entweder ein vollständiger Pfad zu einem Server und Namespace oder ein relativer Pfad zu einem anderen Objekt im gleichen Namespace sein. Sie können ein **ref** -Schlüsselwort verwenden, um zwei oder mehr Klassen zu verknüpfen. WMI unterstützt zwei Typen von Objekt Pfaden, die verwenden, um allgemeine oder bestimmte Pfade innerhalb von WMI zu definieren.

Der Hauptzweck des **ref** -Schlüssel Worts besteht darin, die Transportzeit und die Codierung zwischen Objekten zu reduzieren, die vollständig im WMI-Repository vorhanden sind. Sie können auch das **ref** -Schlüsselwort verwenden, um eine Zuordnung zwischen zwei Klassen zu erstellen. Weitere Informationen finden Sie unter [Deklarieren einer Association-Klasse](declaring-an-association-class.md). Wenn sich das Element, auf das verwiesen wird, innerhalb derselben MOF-Datei befindet, verwenden Sie einen Alias, um den **ref** -Wert zu initialisieren. Weitere Informationen finden Sie unter [Erstellen eines Alias](creating-an-alias.md).

> [!Note]  
> Wenn ein **ref** -Schlüsselwort auf eine Schlüsseleigenschaft angewendet wird, können Sie Objekt Verweise durch den Objekt Zeichen folgen Wert anstelle des dereferenzierten Werts unterscheiden.

 

MOF unterstützt das Konzept eines schwach typisierten und stark typisierten Objekt Pfads. Ein schwach typisierter Objekt Pfad zeigt auf ein Objekt einer nicht angegebenen Klasse und verwendet das **ref** -Schlüsselwort mit dem [Object](object.md) -Schlüsselwort. Ein stark typisiertes Objekt verweist auf ein Objekt einer bestimmten Klasse und verwendet **ref** mit dem Klassennamen. Das folgende Beispiel beschreibt einen schwach typisierten **reftoanyclass** -Verweis, der auf eine beliebige Klassen-oder Klasseninstanz verweisen kann, sowie einen **reftoclassx** -Verweis, der nur auf eine **ClassX** -Klasse oder-Instanz verweisen kann:

``` syntax
class MyClass
{
    object ref RefToAnyClass;       // Weakly typed
    ClassX ref RefToClassX;         // Strongly typed
};
```

Im folgenden Beispiel werden zwei-Instanzen und ein Association-Objekt beschrieben, das auf die vorherigen-Instanzen verweist:

``` syntax
#pragma namespace("\\\\.\\root")

instance of __Namespace
{
    Name = "WMI" ;
} ;

#pragma namespace("\\\\.\\root\\WMI")

Class A{
    [key] string aKey;
};

Class C{
    [key] string cKey;
};

// The following class creates an association 
// between the "A" class and the "C" class
    [Association] Class B{
    [key] A ref aRef;
    [Key, Min(1)] C ref cRef;
};

instance of a
{
    aKey = "This is the key for the A class";
};

instance of c
{
    cKey = "This is the key for the c class";
};
```

 

 



