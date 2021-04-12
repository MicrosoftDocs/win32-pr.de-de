---
description: Eine Anwendung kann die Zugriffs Steuerungs Liste eines Objekts nur dann ändern, wenn die Anwendung über die entsprechenden Rechte verfügt.
ms.assetid: 5f710fd8-33de-47c0-a8b2-baf3008c4ed7
title: Zugriffsrechte für Access-Token Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb6a62a8c1518dca30f2abbc4481fa5e11cf081
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345149"
---
# <a name="access-rights-for-access-token-objects"></a>Zugriffsrechte für Access-Token Objekte

Eine Anwendung kann die Zugriffs Steuerungs Liste eines Objekts nur dann ändern, wenn die Anwendung über die entsprechenden Rechte verfügt. Diese Rechte werden von einer Sicherheits Beschreibung im Zugriffs Token für das-Objekt gesteuert. Weitere Informationen zur Sicherheit finden Sie unter [Access Control Modell](access-control-model.md).

Um die [Sicherheits Beschreibung](security-descriptors.md) für ein [*Zugriffs Token*](/windows/desktop/SecGloss/a-gly)abzurufen oder festzulegen, müssen Sie die Funktionen [**getkernelobjectsecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity) und [**setkernelobjectsecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity) aufrufen.

Wenn Sie die [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) -Funktion oder die [**openthletotokenfunktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) aufrufen, um ein Handle für ein Zugriffs Token abzurufen, überprüft das System die angeforderten [Zugriffsrechte](access-rights-and-access-masks.md) auf die DACL in der Sicherheits Beschreibung des Tokens.

Im folgenden finden Sie gültige Zugriffsrechte für Access-Token-Objekte:

-   Die \_ \_ \_ [Standard Zugriffsrechte](standard-access-rights.md)für das Löschen, lesen, schreiben und Schreiben von Besitzern. Zugriffs Token unterstützen das Standard Zugriffsrecht synchronisieren nicht.
-   Das [ \_ \_ Sicherheitsrecht des Zugriffs Systems zum Abrufen](sacl-access-right.md) oder Festlegen der SACL in der Sicherheits Beschreibung des Objekts.
-   Die spezifischen Zugriffsrechte für Zugriffs Token, die in der folgenden Tabelle aufgeführt sind.

    | Wert                     | Bedeutung                                                                                                                                                                                                                                                                           |
    |---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | \_ \_ Standardeinstellung für Token anpassen    | Erforderlich, um den Standard Besitzer, die primäre Gruppe oder die DACL eines Zugriffs Tokens zu ändern.                                                                                                                                                                                                  |
    | tokenanpassungsgruppen \_ \_     | Erforderlich, um die Attribute der Gruppen in einem Zugriffs Token anzupassen.                                                                                                                                                                                                               |
    | Token zum Anpassen von Token \_ \_ | Erforderlich, um die Berechtigungen in einem Zugriffs Token zu aktivieren oder zu deaktivieren.                                                                                                                                                                                                                  |
    | \_SessionID für tokenanpassung \_  | Erforderlich, um die Sitzungs-ID eines Zugriffs Tokens anzupassen. Die SE \_ TCB- \_ namens Berechtigung ist erforderlich.                                                                                                                                                                                    |
    | \_primär Token zuweisen \_    | Ist erforderlich, um ein [*primäres Token*](/windows/desktop/SecGloss/p-gly) an einen [*Prozess*](/windows/desktop/SecGloss/p-gly)anzufügen. \_ \_ Zum Ausführen dieser Aufgabe ist auch die Name-Berechtigung "SE zubenenname" erforderlich. |
    | Token \_ Duplizieren          | Erforderlich, um ein Zugriffs Token zu duplizieren.                                                                                                                                                                                                                                            |
    | Token \_ Ausführen            | Kombiniert Standard \_ Rechte \_ Execute-und Token-Identitätswechsel \_ .                                                                                                                                                                                                                        |
    | Token-Identitätswechsel \_        | Erforderlich, um ein Identitätswechsel-Zugriffs Token an einen Prozess anzufügen.                                                                                                                                                                                                                    |
    | \_tokenabfrage              | Erforderlich, um ein Zugriffs Token abzufragen.                                                                                                                                                                                                                                                |
    | \_tokenfragequelle \_      | Erforderlich, um die Quelle eines Zugriffs Tokens abzufragen.                                                                                                                                                                                                                                  |
    | \_tokenlese Vorgang               | Kombiniert Standard \_ Rechte für \_ Lese-und \_ tokenabfragen.                                                                                                                                                                                                                                 |
    | \_tokenschreib Vorgang              | Kombiniert Standard \_ Rechte \_ schreiben, Token- \_ Anpassungs \_ Berechtigungen, tokenanpassungsgruppen und Standardeinstellungen für die \_ \_ tokenanpassung \_ \_ .                                                                                                                                                                   |
    | Token für den \_ gesamten \_ Zugriff        | Kombiniert alle möglichen Zugriffsrechte für ein Token.                                                                                                                                                                                                                                  |

    

     

 

 
