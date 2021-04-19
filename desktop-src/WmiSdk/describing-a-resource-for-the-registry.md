---
description: Die Systemregistrierung enthält ressourcenbezogene Daten.
ms.assetid: e66f1db8-a5f3-41d3-9835-34b81b9da5ed
ms.tgt_platform: multiple
title: Beschreiben einer Ressource für die Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba175120b5abec238d1b9078010359effef8ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373207"
---
# <a name="describing-a-resource-for-the-registry"></a>Beschreiben einer Ressource für die Registrierung

Die Systemregistrierung enthält ressourcenbezogene Daten. Diese Daten befinden sich unter dem folgenden Registrierungsschlüssel und werden in einem speziellen Registrierungs Datentyp namens " **reg \_ Resource \_ List**" gespeichert. Anwendungen können die ressourcenbezogenen Daten über den System Registrierungs Anbieter abrufen. Sie können Systemressourcen in der Registrierung hinzufügen und ändern.

```
HKEY_LOCAL_MACHINE
   Hardware
      ResourceMap
```

Im folgenden Verfahren wird beschrieben, wie ressourcenbezogene Informationen in der Systemregistrierung gespeichert werden.

**So speichern Sie ressourcenbezogene Informationen in der Systemregistrierung**

1.  Erstellen Sie eine Zeichenfolge, die die folgenden Felder enthält.

    

    <table>
    <thead>
    <tr class="header">
    <th>Feld</th>
    <th>Enthält</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Schnittstellentyp</td>
    <td>Einer der folgenden Werte:<br/> <dl> Intern<br />
    ISA<br />
    EISA<br />
    Mikrochannel<br />
    TURBOchannel<br />
    PCIBus<br />
    VMEbus<br />
    NuBus<br />
    PCMCIABus<br />
    CBUS<br />
    Mpibus<br />
    Mpsabus<br />
    </dl></td>
    </tr>
    <tr class="even">
    <td>Busnummer</td>
    <td>Eine ganze Zahl, die die Busnummer angibt.</td>
    </tr>
    <tr class="odd">
    <td>Partielle deskriptornummer</td>
    <td>Eine ganze Zahl, die die deskriptornummer angibt.</td>
    </tr>
    <tr class="even">
    <td>Offset-oder Union-Typ</td>
    <td>Einer der folgenden Werte:<br/> <dl> Port. Start<br />
    Port. PhysicalAddress<br />
    Port. length<br />
    Interrupt. Level<br />
    Interrupt. Vector<br />
    Interrupt. Affinität<br />
    Arbeitsspeicher. Start<br />
    "Memory. PhysicalAddress"<br />
    Arbeitsspeicher. Länge<br />
    DMA. Channel<br />
    DMA. Port<br />
    DMA. "reserved1"<br />
    "De vicespecificdata. DataSize"<br />
    "De vicespecificdata." reserved1 ""<br />
    "De vicespecificdata." reserved2 ""<br />
    </dl></td>
    </tr>
    </tbody>
    </table>

    

     

2.  Platzieren Sie die Zeichenfolge im entsprechenden Schlüssel unter dem Registrierungsschlüssel.

    ```
    HKEY_LOCAL_MACHINE
       Hardware
          ResourceMap
    ```

Im folgenden Codebeispiel wird ein gültiger Ressourcen Deskriptor beschrieben.

``` syntax
local|hkey_local_machine\hardware\resourcemap\
  hardware abstraction layer\
  pc compatible eisa/isa HAL|.raw("eisa",0,0,"interrupt.affinity")
```

Das folgende Codebeispiel zeigt die gültige MOF-Syntax zum Abrufen eines Ressourcen Deskriptors.

``` syntax
[DYNPROPS] 
class MyRegProp
{    
   [KEY]  
   STRING MyKey; 
   STRING MyReservedTranslated;
};

[DYNPROPS] 
instance of MyRegProp
{
   MyKey = "1";
   [PropertyContext("local|hkey_local_Machine\\hardware\\ResourceMap\\
                   System Resources\\Reserved|.Translated
                   (\"Internal\")(0)(1)(\"Memory.PhysicalAddress\")"),
   Dynamic, Provider("RegPropProv")] 
   MyReservedTranslated;
};
```

 

 




