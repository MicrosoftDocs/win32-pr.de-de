---
description: Sie können eine einfache Instanz einer Klasse im Windows-Verwaltungsdienst mit Managed Object Format (MOF) deklarieren. Sie können auch die Standardwerte für eine Instanz überschreiben. Weitere Informationen finden Sie unter Festlegen des Eigenschafts Werts einer Instanz.
ms.assetid: 12eda062-9614-455d-ae99-7706c685137b
ms.tgt_platform: multiple
title: Erstellen einer Instanz mit MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5078c5fcddaab4e8437a33e8cb3210d515360fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343435"
---
# <a name="creating-an-instance-using-mof"></a>Erstellen einer Instanz mit MOF

Sie können eine einfache Instanz einer Klasse im Windows-Verwaltungsdienst mit Managed Object Format (MOF) deklarieren. Sie können auch die Standardwerte für eine Instanz überschreiben. Weitere Informationen finden Sie unter [Festlegen des Eigenschafts Werts einer Instanz](#setting-an-instance-property-value).

Im folgenden Verfahren wird beschrieben, wie Sie mithilfe von MOF-Code eine einfache Instanz einer Klasse deklarieren.

**So deklarieren Sie eine einfache Instanz einer Klasse mithilfe von MOF-Code**

1.  Verwenden Sie die **Instanz von** -Schlüsselwörtern, gefolgt vom Klassennamen, geschweiften Klammern und einem Semikolon.

    Im folgenden Codebeispiel wird gezeigt, wie eine Instanz einer-Klasse deklariert wird.

    ```mof
    instance of ClassName
    {
    };
    ```

    

2.  Wenn Sie fertig sind, fügen Sie den MOF-Code mithilfe des MOF-Compilers in das WMI-Repository ein.

    Weitere Informationen finden Sie unter [Kompilieren von MOF-Dateien](compiling-mof-files.md).

Eine Instanz einer-Klasse enthält alle Eigenschaften der-Klasse. Wenn die Klasse eine abgeleitete Klasse ist, schließen-Instanzen die Eigenschaften ein, die zu allen in der Hierarchie höheren Klassen gehören. Jede Klasse, von der eine Instanz erstellt wird, verfügt über eine oder mehrere Schlüsseleigenschaften. Eine Instanz mit mehr als 256 Schlüsseln kann nicht erstellt werden.

## <a name="setting-an-instance-property-value"></a>Festlegen des Werts einer Instanzeigenschaft

Da Eigenschaften von WMI stark Typen sind, können Sie keine Eigenschafts Typen ändern. Sie können jedoch Eigenschaftswerte in-Instanzen festlegen. Wenn eine Klasse eine Standardwert einer Eigenschaft zuweist, weist WMI jeder Instanz den Standardwert zu. Sie können diesen Wert in der Instanzdeklaration überschreiben.

Im folgenden Verfahren wird beschrieben, wie Sie einen Eigenschafts Wert festlegen oder einen Standardwert überschreiben, indem Sie MOF-Code verwenden.

**So legen Sie einen Eigenschafts Wert fest oder Überschreiben einen Standardwert mithilfe von MOF-Code**

1.  Platzieren Sie eine Zuweisungsanweisung zwischen den geschweiften Klammern der Instanzdeklaration.

    Im folgenden Codebeispiel wird gezeigt, wie ein Eigenschafts Wert festgelegt wird.

    ``` syntax
    instance of ClassName
    {
        Prop = "value";
    };
    ```

    WMI erfordert nicht, dass Sie während der Instanzerstellung eine Eigenschaft festlegen. Die Ausnahme ist jede Eigenschaft, die mit dem [**Schlüssel**](key-qualifier.md) Qualifizierer gekennzeichnet ist. Da WMI Schlüsseleigenschaften zum eindeutigen Identifizieren von Instanzen verwendet, müssen Sie alle Schlüsseleigenschaften so festlegen, wie Sie Sie finden. Im Gegensatz dazu dürfen Sie in einer Instanzdeklaration keine System Eigenschaft festlegen. Stattdessen weist WMI bei Bedarf die entsprechenden Werte einer System Eigenschaft zu.

2.  Wenn Sie fertig sind, fügen Sie den MOF-Code in das WMI-Repository ein, indem Sie den MOF-Compiler aufzurufen.

    Weitere Informationen finden Sie unter [Kompilieren von MOF-Dateien](compiling-mof-files.md).

In den folgenden Codebeispielen wird veranschaulicht, wie eine Instanz Daten für Eigenschaften angibt, die von einer-Klasse definiert werden.

``` syntax
class MyClass 
{
    [key] string   strProp;
    sint32   dwProp1;
    uint32       dwProp2;
};

instance of MyClass 
{
    strProp = "hello";
    dwProp1 = -1;
    dwProp2 = 0xffffffff;
};
```

Im vorherigen Beispiel definiert die-Klasse drei Eigenschaften: eine Zeichenfolge, eine 32-Bit-Ganzzahl mit Vorzeichen und eine 32-Bit-Ganzzahl ohne Vorzeichen. Die-Instanz stellt Datenwerte für jede dieser Eigenschaften bereit.

 

 



