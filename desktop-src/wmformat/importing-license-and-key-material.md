---
title: Importieren von Lizenz- und Schlüsselmaterial
description: Importieren von Lizenz- und Schlüsselmaterial
ms.assetid: 72ce5901-3e5b-4339-b695-592895ac6bfe
keywords:
- Windows Medienformat-SDK, DRM-Import
- Windows Medienformat-SDK,Importieren
- Windows Medienformat-SDK, Lizenzen
- Digital Rights Management (DRM), Importieren
- DRM (Verwaltung digitaler Rechte),Importieren
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Digital Rights Management (DRM), Schlüsselmaterial
- DRM (Digital Rights Management), Schlüsselmaterial
- Erweiterte APIs des DRM-Clients, Importieren
- Erweiterte Client-APIs, Importieren
- Erweiterte APIs des DRM-Clients, Lizenzen
- Erweiterte Client-APIs, Lizenzen
- Erweiterte DRM-Client-APIs, Schlüsselmaterial
- Erweiterte Client-APIs, Schlüsselmaterial
- Lizenzen,Importieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c9852102ab282c983488c2e5c35b7187bf0daccb62d347c312d1afb343b60f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118702504"
---
# <a name="importing-license-and-key-material"></a>Importieren von Lizenz- und Schlüsselmaterial

Wenn Sie über Medieninhalte verfügen, die mit einem Inhaltsschutzsystem eines Drittanbieters verschlüsselt wurden, und Sie die Lizenz und das Schlüsselmaterial in Windows Medien-DRM importieren möchten, führen Sie die folgenden Schritte aus:

1.  Rufen Sie die Windows Media DRM-Computerzertifikatsammlung ab, indem Sie die [**IWMDRMSecurity::GetMachineCertificate-Methode**](iwmdrmsecurity-getmachinecertificate.md) aufrufen.
2.  Analysieren Sie die Zertifikatsammlung, und stellen Sie sicher, dass sie ordnungsgemäß signiert und mit einem bekannten öffentlichen Microsoft-Stammschlüssel überprüft wird. Die Zertifikatauflistung entspricht dem XMR-Schema. Weitere Informationen finden Sie unter [Erstellen einer XMR-Lizenz.](building-an-xmr-license.md)
3.  Optional: Extrahieren Sie die Sperrliste, indem Sie die [**IWMDRMSecurity::GetRevocationData-Methode**](iwmdrmsecurity-getrevocationdata.md) aufrufen.
4.  Optional: Stellt sicher, dass kein Zertifikat in der Auflistung widerrufen wird. Weitere Informationen finden Sie unter [Überprüfen der Zertifikatsperrung.](checking-certificate-revocation.md)
5.  Generieren Sie eine Lizenz im XMR-Format, die die Richtlinienanforderungen für den Importinhalt darstellt und das entsprechende Windows Medien-DRM-Schlüsselmaterial enthält. Weitere Informationen finden Sie im Thema [Erstellen einer XMR-Lizenz.](building-an-xmr-license.md)
6.  Übergeben Sie die XMR-Lizenz zur Verarbeitung an das Windows Media DRM-System, indem Sie die [**IWMDRMLicenseManagement::StoreLicense-Methode**](iwmdrmlicensemanagement-storelicense.md) verwenden.

> [!Note]  
> Details zum XMR-Schema werden Ihnen bereitgestellt, wenn Sie Windows Media DRM lizenziert haben.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Überprüfen der Zertifikatsperrung**](checking-certificate-revocation.md)
</dt> <dt>

[**Erstellen einer XMR-Lizenz**](building-an-xmr-license.md)
</dt> <dt>

[**DRM-Import**](drm-import.md)
</dt> </dl>

 

 




