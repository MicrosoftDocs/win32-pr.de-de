---
description: Die Systemregistrierung enthält ressourcenbezogene Daten.
ms.assetid: e66f1db8-a5f3-41d3-9835-34b81b9da5ed
ms.tgt_platform: multiple
title: Beschreiben einer Ressource für die Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30be25eed569f212e435827023eed132cf1c6ead49be37eabb6fe4ac30e8e3b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097270"
---
# <a name="describing-a-resource-for-the-registry"></a>Beschreiben einer Ressource für die Registrierung

Die Systemregistrierung enthält ressourcenbezogene Daten. Diese Daten befinden sich unter dem folgenden Registrierungsschlüssel und werden in einem speziellen Registrierungsdatentyp mit dem Namen **REG \_ RESOURCE \_ LIST** gespeichert. Anwendungen können die ressourcenbezogenen Daten über den Systemregistrierungsanbieter abrufen. Sie können Systemressourcen in der Registrierung hinzufügen und ändern.

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
    Isa<br />
    Eisa<br />
    MicroChannel<br />
    Turbochannel<br />
    PCIBus<br />
    Vmebus<br />
    NuBus<br />
    PCMCIABus<br />
    CBus<br />
    MPIBus<br />
    MPSABus<br />
    </dl></td>
    </tr>
    <tr class="even">
    <td>Busnummer</td>
    <td>Ganze Zahl, die die Busnummer angibt.</td>
    </tr>
    <tr class="odd">
    <td>Partielle Deskriptornummer</td>
    <td>Ganze Zahl, die die Deskriptornummer angibt.</td>
    </tr>
    <tr class="even">
    <td>Offset- oder Union-Typ</td>
    <td>Einer der folgenden Werte:<br/> <dl> Port.Start<br />
    Port.PhysicalAddress<br />
    Port.Length<br />
    Interrupt.Level<br />
    Interrupt.Vector<br />
    Interrupt.Affinity<br />
    Memory.Start<br />
    Memory.PhysicalAddress<br />
    Memory.Length<br />
    Dma.Channel<br />
    Dma.Port<br />
    Dma.Reserved1<br />
    DeviceSpecificData.DataSize<br />
    DeviceSpecificData.Reserved1<br />
    DeviceSpecificData.Reserved2<br />
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

Im folgenden Codebeispiel wird ein gültiger Ressourcendeskriptor beschrieben.

``` syntax
local|hkey_local_machine\hardware\resourcemap\
  hardware abstraction layer\
  pc compatible eisa/isa HAL|.raw("eisa",0,0,"interrupt.affinity")
```

Das folgende Codebeispiel zeigt eine gültige MOF-Syntax zum Abrufen eines Ressourcendeskriptors.

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

 

 




