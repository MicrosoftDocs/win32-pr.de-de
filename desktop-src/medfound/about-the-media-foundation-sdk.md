---
description: Microsoft Media Foundation ist die Multimediaplattform der nächsten Generation für Windows, mit der Entwickler, Consumer und Inhaltsanbieter die neue Welle von Premium-Inhalten mit verbesserter Stabilität, erstklassiger Qualität und nahtloser Interoperabilität nutzen können.
ms.assetid: 3f933e39-8f9b-4c62-b528-4f1bba4b45d1
title: Info über Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f2f8510cc6d967f7a3a809d395f032e277290074002399f9b54e6c54025c312
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959650"
---
# <a name="about-media-foundation"></a>Info über Media Foundation

Microsoft Media Foundation ist die Multimediaplattform der nächsten Generation für Windows, mit der Entwickler, Consumer und Inhaltsanbieter die neue Welle von Premium-Inhalten mit verbesserter Stabilität, erstklassiger Qualität und nahtloser Interoperabilität nutzen können.

Media Foundation erfordert Windows Vista oder höher. Es verwendet das Komponentenobjektmodell (COM) und erfordert C/C++. Microsoft stellt keine verwaltete API für Media Foundation bereit.

Die Media Foundation-APIs sind Teil des [Windows SDK.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Um eine Media Foundation Anwendung zu entwickeln, installieren Sie die neueste Version des Windows SDK.

## <a name="audio-and-video-quality"></a>Audio- und Videoqualität

Media Foundation wurde entwickelt, um die Herausforderungen zu erfüllen, die sich durch high-definition-Inhalte ergeben. Verbesserungen der Audio- und Videoqualität, die auf der gesamten Plattform vorgenommen wurden, ermöglichen es jetzt, eine hervorragende Erfahrung für high-definition-Inhalte der nächsten Generation bereitzustellen.

-   DirectX Video Acceleration (DXVA) 2.0 bietet im Vergleich zu DXVA 1.0 eine effizientere Videobeschleunigung mit stabilerer und optimierter Videodecodierung und erweiterter Verwendung von Hardware in der Videoverarbeitung. Mit DXVA 2.0 können Windows einige der anspruchsvollsten High-Definition-Inhalte mit hoher Qualität und verbesserter Ausfallsicherheit verarbeiten.

-   Farbrauminformationen werden in der gesamten Videopipeline beibehalten. Benutzer können Videoinhalte mit voller Genauigkeit nutzen. Farbinformationen und Verschachtelungsbilder werden jetzt für Singlepass-Kompositionen an die Hardware übergeben. Die Beibehaltung von Farbrauminformationen reduziert auch unnötige Farbraumkonvertierungen, wodurch mehr Zyklen für die Verarbeitung anspruchsvoller HD-Inhalte freigegeben werden.
-   Der erweiterte Videorenderer (EVR) bietet bessere Zeitsteuerungsunterstützung, verbesserte Videoverarbeitung und verbesserte Ausfallsicherheit. Die Unterstützung der Vollbildwiedergabe wurde verbessert, und das Videolöschen im Fenstermodus wurde minimiert.
-   Media Foundation verwendet den Multimedia Class Scheduler Service (MMCSS), einen neuen Systemdienst in Windows Vista. MIT MMCSS können Multimediaanwendungen sicherstellen, dass ihre zeitkritische Verarbeitung priorisierten Zugriff auf CPU-Ressourcen erhält.

## <a name="content-access"></a>Inhaltszugriff

Wenn digitale Unterhaltung in die High-Definition-Zeit übergeht und Inhalte portierbarer und ubiquitärer werden, wird der Inhaltsschutz zu einem integralen Bestandteil digitaler Medienprodukte. Die Erweiterbarkeit von Media Foundation stellt sicher, dass diese Trends unterstützt werden können.

Darüber hinaus ermöglicht Media Foundation Erweiterbarkeit die Zusammenarbeit verschiedener Content Protection-Systeme.

## <a name="about-media-foundation"></a>Info über Media Foundation

Dieser Abschnitt enthält allgemeine Informationen zu den Media Foundation-APIs. Ausführliche Programmierinformationen finden Sie im [Media Foundation Programmierhandbuch.](media-foundation-programming-guide.md)



| `Section`                                                                              | BESCHREIBUNG                                                               |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Neuerungen bei Media Foundation](whats-new-for-media-foundation.md)                | Beschreibt neue Features in Media Foundation.                               |
| [Media Foundation Header und Bibliotheken](media-foundation-headers-and-libraries.md) | Listet die Header- und Bibliotheksdateien auf, die die Media Foundation-APIs definieren. |
| [Media Foundation Tools](media-foundation-tools.md)                                 | Beschreibt die Entwicklungstools, die für Media Foundation verfügbar sind.  |



 

Media Foundation ist nicht in den N- und KN-Editionen von Windows 8 enthalten. Weitere Informationen finden Sie unter [Microsoft Windows Media Feature Pack für N- und KN-Versionen aller Windows 8 Editionen.](https://support.microsoft.com/kb/2703761)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Microsoft Media Foundation](microsoft-media-foundation-sdk.md)
</dt> </dl>

 

 



