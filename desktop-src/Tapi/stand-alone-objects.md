---
description: TAPI 3 umfasst eine Reihe von Objekten, die von den fünf Haupt-TAPI-Objekten (TAPI, Address, Callcenter, callhub und Terminal) unabhängig sind.
ms.assetid: 090fa8e5-58a5-46ee-89a3-bd97fcfbf0f0
title: Stand-Alone Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e71fdea9c7ed4b66f57c3c0fe35625f35656555e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865003"
---
# <a name="stand-alone-objects"></a>Stand-Alone Objekte

TAPI 3 umfasst eine Reihe von Objekten, die von den fünf Haupt-TAPI-Objekten (TAPI, Address, Callcenter, callhub und Terminal) unabhängig sind. [Ereignis Schnittstellen](./event-interfaces.md) und [Enumeratorschnittstellen](enumerator-interfaces.md) sind eigenständige Objekte und werden separat zusammengefasst. Im folgenden werden eigenständige nicht-Ereignis-und nicht-Enumerator-Schnittstellen zusammengefasst.



| Schnittstelle                                             | BESCHREIBUNG                                                                                                                                                                                                   |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Itcollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)                  | Stellt Methoden bereit, mit denen Automatisierungs Client Anwendungen, wie z. b. Visual Basic, Sammlungs Informationen abrufen können.                                                                                             |
| [**ITCollection2**](/windows/desktop/api/Tapi3if/nn-tapi3if-itcollection2)                | Erweitert die [**itcollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) durch Bereitstellen zusätzlicher Methoden zum Ändern von Auflistungen.                                                                                                       |
| [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) | Standard-COM-Schnittstelle zum Implementieren von Automation.                                                                                                                                                           |
| [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)                         | Standard-COM-Schnittstelle zum erhalten von Zeigern auf Objekt Schnittstellen.                                                                                                                                             |
| [**Itdispatchmapper**](/windows/desktop/api/tapi3if/nn-tapi3if-itdispatchmapper)          | Ermöglicht es einer Anwendung, den Dispatch-Zeiger einer anderen Schnittstelle für ein Objekt abzurufen, wenn ein aktueller [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) -Zeiger angegeben ist. Nützlich für einige Skriptsprachen. |
| [**Itrequest**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest)                        | Stellt Methoden bereit, die es einer TAPI 3-Anwendung ermöglichen, unter [stützte Telefonie](assisted-telephony-overview.md)zu verwenden.                                                                                                |



 



| Schnittstelle                                  | BESCHREIBUNG                                                                                                                                                                |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Itmediacontrol**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol)   | Startet, beendet und hält aktuelle Aktionen wie z. b. eine Wiedergabe an.                                                                                                             |
| [**Itmediaplayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) | Stellt Wiedergabe spezifische Methoden bereit, die es einer Anwendung ermöglichen, Vorgänge wie das Festlegen der Liste der wieder zugebende Dateien und das Ändern der Wiedergabegeschwindigkeit auszuführen.              |
| [**Itmediarecord**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord)     | Stellt Aufzeichnungs spezifische Methoden bereit, die es einer Anwendung ermöglichen, Vorgänge wie das Festlegen der Namen von Dateien zum Aufzeichnen und Ändern der Dauer einer Aufzeichnung auszuführen. |



 



| Schnittstelle                                                  | BESCHREIBUNG                                                                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Itscriptableaudioformat**](/windows/desktop/api/tapi3if/nn-tapi3if-itscriptableaudioformat) | Ruft das Audioformat ab oder legt das Audioformat für, eine Spur, fest.                                                                                             |
| [**Itstaticaudioterminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itstaticaudioterminal)     | Stellt Methoden für statische audioterminalobjekte bereit, die zur Unterstützung von Telefongeräten benötigt werden. TAPI 3,1-Msps müssen diese Schnittstelle für alle statischen audioterminals verfügbar machen. |



 

 

 
