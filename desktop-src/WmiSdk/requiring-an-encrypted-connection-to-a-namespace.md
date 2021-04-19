---
description: Sie können anfordern, dass Client Skripts und-Anwendungen eine verschlüsselte Verbindung für die Authentifizierung herstellen, indem Sie den "Requirements sencryption"-Qualifizierer der MOF-Datei (Managed Object Format) hinzufügen, die den Namespace erstellt.
ms.assetid: 07b225a2-3834-4879-beae-f5b9180d112f
ms.tgt_platform: multiple
title: Eine verschlüsselte Verbindung mit einem Namespace ist erforderlich.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e42415c0f714f99a51d6a1a0ee1a0b22f398b1b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360848"
---
# <a name="requiring-an-encrypted-connection-to-a-namespace"></a>Eine verschlüsselte Verbindung mit einem Namespace ist erforderlich.

Sie können anfordern, dass Client Skripts und-Anwendungen eine verschlüsselte Verbindung für die Authentifizierung herstellen, indem Sie den "Requirements **sencryption** "-Qualifizierer der MOF-Datei (Managed Object Format) hinzufügen, die den Namespace erstellt.


Eine verschlüsselte Verbindung mit einem WMI-Namespace gibt die **\_ \_ \_ \_ Pkt- \_ Datenschutzebene** (oder **PKTPRIVACY** in einem Skript) der RPC-C-authn für die Authentifizierung an. Der **"** Requirements"-Qualifizierer bewirkt, dass WMI eingehende Datenanforderungen ablehnt, es sei denn, Sie verwenden explizit verschlüsselte Authentifizierung. Weitere Informationen finden Sie unter [Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von VBScript](setting-the-default-process-security-level-using-vbscript.md) oder [Festlegen der Authentifizierung mithilfe von C++](setting-authentication-using-c-.md).

Sie können auch einen vorhandenen Namespace ändern, indem Sie dieses Attribut hinzufügen und die MOF-Datei dann erneut kompilieren. "Requirements- **cryption** " wird in [*MOF*](gloss-m.md) mit der Namespace-Präprozessoranweisung " [pragma](pragma-namespace.md) " verwendet.

Im folgenden Verfahren wird der-Namespace so festgelegt, dass eine verschlüsselte Verbindung erforderlich ist.

**So legen Sie die erforderliche Verschlüsselung fest**

1.  Erstellen Sie eine Managed Object Format Datei (MOF), oder ändern Sie die vorhandene MOF-Datei, die den Namespace definiert.

    Das folgende Codebeispiel zeigt, wie der Namespace, der geändert wird, der Stamm *\\ MyNamespace* und die Datei den Namen *MyNamespace \_ Security. MOF* hat. "Requirements **sencryption** " weist einen booleschen Datentyp auf, sodass er auf " **true** " oder " **false**" festgelegt werden muss.

    ```mof
    #pragma namespace("\\\\.\\Root\\MyNamespace") 

    [RequiresEncryption(TRUE)] 
    instance of __systemSecurity { };
    ```

    

2.  Führen Sie [**mofcomp.exe**](mofcomp.md) aus, um die MOF-Datei zu kompilieren.

    **c: " \\ mynamespace" " \_ Security. mof"**

    Verwenden Sie in C++ die [**imuf Compiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) -Methoden.

WMI lehnt einen Client ab, der die Standard Authentifizierungs Ebene verwendet, da DCOM die Sicherheit auf die Ebene aushandiert, die für den Svchost-Prozess erforderlich ist, in dem der WMI-Dienst ausgeführt wird. Weitere Informationen zu Dienst Hosts finden Sie unter [Anbieter Hosting und-Sicherheit](provider-hosting-and-security.md). Weitere Informationen zum Festlegen von Authentifizierungs Ebenen beim Herstellen einer Verbindung mit WMI-Namespaces finden Sie unter [Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von C++](setting-the-default-process-security-level-using-c-.md), [Festlegen der Authentifizierung mithilfe von C++](setting-authentication-using-c-.md)oder [Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von VBScript](setting-the-default-process-security-level-using-vbscript.md).

Beim Zurückgeben von Daten in einer asynchronen Rückruf Verbindung gibt WMI die Meldung "Zugriff verweigert" an den anfordernden Computer zurück. WMI erstellt auch einen Protokolleintrag im NT-Ereignisprotokoll des Computers mit dem verschlüsselten Namespace, der besagt, dass keine sichere Verbindung mit dem Client hergestellt werden kann.

Ab Windows Vista ist die Datei "wbemcore. log" nicht mehr vorhanden. Sie können das NT-Ereignisprotokoll auf Einträge überprüfen, die auf abgelehnte eingehende Datenanforderungen an Namespaces hindeuten, die eine Verschlüsselung erfordern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen von namepace-Sicherheits Deskriptoren](setting-namespace-security-descriptors.md)
</dt> <dt>

[**Wbemauthenticationlevelerum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[Sichern einer Remote-WMI-Verbindung](securing-a-remote-wmi-connection.md)
</dt> </dl>

 

 



