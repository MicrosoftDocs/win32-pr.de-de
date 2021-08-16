---
title: Konvertieren einer DRM-Protected-Datei in einen Windows Media DRM 10 for Network Devices Stream
description: Konvertieren einer DRM-Protected-Datei in einen Windows Media DRM 10 for Network Devices Stream
ms.assetid: 11aa0cfd-6d87-4ec4-82d8-db2507402911
keywords:
- Windows Medienformat-SDK, Konvertieren von DRM-geschützten Dateien
- Windows Medienformat-SDK, DRM-geschützte Dateien
- Advanced Systems Format (ASF), Konvertieren von DRM-geschützten Dateien
- ASF (Advanced Systems Format), Konvertieren von DRM-geschützten Dateien
- Advanced Systems Format (ASF), DRM-geschützte Dateien
- ASF (Advanced Systems Format), DRM-geschützte Dateien
- Digital Rights Management (DRM), Konvertieren von DRM-geschützten Dateien
- DRM (Digital Rights Management), Konvertieren von DRM-geschützten Dateien
- Digital Rights Management (DRM), DRM-geschützte Dateien
- DRM (Digital Rights Management), DRM-geschützte Dateien
- Windows Medienformat-SDK, Windows Media DRM 10 für Netzwerkgeräte
- Windows Medienformat-SDK, DRM 10 für Netzwerkgeräte
- Advanced Systems Format (ASF), Windows Media DRM 10 für Netzwerkgeräte
- ASF (Advanced Systems Format), Windows Media DRM 10 für Netzwerkgeräte
- Advanced Systems Format (ASF), DRM 10 für Netzwerkgeräte
- ASF (Advanced Systems Format), DRM 10 für Netzwerkgeräte
- Digital Rights Management (DRM), Windows Media DRM 10 für Netzwerkgeräte
- DRM (Digital Rights Management), Windows Media DRM 10 für Netzwerkgeräte
- Digital Rights Management (DRM), DRM 10 für Netzwerkgeräte
- DRM (Digital Rights Management), DRM 10 für Netzwerkgeräte
- Windows Medien-DRM 10 für Netzwerkgeräte, Konvertieren von DRM-geschützten Dateien
- DRM 10 für Netzwerkgeräte, Konvertieren von DRM-geschützten Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebe5aa16b13f41c0376da84237a846612b7ae6e730e630be6ec4a45ce48ff4fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848911"
---
# <a name="converting-a-drm-protected-file-to-a-windows-media-drm-10-for-network-devices-stream"></a>Konvertieren einer DRM-Protected-Datei in einen Windows Media DRM 10 for Network Devices Stream

Nachdem ein Gerät registriert und überprüft wurde, können Sie damit beginnen, Lizenzanforderungsnachrichten zu verarbeiten. Lizenzanforderungsnachrichten werden von Geräten gesendet, wenn eine Aktion von der Anwendung erforderlich ist. Die einzige derzeit unterstützte Aktion ist "Play", bei der es sich um eine Anforderung sicherer Daten für die Wiedergabe handelt.

Wenn Sie eine Lizenzanforderungsmeldung erhalten, sollten Sie die folgenden Schritte ausführen:

1.  Analysieren Sie die Lizenzanforderungsnachricht, indem Sie [**die IWMDRMMessageParser::P arseLicenseRequestMsg-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parselicenserequestmsg) aufrufen.
2.  Rufen Sie die [**IWMRegisteredDevice-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice) für das Gerät ab, indem Sie die [**IWMDeviceRegistration::GetRegisteredDeviceByID-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) aufrufen und das In Schritt 1 erhaltene Zertifikat und die Seriennummer übergeben.
3.  Vergewissern Sie sich, dass das Gerät für den Empfang sicherer Daten bereit ist:
    -   Rufen [**Sie IWMRegisteredDevice::IsApproved**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isapproved) auf, um zu überprüfen, ob das Gerät genehmigt wurde. Die Genehmigung sollte immer auf der Benutzereinstellung basieren.
    -   Rufen [**Sie IWMRegisteredDevice::IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) auf, um zu überprüfen, ob das Gerät innerhalb der letzten 48 Stunden überprüft wurde. Wenn das Gerät ungültig ist, müssen Sie die Näherungserkennung durchführen. Weitere Informationen finden Sie unter [Ausführen der Näherungserkennung.](performing-proximity-detection.md)
    -   Rufen [**Sie IWMRegisteredDevice::IsOpened**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isopened) auf, um zu überprüfen, ob das Gerät geöffnet wurde. Wenn das Gerät nicht geöffnet ist, können Sie es öffnen, indem Sie [**IWMRegisteredDevice::Open aufrufen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open) Auf dem Computer können nur zehn Geräte gleichzeitig geöffnet sein. Möglicherweise müssen Sie ein anderes Gerät schließen, bevor Sie das Gerät öffnen können, für das Sie die Anforderung verarbeiten. Um ein Gerät zu schließen, rufen Sie die [**IWMRegisteredDevice::Close-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-close) auf.
4.  Erstellen Sie eine Instanz des DRM-Transcryptorobjekts, indem Sie die [**WMCreateDRMTranscryptor-Funktion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor) aufrufen.
5.  Rufen Sie [**die IWMDRMTranscryptor::Initialize-Methode auf,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-initialize) um den Transcryptor zu initialisieren. Diese Methode verwendet einen Zeiger auf Ihre Implementierung der [**IWMStatusCallback-Schnittstelle,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) die zum Senden von Statusmeldungen verwendet wird. Diese Methode gibt auch eine Lizenzanforderungsnachricht zurück, die an das Gerät gesendet werden muss, bevor Sie fortfahren.
6.  Wenn die [**IWMStatusCallback::OnStatus-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) Ihrer Anwendung die WMT TRANSCRYPTOR INIT-Statusmeldung empfängt, rufen Sie die \_ \_ [**IWMDRMTranscryptor::Seek-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-seek) auf, um die entsprechende Startposition in der Datei zu suchen. Um am Anfang der Datei zu beginnen, müssen Sie **Seek** mit der Zeit 0 aufrufen.
7.  Der Transcryptor sendet eine WMT TRANSCRYPTOR SEEKED-Nachricht, wenn er bereit ist, Daten aus der Datei zur \_ \_ neuen Präsentationszeit zu liefern. Führen Sie wiederholte Aufrufe an [**die IWMDRMTranscryptor::Read-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-read) aus, um konvertierte Mediendaten zu erhalten. Jeder Aufruf ist asynchron und erst abgeschlossen, wenn eine WMT \_ TRANSCRYPTOR \_ READ-Nachricht empfangen wird. Wenn Sie die Nachricht erhalten, können Sie die Daten an das empfangende Gerät senden.
8.  Wenn Sie eine WMT TRANSCRYPTOR READ-Nachricht mit dem parameter hr erhalten, der auf \_ \_ NS S  \_ \_ TRANSCRYPTOR EOF festgelegt ist, \_ wurde die gesamte Datei gelesen. Rufen Sie an diesem Punkt die [**IWMDRMTranscryptor::Close-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-close) auf, um die Datei und die freien Ressourcen zu schließen.
9.  Wenn die WMT \_ TRANSCRYPTOR \_ CLOSED-Nachricht empfangen wird, können Sie die [**IWMDRMTranscryptor-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmtranscryptor) veröffentlichen.

> [!Note]  
> DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden des Windows Media DRM 10 for Network Devices Protocol**](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




