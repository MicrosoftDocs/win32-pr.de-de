---
description: Listet die Zugriffstypen des Richtlinienobjekts auf und beschreibt sie.
ms.assetid: 592dea65-9da1-4e49-82e4-8e08c451e026
title: Zugriffsrechte für Richtlinienobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ae22db51c28e76e7122a1f7baf781671d9cc445e253fb6df7d63f87e3f7e921
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005098"
---
# <a name="policy-object-access-rights"></a>Zugriffsrechte für Richtlinienobjekte

Das [**Policy-Objekt**](policy-object.md) verfügt über die folgenden objektspezifischen Zugriffstypen:



| Zugriffstyp                         | Beschreibung                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RICHTLINIENANSICHT \_ \_ : LOKALE \_ INFORMATIONEN    | Dieser Zugriffstyp ist erforderlich, um die verschiedenen Sicherheitsrichtlinieninformationen des Zielsystems zu lesen. Dies schließt die Standardkontingent-, Überwachungs-, Serverstatus- und Rolleninformationen sowie Vertrauensinformationen ein. Dieser Zugriffstyp ist auch erforderlich, um vertrauenswürdige Domänen, Konten und [*Berechtigungen*](/windows/desktop/SecGloss/p-gly)aufzuzählen. |
| RICHTLINIE \_ ABRUFEN \_ PRIVATER \_ INFORMATIONEN   | Dieser Zugriffstyp ist erforderlich, um vertrauliche Informationen anzuzeigen, z. B. die Namen von Konten, die für vertrauenswürdige Domänenbeziehungen eingerichtet wurden.                                                                                                                                                                                                                              |
| ADMINISTRATOR \_ DER RICHTLINIENVERTRAUENSSTELLUNG \_                | Dieser Zugriffstyp ist erforderlich, um die Informationen zur Kontodomäne oder zur primären Domäne zu ändern.                                                                                                                                                                                                                                                                             |
| \_ \_ RICHTLINIENSATZ– \_ \_ STANDARDKONTINGENTGRENZEN | Legen Sie die Standardsystemkontingente fest, die auf Benutzerkonten angewendet werden.                                                                                                                                                                                                                                                                                                   |
| POLICY \_ CREATE \_ SECRET              | Dieser Zugriffstyp ist erforderlich, um ein neues Private Data-Objekt zu erstellen.                                                                                                                                                                                                                                                                                                    |
| POLICY \_ CREATE \_ ACCOUNT             | Dieser Zugriffstyp ist erforderlich, um ein neues [**Kontoobjekt**](account-object.md) zu erstellen.                                                                                                                                                                                                                                                                               |
| \_ÜBERWACHUNGSANFORDERUNGEN FÜR RICHTLINIENSATZ \_ \_    | Dieser Zugriffstyp ist erforderlich, um die Überwachungsanforderungen des Systems zu aktualisieren.                                                                                                                                                                                                                                                                                      |
| \_ \_ \_ RICHTLINIENÜBERWACHUNGSPROTOKOLLADMINISTRATOR           | Dieser Zugriffstyp ist erforderlich, um die Merkmale des Überwachungspfads zu ändern, z. B. die maximale Größe oder den Aufbewahrungszeitraum für Überwachungsdatensätze, oder um das Protokoll zu löschen.                                                                                                                                                                                               |
| RICHTLINIENANSICHT \_ \_ – \_ ÜBERWACHUNGSINFORMATIONEN    | Dieser Zugriffstyp ist erforderlich, um Überwachungspfad- oder Überwachungsanforderungsinformationen anzuzeigen.                                                                                                                                                                                                                                                                                  |
| \_ \_ RICHTLINIENSERVERADMINISTRATOR               | Dieser Zugriffstyp ist erforderlich, um die Serverstatus- oder Rolleninformationen (Master/Replikat) zu ändern. Es ist auch erforderlich, die Informationen zur Replikatquelle und zum Kontonamen zu ändern.                                                                                                                                                                                           |
| \_RICHTLINIENS \_ LOOKUP-NAMEN               | Dieser Zugriffstyp ist erforderlich, um zwischen Namen und SIDs zu übersetzen.                                                                                                                                                                                                                                                                                                    |
| BERECHTIGUNG ZUM ERSTELLEN VON RICHTLINIEN \_ \_           | Noch nicht unterstützt.                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="generic-access-masks"></a>Generische Zugriffsmasken

Das [**Policy-Objekt**](policy-object.md) veröffentlicht die folgenden Zuordnungen von generischen Zugriffstypen zu bestimmten Zugriffstypen:

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

## <a name="standard-access-types"></a>Standardzugriffstypen

Dieses Objekt unterstützt den (optionalen) SYNCHRONIZE-Standardzugriffstyp nicht. Alle erforderlichen Zugriffstypen werden unterstützt. Die Maske aller unterstützten Zugriffstypen für diesen Objekttyp lautet:

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

 

 
