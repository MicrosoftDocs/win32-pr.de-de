---
description: Das MOF-Ref-Schlüsselwort beschreibt einen Objektpfad und wird einem \_ VT-BSTR-Automatisierungstyp zugeordnet.
ms.assetid: 9da25435-4ccc-4251-a4be-37239156e320
ms.tgt_platform: multiple
title: Verweise (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea004a4d0a1cf160d387b07e9c9d7ac85eaaaf21851bd315ecd1bb4ba6f2b49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050458"
---
# <a name="references-wmi"></a>Verweise (WMI)

Das **MOF-Ref-Schlüsselwort** beschreibt einen Objektpfad und wird einem \_ VT-BSTR-Automatisierungstyp zugeordnet. Der Objektpfad kann entweder ein vollständiger Pfad zu einem Server und Namespace oder ein relativer Pfad zu einem anderen Objekt im gleichen Namespace sein. Sie können ein **ref-Schlüsselwort** verwenden, um zwei oder mehr Klassen miteinander zu verknüpfen. WMI unterstützt zwei Typen von Objektpfaden, die verwenden, um allgemeine oder spezifische Pfade innerhalb von WMI zu definieren.

Der Hauptzweck des **Ref-Schlüsselworts** besteht darin, die Transportzeit und die Codierung zwischen Objekten zu reduzieren, die vollständig innerhalb des WMI-Repositorys vorhanden sind. Sie können auch das **Ref-Schlüsselwort** verwenden, um eine Zuordnung zwischen zwei Klassen zu erstellen. Weitere Informationen finden Sie unter [Deklarieren einer Zuordnungsklasse.](declaring-an-association-class.md) Wenn sich das Element, auf das verwiesen wird, in derselben MOF-Datei befindet, verwenden Sie einen Alias, um den **Verweiswert** zu initialisieren. Weitere Informationen finden Sie unter [Erstellen eines Alias.](creating-an-alias.md)

> [!Note]  
> Wenn ein **Verweisschlüsselwort** auf eine Schlüsseleigenschaft angewendet wird, können Sie Objektverweise durch den Objektzeichenfolgenwert und nicht durch den dereferenzierten Wert unterscheiden.

 

MOF unterstützt das Konzept eines schwach typisierten und stark typisierten Objektpfads. Ein schwach typisierter Objektpfad zeigt auf ein Objekt einer nicht angegebenen Klasse und verwendet das **Ref-Schlüsselwort** mit dem [OBJECT-Schlüsselwort.](object.md) Ein stark typisiertes Objekt zeigt auf ein Objekt einer bestimmten Klasse und verwendet **ref** mit dem Klassennamen. Das folgende Beispiel beschreibt einen schwach typisierten **RefToAnyClass-Verweis,** der auf eine beliebige Klasse oder Klasseninstanz verweisen kann, und einen **RefToClassX-Verweis,** der nur auf eine **ClassX-Klasse** oder -Instanz verweisen kann:

``` syntax
class MyClass
{
    object ref RefToAnyClass;       // Weakly typed
    ClassX ref RefToClassX;         // Strongly typed
};
```

Im folgenden Beispiel werden zwei Instanzen und ein Zuordnungsobjekt beschrieben, das auf die vorherigen Instanzen verweist:

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

 

 



