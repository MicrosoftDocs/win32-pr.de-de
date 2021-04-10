---
description: Asfparser-Beispiel
ms.assetid: 6be1e12f-7d4a-4564-88ae-14fd71fd2cf9
title: Asfparser-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c159b481e22d77b0bee9adccbbb74073398c12b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214344"
---
# <a name="asfparser-sample"></a>Asfparser-Beispiel

Zeigt, wie Sie Daten aus einer ASF-Datei (Advanced Systems Format) mithilfe der-ASF-Komponenten auf niedriger Ebene in Media Foundation analysieren. Das Beispiel veranschaulicht die folgenden Aufgaben:

-   Auflisten der Audiodaten und Videostreams in einer ASF-Datei.
-   Auswählen eines Audiodaten-oder Videodaten Stroms für die Analyse.
-   Es wird versucht, ein Paket zu einer gewünschten Wiedergabezeit zu suchen.
-   Komprimierte Beispiele für den ausgewählten Stream werden erzeugt.
-   Decodieren von Audio-und Videobeispielen.

## <a name="apis-demonstrated"></a>Gezeigte APIs

In diesem Beispiel werden die folgenden Microsoft Media Foundation Schnittstellen veranschaulicht:

-   [**Imfasf ContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)
-   [**Imfasfindexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer)
-   [**Imfasfäsplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter)

## <a name="usage"></a>Verbrauch

1.  Um eine ASF-Datei zu öffnen, klicken Sie auf die Schaltfläche **Mediendatei öffnen...** .
2.  Wählen Sie eine ASF-Datei und klicken Sie auf **Öffnen**. Informationen zur Datei werden im **Informations** Bereich angezeigt.
3.  Wählen Sie unter **parserkonfiguration** einen zu testenden Stream aus.
4.  Um Beispiele in umgekehrter Reihenfolge zu generieren, wählen Sie **umkehren**.
5.  Um den Startpunkt anzugeben, ziehen Sie den Schieberegler an den gewünschten Speicherort.
6.  Um mit der Verarbeitung zu beginnen, klicken Sie auf die Schaltfläche **Beispiele generieren** . Informationen zu den Beispielen werden im **Informations** Bereich angezeigt.
7.  Um die Beispiele für den Audiostream zu testen, klicken Sie auf die Schaltfläche " **Testdatei** ".
8.  Um die Beispiele für den Videostream zu testen, klicken Sie auf die Schaltfläche **Bitmap anzeigen** .

## <a name="requirements"></a>Anforderungen



| Produkt                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist im [GitHub-Repository für klassische Windows-Beispiele](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/asfparser)verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation-SDK-Beispiele](media-foundation-sdk-samples.md)
</dt> <dt>

[Unterstützung von ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Tutorial: Lesen einer ASF-Datei](tutorial--reading-an-asf-file.md)
</dt> <dt>

[Wmcontainer-ASF-Komponenten](wmcontainer-asf-components.md)
</dt> </dl>

 

 



