---
description: Der Quellleser ist eine Alternative zur Verwendung der Mediensitzung und der Microsoft Media Foundation Pipeline zum Verarbeiten von Mediendaten.
ms.assetid: 8a17a754-53ef-4c05-9189-7978d864b17a
title: Quellleser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81527392c97aae039de8b8cdbd76b1251e03842b6b66c22cc224118d4f428620
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119101813"
---
# <a name="source-reader"></a>Quellleser

Der Quellleser ist eine Alternative zur Verwendung der [Mediensitzung](media-session.md) und der Microsoft Media Foundation Pipeline zum Verarbeiten von Mediendaten.

## <a name="why-use-the-source-reader"></a>Gründe für die Verwendung des Quelllesers

Media Foundation stellt eine Pipeline bereit, die für die Wiedergabe optimiert ist. Die Pipeline ist end-to-end, d.h. sie verarbeitet den Datenfluss von der Quelle (z. B. einer Videodatei) bis zum Ziel (z. B. die Grafikanzeige). Wenn Sie die Daten jedoch während der Pipeline lesen oder ändern möchten, müssen Sie ein benutzerdefiniertes Plug-In schreiben. Dies erfordert eine ziemlich tiefe Kenntnis der Media Foundation Pipeline. Für bestimmte Aufgaben ist das Erstellen eines neuen Plug-Ins zu viel Aufwand. Der Quellleser ist für diese Art von Situation konzipiert, wenn Sie die Rohdaten ohne den Mehraufwand der gesamten Pipeline aus einer Quelle abrufen möchten.

Intern enthält der Quellleser einen Zeiger auf eine Medienquelle. Eine *Medienquelle* ist ein Media Foundation Objekt, das Mediendaten aus einer externen Quelle generiert, z. B. einer Mediendatei oder einem Videoaufnahmegerät. Der Quellleser verwaltet alle Methodenaufrufe an die Medienquelle. (Weitere Informationen zu Medienquellen finden Sie unter [Medienquellen](media-sources.md).)

Wenn die Medienquelle komprimierte Daten übermittelt, können Sie den Quellleser verwenden, um die Daten zu decodieren. In diesem Fall lädt der Quellleser den richtigen Decoder und verwaltet den Datenfluss zwischen der Medienquelle und dem Decoder. Der Quellleser kann auch eine eingeschränkte Videoverarbeitung durchführen: Farbkonvertierung von YUV in RGB-32 und Softwaredeinterlacing, obwohl diese Vorgänge für das Rendern von Echtzeitvideos nicht empfohlen werden. Die folgende Abbildung veranschaulicht diesen Prozess.

![Diagramm des Quelllesers](images/sourcereader.png)

Der Quellleser sendet die Daten nicht an ein Ziel. es liegt an der Anwendung, die Daten zu nutzen. Beispielsweise kann der Quellleser eine Videodatei lesen, das Video wird jedoch nicht auf dem Bildschirm gerendert. Außerdem verwaltet der Quellleser keine Präsentationsuhr, behandelt keine Zeitsteuerungsprobleme oder synchronisiert Videos nicht mit Audio.

Erwägen Sie die Verwendung des Quelllesers in den:

-   Sie möchten Daten aus einer Mediendatei abrufen, ohne sich Gedanken über die zugrunde liegende Dateistruktur machen zu müssen.
-   Sie möchten Daten von einem Audio- oder Videoaufnahmegerät abrufen.
-   Ihre Datenverarbeitungsaufgaben sind nicht zeitabhängig, oder Sie benötigen keine Präsentationsuhr.
-   Sie verfügen bereits über eine Medienpipeline, die nicht auf Media Foundation basiert, und Sie möchten die Media Foundation Medienquellen in Ihre eigene Pipeline integrieren.

Der Quellleser wird in den folgenden Situationen nicht empfohlen:

-   Für geschützten Inhalt. Der Quellleser unterstützt digital rights management (DRM) nicht.
-   Wenn Sie die Details der zugrunde liegenden Dateistruktur interessieren. Der Quellleser blendet diesen Detailtyp aus.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                        | Beschreibung                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [Verwenden des Quelllesers zum Verarbeiten von Mediendaten](processing-media-data-with-the-source-reader.md)<br/> | In diesem Thema wird beschrieben, wie Der Quellleser zum Verarbeiten von Mediendaten verwendet wird.<br/>                                               |
| [Verwenden des Quelllesers im asynchronen Modus](using-the-source-reader-in-asynchronous-mode.md)<br/>  | In diesem Thema wird beschrieben, wie der Quellleser im asynchronen Modus verwendet wird.<br/>                                                |
| [Tutorial: Decodieren von Audio](tutorial--decoding-audio.md)<br/>                                          | In diesem Tutorial wird gezeigt, wie Sie den Quellleser verwenden, um Audiodaten aus einer Mediendatei zu decodieren und die Audiodaten in eine WAVE-Datei zu schreiben.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation-Architektur](media-foundation-architecture.md)
</dt> <dt>

[Media Foundation Programmierhandbuch](media-foundation-programming-guide.md)
</dt> <dt>

[**SOURCEReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 




