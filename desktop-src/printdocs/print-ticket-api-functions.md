---
description: Die folgenden Funktionen werden zum Verwalten von Drucktickets verwendet.
ms.assetid: 9e942a1d-660b-4691-9282-ffb49e0b9848
title: Druckticket-API-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a908da3aee9e9fa1c3b7181261164860be95193cb4dc0d34a7fe17e6f2a4bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033918"
---
# <a name="print-ticket-api-functions"></a>Druckticket-API-Funktionen

Die folgenden Funktionen werden zum Verwalten von Drucktickets verwendet.

## <a name="in-this-section"></a>In diesem Abschnitt



| Funktion                                                                                  | Beschreibung                                                                                                                                            |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ConvertDevModeToPrintTicketThunk2**](convertdevmodetoprintticketthunk2.md)<br/> | Konvertiert eine [**DEVMODE-Struktur**](/windows/win32/api/wingdi/ns-wingdi-devmodea) in ein Druckticket.<br/>                                                                          |
| [**ConvertPrintTicketToDevModeThunk2**](convertprinttickettodevmodethunk2.md)<br/> | Konvertiert ein Druckticket in eine [**DEVMODE-Struktur.**](/windows/win32/api/wingdi/ns-wingdi-devmodea)<br/>                                                                          |
| [**MergeAndValidatePrintTicketThunk2**](mergeandvalidateprintticketthunk2.md)<br/> | Führt zwei Drucktickets zusammen und gibt ein gültiges, gültiges Druckticket zurück.<br/>                                                                          |
| [**PTCloseProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider)<br/>                                     | Schließt ein Handle des Druckticketanbieters.<br/>                                                                                                      |
| [**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket)<br/>         | Konvertiert eine [**DEVMODE-Struktur**](/windows/win32/api/wingdi/ns-wingdi-devmodea) in ein Druckticket in einem [**IStream.**](/windows/desktop/Stg/istream-compound-file-implementation)<br/>        |
| [**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode)<br/>         | Konvertiert ein Druckticket in eine [**DEVMODE-Struktur.**](/windows/win32/api/wingdi/ns-wingdi-devmodea)<br/>                                                                        |
| [**PTGetPrintCapabilities**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities)<br/>                       | Ruft die Funktionen des Druckers ab, die in Übereinstimmung mit dem XML-Druckschema [formatiert sind.](./printschema.md)<br/>                   |
| [**PTGetPrintDeviceCapabilities**](/windows/win32/api/prntvpt/nf-prntvpt-ptgetprintdevicecapabilities)<br/>    | Ruft die Funktionen des Gerätedruckers ab, die in Übereinstimmung mit dem XML-Druckschema [formatiert sind.](./printschema.md)<br/>            |
| [**PTGetPrintDeviceResources**](/windows/win32/api/prntvpt/nf-prntvpt-ptgetprintdeviceresources)<br/>          | Es ruft die Druckgeräteressourcen für einen Drucker ab, der in Übereinstimmung mit dem XML-Druckschema [formatiert ist.](./printschema.md)<br/> |
| [**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket)<br/>         | Führt zwei Drucktickets zusammen und gibt ein gültiges, gültiges Druckticket zurück.<br/>                                                                          |
| [**PTOpenProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenprovider)<br/>                                       | Öffnet eine Instanz eines Druckticketanbieters.<br/>                                                                                               |
| [**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex)<br/>                                   | Öffnet eine Instanz eines Druckticketanbieters.<br/>                                                                                               |
| [**PTQuerySchemaVersionSupport**](/windows/desktop/api/prntvpt/nf-prntvpt-ptqueryschemaversionsupport)<br/>             | Ruft die höchste (neueste) [](./printschema.md) Version des Druckschemas ab, die der angegebene Drucker unterstützt.<br/>           |
| [**PTReleaseMemory**](/windows/desktop/api/prntvpt/nf-prntvpt-ptreleasememory)<br/>                                     | Gibt Puffer frei, die Drucktickets und Druckfunktionen zugeordnet sind.<br/>                                                                      |
| [**UnbindPTProviderThunk**](unbindptproviderthunk.md)<br/>                         | Schließt ein Handle für einen Druckticketanbieter.<br/>                                                                                                 |



 

 

