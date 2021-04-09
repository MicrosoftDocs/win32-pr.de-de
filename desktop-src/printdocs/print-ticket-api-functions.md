---
description: Die folgenden Funktionen werden zum Verwalten von Druck Tickets verwendet.
ms.assetid: 9e942a1d-660b-4691-9282-ffb49e0b9848
title: Druckticket-API-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5dfda941d0b0f7d99b0ffbef703a98e357ccc6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866176"
---
# <a name="print-ticket-api-functions"></a>Druckticket-API-Funktionen

Die folgenden Funktionen werden zum Verwalten von Druck Tickets verwendet.

## <a name="in-this-section"></a>In diesem Abschnitt



| Funktion                                                                                  | BESCHREIBUNG                                                                                                                                            |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ConvertDevModeToPrintTicketThunk2**](convertdevmodetoprintticketthunk2.md)<br/> | Konvertiert eine [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur in ein Druck Ticket.<br/>                                                                          |
| [**ConvertPrintTicketToDevModeThunk2**](convertprinttickettodevmodethunk2.md)<br/> | Konvertiert ein Druck Ticket in eine [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur.<br/>                                                                          |
| [**MergeAndValidatePrintTicketThunk2**](mergeandvalidateprintticketthunk2.md)<br/> | Führt zwei Druck Tickets zusammen und gibt ein gültiges, brauchbares Druck Ticket zurück.<br/>                                                                          |
| [**Ptcloseprovider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider)<br/>                                     | Schließt das Handle eines Druck Ticket Anbieters.<br/>                                                                                                      |
| [**Ptconvertdevmodetoprintticket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket)<br/>         | Konvertiert eine [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur in ein Druck Ticket in einem [**IStream**](/windows/desktop/Stg/istream-compound-file-implementation).<br/>        |
| [**Ptconvertprintticketdedevmode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode)<br/>         | Konvertiert ein Druck Ticket in eine [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur.<br/>                                                                        |
| [**Ptgetprint-Funktionen**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities)<br/>                       | Ruft die Funktionen des Druckers ab, die in Übereinstimmung mit dem XML- [Druck Schema](./printschema.md)formatiert sind.<br/>                   |
| [**Ptgetprintdebug-Funktionen**](/windows/win32/api/prntvpt/nf-prntvpt-ptgetprintdevicecapabilities)<br/>    | Ruft die Funktionen des Geräte Druckers ab, die in Übereinstimmung mit dem XML- [Druck Schema](./printschema.md)formatiert sind.<br/>            |
| [**Ptgetprintdeviceresources**](/windows/win32/api/prntvpt/nf-prntvpt-ptgetprintdeviceresources)<br/>          | Die Druckgeräte Ressourcen für einen Drucker, der mit dem XML- [Druck Schema](./printschema.md)formatiert ist, werden abgerufen.<br/> |
| [**Ptmergeandvalidateprintticket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket)<br/>         | Führt zwei Druck Tickets zusammen und gibt ein gültiges, brauchbares Druck Ticket zurück.<br/>                                                                          |
| [**Ptopenprovider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenprovider)<br/>                                       | Öffnet eine Instanz eines Druck Ticket Anbieters.<br/>                                                                                               |
| [**Ptopzuproviderex**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex)<br/>                                   | Öffnet eine Instanz eines Druck Ticket Anbieters.<br/>                                                                                               |
| [**Ptqueryschemaversionsupport**](/windows/desktop/api/prntvpt/nf-prntvpt-ptqueryschemaversionsupport)<br/>             | Ruft die höchste (neueste) Version des [Druck Schemas](./printschema.md) ab, das der angegebene Drucker unterstützt.<br/>           |
| [**Ptreleasememory**](/windows/desktop/api/prntvpt/nf-prntvpt-ptreleasememory)<br/>                                     | Gibt Puffer frei, die mit Druck Tickets und Druckfunktionen verknüpft sind.<br/>                                                                      |
| [**Unbindptproviderthunk**](unbindptproviderthunk.md)<br/>                         | Schließt ein Handle für einen Druck ticketanbieter.<br/>                                                                                                 |



 

 

