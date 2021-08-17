---
title: Unbeaufsichtigter Lizenzerwerb
description: Unbeaufsichtigter Lizenzerwerb
ms.assetid: bf88f1bb-0cbb-4c30-92e0-3d342977d67f
keywords:
- Windows Medienformat-SDK, unbeaufsichtigter Lizenzerwerb
- Windows Medienformat-SDK, Lizenzen
- Digital Rights Management (DRM), unbeaufsichtigter Lizenzerwerb
- DRM (Digital Rights Management), unbeaufsichtigter Lizenzerwerb
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Erweiterte DRM-Client-APIs, unbeaufsichtigter Lizenzerwerb
- Erweiterte Client-APIs, automatischer Lizenzerwerb
- Unbeaufsichtigter Lizenzerwerb
- Lizenzen, unbeaufsichtigter Lizenzerwerb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eff454ce673230f0c7dbe6f64afbf46e9bbe8b5f948609f5fb67d647a4151ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197462"
---
# <a name="silent-license-acquisition"></a>Unbeaufsichtigter Lizenzerwerb

Der automatische Lizenzerwerb erfordert nur einen einzigen Methodenaufruf, der die gesamte Netzwerkkommunikation mit dem Lizenzserver asynchron verarbeitet.

Diese Art des Lizenzerwerbs wird in der Regel als Reaktion auf den Endbenutzer verwendet, der versucht, auf geschützte Inhalte zuzugreifen, z. B. beim Versuch, eine geschützte Datei in einer Media Player-Anwendung wiederzugeben. Da der automatische Lizenzerwerb die Lizenz mit einem einzigen Aufruf abruft, kann sie nicht verwendet werden, wenn zusätzliche Eingaben vom Benutzer erforderlich sind, z. B. eine Zahlung für den Inhalt.

Führen Sie die folgenden Schritte aus, um den automatischen Lizenzerwerb durchzuführen:

1.  Rufen Sie die [**IWMDRMLicenseManagement::AcquireLicense-Methode**](iwmdrmlicensemanagement-acquirelicense.md) auf. Übergeben Sie den DRM-Header aus der geschützten Datei als *bstrHeaderData-Parameter.* Geben Sie im *bstrActions-Parameter* an, welche Rechte die Lizenz erteilen soll. Legen Sie abschließend den *dwFlags-Parameter* auf WMDRM \_ ACQUIRE LICENSE SILENT \_ \_ fest.
2.  Trapereignisse für die [**IWMDRMLicenseManagement-Schnittstelle.**](iwmdrmlicensemanagement.md) Wenn Sie das **MEWMDRMLicenseAcquisitionCompleted-Ereignis** erhalten, überprüfen Sie dessen Rückgabecode, indem Sie die **METHODE "WFMediaEvent::GetStatus"** aufrufen, die in der Media Foundation-Dokumentation dokumentiert ist. Wenn der abgerufene **HRESULT-Wert** ein Erfolgscode ist, wurde die Lizenz erfolgreich heruntergeladen und befindet sich im lokalen Lizenzspeicher, der zur Verwendung bereit ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erwerben von Lizenzen**](acquiring-licenses.md)
</dt> <dt>

[**Verwenden des Media Foundation-Ereignismodells**](using-the-media-foundation-model.md)
</dt> </dl>

 

 




