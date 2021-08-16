---
title: Importieren von Lizenz- und Schlüsselmaterial
description: Importieren von Lizenz- und Schlüsselmaterial
ms.assetid: 72ce5901-3e5b-4339-b695-592895ac6bfe
keywords:
- Windows Medienformat-SDK, DRM-Import
- Windows Media Format SDK,import
- Windows Medienformat-SDK, Lizenzen
- Digital Rights Management (DRM), Importieren
- DRM (Digital Rights Management), Import
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Digital Rights Management (DRM), Schlüsselmaterial
- DRM (Digital Rights Management), Schlüsselmaterial
- ERWEITERTE APIs des DRM-Clients,Import
- Erweiterte Client-APIs,Import
- ERWEITERTE APIs für DEN DRM-Client, Lizenzen
- Erweiterte Client-APIs,Lizenzen
- ERWEITERTE APIs des DRM-Clients, Schlüsselmaterial
- Erweiterte Client-APIs, Schlüsselmaterial
- licenses,importing
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

Wenn Sie über Medieninhalte verfügen, die mit einem Inhaltsschutzsystem eines Drittanbieters verschlüsselt wurden, und Sie die Lizenz und das Schlüsselmaterial in Windows Media DRM importieren möchten, führen Sie die folgenden Schritte aus:

1.  Rufen Sie die Windows Media DRM-Computerzertifikatsammlung ab, indem Sie [**die IWMDRMSecurity::GetMachineCertificate-Methode**](iwmdrmsecurity-getmachinecertificate.md) aufrufen.
2.  Analysieren Sie die Zertifikatsammlung, und stellen Sie sicher, dass sie ordnungsgemäß signiert und auf einen bekannten öffentlichen Microsoft-Stammschlüssel überprüft wird. Die Zertifikatsammlung entspricht dem XMR-Schema. Weitere Informationen finden Sie unter [Erstellen einer XMR-Lizenz.](building-an-xmr-license.md)
3.  Optional: Extrahieren Sie die Sperrliste, indem Sie [**die IWMDRMSecurity::GetRevocationData-Methode**](iwmdrmsecurity-getrevocationdata.md) aufrufen.
4.  Optional: Sie können sicher sein, dass kein Zertifikat in der Sammlung widerrufen wird. Weitere Informationen finden Sie unter [Überprüfen der Zertifikatsperrung.](checking-certificate-revocation.md)
5.  Generieren Sie eine Lizenz im XMR-Format, die die Richtlinienanforderungen für den Importinhalt darstellt und das entsprechende Windows Media DRM-Schlüsselmaterial enthält. Weitere Informationen finden Sie im Thema [Erstellen einer XMR-Lizenz.](building-an-xmr-license.md)
6.  Übergeben Sie die XMR-Lizenz mithilfe der [**IWMDRMLicenseManagement::StoreLicense-Methode**](iwmdrmlicensemanagement-storelicense.md) an das Windows Media DRM-System für die Verarbeitung.

> [!Note]  
> Details zum XMR-Schema werden Ihnen zur Verfügung gestellt, wenn Sie eine Lizenz Windows Media DRM erstellen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Überprüfen der Zertifikatsperrung**](checking-certificate-revocation.md)
</dt> <dt>

[**Erstellen einer XMR-Lizenz**](building-an-xmr-license.md)
</dt> <dt>

[**DRM-Import**](drm-import.md)
</dt> </dl>

 

 




