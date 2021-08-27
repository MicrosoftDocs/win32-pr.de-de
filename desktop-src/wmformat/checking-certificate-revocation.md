---
title: Überprüfen der Zertifikatsperrung
description: Überprüfen der Zertifikatsperrung
ms.assetid: 498bd2a5-4336-4fc4-9718-6c5fe2db9066
keywords:
- Windows Medienformat-SDK, DRM-Import
- Windows Medienformat-SDK,Importieren
- Windows Medienformat-SDK, Zertifikatsperrung
- Windows Medienformat-SDK,Sperrung von Zertifikaten
- Digital Rights Management (DRM), Importieren
- DRM (Verwaltung digitaler Rechte),Importieren
- Digital Rights Management (DRM), Zertifikatsperrung
- DRM (Digital Rights Management), Zertifikatsperrung
- Digital Rights Management (DRM), Sperrung von Zertifikaten
- DRM (Verwaltung digitaler Rechte),Sperrung von Zertifikaten
- Erweiterte APIs des DRM-Clients, Importieren
- Erweiterte Client-APIs, Importieren
- Erweiterte APIs des DRM-Clients, Zertifikatsperrung
- Erweiterte Client-APIs, Zertifikatsperrung
- Erweiterte DRM-Client-APIs, Sperrung von Zertifikaten
- Erweiterte Client-APIs,Sperrung von Zertifikaten
- Zertifikate,Sperrung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c3d9f8aaa299873513f88a2be258cf2ddd96147934e461cbde49630542fd9b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028068"
---
# <a name="checking-certificate-revocation"></a>Überprüfen der Zertifikatsperrung

Beim Importieren von Inhalten in Windows Medien-DRM müssen Sie sicherstellen, dass kein Zertifikat in einer Zertifikatsammlung widerrufen wurde, indem Sie überprüfen, ob kein Zertifikat in der Sammlung in der Sperrliste enthalten ist. Die Sperrliste wird mithilfe der [**IWMDRMSecurity::GetRevocationData-Methode**](iwmdrmsecurity-getrevocationdata.md) extrahiert.

Verwenden Sie dann die [**IWMDRMSecurity::CheckCertForRevocation-Methode,**](iwmdrmsecurity-checkcertforrevocation.md) um zu überprüfen, ob das Zertifikat nicht widerrufen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**DRM-Import**](drm-import.md)
</dt> </dl>

 

 




