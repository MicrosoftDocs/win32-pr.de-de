---
description: In diesem Abschnitt wird der allgemeine Entwurf von Microsoft Media Foundation beschrieben. Informationen zur Verwendung von Media Foundation für bestimmte Programmieraufgaben finden Sie unter Media Foundation Programmierhandbuch.
ms.assetid: 33820c6a-859d-4df6-a605-4e0f64f45c5b
title: Media Foundation-Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abcc95b1fdb39ad7d0e90e44b66df0dd7eb3c06418c16b4efc452abba4a9738d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974215"
---
# <a name="media-foundation-architecture"></a>Media Foundation-Architektur

In diesem Abschnitt wird der allgemeine Entwurf von Microsoft Media Foundation beschrieben. Informationen zur Verwendung von Media Foundation für bestimmte Programmieraufgaben finden Sie im [Media Foundation-Programmierhandbuch.](media-foundation-programming-guide.md)

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                         | BESCHREIBUNG                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Übersicht über die Media Foundation Architektur](overview-of-the-media-foundation-architecture.md)<br/> | Bietet eine allgemeine Übersicht über die architektur Media Foundation.<br/>                                                                                                                                                                                                               |
| [Media Foundation Primitive](media-foundation-primitives.md)<br/>                                     | Beschreibt einige grundlegende Schnittstellen, die in Media Foundation verwendet werden.<br/> Fast alle Media Foundation Anwendungen verwenden diese Schnittstellen.<br/>                                                                                                                       |
| [Media Foundation-Plattform-APIs](media-foundation-platform-apis.md)<br/>                               | Beschreibt kern Media Foundation Funktionen, z. B. asynchrone Rückrufe und Arbeitswarteschlangen.<br/> Einige Anwendungen verwenden möglicherweise Schnittstellen auf Plattformebene. Außerdem verwenden benutzerdefinierte Plug-Ins wie Medienquellen und MFTs diese Schnittstellen.<br/>                                       |
| [Media Foundation Pipeline](media-foundation-pipeline.md)<br/>                                         | Die Media Foundation Pipelineebene besteht aus Medienquellen, MFTs und Mediensenken. Die meisten Anwendungen rufen Methoden nicht direkt auf der Pipelineebene auf. Stattdessen verwenden Anwendungen eine der höheren Ebenen, z. B. die Mediensitzung oder den Quellleser und Senkenwriter.<br/> |
| [Mediensitzung](media-session.md)<br/>                                                                 | Die Mediensitzung verwaltet den Datenfluss in der Media Foundation Pipeline.<br/>                                                                                                                                                                                                           |
| [Quellleser](source-reader.md)<br/>                                                                 | Der Quellleser ermöglicht einer Anwendung das Abrufen von Daten aus einer Medienquelle, ohne dass die Medienquell-APIs direkt aufgerufen werden müssen. Der Quellleser kann auch die Decodierung komprimierter Datenströme durchführen.<br/>                                                            |
| [Pfad zu geschützten Medien](protected-media-path.md)<br/>                                                   | Der Geschützte Medienpfad (Protected Media Path, PMP) bietet eine geschützte Umgebung für die Wiedergabe von Premium-Videoinhalten. Es ist nicht erforderlich, den PMP zu verwenden, wenn Sie eine Media Foundation Anwendung schreiben. <br/>                                                                                             |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Info über Media Foundation](about-the-media-foundation-sdk.md)
</dt> <dt>

[Media Foundation: Grundlegende Konzepte](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[Media Foundation und COM](media-foundation-and-com.md)
</dt> <dt>

[Media Foundation Programmierhandbuch](media-foundation-programming-guide.md)
</dt> </dl>

 

 




