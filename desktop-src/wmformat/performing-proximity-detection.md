---
title: Durchführen der Näherungserkennung
description: Durchführen der Näherungserkennung
ms.assetid: 73207c4c-2d8d-4ec3-b3d0-78f55ee0a754
keywords:
- Windows Medienformat-SDK, Durchführen der Näherungserkennung
- Windows Medienformat-SDK, Näherungserkennung
- Advanced Systems Format (ASF), durchführen der Näherungserkennung
- ASF (Advanced Systems Format), durchführen der Näherungserkennung
- Advanced Systems Format (ASF), Näherungserkennung
- ASF (Advanced Systems Format), Näherungserkennung
- Digital Rights Management (DRM), Durchführen der Näherungserkennung
- DRM (Digital Rights Management), Durchführen der Näherungserkennung
- Digital Rights Management (DRM), Näherungserkennung
- DRM (Digital Rights Management), Näherungserkennung
- Näherungserkennung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 181b13d56e4c2b1fea0da1ff761f6d915680ff89c42747b9faf4260184ae4205
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963979"
---
# <a name="performing-proximity-detection"></a>Durchführen der Näherungserkennung

Bevor Sie verschlüsselte Daten an ein registriertes Gerät im Windows Media DRM 10 for Network Devices-Protokoll streamen können, müssen Sie einen Prozess namens Näherungserkennung (auch validierung genannt) ausführen. Dieser Prozess umfasst das Senden von Nachrichten an das Gerät und das Empfangen von Antworten. Die Zeit, die zum Empfangen einer Antwort benötigt wird, wird verwendet, um zu bestimmen, ob das Gerät dem Computer im Netzwerk "nahe" genug ist, um sichere Daten zu empfangen. Die Bestätigung, dass sich das Gerät physisch in der Nähe des Clientcomputers im Netzwerk befindet, trägt dazu bei, Spoofing und anderen nicht autorisierten Zugriff zu verhindern.

Wenn die Näherungserkennung erfolgreich abgeschlossen wurde, wird das Gerät als gültig bezeichnet. Sie können überprüfen, ob ein Gerät gültig ist, indem Sie die [**IWMRegisteredDevice::IsValid-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) aufrufen. Geräte müssen alle 48 Stunden überprüft werden. Ein Gerät, das mehr als 48 Stunden vor der Ausführung des Programms überprüft wurde, muss durch erneutes Ausführen des Näherungserkennungsprozesses erneut überprüft werden.

Um die Näherungserkennung durchzuführen, müssen Sie eine Kommunikation mit dem Gerät herstellen und dann die [**IWMProximityDetection::StartDetection-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmproximitydetection-startdetection) aufrufen. Der Erkennungsprozess wird asynchron von den internen DRM-Komponenten des Windows Media Format SDK abgeschlossen. Ihre Anwendung muss eine Implementierung der [**IWMStatusCallback-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) enthalten, um Näherungserkennungsmeldungen zu verarbeiten.

Es gibt zwei Nachrichten, die vom Näherungserkennungsprozess gesendet werden: eine Ergebnisnachricht und eine Abschlussmeldung.

Die Ergebnismeldung WMT \_ PROXIMITY \_ RESULT wird gesendet, wenn der Erkennungsprozess abgeschlossen ist. Der *hr-Parameter* der [**OnStatus-Rückrufmethode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) gibt an, ob das Gerät in der Nähe des Clientcomputers gefunden wurde. Wenn der *hr-Parameter* der Ergebnismeldung auf Erfolg hinweist, enthält der *pValue-Parameter* ein **DWORD,** das die gemessene Latenz für das Gerät in Millisekunden angibt.

Die Abschlussmeldung WMT \_ PROXIMITY \_ COMPLETED wird gesendet, wenn die Erkennung abgeschlossen ist. Sie sollten die [**IWMProximityDetection-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) erst freigeben, nachdem Sie diese Nachricht erhalten haben.

Wenn die Näherungserkennung für ein Gerät erfolgreich ist, wird die Geräteregistrierungsdatenbank automatisch aktualisiert. Nachfolgende Aufrufe von [**IWMRegisteredDevice::IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) geben **TRUE** zurück, bis 48 Stunden vergangen sind und das Gerät erneut überprüft werden muss.

**Hinweis** DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden des Windows Media DRM 10 for Network Devices Protocol**](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




