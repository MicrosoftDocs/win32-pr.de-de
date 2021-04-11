---
description: Listet die Enumerationen auf, die von den LSA-Richtlinien Verwaltungsfunktionen verwendet werden.
ms.assetid: f4fd2a61-61bc-44d2-b01f-3ca07699bcb8
title: Sicherheitsverwaltungs-Enumerationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39bec2cdd731e2a3befe75e543f692d93bc5d9ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216193"
---
# <a name="security-management-enumerations"></a>Sicherheitsverwaltungs-Enumerationen

Die Sicherheitsverwaltungs-Enumerationen umfassen Folgendes:

-   [LSA-Richtlinien Enumerationen](#lsa-policy-enumerations)
-   [Sicherere Enumerationen](#safer-enumerations)

## <a name="lsa-policy-enumerations"></a>LSA-Richtlinien Enumerationen

Die folgenden Enumerationstypen werden von den LSA-Richtlinien Verwaltungsfunktionen verwendet.



| Enumeration                                                                               | Beschreibung                                                                                                                           |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**Richtlinien Überwachungs- \_ \_ \_ Ereignistyp**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_audit_event_type)                             | Definiert die Arten von Ereignissen, die das System überwachen kann.                                                                                     |
| [**Richtlinien \_ Informations \_ Klasse**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_information_class)                            | Definiert die Typen von Informationen, die für ein [**Richtlinien**](policy-object.md) Objekt festgelegt oder abgefragt werden können.                             |
| [**LSA-Richtlinien- \_ \_ Server \_ Rolle**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_lsa_server_role)                               | Geben Sie die Rolle eines LSA-Servers an.                                                                                                   |
| [**Richtlinien \_ Benachrichtigungs \_ Informations \_ Klasse**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_notification_information_class) | Definiert die Typen von Richtlinien Informationen und Informationen zur Richtlinien Domäne, für die Ihre Anwendung eine Benachrichtigung über Änderungen anfordern kann. |
| [**Richtlinien \_ Server \_ \_ Status aktivieren**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_server_enable_state)                       | Stellt den Status des LSA-Servers dar, d. h. ob er aktiviert oder deaktiviert ist.                                                   |
| [**vertrauenswürdige \_ Informations \_ Klasse**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-trusted_information_class)                          | Definiert die Typen von Informationen, die für eine vertrauenswürdige Domäne festgelegt oder abgefragt werden können.                                                     |



 

## <a name="safer-enumerations"></a>Sicherere Enumerationen

[Sicherer](safer.md) verwendet die folgenden Enumerationstypen.



| Name                                                               | BESCHREIBUNG                                                                                                                                                                                      |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**sicherere \_ Identifikations \_ Typen**](/windows/desktop/api/WinSafer/ne-winsafer-safer_identification_types) | Enumerationstyp, der die möglichen Typen von Identifikations Regel Strukturen definiert, die von der [**sicheren \_ Identifikations \_ Header**](/windows/desktop/api/WinSafer/ns-winsafer-safer_identification_header) Struktur identifiziert werden können. |
| [**sicherere \_ Objekt \_ Informations \_ Klasse**](/windows/desktop/api/WinSafer/ne-winsafer-safer_object_info_class)      | Enumerationstyp, der den Typ der angeforderten Informationen zu einem sichereren Objekt definiert.                                                                                                            |
| [**\_ \_ Informations Klasse der sichereren Richtlinie \_**](/windows/desktop/api/WinSafer/ne-winsafer-safer_policy_info_class)      | Enumerationstyp, der die Art und Weise definiert, in der eine Richtlinie abgefragt werden kann.                                                                                                                         |



 

 

 



