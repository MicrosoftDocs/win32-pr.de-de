---
description: Ein Array ist eine indizierte Liste von Datenwerten, die denselben Datentyp aufweisen, auf den Sie verweisen können. Zusätzlich zu Zeichenfolgen- und numerischen Arrays unterstützt MOF Arrays eingebetteter Objekte und Verweise.
ms.assetid: f63c222f-499d-4776-8901-65cb8b142d2b
ms.tgt_platform: multiple
title: MOF-Arrays
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1231b89302e15d5a7467ab7ff99d23b200badd67e6c5c95054c90b84554548d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992800"
---
# <a name="mof-arrays"></a>MOF-Arrays

Ein Array ist eine indizierte Liste von Datenwerten, die denselben Datentyp aufweisen, auf den Sie verweisen können. Zusätzlich zu Zeichenfolgen- und numerischen Arrays unterstützt MOF Arrays eingebetteter Objekte und Verweise.

Die folgenden Regeln definieren ein MOF-Array:

-   Klammern, die nach dem Eigenschaftenbezeichner verwendet werden, geben ein Array in einer Klassendefinition an.

    ``` syntax
    Class ArrayDataSample1
    {
        string strArray1[];
    };
    ```

-   Alle Arrays müssen eindimensional sein.
-   Arrays können ungebunden sein oder eine explizite Größe aufweisen.

    ``` syntax
    Class MyClass
    {
        sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk DiskArray1[]);
        sint32 MyMethod2 ([in, id(0)] Win32_LogicalDisk DiskArray2[32]);
    };
    ```

    WMI implementiert umgrenzte und ungebundene Arrays als **SAFEARRAY-Strukturen,** die es WMI ermöglichen, Arraydimensionen zur Laufzeit zu variieren. Wenn Sie ein Array mit einer expliziten Größe deklarieren, speichert WMI die Größe als Qualifizierer und behandelt die Größe als vorgeschlagene maximale Größe. WMI kann die Größe jedoch bei Bedarf erweitern. Das Ändern der expliziten Größe hat keine Auswirkungen auf die tatsächlichen Daten.

-   Arrays werden initialisiert, indem Werte des entsprechenden Typs in einer durch Trennzeichen getrennten Liste angegeben werden.

    ``` syntax
    Class ArrayDataSample2
    {
        [key] string s;
        string strArray2[] = {"hello", "there"};
        sint32 dwArray[] = {1,2,3};
    };
    ```

-   Ein Array von Verweisen wird als Array von Objektpfadzeichenfolgen deklariert.

    Wenn Sie eine Objektpfadzeichenfolge deklarieren, sollten Sie zwischen den Elementen des Objektpfads keinen Leerraum platzieren. Im folgenden Beispiel wird beschrieben, wie ein Objektpfadverweis deklariert wird.

    ``` syntax
    Class ClassWithRefArray
        { 
        [key] string s; 
        object ref refArray[]; 
        };

    instance of ClassWithRefArray
        {
        s = 23;
        refArray = {"Disk.Name=\"C:\"", "Disk.Name=\"E:\""};
        };
    ```

-   Sie können ein Array als Parameter für eine Methode verwenden, jedoch nicht als Rückgabewert für einen Eingabe- oder Eingabe-/Ausgabeparameter.
-   Alle Elemente in einem Array werden als Werte desselben Typs erstellt.

    Wenn die Elemente eines Arrays vom **Objekttyp** sind, können Sie jede Art von Objekt im Array platzieren. Wenn Sie dagegen einen bestimmten Objekttyp deklarieren, lässt WMI nur Objekte dieser Klasse oder Unterklasse im Array zu. Die folgenden Beispiele zeigen Arraydeklarationen, die die Verwendung des **Objekttyps** enthalten.

    ``` syntax
    Class EmbedClass
    {
        [key] sint32 PropOfClass;
    };

    Class ArrayDataClass
    {
        [key] string s;
        string strArray1[];
        string strArray2[] = {"hello", "there"};
        sint32 dwArray[] = {1,2,3};
        EmbedClass objArray[];
    };

    instance of ArrayDataClass
    { 
        s = "keyStuff";
        strArray1 = { "1.2.3.4", "1.2.3.5", "1.2.3.7"};
        strArray2 = 
            {
                "SELECT * FROM RegistryKeyChangeEvent",
                "SELECT * FROM RegistryValueChangeEvent",
                "SELECT * FROM RegistryTreeChangeEvent"
            };
        dwArray  = { 1,2,3,5,6 };
        objArray = {
                       instance of EmbedClass{PropOfClass=3;},
                       instance of EmbedClass{PropOfClass=4;}
                   };
    };
    ```

 

 



