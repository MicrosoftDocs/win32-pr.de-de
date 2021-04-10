---
title: Automatische Lizenz Beschaffung
description: Automatische Lizenz Beschaffung
ms.assetid: bf88f1bb-0cbb-4c30-92e0-3d342977d67f
keywords:
- Windows Media-Format-SDK, automatische Lizenz Beschaffung
- Windows Media-Format-SDK, Lizenzen
- Digital Rights Management (DRM), automatische Lizenz Beschaffung
- DRM (Digital Rights Management), automatische Lizenz Beschaffung
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Erweiterte APIs für den DRM-Client, automatische Lizenz Beschaffung
- Erweiterte Client-APIs, automatische Lizenz Beschaffung
- Automatische Lizenz Beschaffung
- Lizenzen, automatische Lizenz Beschaffung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7ef92eaf4e347e8eb30f56c1111ec5b27f1e62d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037250"
---
# <a name="silent-license-acquisition"></a>Automatische Lizenz Beschaffung

Der automatische Erwerb von Lizenzen erfordert nur einen einzigen Methoden Aufrufs, der die gesamte Netzwerkkommunikation mit dem Lizenzserver asynchron verarbeitet.

Diese Art der Lizenz Erfassung wird normalerweise als Antwort an den Endbenutzer verwendet, der versucht, auf geschützte Inhalte zuzugreifen – beispielsweise, wenn versucht wird, eine geschützte Datei in einer Media Player-Anwendung wiederzugeben. Da der automatische Lizenzerwerb die Lizenz mit einem einzigen-Befehl erhält, kann er nicht verwendet werden, wenn zusätzliche Benutzereingaben, z. b. die Zahlung für den Inhalt, erforderlich sind.

Führen Sie die folgenden Schritte aus, um eine automatische Lizenz Erfassung durchzuführen:

1.  Nennen Sie die [**iwmdrmlicenabmanagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) -Methode. Übergeben Sie den DRM-Header aus der geschützten Datei als *bstrinheaderdata* -Parameter. Geben Sie an, welche Rechte von der Lizenz im *bstractions* -Parameter erteilt werden sollen. Legen Sie schließlich den *dwFlags* -Parameter auf "WMDRM-Lizenz abrufen" automatisch fest \_ \_ \_ .
2.  Trap Ereignisse für die [**iwmdrmlicentsmanagement**](iwmdrmlicensemanagement.md) -Schnittstelle. Wenn Sie das **mewmdrmlicenseacquisitionabgeschlossene** -Ereignis empfangen, überprüfen Sie seinen Rückgabecode, indem Sie die **imfmediaevent:: GetStatus** -Methode aufrufen, die in der Media Foundation-Dokumentation dokumentiert ist. Wenn der abgerufene **HRESULT** -Wert ein Erfolgs Code ist, wurde die Lizenz erfolgreich heruntergeladen und befindet sich im lokalen Lizenz Speicher, der verwendet werden kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erwerben von Lizenzen**](acquiring-licenses.md)
</dt> <dt>

[**Verwenden des Media Foundation-Ereignis Modells**](using-the-media-foundation-model.md)
</dt> </dl>

 

 




