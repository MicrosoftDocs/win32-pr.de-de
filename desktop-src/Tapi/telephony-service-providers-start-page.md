---
description: Ein Telefoniedienstanbieter (Telefoniedienstanbieter, TSP) ist eine Dll (Dynamic Link Library), die die Steuerung von Kommunikationsgeräten über eine Reihe von exportierten Dienstfunktionen unterstützt.
ms.assetid: 276c27ac-b6ee-42a7-8327-33dfd87e69bd
title: Telefoniedienstanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c1e7ff98bfbc898a419e385be07ebdae56d2067061d2ac7951b8c0aff42dcd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872870"
---
# <a name="telephony-service-providers"></a>Telefoniedienstanbieter

## <a name="purpose"></a>Zweck

Ein Telefoniedienstanbieter (Telefoniedienstanbieter, TSP) ist eine Dll (Dynamic Link Library), die die Steuerung von Kommunikationsgeräten über eine Reihe von exportierten Dienstfunktionen unterstützt. Eine TAPI-Anwendung verwendet standardisierte Befehle, TAPI übergibt Informationen an den Telefoniedienstanbieter, und der TSP verarbeitet die spezifischen Befehle, die mit dem Gerät ausgetauscht werden müssen.

Ein TSP muss der Telefoniedienstanbieterschnittstelle (Telefoniedienstanbieterschnittstelle, TSPI) entsprechen, um als Dienstanbieter innerhalb der Microsoft-Telefonieumgebung zu fungieren. TSPI definiert die externen Funktionen, die von einem Telefoniedienstanbieter verfügbar gemacht werden, der mit Kommunikationsgeräten geliefert wird.

## <a name="developer-audience"></a>Entwicklergruppe

Sie können TAPI-fähige Anwendungen in vielen Sprachen schreiben, einschließlich Java, Visual Basic und C/C++. Frühere Entwicklungserfahrungen mit Telekommunikation oder anderen Telefonieanwendungen sind hilfreich, aber nicht erforderlich.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

TSPI ermöglicht die Entwicklung von TSPs für alle Versionen von Windows.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                | Beschreibung                                                              |
|----------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Übersicht](about-the-telephony-service-provider-tsp-.md)<br/> | Allgemeine Informationen zur Architektur und den Komponenten von TSPI.<br/> |
| [Referenz](tspi-reference.md)<br/>                           | Dokumentation zu den TSPI-Schnittstellen.<br/>                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Microsoft-Telefonie – Übersicht](./microsoft-telephony-overview.md)
</dt> <dt>

[Mediendienstanbieter](./media-service-providers-start-page.md)
</dt> <dt>

[TAPI 2.2](./tapi-2-2-start-page.md)
</dt> <dt>

[TAPI 3.1](./tapi-3-1-start-page.md)
</dt> </dl>

 

