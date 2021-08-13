---
description: 'Führen Sie beim Erstellen einer Instanz mit eingebetteten Objekten die folgenden Aufgaben aus:'
ms.assetid: 2abf6197-8b95-4c04-b154-508aa85fe12f
ms.tgt_platform: multiple
title: Erstellen eingebetteter Objekte
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2e54e16005669ebd77b0bc08e5d3174f7aa5fadee2a47477920e91aaa2ae155b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464170"
---
# <a name="creating-embedded-objects"></a>Erstellen eingebetteter Objekte

Führen Sie beim Erstellen einer Instanz mit eingebetteten Objekten die folgenden Aufgaben aus:

-   Sie müssen ein eingebettetes Objekt als stark typisch oder schwach typisch deklarieren.

    Ein stark typiertes Objekt verweist auf ein Objekt einer bestimmten Klasse und verwendet den Klassennamen. Ein schwach typisiertes Objekt verweist auf ein Objekt einer nicht angegebenen Klasse und verwendet das **Object-Schlüsselwort.** Beide Objekte sind dem **VT \_ UNKNOWN-Typ** zuordnen.

-   Sie können **NULL für** den Standardwert eingebetteter Objekte und Pfade in Initialisierungen und Deklarationen verwenden.
-   Platzieren Sie beim Einbetten eines Objektpfads keinen Leerraum zwischen den Elementen des eingebetteten Pfads. Beispielsweise enthält der Objektpfad "Class1Index=3;" kein Leerzeichen zwischen dem Eigenschaftennamen "Class1index" und dem zugewiesenen Wert, der "3" ist.

Die folgende Klassendeklaration zeigt, wie Sie stark typierte und schwach typierte eingebettete Objekte deklarieren.

``` syntax
Class MyClass
{
    EmbedClass    Object1;          // Strongly typed
    object        Object2;          // Weakly typed
};
```

In den folgenden Beispielen wird beschrieben, wie eingebettete Objekte in einer Klassendeklaration deklariert werden.

``` syntax
Class Class1 
{ 
     [key] sint32 Class1Index;
};

Class Class2 
{
    [key] sint32 Class2Index;
    Class1 EmbedObject1 = instance of Class1{Class1Index=3;};
};

Class Class3
{
    [key] sint32 Class3Index;
    Class2 EmbedObject2 = instance of Class2 {Class2Index=4;};
};
```

Im folgenden Beispiel wird die Initialisierung einer Eigenschaft beschrieben, bei der es sich um ein stark typiertes Objekt handelt, und einer anderen Eigenschaft, bei der es sich um ein Array von schwach typierten Objekten handelt.

``` syntax
Class EmbedClass1
{
    [key] sint32 intval;
};

Class EmbedClass2
{
    [key] string sval;
};

Class ContainerClass
{
    [key] sint32 intval;
    EmbedClass1 SingleObject;
    Object ArrayObject[];
};

Instance of ContainerClass
{
    intval = 33;
    SingleObject = instance of EmbedClass1 {intval=99;};
    ArrayObject = {instance of EmbedClass2 {sval="something";},
                   instance of EmbedClass1 {intval=100;}};
};
```

 

 



