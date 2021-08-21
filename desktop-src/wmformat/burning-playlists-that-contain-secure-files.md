---
title: Brennen von Wiedergabelisten, die sichere Dateien enthalten
description: Brennen von Wiedergabelisten, die sichere Dateien enthalten
ms.assetid: 0d9415a1-a154-4fe4-af4c-cce4cb05ade5
keywords:
- Windows Medienformat-SDK, Wiedergabelisten mit sicheren Dateien
- Windows Medienformat-SDK, Wiedergabelisten mit sicheren Dateien
- Advanced Systems Format (ASF), Wiedergabelisten mit sicheren Dateien
- ASF (Advanced Systems Format), Wiedergabelisten mit sicheren Dateien
- Advanced Systems Format (ASF), Wiedergabelisten mit sicheren Dateien
- ASF (Advanced Systems Format), Wiedergabelisten mit sicheren Dateien
- Digital Rights Management (DRM), Wiedergabelisten mit sicheren Dateien
- DRM (Digital Rights Management), Wiedergabelisten mit sicheren Dateien
- Digital Rights Management (DRM), Wiedergabelisten mit sicheren Dateien
- DRM (Digital Rights Management), Wiedergabelisten mit sicheren Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d43cfbf3bb6e8ce4bac5cc1006fe73292988547ef2fc35289a4ced13e6f0d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028118"
---
# <a name="burning-playlists-that-contain-secure-files"></a>Brennen von Wiedergabelisten, die sichere Dateien enthalten

Lizenzen, die mithilfe der Objekte des Windows Media Rights Manager 10 SDK erstellt wurden, können das Recht zum Kopieren einer Datei auf einen Datenträger als Teil einer Wiedergabeliste angeben. Dieses Feature, das als Wiedergabelisten-Wiedergabeliste bezeichnet wird, erfordert, dass Sie die Lizenzen aller Dateien in der Wiedergabeliste überprüfen, bevor Sie mit dem Kopieren von Daten beginnen. Das Windows Media Format SDK stellt die [**IWMReaderPlaylistList-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) bereit, um die Dateiüberprüfung für Sie durchzuführen.

Führen Sie die folgenden Schritte aus, um Wiedergabelisten zu implementieren:

1.  Erstellen Sie eine Instanz des Readerobjekts oder des synchronen Readerobjekts. Weitere Informationen finden Sie unter [Lesen von ASF-Dateien.](reading-asf-files.md)
2.  Rufen Sie **die QueryInterface-Methode** der Readerschnittstelle [**(IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader) oder [**IWMSyncReader)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)auf, um einen Zeiger auf die [**IWMReaderPlaylistList-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) zu erhalten.
3.  Kopieren Sie die Dateinamen aus der Wiedergabeliste in ein Array von Breitzeichenzeichenfolgen. Die Dateinamen im Array müssen in der gleichen Reihenfolge wie in der Wiedergabeliste angezeigt werden.
4.  Rufen Sie [**die IWMReaderPlaylist Arrays::InitPlaylistList-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-initplaylistburn) auf, und übergeben Sie dabei einen Zeiger auf das in Schritt 3 erstellte Array, um die Lizenzüberprüfung für die Dateien zu initialisieren.
5.  Wenn die Lizenzüberprüfung abgeschlossen ist, sendet das Readerobjekt eine WMT INIT PLAYLIST BURN-Nachricht an Ihre Implementierung der \_ \_ \_ [**IWMStatusCallback::OnStatus-Rückrufmethode.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) Wenn Ihr Rückruf diese Nachricht empfängt, rufen Sie die [**IWMReaderPlaylistList-Methode::GetInitResults**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-getinitresults) auf, um die Ergebnisse der Lizenzüberprüfung zu erhalten. Diese Methode verwendet ein Array von **HRESULT-Variablen,** die den Dateinamen im Array entsprechen, die **an InitPlaylistList Übergeben werden.** Wenn alle Werte im Ergebnisarray gleich S \_ OK sind, können Sie fortfahren. Wenn ein Ergebnis ein Fehlercode ist, darf die Wiedergabeliste nicht kopiert werden.
6.  Öffnen und lesen Sie jede Datei, indem Sie dieselbe Instanz des Readers verwenden. Sie müssen die Dateien in der Reihenfolge öffnen, in der die Dateinamen in dem An **initPlaylistList** Übergebenen Dateinamenarray enthalten sind.
7.  Wenn Sie alle Dateien in die Wiedergabeliste kopiert haben, rufen Sie [**die IWMReaderPlaylistListWiederherstellen::EndPlaylistList Auf,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-endplaylistburn) um den Wiedergabelisten-Burn-Prozess fertig zu stellen und die vom Reader verwendeten Ressourcen frei zu geben.

> [!Note]  
> DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Aktivieren der DRM-Unterstützung**](enabling-drm-support.md)
</dt> </dl>

 

 




