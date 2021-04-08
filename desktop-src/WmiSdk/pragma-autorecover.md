---
description: Fügt eine MOF-Datei zur Liste der Dateien hinzu, die während der Wiederherstellung des Repository kompiliert wurden.
ms.assetid: 8901c04e-f8c1-45b0-b69d-e2ebc948f088
ms.tgt_platform: multiple
title: pragma-Auto Wiederherstellen
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
ms.openlocfilehash: 9bb1cfca44e0bc5437d05d721ffcd57203e5aa9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960436"
---
# <a name="pragma-autorecover"></a>pragma-Auto Wiederherstellen

Der Präprozessorbefehl **pragma Auto Wiederherstellen** fügt eine MOF-Datei zur Liste der Dateien hinzu, die während der Wiederherstellung des Repository kompiliert wurden. Die Liste der **Auto Wiederherstellen** -MOF-Dateien wird in diesem Registrierungsschlüssel gespeichert:

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **Auto Wiederherstellen-mufs**

WMI prüft die Integrität des WMI-Repository, wenn das Betriebssystem WMI startet. Wenn das Repository beschädigt ist, erstellt WMI das Repository automatisch neu und kompiliert alle MOF-Dateien, die in diesem Schlüssel in der Registrierung aufgeführt sind.

Im folgenden wird die Syntax für den Pragma Auto Wiederherstellen-Befehl beschrieben:


```mof
#pragma autorecover
```



Beachten Sie jedoch die folgenden Einschränkungen, wenn Sie diesen Befehl verwenden:

-   WMI kann keine MOF-Dateien wiederherstellen, die sich auf einem Remote Computer befinden.

    Daher müssen sich die MOF-Dateien, die in diesem Registrierungsschlüssel aufgelistet sind, auf dem lokalen Computer befinden.

-   Sie können nicht die Befehls Zeilenschalter angeben, die der MOF-Compiler verwendet, wenn eine MOF-Datei von WMI wieder hergestellt wird.

    Daher sollten Sie [pragma](-pragma.md) -Befehle in die MOF-Datei einschließen, die Befehls Zeilenschalter unnötig machen. Im folgenden Beispiel wird ein allgemeiner Befehls Zeilenschalter beschrieben, der von WMI nicht verwendet wird, wenn eine MOF-Datei aus diesem Registrierungsschlüssel wieder hergestellt wird: " **mufcomp-n:root \\ Test mymof. mof".**

    Sie können den Namespace jedoch mit einem [pragma](-pragma.md) -Befehl in der MOF-Datei angeben.

    ```mof
    #pragma namespace ("\\\\.\\Root\\test")
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

 

 




