---
description: Weist den MOF-Compiler an, eine MOF-Datei in sprachneutrale und sprachspezifische Versionen zu untergliedern.
ms.assetid: c1aec33c-b936-4cca-8fcd-7bd088af7116
ms.tgt_platform: multiple
title: Pragma-Zusatz
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6204ac7f3cd78de8d2eed9740fc165475d387e65284bcbf6be1ea10ed91a0926
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992730"
---
# <a name="pragma-amendment"></a>Pragma-Zusatz

Der **Pragma-Zusatzpräprozessorbefehl** weist den MOF-Compiler an, eine MOF-Datei in sprachneutrale und sprachspezifische Versionen zu untergliedern. Die sprachspezifische MOF-Datei verschiebt geänderte Qualifizierer in einen Namespace für ein bestimmtes Gebietsschema. Anschließend kompilieren Sie die sprachspezifischen und sprachneutralen MOF-Dateien, um Klasseninformationen im WMI-Repository zu speichern.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie Sie eine MOF-Datei erstellen, die geänderte Qualifizierer enthält. Anschließend können Sie den MOF-Code mit dem folgenden Befehl kompilieren:

**mofcomp** **-MOF:Lnmof.mof** **-MFL:Lsmof.mfl** **Mastermof.mof**

Der Befehl weist den MOF-Compiler an, zwei MOF-Dateien aus der ursprünglichen Datei "Mastermof.mof" zu erstellen. Der MOF-Compiler erzeugt eine sprachneutrale Version der MOF-Datei namens Lnmof.mof, wobei alle sprachspezifischen Elemente entfernt wurden. Der Compiler erstellt auch eine zweite sprachspezifische MOF-Datei namens Lsmof.mfl, die nur Elemente enthält, die Sie lokalisieren müssen.

> [!Note]  
> Wenn Sie eine MOF-Datei mit dem **Zusatzqualifizierer** oder dem **Pragma-Zusatzbefehl** teilen, müssen Sie die Optionen **-MOF** und **-MFL** angeben. Andernfalls generiert der Compiler keine Ausgabedateien. Anschließend müssen Sie die beiden Ausgabedateien kompilieren, um die Klasseninformationen für WMI verfügbar zu machen.

 


```mof
#pragma amendment ("MS_409")

[Description("Localized version of MyClass" for American English") :
    Amended, LOCALE(0x409)] 

Class myclass
{
     [DisplayName("User Name") : Amended,
     Description("The Name property contains the name of the user") : 
     Amended, key]
    string Name;

    uint64 Value; // non-localized value field

     [DisplayName("Time Stamp") : Amended,
     Description("This property shows when the object was created") : 
     Amended] 
    uint64 Timestamp;
};
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Präprozessorbefehle](preprocessor-commands.md)
</dt> </dl>

 

 




