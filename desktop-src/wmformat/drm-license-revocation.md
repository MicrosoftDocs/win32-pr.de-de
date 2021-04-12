---
title: Lizenz Sperrung (Microsoft Windows Media DRM-Client)
description: Lizenz Sperrung (Microsoft Windows Media DRM-Client)
ms.assetid: 615ddddf-4f2f-400d-9c4d-ff3a2851d699
keywords:
- Windows Media-Format-SDK, Lizenzen
- Windows Media-Format-SDK, Lizenz Sperrung
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Digital Rights Management (DRM), Lizenz Sperrung
- DRM (Digital Rights Management), Lizenz Sperrung
- Erweiterte APIs für den DRM-Client, Lizenzen
- Erweiterte Client-APIs, Lizenzen
- Erweiterte APIs für den DRM-Client, Lizenz Sperrung
- Erweiterte Client-APIs, Lizenz Sperrung
- Lizenzen, Sperren
- Lizenz Sperrung, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90388a7392c79f583143e06fb78ecfe45e188612
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104218928"
---
# <a name="license-revocation-microsoft-windows-media-drm-client"></a>Lizenz Sperrung (Microsoft Windows Media DRM-Client)

Der Lizenz Widerruf bezieht sich auf das Entfernen von Lizenzen aus einem lokalen Lizenz Speicher. Ein häufiges Szenario für die Lizenz Sperrung tritt auf, wenn ein Dienstanbieter, z. b. ein Musik Abonnement Dienst, den Dienst auf dem Computer eines Benutzers deaktivieren muss.

Der Lizenz Sperrprozess wird von einem Dienst initiiert, der vom Lizenz Aussteller bereitgestellt wird. Die Anwendung kann diesen Dienst hosten, oder es kann eine Webanwendung sein. In beiden Fällen muss Ihre Anwendung in der Lage sein, eine vom Dienst erstellte Lizenz Herausforderung zu erhalten.

Gehen Sie folgendermaßen vor, um Lizenzen aus dem Lizenz Speicher zu entfernen:

1.  Erstellen Sie nach dem Empfang einer Lizenzanfrage vom Lizenz Aussteller eine Sperranforderung mithilfe der Methode [**iwmdrmlicencmanagement:: featelicenserevocationchallenge**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) . Diese Methode weist einen Puffer zu, der Sperr Aufforderungs Daten enthält, die über den Parameter *ppbdeleggeoutput* an die Anwendung übergeben werden.
2.  Senden Sie die Lizenz Sperr Aufforderung an einen Lizenz Sperr Dienst. Der Server generiert als Antwort ein Lizenz Sperr-BLOB (LRB).
3.  Entfernen Sie die Lizenz aus dem lokalen Speicher mithilfe der [**iwmdrmlicenlmanagement::P rocess licenserevocationresponse**](iwmdrmlicensemanagement-processlicenserevocationresponse.md) -Methode, und übergeben Sie dabei die vom Lizenzserver zurückgegebene LRB.
4.  Hebt die Zuordnung des Puffers auf, **der von "" mit der** Funktion " **CoTaskMemFree** " zugeordnet wurde.

Weitere Informationen zur Funktionsweise der Lizenz Sperrung oder zum Schreiben eines Sperr Dienstanbieter finden Sie unter [Implementieren der Lizenz](/documentation/?url=%2flibrary%2fwmrm10%2fhtm%2fhowlicenserevokationworks.asp)Sperrung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Aktivieren DRM-Unterstützung**](enabling-drm-support.md)
</dt> <dt>

[**Lokaler Lizenz Speicher**](local-license-store.md)
</dt> <dt>

[**Programmierhandbuch**](drm-programming-guide.md)
</dt> </dl>

 

 