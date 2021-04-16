---
description: Der Quell Leser ist eine Alternative zur Verwendung der Medien Sitzung und der Microsoft Media Foundation Pipeline zum Verarbeiten von Mediendaten.
ms.assetid: 8a17a754-53ef-4c05-9189-7978d864b17a
title: Quell Leser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ba67b32fba7fcf899f339e9e2d0512d2574bad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527830"
---
# <a name="source-reader"></a>Quell Leser

Der Quell Leser ist eine Alternative zur Verwendung der [Medien Sitzung](media-session.md) und der Microsoft Media Foundation Pipeline zum Verarbeiten von Mediendaten.

## <a name="why-use-the-source-reader"></a>Gründe für die Verwendung des Quell Readers

Media Foundation eine Pipeline bereitstellt, die für die Wiedergabe optimiert ist. Die Pipeline ist End-to-End, d. h., Sie verarbeitet den Datenfluss von der Quelle (z. b. eine Videodatei) bis zum Ziel (z. b. die Grafik Anzeige). Wenn Sie jedoch die Daten beim Durchlaufen der Pipeline lesen oder ändern möchten, müssen Sie ein benutzerdefiniertes Plug-in schreiben. Dies erfordert eine recht tiefe Kenntnis der Media Foundation Pipeline. Für bestimmte Aufgaben ist das Erstellen eines neuen Plug-ins zu viel mehr Aufwand. Der Quell Leser ist für diese Art von Situation konzipiert, wenn Sie die Rohdaten aus einer Quelle ohne den Aufwand der gesamten Pipeline erhalten möchten.

Intern enthält der Quell Leser einen Zeiger auf eine Medienquelle. Eine *Medienquelle* ist ein Media Foundation Objekt, das Mediendaten aus einer externen Quelle, z. b. einer Mediendatei oder einem Video Erfassungsgerät, generiert. Der Quell Leser verwaltet alle Methodenaufrufe der Medienquelle. (Weitere Informationen zu Medienquellen finden Sie unter [Medienquellen](media-sources.md).)

Wenn die Medienquelle komprimierte Daten bereitstellt, können Sie die Daten mithilfe des Quell Readers decodieren. In diesem Fall lädt der Quell Leser den richtigen Decoder und verwaltet den Datenfluss zwischen der Medienquelle und dem Decoder. Der Quell Leser kann auch eine begrenzte Videoverarbeitung durchführen: Farbkonvertierung von YUV zu RGB-32 und Software Deinterlacing, obwohl diese Vorgänge für Video Rendering in Echtzeit nicht empfohlen werden. Dieses Verfahren wird in der folgenden Abbildung veranschaulicht.

![Diagramm des Quell Readers](images/sourcereader.png)

Der Quell Leser sendet die Daten nicht an ein Ziel. die Anwendung kann die Daten nutzen. Der Quell Leser kann z. b. eine Videodatei lesen, aber das Video wird nicht auf dem Bildschirm angezeigt. Außerdem verwaltet der Quell Leser keine Präsentations Uhr, behandelt Zeit Steuerungsprobleme oder synchronisiert Videos mit Audiodaten.

Verwenden Sie ggf. den Quell Leser:

-   Sie möchten Daten aus einer Mediendatei erhalten, ohne sich Gedanken über die zugrunde liegende Dateistruktur machen zu müssen.
-   Sie möchten Daten von einem Audiogerät oder Video Erfassungsgerät erhalten.
-   Ihre Datenverarbeitungs Aufgaben sind nicht Zeit empfindlich, oder Sie benötigen keine Präsentations Uhr.
-   Sie verfügen bereits über eine Medien Pipeline, die nicht auf Media Foundation basiert, und Sie möchten die Media Foundation Medienquellen in Ihre eigene Pipeline integrieren.

Der Quell Leser wird in den folgenden Situationen nicht empfohlen:

-   Für geschützten Inhalt. Der Quell Leser unterstützt Digital Rights Management (DRM) nicht.
-   Wenn Sie sich für die Details der zugrunde liegenden Dateistruktur interessieren. Der Quell Reader verbirgt diese Art von Details.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                        | BESCHREIBUNG                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [Verwenden des Quell Readers zum Verarbeiten von Mediendaten](processing-media-data-with-the-source-reader.md)<br/> | In diesem Thema wird beschrieben, wie Sie den Quell Leser zum Verarbeiten von Mediendaten verwenden können.<br/>                                               |
| [Verwenden des Quell Readers im asynchronen Modus](using-the-source-reader-in-asynchronous-mode.md)<br/>  | In diesem Thema wird beschrieben, wie der Quell Leser im asynchronen Modus verwendet wird.<br/>                                                |
| [Tutorial: Decodieren von Audiodaten](tutorial--decoding-audio.md)<br/>                                          | In diesem Tutorial wird gezeigt, wie Sie den Quell Leser zum Decodieren von Audiodaten aus einer Mediendatei und zum Schreiben der Audiodatei in eine Wave-Datei verwenden.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation-Architektur](media-foundation-architecture.md)
</dt> <dt>

[Media Foundation-Programmier Handbuch](media-foundation-programming-guide.md)
</dt> <dt>

[**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 




