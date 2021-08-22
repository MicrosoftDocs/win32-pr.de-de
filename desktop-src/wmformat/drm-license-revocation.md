---
title: Lizenzsperrung (Microsoft Windows Media DRM-Client)
description: Lizenzsperrung (Microsoft Windows Media DRM-Client)
ms.assetid: 615ddddf-4f2f-400d-9c4d-ff3a2851d699
keywords:
- Windows Medienformat-SDK, Lizenzen
- Windows Medienformat-SDK,Lizenzsperrung
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Digital Rights Management (DRM), Lizenzsperrung
- DRM (Digital Rights Management), Lizenzsperrung
- Erweiterte APIs des DRM-Clients, Lizenzen
- Erweiterte Client-APIs, Lizenzen
- Erweiterte APIs des DRM-Clients, Lizenzsperrung
- Erweiterte Client-APIs, Lizenzsperrung
- Lizenzen, Sperrung
- Lizenzsperrung,Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f3cd295ddc1aec40c04f5284d791d7482854208a17875bdd3ed60d998f4ccf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027838"
---
# <a name="license-revocation-microsoft-windows-media-drm-client"></a>Lizenzsperrung (Microsoft Windows Media DRM-Client)

Lizenzsperrung bezieht sich auf das Entfernen von Lizenzen aus einem lokalen Lizenzspeicher. Ein häufiges Szenario für die Lizenzsperrung tritt auf, wenn ein Dienstanbieter, z. B. ein Musikabonnementdienst, den Dienst auf dem Computer eines Benutzers deaktivieren muss.

Der Lizenzsperrprozess wird von einem Vom Lizenzaussteller bereitgestellten Dienst initiiert. Ihre Anwendung kann diesen Dienst hosten, oder es kann sich um eine Webanwendung handelt. In beiden Fällen muss Ihre Anwendung in der Lage sein, eine vom Dienst erstellte Lizenzaufforderung zu erhalten.

Gehen Sie wie folgt vor, um Lizenzen aus dem Lizenzspeicher zu entfernen:

1.  Nachdem Sie eine Lizenzaufforderung vom Lizenzaussteller erhalten haben, erstellen Sie eine Sperraufforderung mithilfe der [**IWMDRMLicenseManagement::CreateLicenseRevocationChallenge-Methode.**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) Diese Methode ordnet einen Puffer zu, der sperraufforderungsdaten enthält, die über den *ppbChallengeOutput-Parameter* an Ihre Anwendung übergeben werden.
2.  Senden Sie die Lizenzsperrungsaufforderung an einen Lizenzsperrdienst. Der Server generiert als Antwort ein Lizenzsperrblob (LRB).
3.  Entfernen Sie die Lizenz mithilfe der [**IWMDRMLicenseManagement::P rocessLicenseRevocationResponse-Methode**](iwmdrmlicensemanagement-processlicenserevocationresponse.md) aus dem lokalen Speicher, und übergeben Sie dabei den vom Lizenzserver zurückgegebenen LRB.
4.  Zuordnen des von **CreateLicenseRevocationChallenge zugeordneten** Puffers mithilfe der **CoTaskMemFree-Funktion.**

Weitere Informationen zur Funktionsweise der Lizenzsperrung oder zum Schreiben eines Sperrdiensts finden Sie unter [Implementing License Revocation](/documentation/?url=%2flibrary%2fwmrm10%2fhtm%2fhowlicenserevokationworks.asp).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Aktivieren der DRM-Unterstützung**](enabling-drm-support.md)
</dt> <dt>

[**Lokale Lizenz Store**](local-license-store.md)
</dt> <dt>

[**Programmierhandbuch**](drm-programming-guide.md)
</dt> </dl>

 

 