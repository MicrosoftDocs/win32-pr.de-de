---
description: Listet die Datentypen auf, die von den Sicherheitskonfigurations-Anlagen-DLLs und ihren unterstützenden Funktionen verwendet werden.
ms.assetid: 1d3bdf0d-320c-4b25-9e9b-fda134876979
title: Security Management-Datentypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c23c22ef996f54a9664dfa128a90fdb0c2825d60b68b7deafe7534d2b3b05737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117969017"
---
# <a name="security-management-data-types"></a>Security Management-Datentypen

Die Sicherheitsverwaltungsdatentypen umfassen Folgendes:

-   [Anlagendatentypen](#attachment-data-types)
-   [LSA-Richtliniendatentypen](#lsa-policy-data-types)

## <a name="attachment-data-types"></a>Anlagendatentypen

Die folgenden Datentypen werden von den Sicherheitskonfigurations-Anlagen-DLLs und ihren unterstützenden Funktionen verwendet.



| Datentyp                                                    | Beschreibung                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_SCE-ENUMERATIONSKONTEXT \_**](sce-enumeration-context.md) | Wird von der [**PFSCE \_ QUERY \_ INFO-Funktion**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) verwendet, um durch die Sicherheitsdatenbank zu navigieren.                                                                                                                                              |
| [**\_SCE-HANDLE**](sce-handle.md)                            | Wird von [**PFSCE \_ QUERY INFO \_ und**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) [**PFSCE \_ SET \_ INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) verwendet, um Informationen zwischen der Anlage und der Sicherheitsdatenbank zu übergeben.                                                                                 |
| [**SCESTATUS**](scestatus.md)                               | Der Datentyp wird von der API zum Festlegen des Sicherheitskonfigurationstools verwendet, um Informationen zu den Ergebnissen eines Funktionsaufrufs zurück zu geben.                                                                                                                                    |
| [**SCESVC-HANDLE \_**](scesvc-handle.md)                      | Wird von Methoden der [**Schnittstellen ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) und [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) verwendet, um Informationen zwischen dem Sicherheitskonfigurations-Snap-In und der Snap-In-Erweiterung zu übergeben. |
| [**\_SCESVC-INFORMATIONSTYP \_**](/windows/desktop/api/Scesvc/ne-scesvc-scesvc_info_type)               | Die Enumeration wird von [**PFSCE \_ QUERY \_ INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) und [**PFSCE \_ SET \_ INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) verwendet, um den Typ der Informationen anzugeben, die von der Sicherheitsdatenbank angefordert oder an diese übergeben werden.                                                 |



 

## <a name="lsa-policy-data-types"></a>LSA-Richtliniendatentypen

Die folgenden Datentypen werden von den LSA-Richtlinienverwaltungsfunktionen verwendet.



| Datentyp                                                  | Beschreibung                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------|
| [**\_LSA-ENUMERATIONSHANDL \_**](lsa-enumeration-handle.md) | Wird zum Nachverfolgen von Enumerationen verwendet, in denen mehrere Funktionsaufrufe erforderlich sind. |
| [**LSA \_ HANDLE**](lsa-handle.md)                          | Handle für ein [**Policy-Objekt.**](policy-object.md)                       |



 

 

 
