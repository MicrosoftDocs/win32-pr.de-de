---
description: In diesem Abschnitt wird der allgemeine Entwurf von Microsoft Media Foundation beschrieben. Weitere Informationen zum Verwenden von Media Foundation für bestimmte Programmieraufgaben finden Sie unter Media Foundation Programming Guide.
ms.assetid: 33820c6a-859d-4df6-a605-4e0f64f45c5b
title: Media Foundation-Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0914b0f4c43966edcdc6d30efa7c9dbdbbd4e8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106363035"
---
# <a name="media-foundation-architecture"></a>Media Foundation-Architektur

In diesem Abschnitt wird der allgemeine Entwurf von Microsoft Media Foundation beschrieben. Weitere Informationen zum Verwenden von Media Foundation für bestimmte Programmieraufgaben finden Sie unter [Media Foundation Programming Guide](media-foundation-programming-guide.md).

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                         | BESCHREIBUNG                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Übersicht über die Media Foundation-Architektur](overview-of-the-media-foundation-architecture.md)<br/> | Bietet eine allgemeine Übersicht über die Media Foundation Architektur.<br/>                                                                                                                                                                                                               |
| [Media Foundation primitiver](media-foundation-primitives.md)<br/>                                     | Beschreibt einige grundlegende Schnittstellen, die in Media Foundation verwendet werden.<br/> Fast alle Media Foundation Anwendungen verwenden diese Schnittstellen.<br/>                                                                                                                       |
| [Media Foundation Plattform-APIs](media-foundation-platform-apis.md)<br/>                               | Beschreibt Kern Media Foundation Funktionen, z. b. asynchrone Rückrufe und Arbeits Warteschlangen.<br/> Einige Anwendungen verwenden möglicherweise Schnittstellen auf Platt Form Ebene. Außerdem verwenden benutzerdefinierte Plug-ins, z. b. Medienquellen und MFTs, diese Schnittstellen.<br/>                                       |
| [Media Foundation Pipeline](media-foundation-pipeline.md)<br/>                                         | Die Media Foundation Pipeline Schicht besteht aus Medienquellen, MFTs und Medien senken. Die meisten Anwendungen werden Methoden nicht direkt auf der Pipeline Ebene aufruft. Stattdessen verwenden Anwendungen eine der höheren Ebenen, wie z. b. die Medien Sitzung oder den Quell-und senderwriter.<br/> |
| [Medien Sitzung](media-session.md)<br/>                                                                 | Die Medien Sitzung verwaltet den Datenfluss in der Media Foundation Pipeline.<br/>                                                                                                                                                                                                           |
| [Quell Leser](source-reader.md)<br/>                                                                 | Der Quell Reader ermöglicht einer Anwendung das Abrufen von Daten aus einer Medienquelle, ohne dass die Anwendung die Medienquellen-APIs direkt abrufen muss. Der Quell Leser kann auch die Decodierung von komprimierten Datenströmen ausführen.<br/>                                                            |
| [Geschützter Medien Pfad](protected-media-path.md)<br/>                                                   | Der geschützte Medien Pfad (PMP) bietet eine geschützte Umgebung für die Wiedergabe von Premium-Videoinhalten. Das PMP muss beim Schreiben einer Media Foundation Anwendung nicht verwendet werden. <br/>                                                                                             |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Info über Media Foundation](about-the-media-foundation-sdk.md)
</dt> <dt>

[Media Foundation: Grundlegende Konzepte](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[Media Foundation und com](media-foundation-and-com.md)
</dt> <dt>

[Media Foundation-Programmier Handbuch](media-foundation-programming-guide.md)
</dt> </dl>

 

 




