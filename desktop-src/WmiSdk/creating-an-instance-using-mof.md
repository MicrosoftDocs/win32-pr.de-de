---
description: Sie können eine einfache Instanz einer -Klasse im Windows Management-Dienst mithilfe Managed Object Format (MOF) deklarieren. Sie können auch die Standardwerte für eine -Instanz überschreiben. Weitere Informationen finden Sie unter Festlegen eines Instanzeigenschaftswerts.
ms.assetid: 12eda062-9614-455d-ae99-7706c685137b
ms.tgt_platform: multiple
title: Erstellen einer Instanz mit MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05290fd02de80a905e74eeddeb1a04f316901209a97e0e298d038ac2f8888552
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097320"
---
# <a name="creating-an-instance-using-mof"></a>Erstellen einer Instanz mit MOF

Sie können eine einfache Instanz einer -Klasse im Windows Management-Dienst mithilfe Managed Object Format (MOF) deklarieren. Sie können auch die Standardwerte für eine -Instanz überschreiben. Weitere Informationen finden Sie unter [Festlegen eines Instanzeigenschaftswerts.](#setting-an-instance-property-value)

Im folgenden Verfahren wird beschrieben, wie sie eine einfache Instanz einer Klasse mithilfe von MOF-Code deklarieren.

**So deklarieren Sie eine einfache Instanz einer Klasse mit MOF-Code**

1.  Verwenden Sie **die Instanz von Schlüsselwörtern** gefolgt vom Klassennamen, geschweiften Klammern und einem Semikolon.

    Das folgende Codebeispiel zeigt, wie eine Instanz einer Klasse deklariert wird.

    ```mof
    instance of ClassName
    {
    };
    ```

    

2.  Wenn Sie fertig sind, fügen Sie Ihren MOF-Code mithilfe des MOF-Compilers in das WMI-Repository ein.

    Weitere Informationen finden Sie unter [Kompilieren von MOF-Dateien.](compiling-mof-files.md)

Eine Instanz einer Klasse enthält alle Eigenschaften der -Klasse. Wenn es sich bei der Klasse um eine abgeleitete Klasse handelt, enthalten -Instanzen die Eigenschaften, die zu allen klassen weiter oben in der Hierarchie gehören. Jede Klasse, aus der eine Instanz erstellt wird, verfügt über mindestens eine Schlüsseleigenschaften. Sie können keine Instanz mit mehr als 256 Schlüsseln erstellen.

## <a name="setting-an-instance-property-value"></a>Festlegen eines Instanzeigenschaftswerts

Da WMI Eigenschaften stark typt, können Sie Eigenschaftstypen nicht ändern. Sie können jedoch Eigenschaftswerte in -Instanzen festlegen. Wenn eine Klasse einer Eigenschaft einen Standardwert zu weist, weist WMI den Standardwert jeder Instanz zu. Sie können diesen Wert in der Instanzdeklaration überschreiben.

Im folgenden Verfahren wird beschrieben, wie Sie einen Eigenschaftswert festlegen oder einen Standardwert mithilfe von MOF-Code überschreiben.

**So legen Sie einen Eigenschaftswert fest oder überschreiben einen Standardwert mithilfe von MOF-Code**

1.  Platzieren Sie eine Zuweisungs-Anweisung zwischen den geschweiften Klammern der Instanzdeklaration.

    Das folgende Codebeispiel zeigt, wie ein Eigenschaftswert festgelegt wird.

    ``` syntax
    instance of ClassName
    {
        Prop = "value";
    };
    ```

    WMI erfordert nicht, dass Sie während der Instanzerstellung eine Eigenschaft festlegen. Die Ausnahme ist jede Eigenschaft, die mit dem [**Schlüsselqualifizierer**](key-qualifier.md) markiert ist. Da WMI Schlüsseleigenschaften verwendet, um Instanzen eindeutig zu identifizieren, müssen Sie alle Schlüsseleigenschaften festlegen, sobald sie auftreten. Im Gegensatz dazu dürfen Sie keine Systemeigenschaft in einer Instanzdeklaration festlegen. Stattdessen weist WMI bei Bedarf die entsprechenden Werte einer Systemeigenschaft zu.

2.  Wenn Sie fertig sind, fügen Sie Ihren MOF-Code mit einem Aufruf des MOF-Compilers in das WMI-Repository ein.

    Weitere Informationen finden Sie unter [Kompilieren von MOF-Dateien.](compiling-mof-files.md)

Die folgenden Codebeispiele zeigen, wie eine -Instanz Daten für Eigenschaften angibt, die von einer -Klasse definiert werden.

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

Im vorherigen Beispiel definiert die -Klasse drei Eigenschaften: eine Zeichenfolge, eine 32-Bit-Ganzzahl mit Vorzeichen und eine 32-Bit-Ganzzahl ohne Vorzeichen. Die -Instanz bietet Datenwerte für jede dieser Eigenschaften.

 

 



