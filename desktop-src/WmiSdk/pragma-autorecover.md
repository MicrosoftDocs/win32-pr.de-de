---
description: Fügt der Liste der Dateien, die während der Repositorywiederherstellung kompiliert wurden, eine MOF-Datei hinzu.
ms.assetid: 8901c04e-f8c1-45b0-b69d-e2ebc948f088
ms.tgt_platform: multiple
title: pragma autorecover
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
ms.openlocfilehash: cc36191482731e77d0f82c4e3734350da2f6ed2fbd3faad7b2972dca4e0e6bd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992700"
---
# <a name="pragma-autorecover"></a>pragma autorecover

Der **Präprozessorbefehl pragma autorecover** fügt der Liste der Dateien, die während der Repositorywiederherstellung kompiliert wurden, eine MOF-Datei hinzu. Die Liste der **MOF-Dateien zum automatischen Wiederherstellen** wird in diesem Registrierungsschlüssel gespeichert:

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **autorecover mofs**

WMI überprüft die Integrität des WMI-Repositorys, wenn das Betriebssystem WMI startet. Wenn das Repository beschädigt ist, erstellt WMI das Repository automatisch neu und kompiliert alle MOF-Dateien, die in diesem Schlüssel in der Registrierung aufgeführt sind, neu.

Im Folgenden wird die Syntax für den Pragma autorecover-Befehl beschrieben:


```mof
#pragma autorecover
```



Sie müssen jedoch die folgenden Einschränkungen beachten, wenn Sie diesen Befehl verwenden:

-   WMI kann MOF-Dateien, die sich auf einem Remotecomputer befinden, nicht wiederherstellen.

    Daher müssen sich die in diesem Registrierungsschlüssel aufgeführten MOF-Dateien auf dem lokalen Computer befinden.

-   Sie können die Befehlszeilenschalter nicht angeben, die der MOF-Compiler verwendet, wenn WMI eine MOF-Datei wiederhergestellt.

    Daher sollten Sie [Pragmabefehle](-pragma.md) in Ihre MOF-Datei einschließen, die Befehlszeilenschalter überflüssig machen. Im folgenden Beispiel wird ein gängiger Befehlszeilenschalter beschrieben, den WMI beim Wiederherstellen einer MOF-Datei aus diesem Registrierungsschlüssel nicht verwendet: **mofcomp -N:Root \\ Test mymof.mof**

    Sie können den Namespace jedoch mithilfe eines [Pragmabefehls](-pragma.md) in der MOF-Datei angeben.

    ```mof
    #pragma namespace ("\\\\.\\Root\\test")
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

 

 




