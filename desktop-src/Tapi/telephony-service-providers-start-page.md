---
description: Bei einem Telefoniedienstanbieter (TSP) handelt es sich um eine Dynamic Link Library (dll), die die Kommunikation von Geräten über einen Satz exportierter Dienstfunktionen unterstützt.
ms.assetid: 276c27ac-b6ee-42a7-8327-33dfd87e69bd
title: Telefoniedienstanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c3c8887723cc74a1bf0d77bcdcfd06c8468a4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868144"
---
# <a name="telephony-service-providers"></a>Telefoniedienstanbieter

## <a name="purpose"></a>Zweck

Bei einem Telefoniedienstanbieter (TSP) handelt es sich um eine Dynamic Link Library (dll), die die Kommunikation von Geräten über einen Satz exportierter Dienstfunktionen unterstützt. Eine TAPI-Anwendung verwendet standardisierte Befehle, TAPI übergibt Informationen an den Telefoniedienstanbieter, und der TSP verarbeitet die spezifischen Befehle, die mit dem Gerät ausgetauscht werden müssen.

Ein TSP muss der Telefoniedienstanbieter-Schnittstelle (TSPI) entsprechen, um in der Microsoft-Telefonieumgebung als Dienstanbieter zu fungieren. TSPI definiert die externen Funktionen, die von einem Telefoniedienstanbieter zur Verfügung gestellt werden

## <a name="developer-audience"></a>Entwicklergruppe

Sie können TAPI-fähige Anwendungen in vielen Sprachen schreiben, einschließlich Java, Visual Basic und C/C++. Vorherige Entwicklungsarbeiten mit Telekommunikations-oder anderen Telefonieanwendungen sind hilfreich, aber nicht erforderlich.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

TSPI ermöglicht die Entwicklung von TSPS für alle Versionen von Windows.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                | BESCHREIBUNG                                                              |
|----------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Übersicht](about-the-telephony-service-provider-tsp-.md)<br/> | Allgemeine Informationen über die Architektur und Komponenten von TSPI.<br/> |
| [Verweis](tspi-reference.md)<br/>                           | Dokumentation für die TSPI-Schnittstellen.<br/>                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über Microsoft-Telefonie](./microsoft-telephony-overview.md)
</dt> <dt>

[Medien Dienstanbieter](./media-service-providers-start-page.md)
</dt> <dt>

[TAPI 2,2](./tapi-2-2-start-page.md)
</dt> <dt>

[TAPI 3,1](./tapi-3-1-start-page.md)
</dt> </dl>

 

