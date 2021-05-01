---
description: Eine Anwendung kann die Zugriffssteuerungsliste eines Objekts nur ändern, wenn die Anwendung über die dafüren Rechte verfügt.
ms.assetid: 5f710fd8-33de-47c0-a8b2-baf3008c4ed7
title: Zugriffsrechte für Access-Token-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 469081d2caa4e5ff7c9b7c55b4c09c31cff1acac
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327195"
---
# <a name="access-rights-for-access-token-objects"></a>Zugriffsrechte für Access-Token-Objekte

Eine Anwendung kann die Zugriffssteuerungsliste eines Objekts nur ändern, wenn die Anwendung über die dafüren Rechte verfügt. Diese Rechte werden durch einen Sicherheitsdeskriptor im Zugriffstoken für das Objekt gesteuert. Weitere Informationen zur Sicherheit finden Sie unter [Access Control Model](access-control-model.md).

Um die [Sicherheitsbeschreibung](security-descriptors.md) für ein [*Zugriffstoken*](/windows/desktop/SecGloss/a-gly)abzurufen oder festzulegen, rufen Sie die Funktionen [**GetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity) und [**SetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity) auf.

Wenn Sie die [**OpenProcessToken-**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) oder [**OpenThreadToken-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) aufrufen, um ein Handle für ein Zugriffstoken abzurufen, überprüft das System die angeforderten [Zugriffsrechte](access-rights-and-access-masks.md) anhand der DACL im Sicherheitsdeskriptor des Tokens.

Im Folgenden sind gültige Zugriffsrechte für Zugriffstokenobjekte enthalten:

-   Die \_ Standardzugriffsrechte DELETE, READ CONTROL, WRITE \_ DAC und WRITE \_ OWNER. [](standard-access-rights.md) Zugriffstoken unterstützen das SYNCHRONIZE-Standardzugriffsrecht nicht.
-   Das [ACCESS \_ SYSTEM \_ SECURITY-Recht](sacl-access-right.md) zum Abrufen oder Festlegen der SACL im Sicherheitsdeskriptor des Objekts.
-   Die spezifischen Zugriffsrechte für Zugriffstoken, die in der folgenden Tabelle aufgeführt sind.

    | Wert                     | Bedeutung                                                                                                                                                                                                                                                                           |
    |---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | \_ \_ TOKENANPASSUNGSSTANDARD    | Erforderlich, um den Standardbesitzer, die primäre Gruppe oder die DACL eines Zugriffstokens zu ändern.                                                                                                                                                                                                  |
    | ANPASSEN \_ VON \_ TOKENGRUPPEN     | Erforderlich, um die Attribute der Gruppen in einem Zugriffstoken anzupassen.                                                                                                                                                                                                               |
    | ANPASSEN \_ VON BERECHTIGUNGEN FÜR TOKEN \_ | Erforderlich, um die Berechtigungen in einem Zugriffstoken zu aktivieren oder zu deaktivieren.                                                                                                                                                                                                                  |
    | \_ \_ TOKENANPASSUNGSSITZUNGS-ID  | Erforderlich, um die Sitzungs-ID eines Zugriffstokens anzupassen. Die SE \_ TCB \_ NAME-Berechtigung ist erforderlich.                                                                                                                                                                                    |
    | TOKEN \_ ASSIGN \_ PRIMARY    | Erforderlich, um ein [*primäres Token an*](/windows/desktop/SecGloss/p-gly) einen Prozess [*anfügen zu können.*](/windows/desktop/SecGloss/p-gly) Für diese Aufgabe ist auch die \_ SE ASSIGNPRIMARYTOKEN \_ NAME-Berechtigung erforderlich. |
    | \_TOKENDUPLIZIEREN          | Erforderlich, um ein Zugriffstoken zu duplizieren.                                                                                                                                                                                                                                            |
    | TOKEN \_ EXECUTE            | Identisch mit STANDARD \_ RIGHTS \_ EXECUTE.                                                                                                                                                                                                                                                |
    | TOKEN \_ IMPERSONATE        | Erforderlich, um ein Identitätswechsel-Zugriffstoken an einen Prozess anfügen zu können.                                                                                                                                                                                                                    |
    | \_TOKENABFRAGE              | Erforderlich zum Abfragen eines Zugriffstokens.                                                                                                                                                                                                                                                |
    | \_ \_ TOKENABFRAGEQUELLE      | Erforderlich zum Abfragen der Quelle eines Zugriffstokens.                                                                                                                                                                                                                                  |
    | \_TOKENLESE               | Kombiniert STANDARD \_ RIGHTS READ und TOKEN \_ \_ QUERY.                                                                                                                                                                                                                                 |
    | TOKEN \_ WRITE              | Kombiniert STANDARD \_ RIGHTS \_ WRITE, TOKEN \_ ADJUST \_ PRIVILEGES, TOKEN \_ ADJUST GROUPS und TOKEN ADJUST \_ \_ \_ DEFAULT.                                                                                                                                                                   |
    | TOKEN \_ ALL \_ ACCESS        | Kombiniert alle möglichen Zugriffsrechte für ein Token.                                                                                                                                                                                                                                  |

    

     

 

 
