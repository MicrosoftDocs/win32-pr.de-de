---
description: Eine Anwendung kann die Zugriffssteuerungsliste eines Objekts nur ändern, wenn die Anwendung dazu über die Rechte verfügt.
ms.assetid: 5f710fd8-33de-47c0-a8b2-baf3008c4ed7
title: Zugriffsrechte für Access-Token Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac3145aef5fcf3a20f2569ac02df0de0638c2be1f42f5e1a74785d8ae1aedb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785473"
---
# <a name="access-rights-for-access-token-objects"></a>Zugriffsrechte für Access-Token Objekte

Eine Anwendung kann die Zugriffssteuerungsliste eines Objekts nur ändern, wenn die Anwendung dazu über die Rechte verfügt. Diese Rechte werden durch eine Sicherheitsbeschreibung im Zugriffstoken für das Objekt gesteuert. Weitere Informationen zur Sicherheit finden Sie unter [Access Control Model](access-control-model.md).

Rufen Sie zum Abrufen oder Festlegen [](/windows/desktop/SecGloss/a-gly)der [Sicherheitsbeschreibung](security-descriptors.md) für ein Zugriffstoken die [**Funktionen GetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity) und [**SetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity) auf.

Wenn Sie die [**OpenProcessToken-**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) oder [**OpenThreadToken-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) aufrufen, um ein [](access-rights-and-access-masks.md) Handle für ein Zugriffstoken abzurufen, überprüft das System die angeforderten Zugriffsrechte mit der DACL im Sicherheitsdeskriptor des Tokens.

Im Folgenden finden Sie gültige Zugriffsrechte für Zugriffstokenobjekte:

-   Die Standardzugriffsrechte DELETE, READ \_ CONTROL, WRITE DAC und \_ WRITE OWNER \_ . [](standard-access-rights.md) Zugriffstoken unterstützen das SYNCHRONIZE-Standardzugriffsrecht nicht.
-   Das [ACCESS \_ SYSTEM \_ SECURITY-Recht](sacl-access-right.md) zum Erhalten oder Festlegen der SACL im Sicherheitsdeskriptor des Objekts.
-   Die spezifischen Zugriffsrechte für Zugriffstoken, die in der folgenden Tabelle aufgeführt sind.

    | Wert                     | Bedeutung                                                                                                                                                                                                                                                                           |
    |---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | STANDARDEINSTELLUNG \_ FÜR \_ TOKEN ANPASSEN    | Erforderlich, um den Standardbesitzer, die primäre Gruppe oder die DACL eines Zugriffstokens zu ändern.                                                                                                                                                                                                  |
    | TOKEN \_ ANPASSEN VON \_ GRUPPEN     | Erforderlich, um die Attribute der Gruppen in einem Zugriffstoken anzupassen.                                                                                                                                                                                                               |
    | BERECHTIGUNGEN \_ ZUM ANPASSEN VON \_ TOKEN | Erforderlich, um die Berechtigungen in einem Zugriffstoken zu aktivieren oder zu deaktivieren.                                                                                                                                                                                                                  |
    | TOKEN \_ ADJUST \_ SESSIONID  | Erforderlich, um die Sitzungs-ID eines Zugriffstokens anzupassen. Die SE \_ TCB \_ NAME-Berechtigung ist erforderlich.                                                                                                                                                                                    |
    | TOKEN \_ ASSIGN \_ PRIMARY    | Erforderlich, um ein [*primäres Token an*](/windows/desktop/SecGloss/p-gly) einen Prozess [*anfügen zu können.*](/windows/desktop/SecGloss/p-gly) Die SE \_ ASSIGNPRIMARYTOKEN \_ NAME ist ebenfalls erforderlich, um diese Aufgabe auszuführen. |
    | \_TOKENDUPLIZIEREN          | Erforderlich, um ein Zugriffstoken zu duplizieren.                                                                                                                                                                                                                                            |
    | TOKEN \_ EXECUTE            | Identisch mit STANDARD \_ RIGHTS \_ EXECUTE.                                                                                                                                                                                                                                                |
    | TOKEN \_ IMPERSONATE        | Erforderlich, um ein Identitätswechsel-Zugriffstoken an einen Prozess anfügen zu können.                                                                                                                                                                                                                    |
    | \_TOKENABFRAGE              | Erforderlich zum Abfragen eines Zugriffstokens.                                                                                                                                                                                                                                                |
    | \_ \_ TOKENABFRAGEQUELLE      | Erforderlich zum Abfragen der Quelle eines Zugriffstokens.                                                                                                                                                                                                                                  |
    | \_TOKENLESE               | Kombiniert STANDARD \_ RIGHTS READ und TOKEN \_ \_ QUERY.                                                                                                                                                                                                                                 |
    | TOKEN \_ WRITE              | Kombiniert STANDARD \_ RIGHTS \_ WRITE, TOKEN \_ ADJUST \_ PRIVILEGES, TOKEN \_ ADJUST GROUPS und TOKEN ADJUST \_ \_ \_ DEFAULT.                                                                                                                                                                   |
    | TOKEN \_ ALL \_ ACCESS        | Kombiniert alle möglichen Zugriffsrechte für ein Token.                                                                                                                                                                                                                                  |

    

     

 

 
