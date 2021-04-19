---
description: Listet die Zugriffs Typen des Policy-Objekts auf und beschreibt diese.
ms.assetid: 592dea65-9da1-4e49-82e4-8e08c451e026
title: Zugriffsrechte für Richtlinien Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e5c762955a4c53015241086b2249c5edbc4f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346295"
---
# <a name="policy-object-access-rights"></a>Zugriffsrechte für Richtlinien Objekte

Das [**Policy**](policy-object.md) -Objekt verfügt über die folgenden Objekt spezifischen Zugriffs Typen:



| Zugriffstyp                         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ lokale \_ Informationen zur Richtlinien Anzeige    | Dieser Zugriffstyp ist erforderlich, um die verschiedenen Sicherheitsrichtlinien Informationen des Zielsystems zu lesen. Dies umfasst das Standard Kontingent, die Überwachung, den Serverstatus und die Informationen zur Rolle sowie Informationen zur Vertrauensstellung. Dieser Zugriffstyp wird auch zum Auflisten vertrauenswürdiger Domänen, Konten und [*Berechtigungen*](/windows/desktop/SecGloss/p-gly)benötigt. |
| Richtlinie \_ get \_ private \_ Information   | Dieser Zugriffstyp ist erforderlich, um vertrauliche Informationen anzuzeigen, z. b. die Namen der Konten, die für vertrauenswürdige Domänen Beziehungen hergestellt wurden                                                                                                                                                                                                                              |
| Richtlinien \_ Vertrauensstellungs \_ Administrator                | Dieser Zugriffstyp ist erforderlich, um die Informationen zur Konto Domäne oder zur primären Domäne zu ändern.                                                                                                                                                                                                                                                                             |
| \_ \_ Standard \_ Kontingent \_ Limits für Richtlinien festlegen | Legen Sie die standardmäßigen System Kontingente fest, die auf Benutzerkonten angewendet werden.                                                                                                                                                                                                                                                                                                   |
| Richtlinie \_ Create \_ Secret              | Dieser Zugriffstyp ist erforderlich, um ein neues privates Datenobjekt zu erstellen.                                                                                                                                                                                                                                                                                                    |
| Konto für die Richtlinien \_ Erstellung \_             | Dieser Zugriffstyp wird zum Erstellen eines neuen [**Konto**](account-object.md) Objekts benötigt.                                                                                                                                                                                                                                                                               |
| Richtlinien \_ Satz-Überwachungs \_ \_ Anforderungen    | Dieser Zugriffstyp ist erforderlich, um die Überwachungsanforderungen des Systems zu aktualisieren.                                                                                                                                                                                                                                                                                      |
| Richtlinien \_ Überwachungs \_ Protokoll- \_ Administrator           | Dieser Zugriffstyp wird benötigt, um die Eigenschaften des Überwachungs Pfads zu ändern, z. b. die maximale Größe oder die Beibehaltungs Dauer für Überwachungsdaten Sätze, oder um das Protokoll zu löschen.                                                                                                                                                                                               |
| Überwachungsinformationen für die Richtlinien \_ Ansicht \_ \_    | Dieser Zugriffstyp ist erforderlich, um Informationen über Überwachungs Pfade oder Überwachungsanforderungen anzuzeigen.                                                                                                                                                                                                                                                                                  |
| Richtlinien \_ Server \_ Administrator               | Dieser Zugriffstyp ist erforderlich, um die Informationen zum Serverstatus oder zur Rolle (Master/Replica) zu ändern. Außerdem müssen die Informationen zur Replikat Quelle und zum Kontonamen geändert werden.                                                                                                                                                                                           |
| Namen der Richtlinien \_ Suche \_               | Dieser Zugriffstyp ist erforderlich, um zwischen Namen und SIDs zu übersetzen.                                                                                                                                                                                                                                                                                                    |
| \_ \_ Berechtigungs Erstellungs Berechtigung           | Noch nicht unterstützt.                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="generic-access-masks"></a>Generische Zugriffs Masken

Das [**Policy**](policy-object.md) -Objekt veröffentlicht die folgenden Zuordnungen von generischen Zugriffs Typen auf bestimmte Zugriffs Typen:

``` syntax
    GENERIC_READ    STANDARD_RIGHTS_READ |
                    POLICY_VIEW_AUDIT_INFORMATION |
                    POLICY_GET_PRIVATE_INFORMATION

    GENERIC_WRITE   STANDARD_RIGHTS_WRITE |
                    POLICY_TRUST_ADMIN |
                    POLICY_CREATE_ACCOUNT |
                    POLICY_CREATE_SECRET |
                    POLICY_CREATE_PRIVILEGE |
                    POLICY_SET_DEFAULT_QUOTA_LIMITS |
                    POLICY_SET_AUDIT_REQUIREMENTS |
                    POLICY_AUDIT_LOG_ADMIN |
                                        POLICY_SERVER_ADMIN

    GENERIC_EXECUTE STANDARD_RIGHTS_EXECUTE |
                    POLICY_VIEW_LOCAL_INFORMATION |
                    POLICY_LOOKUP_NAMES
```

## <a name="standard-access-types"></a>Standard Zugriffs Typen

Dieses Objekt unterstützt den (optionalen) Standard Zugriffstyp "synchronisieren" nicht. Alle erforderlichen Zugriffs Typen werden unterstützt. Die Maske aller unterstützten Zugriffs Typen für diesen Objekttyp lautet:

``` syntax
    POLICY_ALL_ACCESS STANDARD_RIGHTS_REQUIRED |
                    POLICY_VIEW_LOCAL_INFORMATION |
                    POLICY_VIEW_AUDIT_INFORMATION |
                    POLICY_GET_PRIVATE_INFORMATION |
                    POLICY_TRUST_ADMIN |
                    POLICY_CREATE_ACCOUNT |
                    POLICY_CREATE_SECRET |
                    POLICY_CREATE_PRIVILEGE |
                    POLICY_SET_DEFAULT_QUOTA_LIMITS |
                    POLICY_SET_AUDIT_REQUIREMENTS |
                    POLICY_AUDIT_LOG_ADMIN |
                    POLICY_SERVER_ADMIN
                    POLICY_LOOKUP_NAMES
```

 

 
