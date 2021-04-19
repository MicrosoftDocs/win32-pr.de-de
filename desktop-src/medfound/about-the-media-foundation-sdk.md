---
description: Microsoft Media Foundation ist die Multimedia-Plattform der nächsten Generation für Windows, mit der Entwickler, Consumer und Inhaltsanbieter die neue Welle von Premium-Inhalten mit verbesserter Stabilität, unvergleichlicher Qualität und nahtloser Interoperabilität nutzen können.
ms.assetid: 3f933e39-8f9b-4c62-b528-4f1bba4b45d1
title: Info über Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a166482bbb0291f702a0e402441e292109a3e10
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106357145"
---
# <a name="about-media-foundation"></a>Info über Media Foundation

Microsoft Media Foundation ist die Multimedia-Plattform der nächsten Generation für Windows, mit der Entwickler, Consumer und Inhaltsanbieter die neue Welle von Premium-Inhalten mit verbesserter Stabilität, unvergleichlicher Qualität und nahtloser Interoperabilität nutzen können.

Media Foundation erfordert Windows Vista oder höher. Dabei wird das Component Object Model (com) verwendet, und es ist C/C++ erforderlich. Microsoft stellt keine verwaltete API für Media Foundation bereit.

Die Media Foundation-APIs sind Teil des [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Installieren Sie die neueste Version des Windows SDK, um eine Media Foundation Anwendung zu entwickeln.

## <a name="audio-and-video-quality"></a>Audioqualität und Video Qualität

Media Foundation wurde entwickelt, um die Herausforderungen von hoch Definitions Inhalten zu erfüllen. Verbesserungen der Audioqualität und Videoqualität, die auf der gesamten Plattform vorgenommen werden, ermöglichen die Bereitstellung einer hervorgehobenen Oberfläche für den Inhalt der nächsten Generation.

-   Die DirectX-Videobeschleunigung (DXVA) 2,0 bietet im Vergleich mit DXVA 1,0 eine effizientere Videobeschleunigung mit robusterer und optimierter Video Decodierung und erweiterter Verwendung von Hardware bei der Videoverarbeitung. Mit DXVA 2,0 kann Windows einige der anspruchsvollsten hoch Definitions Inhalte mit hoher Qualität und verbesserter Ausfallsicherheit verarbeiten.

-   Farb Rauminformationen werden in der gesamten Video Pipeline beibehalten. Benutzer können Videoinhalte mit voller Treue nutzen. Farbinformationen und Zeilen Sprung Bilder werden jetzt für Einzelpass-Kompositionen an Hardware übergeben. Durch die Beibehaltung von Farb Rauminformationen werden auch unnötige Farb Raum Konvertierungen reduziert, wodurch mehr Zyklen zum Verarbeiten anspruchsvoller HD-Inhalte freigegeben werden.
-   Der Enhanced Video Renderer (EVR) bietet eine bessere Zeit Steuerungs Unterstützung, eine verbesserte Videoverarbeitung und eine verbesserte Ausfallsicherheit. Die Vollbildwiedergabe Unterstützung wurde verbessert, und das Abspielen von Videos im Fenstermodus wurde minimiert.
-   In Media Foundation wird der Multimedia Class Scheduler Service (MMCSS) verwendet, einem neuen Systemdienst in Windows Vista. Mit MMCSS können Multimediaanwendungen sicherstellen, dass Ihre Zeit empfindliche Verarbeitung priorisierten Zugriff auf CPU-Ressourcen erhält.

## <a name="content-access"></a>Inhalts Zugriff

Da digitale Unterhaltung in den High-Definition-Zeitraum übergeht und Inhalte portabler und allgemeinerer werden, wird der Inhalts Schutz zu einem integralen Bestandteil digitaler Medienprodukte. Durch die Erweiterbarkeit von Media Foundation wird sichergestellt, dass diese Trends unterstützt werden.

Außerdem ermöglicht die Media Foundation Erweiterbarkeit, dass verschiedene Inhalts Schutzsysteme zusammenarbeiten.

## <a name="about-media-foundation"></a>Info über Media Foundation

Dieser Abschnitt enthält allgemeine Informationen zu den Media Foundation-APIs. Ausführliche Informationen zur Programmierung finden Sie im [Media Foundation-Programmier Handbuch](media-foundation-programming-guide.md).



| `Section`                                                                              | BESCHREIBUNG                                                               |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Neuerungen bei Media Foundation](whats-new-for-media-foundation.md)                | Beschreibt die neuen Funktionen in Media Foundation.                               |
| [Media Foundation-Header und-Bibliotheken](media-foundation-headers-and-libraries.md) | Listet die Header-und Bibliotheksdateien auf, die die Media Foundation-APIs definieren. |
| [Media Foundation Tools](media-foundation-tools.md)                                 | Beschreibt die Entwicklungs Tools, die für Media Foundation verfügbar sind.  |



 

Media Foundation ist nicht in den N-und KN-Editionen von Windows 8 enthalten. Weitere Informationen finden Sie unter [Microsoft Windows Media Feature Pack für N-und KN-Versionen aller Windows 8-Editionen](https://support.microsoft.com/kb/2703761).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Microsoft Media Foundation](microsoft-media-foundation-sdk.md)
</dt> </dl>

 

 



