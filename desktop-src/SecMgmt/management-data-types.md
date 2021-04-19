---
description: Listet die Datentypen auf, die von den DLLs der Sicherheitskonfigurations-Anlage und deren unterstützenden Funktionen verwendet werden.
ms.assetid: 1d3bdf0d-320c-4b25-9e9b-fda134876979
title: Sicherheits Verwaltungs Datentypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae7efedb32ab545b903c61819042e32b7d83dbf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363501"
---
# <a name="security-management-data-types"></a>Sicherheits Verwaltungs Datentypen

Die Sicherheits Verwaltungs Datentypen umfassen Folgendes:

-   [Anlage Datentypen](#attachment-data-types)
-   [LSA-Richtlinien Datentypen](#lsa-policy-data-types)

## <a name="attachment-data-types"></a>Anlage Datentypen

Die folgenden Datentypen werden von den DLLs der Sicherheitskonfigurations-Anlage und deren unterstützenden Funktionen verwendet.



| Datentyp                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SCE- \_ \_ enumerationskontext**](sce-enumeration-context.md) | Wird von der [**pfsce- \_ Abfrage \_ Info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) -Funktion verwendet, um durch die Sicherheitsdatenbank zu navigieren.                                                                                                                                              |
| [**SCE- \_ handle**](sce-handle.md)                            | Wird von [**pfsce- \_ Abfrage \_ Informationen**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) und [**pfsce \_ Set \_ Info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) verwendet, um Informationen zwischen der Anlage und der Sicherheitsdatenbank zu übergeben.                                                                                 |
| [**Scestatus**](scestatus.md)                               | Der-Datentyp wird von der Sicherheitskonfigurations-Toolset-API verwendet, um Informationen zu den Ergebnissen eines Funktions Aufrufes zurückzugeben.                                                                                                                                    |
| [**scesvc- \_ handle**](scesvc-handle.md)                      | Wird von Methoden der Schnittstellen [**iscesvplattachmentdata**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) und [**iscesvplattachmentpersistinfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) verwendet, um Informationen zwischen dem Snap-in "Sicherheitskonfiguration" und der Snap-in-Erweiterung zu übergeben. |
| [**scesvc \_ - \_ Infotyp**](/windows/desktop/api/Scesvc/ne-scesvc-scesvc_info_type)               | Die Enumeration wird von [**pfsce- \_ Abfrage \_ Informationen**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) und [**pfsce \_ Set \_ Info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) verwendet, um den Typ der Informationen anzugeben, die von der Sicherheitsdatenbank angefordert oder an diese übermittelt wurden.                                                 |



 

## <a name="lsa-policy-data-types"></a>LSA-Richtlinien Datentypen

Die folgenden Datentypen werden von den LSA-Richtlinien Verwaltungsfunktionen verwendet.



| Datentyp                                                  | BESCHREIBUNG                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------|
| [**LSA- \_ \_ enumerationshandle**](lsa-enumeration-handle.md) | Dient zum Nachverfolgen von Enumerationen, bei denen mehrere Funktionsaufrufe erforderlich sind. |
| [**LSA- \_ handle**](lsa-handle.md)                          | Handle für ein [**Richtlinien**](policy-object.md) Objekt.                       |



 

 

 
