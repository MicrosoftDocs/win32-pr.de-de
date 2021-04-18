---
title: Brennen von Wiedergabelisten, die sichere Dateien enthalten
description: Brennen von Wiedergabelisten, die sichere Dateien enthalten
ms.assetid: 0d9415a1-a154-4fe4-af4c-cce4cb05ade5
keywords:
- Windows Media-Format-SDK, Brennen von Wiedergabelisten mit sicheren Dateien
- Windows Media-Format-SDK, Wiedergabelisten mit sicheren Dateien
- Advanced Systems Format (ASF), Brennen von Wiedergabelisten mit sicheren Dateien
- ASF (Advanced Systems Format), Brennen von Wiedergabelisten mit sicheren Dateien
- Advanced Systems Format (ASF), Wiedergabelisten mit sicheren Dateien
- ASF (Advanced Systems Format), Wiedergabelisten mit sicheren Dateien
- Digital Rights Management (DRM), Brennen von Wiedergabelisten mit sicheren Dateien
- DRM (Digital Rights Management), Brennen von Wiedergabelisten mit sicheren Dateien
- Digital Rights Management (DRM), Wiedergabelisten mit sicheren Dateien
- DRM (Digital Rights Management), Wiedergabelisten mit sicheren Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214c1dbd4ee08f90b3e5e8aa6186508af5044f29
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "106337211"
---
# <a name="burning-playlists-that-contain-secure-files"></a>Brennen von Wiedergabelisten, die sichere Dateien enthalten

Lizenzen, die mithilfe der Objekte des Windows Media Rights Manager 10 SDK erstellt wurden, können angeben, dass eine Datei im Rahmen einer Wiedergabeliste auf eine kompakte CD kopiert werden soll. Diese Funktion, die als Wiedergabelisten brennen bezeichnet wird, erfordert, dass Sie die Lizenzen aller Dateien in der Wiedergabeliste überprüfen, bevor Sie mit dem Kopieren der Daten beginnen. Das Windows Media-Format-SDK stellt die [**iwmreaderplaylistburn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) -Schnittstelle bereit, um die Dateiüberprüfung auszuführen.

Führen Sie die folgenden Schritte aus, um die Wiedergabelisten Verbrennung zu implementieren:

1.  Erstellen Sie eine Instanz des Reader-Objekts oder des synchronen Reader-Objekts. Weitere Informationen finden Sie unter [Lesen von ASF-Dateien](reading-asf-files.md).
2.  Rufen Sie die **QueryInterface** -Methode der Reader-Schnittstelle ([**iwmreader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader) oder [**iwmsynkreader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)) auf, um einen Zeiger auf die [**iwmreaderplaylistburn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) -Schnittstelle zu erhalten.
3.  Kopieren Sie die Dateinamen aus der Wiedergabeliste in ein Array von Zeichen folgen mit breit Zeichen. Die Dateinamen im-Array müssen in derselben Reihenfolge vorliegen, in der Sie in der Wiedergabeliste angezeigt werden.
4.  Nennen Sie die [**iwmreaderplaylistburn:: initplaylistburn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-initplaylistburn) -Methode, und übergeben Sie einen Zeiger auf das in Schritt 3 erstellte Array, um die Lizenz Überprüfung für die Dateien zu initialisieren.
5.  Wenn die Lizenz Überprüfung abgeschlossen ist, sendet das Reader-Objekt eine WMT-init-Wiedergabelisten- \_ \_ Burn- \_ Meldung an Ihre Implementierung der [**iwmstatuscallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) -Rückruf Methode. Wenn Ihr Rückruf diese Nachricht empfängt, rufen Sie die [**iwmreaderplaylistburn:: getinitresults**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-getinitresults) -Methode auf, um die Ergebnisse der Lizenzprüfung abzurufen. Diese Methode verwendet ein Array von **HRESULT** -Variablen, die den Dateinamen im-Array entsprechen, die an **initplaylistburn** übergeben werden. Wenn alle Werte im Ergebnis Array gleich S \_ OK sind, können Sie den Vorgang fortsetzen. Wenn ein Ergebnis ein Fehlercode ist, darf die Wiedergabeliste nicht kopiert werden.
6.  Wenn Sie die gleiche Instanz des Readers verwenden, öffnen Sie jede Datei, und lesen Sie Sie. Sie müssen die Dateien in der Reihenfolge öffnen, in der die Dateinamen im Dateinamen Array in **initplaylistburn** übergeben wurden.
7.  Wenn Sie alle Dateien in der Wiedergabeliste kopiert haben, nennen Sie die Datei " [**iwmreaderplaylistburn:: endplaylistburn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-endplaylistburn) ", um den Wiedergabe Prozess der Wiedergabeliste abzuschließen und die vom Reader verwendeten Ressourcen freizugeben.

> [!Note]  
> DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Aktivieren DRM-Unterstützung**](enabling-drm-support.md)
</dt> </dl>

 

 




