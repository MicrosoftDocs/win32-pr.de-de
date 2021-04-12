---
description: Sie können statische Eigenschaften mithilfe von partiellen Wert Maps lokalisieren.
ms.assetid: 67e91454-c065-4ab2-a373-245c9392c71c
ms.tgt_platform: multiple
title: Lokalisieren statischer Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecaba200b7880991d349c6e0c0196c88ffa54b11
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104356166"
---
# <a name="localizing-static-properties"></a>Lokalisieren statischer Eigenschaften

Sie können statische Eigenschaften mithilfe von partiellen Wert Maps lokalisieren.

Im folgenden Verfahren wird beschrieben, wie statische Eigenschaften mithilfe von partiellen Wert Maps mit regulären Ausdrücken lokalisiert werden können.

**So verwenden Sie Werte Zuordnungen zum Lokalisieren statischer Eigenschaften**

1.  Erstellen Sie eine MOF-Master Datei (mastervm. MOF).

    Das folgende Codebeispiel kann verwendet werden, um eine MOF-Master Datei (mastervm. MOF) zu erstellen.

    ```syntax
    [Locale(0x409)]
    class Group1
    {
        [key] string ID;
        [DisplayName("Numbers"),
            ValueMap{0,1,2,3}:amended,
            Values{"Zero", "One", "Two", "Three"}:amended]
        Uint32 Numbers;
    };
    ```

2.  Erstellen Sie sprachneutrale und sprachspezifische Versionen der MOF-Datei.

    Geben Sie den folgenden Befehl an einer Eingabeaufforderung ein, um die sprach neutralen und sprachspezifischen Versionen der MOF-Datei zu erstellen.

    ```syntax
    mofcomp -MOF:LnVm.mof -MFL:LsVm.mfl -Amendment:MS_409 MasterVm.mof
    ```

    Der MOF-Compiler generiert die sprachspezifischen und sprach neutralen MOF-Dateien lnvm. mof und lsvm. MFL. Die American English-Werte für die [Numbers](numbers.md) -Eigenschaft befinden sich in der MFL-Datei für den American English-Namespace.

    Im folgenden Codebeispiel wird der Inhalt der Datei "lsvm. MFL" veranschaulicht.

    ```syntax
    #pragma namespace("\\\\.\\root\\default")
    instance of __namespace{ name="ms_409";};
    #pragma namespace("\\\\.\\root\\default\\ms_409")

    [AMENDMENT, LOCALE(0x409)] 
    class Group1
    {
      [ValueMap{0, 1, 2, 3} : Amended,
          Values{"Zero", "One", "Two", "Three"} : Amended] 
      Uint32 Numbers;
    };
    ```

3.  Kompilieren Sie die beiden MOF-Dateien, und speichern Sie die Klassen Informationen im CIM-Repository.

    Geben Sie den folgenden Befehl an einer Eingabeaufforderung ein, um die beiden MOF-Dateien zu kompilieren.

    ```syntax
    Mofcomp LnVm.mof 
    Mofcomp LsVm.mfl
    ```

4.  Lokalisieren Sie die MFL-Datei für andere Gebiets Schemas.

    Das folgende Codebeispiel zeigt den Inhalt einer MFL-Datei für den französischen Namespace.

    ```syntax
    #pragma namespace("\\\\.\\root\\default")
    instance of __namespace{ name="ms_40C";};
    #pragma namespace("\\\\.\\root\\default\\ms_40C")

    [AMENDMENT, LOCALE(0x40C)] 
    class Group1
    {
        [key] string ID;
        [ValueMap{0, 1, 2, 3} : Amended,
            Values{"Zero", "Un", "Deux", "Trois"} : Amended]
        Uint32 Numbers;
    };
    ```

Das Ergebnis ist, dass sowohl der Anzeige Name als auch der Wert der [Numbers](numbers.md) -Eigenschaft vom Gebiets Schema des angemeldeten Benutzers abhängig sind. Wenn der Benutzer ein nicht bereitgestelltes Gebiets Schema angibt, stammen die Standard qualifiziererdaten aus dem englischen \_ Namespace (MS 409).

Die Auswirkung dieses Entwurfs ist, dass jeder Zeichen folgen Wert als Such Bezeichner verwendet wird, der nicht lokalisiert werden kann. Wenn Sie dieses Schema definieren, müssen Sie sicherstellen, dass der Wert, den der Anbieter einfügt, Gebiets Schema unabhängig ist.

> [!Note]  
> WMI bietet derzeit keine Laufzeitunterstützung für die Zuordnung von Werten zu Zeichen folgen, die von Qualifizierern definiert werden. Die Interpretation der empfohlenen Syntax ist die Zuständigkeit der Anwendung.

 

 

 



