---
title: Wandeln Sie eine DRM-Protected Datei in eine Windows Media DRM 10 for Network Devices Stream-Datei um.
description: Wandeln Sie eine DRM-Protected Datei in eine Windows Media DRM 10 for Network Devices Stream-Datei um.
ms.assetid: 11aa0cfd-6d87-4ec4-82d8-db2507402911
keywords:
- Windows Media-Format-SDK, Umrechnen von DRM-geschützten Dateien
- Windows Media-Format-SDK, DRM-geschützte Dateien
- Advanced Systems Format (ASF), das wandeln von DRM-geschützten Dateien
- ASF (Advanced Systems Format), Umrechnen von DRM-geschützten Dateien
- Advanced Systems Format (ASF), DRM-geschützte Dateien
- ASF (Advanced Systems Format), DRM-geschützte Dateien
- Digital Rights Management (DRM), das Umrechnen von DRM-geschützten Dateien
- DRM (Digital Rights Management), Umrechnen von DRM-geschützten Dateien
- Digital Rights Management (DRM), DRM-geschützte Dateien
- DRM-Dateien (Digital Rights Management), DRM-geschützte Dateien
- Windows Media-Format-SDK, Windows Media DRM 10 für Netzwerkgeräte
- Windows Media-Format-SDK, DRM 10 für Netzwerkgeräte
- Advanced Systems Format (ASF), Windows Media DRM 10 für Netzwerkgeräte
- ASF (Advanced Systems Format), Windows Media DRM 10 für Netzwerkgeräte
- Advanced Systems Format (ASF), DRM 10 für Netzwerkgeräte
- ASF (Advanced Systems Format), DRM 10 für Netzwerkgeräte
- Digital Rights Management (DRM), Windows Media DRM 10 für Netzwerkgeräte
- DRM (Digital Rights Management), Windows Media DRM 10 für Netzwerkgeräte
- Digital Rights Management (DRM), DRM 10 für Netzwerkgeräte
- DRM (Digital Rights Management), DRM 10 für Netzwerkgeräte
- Windows Media DRM 10 für Netzwerkgeräte, das Umrechnen von DRM-geschützten Dateien
- DRM 10 für Netzwerkgeräte, Umrechnen von DRM-geschützten Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 644c1b4f7ede688434fbb1dde11b7051c6f644a5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723600"
---
# <a name="converting-a-drm-protected-file-to-a-windows-media-drm-10-for-network-devices-stream"></a>Wandeln Sie eine DRM-Protected Datei in eine Windows Media DRM 10 for Network Devices Stream-Datei um.

Nachdem ein Gerät registriert und überprüft wurde, können Sie mit der Verarbeitung von Lizenz Anforderungs Nachrichten beginnen. Lizenz Anforderungs Nachrichten werden von Geräten gesendet, wenn eine Aktion aus der Anwendung erforderlich ist. Die einzige derzeit unterstützte Aktion ist "Play", bei der es sich um eine Anforderung für sichere Daten für die Wiedergabe handelt.

Wenn Sie eine Lizenz Anforderungs Nachricht erhalten, sollten Sie die folgenden Schritte ausführen:

1.  Analysieren Sie die Lizenz Anforderungs Nachricht, indem Sie die [**iwmdrmmessageparser::P arselicenserequestmsg**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parselicenserequestmsg) -Methode aufrufen.
2.  Rufen Sie die [**iwmregistereddevice**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice) -Schnittstelle für das Gerät ab, indem Sie die [**iwmdeviceregistration:: getregistereddevicebyid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) -Methode aufrufen und das Zertifikat und die Seriennummer übergeben, die Sie in Schritt 1 abgerufen haben.
3.  Vergewissern Sie sich, dass das Gerät für den Empfang sicherer Daten bereit ist:
    -   Nennen Sie [**iwmregistereddevice:: IsApproved**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isapproved) , um zu überprüfen, ob das Gerät genehmigt wurde. Die Genehmigung sollte immer auf der Benutzereinstellung basieren.
    -   Nennen Sie [**iwmregistereddevice:: IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) , um sicherzustellen, dass das Gerät innerhalb der letzten 48 Stunden überprüft wurde. Wenn das Gerät nicht gültig ist, müssen Sie die Near-Erkennung durchführen. Weitere Informationen finden Sie unter [Durchführen der Near-Erkennung](performing-proximity-detection.md).
    -   Nennen Sie [**iwmregistereddevice:: isgeöffnet**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isopened) , um zu überprüfen, ob das Gerät geöffnet wurde. Wenn das Gerät nicht geöffnet ist, können Sie es durch Aufrufen von [**iwmregistereddevice:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open)öffnen. Es können jeweils nur 10 Geräte auf dem Computer geöffnet sein. Möglicherweise müssen Sie ein anderes Gerät schließen, bevor Sie das öffnen können, für das Sie die Anforderung verarbeiten. Um ein Gerät zu schließen, müssen Sie die [**iwmregistereddevice:: Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-close) -Methode aufrufen.
4.  Erstellen Sie eine Instanz des DRM-transryptor-Objekts, indem Sie die [**wmcreatedrmtranscryptor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor) -Funktion aufrufen.
5.  Nennen Sie die [**iwmdrmtranszenryptor:: Initialisieren**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-initialize) -Methode, um den transzenryptor zu initialisieren. Diese Methode nimmt einen Zeiger auf Ihre Implementierung der [**iwmstatuscallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) -Schnittstelle an, die für die Bereitstellung von Statusmeldungen verwendet wird. Diese Methode gibt auch eine Lizenz Anforderungs Nachricht zurück, die an das Gerät gesendet werden muss, bevor Sie fortfahren.
6.  Wenn die [**iwmstatuscallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) -Methode der Anwendung die WMT- \_ transryptor- \_ Init-Statusmeldung empfängt, rufen Sie die [**iwmdrmtranszenryptor:: Seek**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-seek) -Methode auf, um die entsprechende Startposition in der Datei zu suchen. Um am Anfang der Datei zu beginnen, müssen Sie **Seek** mit der Zeit 0 (null) aufzurufen.
7.  Der transryptor sendet eine WMT- \_ \_ transryptornachricht, wenn er bereit ist, Daten aus der Datei zum Zeitpunkt der neuen Präsentation bereitzustellen. Führen Sie wiederholte Aufrufe der [**iwmdrmtranszenryptor:: Read**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-read) -Methode aus, um konvertierte Blöcke von Mediendaten zu erhalten. Jeder-Rückruf ist asynchron und wird erst beendet, wenn eine WMT- \_ transryptor- \_ Lese Nachricht empfangen wird. Wenn Sie die Meldung erhalten, können Sie die Daten an das empfangende Gerät senden.
8.  Wenn Sie eine WMT- \_ transryptor- \_ Lese Nachricht empfangen, bei der der *HR* -Parameter auf NS \_ S- \_ transryptor \_ EOF festgelegt ist, wurde die gesamte Datei gelesen. Nennen Sie an diesem Punkt die [**iwmdrmtranszenryptor:: Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-close) -Methode, um die Datei zu schließen und Ressourcen freizugeben.
9.  Wenn die geschlossene WMT- \_ transryptor- \_ Nachricht empfangen wird, können Sie die [**iwmdrmtranszenryptor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmtranscryptor) -Schnittstelle freigeben.

> [!Note]  
> DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden des Protokolls "Windows Media DRM 10 for Network Devices"**](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




