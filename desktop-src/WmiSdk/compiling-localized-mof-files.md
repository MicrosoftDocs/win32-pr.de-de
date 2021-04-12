---
description: Sie müssen ihre Master-MOF-Datei kompilieren, um die sprach neutralen und sprachspezifischen MOF-Dateien zu erstellen.
ms.assetid: ae2fa320-8294-4991-be30-403088c34b7a
ms.tgt_platform: multiple
title: Kompilieren lokalisierter MOF-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41ab1341a37269ba98fdbbdecaa64b5e5a119703
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346768"
---
# <a name="compiling-localized-mof-files"></a>Kompilieren lokalisierter MOF-Dateien

Sie müssen ihre Master-MOF-Datei kompilieren, um die sprach neutralen und sprachspezifischen MOF-Dateien zu erstellen.

Geben Sie den folgenden Befehl an einer Eingabeaufforderung ein, um eine Master-MOF-Datei zu kompilieren.

**"MOF": "MOF-MFL: lsmof. MFL-Zusatz: ms \_ 409 mastermof. mof"**

Wenn Sie diesen Befehl ausführen, erstellt der MOF-Compiler zwei MOF-Dateien aus der ursprünglichen Datei "mastermof. mof". Der MOF-Compiler erzeugt eine sprachneutrale Version (lnmof. MOF), in der alle sprachspezifischen Elemente entfernt werden. Außerdem wird eine zweite sprachspezifische Version (lsmof. MOF) erstellt. Diese Datei enthält nur Elemente, die mit der [**geänderten**](qualifier-flavors.md) qualifiziererkonfiguration in der Datei mastermof. MOF gekennzeichnet wurden.

Im folgenden Codebeispiel wird der Inhalt der-sprach neutralen MOF-Datei (lnmof. MOF) gezeigt, die generiert wird.

``` syntax
#pragma namespace("\\\\.\\root")

Instance of __Namespace
{
  Name = "TEST";
};
#pragma namespace("\\\\.\\root\\TEST")

[LOCALE(1033)] 
class myclass
{
  [key] string Name;
  uint64 Value;
  uint64 Timestamp;
};
```

Das folgende Codebeispiel zeigt den Inhalt der sprachspezifischen MOF-Datei (lsmof. MFL), die generiert wird.

``` syntax
#pragma namespace("\\\\.\\root\\TEST")
instance of __namespace{ name="ms_409";};
#pragma namespace("\\\\.\\root\\TEST\\ms_409")

[Description("Localized version of MyClass for American English") :
    Amended, LOCALE(0x409)] 

class myclass
{
    [DisplayName("User Name") : Amended,
    Description("The Name property contains the name of the user") : 
    Amended, key]
     string Name;

    [DisplayName("Time Stamp") : Amended,
    Description("This property shows when the object was created") : 
    Amended] 
     uint64 Timestamp;
};
```

Beim Kompilieren einer MOF-Datei mit dem [**geänderten**](qualifier-flavors.md) Qualifizierer werden nur separate sprachneutrale und sprachspezifische MOF-Dateien generiert. das CIM-Repository wird nicht mit den neuen Klassen Informationen aktualisiert. Sie müssen den MOF-Compiler verwenden, um die beiden MOF-Dateien zu kompilieren, die von der ersten Kompilierung erstellt wurden, bevor Klassen Informationen für WMI verfügbar sind.

Wenn Sie eine MOF-Master Datei kompilieren, werden nur Qualifizierer mit der [**geänderten**](qualifier-flavors.md) Konfiguration in die sprachspezifische MOF-Datei verschoben. Qualifizierer, die nicht die **geänderte** Art aufweisen, werden nicht lokalisiert und sind nur in der grundlegenden Klassendefinition in der sprach neutralen MOF-Datei vorhanden. Nicht lokalisierte Qualifizierer können für Standard Beschreibungen verwendet werden, wenn keine lokalisierten Beschreibungen verfügbar sind.

Sie können den [pragma-Zusatz](pragma-amendment.md) Befehl verwenden, anstatt ihn als Schalter für den MOF- [**Compiler anzugeben.**](qualifier-flavors.md) Jede dieser Optionen entspricht der Anforderung von sprachspezifischen und sprach neutralen Versionen einer MOF-Datei. Wenn Sie entweder den Befehl "Pragma-Zusatz" oder die **geänderte** Befehlszeilenoption verwenden, müssen Sie den Namen der Ausgabedateien mithilfe der Optionen " **-MFL** " und " **-MOF** " an der Eingabeaufforderung angeben.

> [!Note]  
> Die sprachneutrale MOF-Datei, die der MOF-Compiler generiert, enthält die dezimale Entsprechung der Gebiets Schema-ID, auch wenn dieser Wert in Hexadezimal eingegeben wurde. Im obigen Beispiel hat der Compiler den Wert 0x409 in die Dezimalzahl 1033 für die Ausgabedatei "lnmof. mof" konvertiert.

 

 

 



