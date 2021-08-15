---
description: Sie können statische Eigenschaften mithilfe von Teilwertzuordnungen lokalisieren.
ms.assetid: 67e91454-c065-4ab2-a373-245c9392c71c
ms.tgt_platform: multiple
title: Lokalisieren statischer Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c51999c68a05e8d7b8cf3fd8c5218bc171931303d86a50c04f32c5d80efb308
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050728"
---
# <a name="localizing-static-properties"></a>Lokalisieren statischer Eigenschaften

Sie können statische Eigenschaften mithilfe von Teilwertzuordnungen lokalisieren.

Im folgenden Verfahren wird beschrieben, wie statische Eigenschaften mithilfe von Teilwertzuordnungen mit regulären Ausdrücken lokalisiert werden können.

**So verwenden Sie Wertzuordnungen zum Lokalisieren statischer Eigenschaften**

1.  Erstellen Sie eine MOF-Masterdatei (Mastervm.mof).

    Das folgende Codebeispiel kann verwendet werden, um eine MOF-Masterdatei (Mastervm.mof) zu erstellen.

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

2.  Erstellen Sie die sprachneutralen und sprachspezifischen Versionen der MOF-Datei.

    Geben Sie den folgenden Befehl an einer Eingabeaufforderung ein, um die sprachneutrale und sprachspezifische Version der MOF-Datei zu erstellen.

    ```syntax
    mofcomp -MOF:LnVm.mof -MFL:LsVm.mfl -Amendment:MS_409 MasterVm.mof
    ```

    Der MOF-Compiler generiert die sprachspezifischen und sprachneutralen MOF-Dateien LnVm.mof und LsVm.mfl. Die Amerikanischen Englisch-Werte für die [Numbers-Eigenschaft](numbers.md) werden in der MFL-Datei für den Namespace "American English" platziert.

    Das folgende Codebeispiel zeigt den Inhalt der Datei LsVm.mfl.

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

3.  Kompilieren Sie die beiden MOF-Dateien, und speichern Sie die Klasseninformationen im CIM-Repository.

    Geben Sie den folgenden Befehl an einer Eingabeaufforderung ein, um die beiden MOF-Dateien zu kompilieren.

    ```syntax
    Mofcomp LnVm.mof 
    Mofcomp LsVm.mfl
    ```

4.  Lokalisieren Sie die MFL-Datei für andere Länder.

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

Das Ergebnis ist, dass sowohl der Anzeigename als auch der Wert der [Numbers-Eigenschaft](numbers.md) vom Locale des angemeldeten Benutzers abhängen. Wenn der Benutzer ein nicht bereitgestelltes Locale angibt, stammen die Standardqualifiziererdaten aus dem englischen Namespace (ms \_ 409).

Die Folge dieses Entwurfs ist, dass jeder Zeichenfolgenwert als Suchbezeichner verwendet wird, der nicht lokalisiert werden kann. Beim Definieren dieses Schemas müssen Sie sicherstellen, dass der Wert, den der Anbieter einrückt, vom Lokalen unabhängig ist.

> [!Note]  
> WMI bietet derzeit keine Laufzeitunterstützung für die Zuordnung von Werten zu Zeichenfolgen, die von Qualifizierern definiert werden. Die Interpretation der vorgeschlagenen Syntax liegt in der Verantwortung der Anwendung.

 

 

 



