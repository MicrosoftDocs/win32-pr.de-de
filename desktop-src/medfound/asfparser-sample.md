---
description: ASFParser-Beispiel
ms.assetid: 6be1e12f-7d4a-4564-88ae-14fd71fd2cf9
title: ASFParser-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50db441be45d28899bc8f2ace68b8f09af40e679449d26aec7adf25ab4fb9e2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959550"
---
# <a name="asfparser-sample"></a>ASFParser-Beispiel

Zeigt, wie Sie Daten aus einer ASF-Datei (Advanced Systems Format) analysieren, indem Sie die ASF-Komponenten auf niedriger Ebene in Media Foundation. Im Beispiel werden die folgenden Aufgaben veranschaulicht:

-   Aufzählen der Audio- und Videostreams in einer ASF-Datei.
-   Auswählen eines Audio- oder Videostreams für die Analyse.
-   Suchen nach einem Paket zu einer gewünschten Wiedergabezeit.
-   Generieren komprimierter Stichproben für den ausgewählten Stream.
-   Decodieren von Audio- und Videobeispielen.

## <a name="apis-demonstrated"></a>Gezeigte APIs

In diesem Beispiel werden die folgenden Microsoft Media Foundation veranschaulicht:

-   [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)
-   [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer)
-   [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter)

## <a name="usage"></a>Verwendung

1.  Um eine ASF-Datei zu öffnen, klicken Sie auf **die Schaltfläche Open Media File... (Mediendatei** öffnen).
2.  Wählen Sie eine ASF-Datei aus, und klicken Sie **auf Öffnen.** Informationen zur Datei werden im Bereich **Informationen** angezeigt.
3.  Wählen **Sie unter Parserkonfiguration** einen zu analysierenden Stream aus.
4.  Wählen Sie umgekehrt aus, um Beispiele in **umgekehrter Reihenfolge zu generieren.**
5.  Um den Startpunkt anzugeben, ziehen Sie den Schieberegler an die gewünschte Position.
6.  Klicken Sie auf die Schaltfläche Beispiele **generieren,** um mit der Analyse zu beginnen. Informationen zu den Beispielen werden im Bereich **Informationen** angezeigt.
7.  Klicken Sie auf die Schaltfläche Audio testen, um die Beispiele für den **Audiostream zu** testen.
8.  Klicken Sie auf die Schaltfläche Bitmap anzeigen, um die Beispiele für den **Videostream zu** testen.

## <a name="requirements"></a>Anforderungen



| Produkt                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist im [GitHub-Repository Windows klassischen Beispielen verfügbar.](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/asfparser)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation-SDK-Beispiele](media-foundation-sdk-samples.md)
</dt> <dt>

[ASF-Unterstützung in Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Tutorial: Lesen einer ASF-Datei](tutorial--reading-an-asf-file.md)
</dt> <dt>

[WMContainer-ASF-Komponenten](wmcontainer-asf-components.md)
</dt> </dl>

 

 



