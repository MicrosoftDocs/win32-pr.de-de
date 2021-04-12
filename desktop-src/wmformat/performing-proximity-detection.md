---
title: Ausführen der Near-Erkennung
description: Ausführen der Near-Erkennung
ms.assetid: 73207c4c-2d8d-4ec3-b3d0-78f55ee0a754
keywords:
- Windows Media-Format-SDK, Ausführen der Near-Erkennung
- Windows Media-Format-SDK, Näherungs Erkennung
- Advanced Systems Format (ASF), durchführen der Near-Erkennung
- ASF (Advanced Systems Format), durchführen der Near-Erkennung
- Advanced Systems Format (ASF), near-Erkennung
- ASF (Advanced Systems Format), near-Erkennung
- Digital Rights Management (DRM), durchführen der Near-Erkennung
- DRM (Digital Rights Management), durchführen der Near-Erkennung
- Digital Rights Management (DRM), Näherungs Erkennung
- DRM (Digital Rights Management), Näherungs Erkennung
- Near-Erkennung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9628a6c33832b56858e5c457f15fd0935c2c436
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389830"
---
# <a name="performing-proximity-detection"></a>Ausführen der Near-Erkennung

Bevor Sie verschlüsselte Daten auf ein registriertes Gerät im Windows Media DRM 10 for Network Devices-Protokoll streamen können, müssen Sie einen Prozess namens near-Erkennung (auch als Validierung bezeichnet) ausführen. Dieser Prozess umfasst das Senden von Nachrichten an das Gerät und das Empfangen von Antworten. Die Zeit, die zum Empfangen einer Antwort benötigt wird, wird verwendet, um zu bestimmen, ob das Gerät für den Computer im Netzwerk "nah" genug ist, um sichere Daten zu erhalten. Wenn Sie bestätigen, dass sich das Gerät physisch in der Nähe des Client Computers im Netzwerk befindet, hilft es, Spoofing und anderen nicht autorisierten Zugriff zu verhindern.

Wenn die Near-Erkennung erfolgreich abgeschlossen wurde, wird das Gerät als gültig bezeichnet. Sie können überprüfen, ob ein Gerät gültig ist, indem Sie die [**iwmregistereddevice:: IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) -Methode aufrufen. Geräte müssen alle 48 Stunden überprüft werden. Ein Gerät, das mehr als 48 Stunden vor der Programmausführung überprüft wurde, muss erneut überprüft werden, indem der Near-Erkennungsprozess erneut ausgeführt wird.

Um die Near-Erkennung durchzuführen, müssen Sie die Kommunikation mit dem Gerät einrichten und dann die [**iwmaccessmityerkennungs:: starterkennungs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmproximitydetection-startdetection) -Methode aufrufen. Der Erkennungs Vorgang wird asynchron von den internen DRM-Komponenten des Windows Media Format SDK abgeschlossen. Die Anwendung muss eine Implementierung der [**iwmstatus Callback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) -Schnittstelle enthalten, um Near-Erkennungs Meldungen zu verarbeiten.

Es gibt zwei Nachrichten, die vom Near-Erkennungsprozess gesendet werden: eine Ergebnis Meldung und eine Abschluss Meldung.

\_Wenn der Erkennungsprozess abgeschlossen ist, wird die Ergebnis Meldung, das WMT-near- \_ Ergebnis, gesendet. Der *HR* -Parameter der [**OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) -Rückruf Methode gibt an, ob das Gerät fast genug für den Client Computer ist. Wenn der *HR* -Parameter der Ergebnis Meldung Erfolg angibt, enthält der *pValue* -Parameter ein **DWORD** , das die gemessene Latenz für das Gerät in Millisekunden angibt.

Die Abschluss Meldung, die WMT- \_ Nähe ist \_ abgeschlossen, wird gesendet, wenn die Erkennung abgeschlossen wird. Sie sollten die [**iwmkurzmityerkennungs**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) -Schnittstelle erst freigeben, nachdem Sie diese Nachricht empfangen haben.

Wenn die Near-Erkennung für ein Gerät erfolgreich ist, wird die Geräte Registrierungsdatenbank automatisch aktualisiert. Nachfolgende Aufrufe von [**iwmregistereddevice:: IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) geben " **true** " zurück, bis 48 Stunden vergangen sind und das Gerät erneut überprüft werden muss.

**Hinweis** DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden des Protokolls "Windows Media DRM 10 for Network Devices"**](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




