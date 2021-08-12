---
description: Sie müssen ihre MOF-Masterdatei kompilieren, um die sprachneutralen und sprachspezifischen MOF-Dateien zu erstellen.
ms.assetid: ae2fa320-8294-4991-be30-403088c34b7a
ms.tgt_platform: multiple
title: Kompilieren lokalisierter MOF-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d23c77fee8a745b6032848c124a24ffb8e7cf626b0ff3c87fecc7e05b14d372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118556799"
---
# <a name="compiling-localized-mof-files"></a>Kompilieren lokalisierter MOF-Dateien

Sie müssen ihre MOF-Masterdatei kompilieren, um die sprachneutralen und sprachspezifischen MOF-Dateien zu erstellen.

Geben Sie den folgenden Befehl an einer Eingabeaufforderung ein, um eine MOF-Masterdatei zu kompilieren.

**mofcomp -MOF:Lnmof.mof -MFL:Lsmof.mfl -Amendment:MS \_ 409 Mastermof.mof**

Wenn Sie diesen Befehl ausführen, erstellt der MOF-Compiler zwei MOF-Dateien aus der ursprünglichen Datei Mastermof.mof. Der MOF-Compiler erzeugt die sprachneutrale Version Lnmof.mof, in der alle sprachspezifischen Elemente entfernt werden. Eine zweite sprachspezifische Version, Lsmof.mof, wird ebenfalls erstellt. Diese Datei enthält nur Elemente, die in der Datei Mastermof.mof mit dem [**geänderten**](qualifier-flavors.md) Qualifizierer flavor markiert wurden.

Das folgende Codebeispiel zeigt den Inhalt der sprachneutralen MOF-Datei (Lnmof.mof), die generiert wird.

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

Das folgende Codebeispiel zeigt den Inhalt der sprachspezifischen MOF-Datei (Lsmof.mfl), die generiert wird.

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

Beim Kompilieren einer MOF-Datei mit dem [**geänderten**](qualifier-flavors.md) Qualifizierer werden nur separate sprachneutrale und sprachspezifische MOF-Dateien generiert. das CIM-Repository wird nicht mit den neuen Klasseninformationen aktualisiert. Sie müssen den MOF-Compiler verwenden, um die beiden MOF-Dateien zu kompilieren, die bei der ersten Kompilierung erstellt wurden, bevor Klasseninformationen für WMI verfügbar sind.

Wenn Sie eine MOF-Masterdatei kompilieren, werden nur Qualifizierer mit der [**geänderten**](qualifier-flavors.md) Variante in die sprachspezifische MOF-Datei verschoben. Qualifizierer ohne **die geänderte** Variante sind nicht lokalisiert und sind nur in der grundlegenden Klassendefinition in der sprachneutralen MOF-Datei vorhanden. Nicht lokalisierte Qualifizierer können für Standardbeschreibungen verwendet werden, wenn lokalisierte Beschreibungen nicht verfügbar sind.

Sie können den [Pragma-Zusatzbefehl](pragma-amendment.md) verwenden, anstatt [**geändert**](qualifier-flavors.md) als Switch zum MOF-Compiler anzugeben. Eine dieser Optionen entspricht dem Anfordern sprachspezifischer und sprachneutraler Versionen einer MOF-Datei. Wenn Sie entweder den Pragma-Zusatzbefehl oder die **geänderte** Befehlszeilenoption verwenden, müssen Sie den Namen der Ausgabedateien mithilfe der Optionen **-MFL** und **-MOF** an der Eingabeaufforderung angeben.

> [!Note]  
> Die sprachneutrale MOF-Datei, die der MOF-Compiler generiert, enthält die dezimale Entsprechung der Gebietsschema-ID, auch wenn dieser Wert hexadezimal eingegeben wurde. Im obigen Beispiel hat der Compiler den Wert 0x409 in die Dezimalzahl 1033 für die Ausgabedatei Lnmof.mof konvertiert.

 

 

 



