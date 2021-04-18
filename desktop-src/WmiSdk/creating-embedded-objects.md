---
description: 'Wenn Sie eine Instanz mit eingebetteten Objekten erstellen, führen Sie die folgenden Aufgaben aus:'
ms.assetid: 2abf6197-8b95-4c04-b154-508aa85fe12f
ms.tgt_platform: multiple
title: Erstellen von eingebetteten Objekten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a76a70fa0e01068622a4f4cdbbbfb6c992b67f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351016"
---
# <a name="creating-embedded-objects"></a>Erstellen von eingebetteten Objekten

Wenn Sie eine Instanz mit eingebetteten Objekten erstellen, führen Sie die folgenden Aufgaben aus:

-   Sie müssen ein eingebettetes Objekt als stark typisiert oder schwach typisiert deklarieren.

    Ein stark typisiertes Objekt verweist auf ein Objekt einer bestimmten Klasse und verwendet den Klassennamen. Ein schwach typisiertes Objekt verweist auf ein Objekt einer nicht angegebenen Klasse und verwendet das **Object** -Schlüsselwort. Beide Objekte werden dem **\_ unbekannten VT** -Typ zugeordnet.

-   Sie können **null** als Standardwert für eingebettete Objekte und Pfade in Initialisierungen und Deklarationen verwenden.
-   Wenn Sie einen Objekt Pfad einbetten, dürfen Sie keinen Leerraum zwischen den Elementen des eingebetteten Pfades platzieren. Der Objekt Pfad "Class1Index = 3;" enthält z. b. kein Leerzeichen zwischen dem Eigenschaftsnamen "Class1Index" und dem zugewiesenen Wert ("3").

Die folgende Klassen Deklaration zeigt, wie stark typisierte und schwach typisierte eingebettete Objekte deklariert werden.

``` syntax
Class MyClass
{
    EmbedClass    Object1;          // Strongly typed
    object        Object2;          // Weakly typed
};
```

In den folgenden Beispielen wird beschrieben, wie eingebettete Objekte innerhalb einer Klassen Deklaration deklariert werden.

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

Im folgenden Beispiel wird die Initialisierung einer Eigenschaft beschrieben, bei der es sich um ein stark typisiertes Objekt handelt, und eine andere Eigenschaft, die ein Array von schwach typisierten Objekten ist.

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

 

 



