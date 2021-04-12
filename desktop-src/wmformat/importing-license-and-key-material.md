---
title: Importieren von Lizenz-und Schlüssel Material
description: Importieren von Lizenz-und Schlüssel Material
ms.assetid: 72ce5901-3e5b-4339-b695-592895ac6bfe
keywords:
- Windows Media-Format-SDK, DRM-Import
- SDK für Windows Media-Format, importieren
- Windows Media-Format-SDK, Lizenzen
- Digital Rights Management (DRM), importieren
- DRM (Digital Rights Management), importieren
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Digital Rights Management (DRM), Schlüsselmaterial
- DRM (Digital Rights Management), Schlüsselmaterial
- Erweiterte APIs für den DRM-Client, Import
- Erweiterte Client-APIs, importieren
- Erweiterte APIs für den DRM-Client, Lizenzen
- Erweiterte Client-APIs, Lizenzen
- Erweiterte APIs für den DRM-Client, Schlüsselmaterial
- Erweiterte Client-APIs, Schlüsselmaterial
- Lizenzen, importieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a142d0087916a45b6dd8661b67f7e42eaed245c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207304"
---
# <a name="importing-license-and-key-material"></a>Importieren von Lizenz-und Schlüssel Material

Wenn Sie über Medieninhalte verfügen, die mit einem Drittanbieter-Inhalts Schutzsystem verschlüsselt wurden, und Sie die Lizenz und das Schlüsselmaterial in Windows Media DRM importieren möchten, führen Sie die folgenden Schritte aus:

1.  Rufen Sie die Zertifikat Sammlung des Windows Media DRM-Computers durch Aufrufen der [**iwmdrmsecurity:: getmachinecertificate**](iwmdrmsecurity-getmachinecertificate.md) -Methode ab.
2.  Analysieren Sie die Zertifikat Sammlung, und stellen Sie sicher, dass Sie ordnungsgemäß signiert und mit einem bekannten öffentlichen Microsoft-Stamm Schlüssel überprüft wird. Die Zertifikat Sammlung entspricht dem XMR-Schema. Weitere Informationen finden Sie unter [Building a XMR License](building-an-xmr-license.md).
3.  Optional: Extrahieren Sie die Sperr Liste, indem Sie die [**iwmdrmsecurity:: getrevocationdata**](iwmdrmsecurity-getrevocationdata.md) -Methode aufrufen.
4.  Optional: Stellen Sie sicher, dass kein Zertifikat in der Sammlung widerrufen wird. Weitere Informationen finden Sie unter über [Prüfen der Zertifikat](checking-certificate-revocation.md)Sperrung.
5.  Generieren Sie eine Lizenz im XMR-Format, die die Richtlinien Anforderungen für den Import Inhalt darstellt und das entsprechende Windows Media DRM-Schlüsselmaterial enthält. Weitere Informationen finden Sie im Thema zum [aufbauen einer XMR-Lizenz](building-an-xmr-license.md).
6.  Übergeben Sie die XMR-Lizenz zur Verarbeitung an das Windows Media DRM-System, indem Sie die [**iwmdrmlicenpasmanagement:: storelicense**](iwmdrmlicensemanagement-storelicense.md) -Methode verwenden.

> [!Note]  
> Details zum XMR-Schema werden Ihnen bei der Lizenzierung von Windows Media DRM bereitgestellt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Zertifikat Sperrung wird überprüft**](checking-certificate-revocation.md)
</dt> <dt>

[**Aufbauen einer XMR-Lizenz**](building-an-xmr-license.md)
</dt> <dt>

[**DRM-Import**](drm-import.md)
</dt> </dl>

 

 




