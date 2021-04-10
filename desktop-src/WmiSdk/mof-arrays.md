---
description: Ein Array ist eine indizierte Liste mit Datenwerten desselben Datentyps, auf die Sie verweisen können. Zusätzlich zu Zeichen folgen-und numerischen Arrays unterstützt MOF auch Arrays von eingebetteten Objekten und verweisen.
ms.assetid: f63c222f-499d-4776-8901-65cb8b142d2b
ms.tgt_platform: multiple
title: MOF-Arrays
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0443f2ef3b3fe8fca398e281de71b0927a4f06f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214982"
---
# <a name="mof-arrays"></a>MOF-Arrays

Ein Array ist eine indizierte Liste mit Datenwerten desselben Datentyps, auf die Sie verweisen können. Zusätzlich zu Zeichen folgen-und numerischen Arrays unterstützt MOF auch Arrays von eingebetteten Objekten und verweisen.

Die folgenden Regeln definieren ein MOF-Array:

-   Die nach dem Eigenschaften Bezeichner verwendeten Klammern geben ein Array in einer Klassendefinition an.

    ``` syntax
    Class ArrayDataSample1
    {
        string strArray1[];
    };
    ```

-   Alle Arrays müssen eindimensional sein.
-   Arrays können unbegrenzt sein oder eine explizite Größe aufweisen.

    ``` syntax
    Class MyClass
    {
        sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk DiskArray1[]);
        sint32 MyMethod2 ([in, id(0)] Win32_LogicalDisk DiskArray2[32]);
    };
    ```

    WMI implementiert begrenzte und ungebundene Arrays als **SAFEARRAY** -Strukturen, sodass WMI die Array Dimensionen zur Laufzeit variieren kann. Wenn Sie ein Array mit einer expliziten Größe deklarieren, wird die Größe von WMI als Qualifizierer gespeichert, und die Größe wird als vorgeschlagene maximale Größe behandelt. Allerdings kann WMI die Größe ggf. erweitern. Das Ändern der expliziten Größe hat keine Auswirkung auf die eigentlichen Daten.

-   Arrays werden initialisiert, indem Werte des entsprechenden Typs in einer durch Trennzeichen getrennten Liste angegeben werden.

    ``` syntax
    Class ArrayDataSample2
    {
        [key] string s;
        string strArray2[] = {"hello", "there"};
        sint32 dwArray[] = {1,2,3};
    };
    ```

-   Ein Array von verweisen wird als Array von Objekt Pfad Zeichenfolgen deklariert.

    Wenn Sie eine Objekt Pfad Zeichenfolge deklarieren, dürfen Sie keinen Leerraum zwischen den Elementen des Objekt Pfads platzieren. Im folgenden Beispiel wird beschrieben, wie Sie einen Objekt Pfad Verweis deklarieren.

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

-   Sie können ein Array als Parameter für eine Methode verwenden, aber nicht als Rückgabewert für einen Eingabe-oder Eingabe-/Ausgabeparameter.
-   Alle Elemente in einem Array werden als Werte desselben Typs erstellt.

    Wenn die Elemente eines Arrays den **Objekttyp** haben, können Sie alle Arten von Objekten im Array platzieren. Wenn Sie dagegen einen bestimmten Objekttyp deklarieren, lässt WMI nur Objekte dieser Klasse oder Unterklasse im Array zu. In den folgenden Beispielen werden Array Deklarationen veranschaulicht,  die den-Objekttyp verwenden.

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

 

 



