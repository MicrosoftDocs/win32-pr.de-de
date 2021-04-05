---
description: Weist den MOF-Compiler an, eine MOF-Datei in sprachneutrale und sprachspezifische Versionen aufzuteilen.
ms.assetid: c1aec33c-b936-4cca-8fcd-7bd088af7116
ms.tgt_platform: multiple
title: pragma-Zusatz
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
ms.openlocfilehash: 1269ac1a96617b72852e687b2a38ce8d331ab3e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753697"
---
# <a name="pragma-amendment"></a>pragma-Zusatz

Der Präprozessorbefehl " **pragma-Zusatz** " weist den MOF-Compiler an, eine MOF-Datei in sprachneutrale und sprachspezifische Versionen zu trennen. Die sprachspezifische MOF-Datei verschiebt geänderte Qualifizierer in einen Namespace für ein bestimmtes Gebiets Schema. Anschließend kompilieren Sie die sprachspezifischen und sprach neutralen MOF-Dateien, um Klassen Informationen im WMI-Repository zu speichern.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie eine MOF-Datei erstellt wird, die geänderte Qualifizierer enthält. Anschließend können Sie den MOF-Code mit dem folgenden Befehl kompilieren:

**MUF Comp** **-MOF: lnmof. MOF** **-MFL: lsmof. MFL** **mastermof. MOF**

Der Befehl weist den MOF-Compiler an, zwei MOF-Dateien aus der ursprünglichen Datei "mastermof. mof" zu entwickeln. Der MOF-Compiler erstellt eine sprachneutrale Version der MOF-Datei mit dem Namen lnmof. MOF, wobei alle sprachspezifischen Elemente entfernt werden. Der Compiler erstellt außerdem eine zweite sprachspezifische MOF-Datei mit dem Namen lsmof. MFL, die nur die Elemente enthält, die Sie lokalisieren müssen.

> [!Note]  
> Wenn Sie eine MOF-Datei mit dem **Zusatz** Qualifizierer oder dem **pragma-Zusatz** Befehl aufteilen, müssen Sie die **-MOF** -und die **-MFL-** Option angeben. Andernfalls generiert der Compiler keine Ausgabedateien. Sie müssen dann die beiden Ausgabedateien kompilieren, um die Klassen Informationen für WMI verfügbar zu machen.

 


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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Präprozessorbefehle](preprocessor-commands.md)
</dt> </dl>

 

 




