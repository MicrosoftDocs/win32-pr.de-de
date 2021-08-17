---
title: Die DRM-Kernelkomponente (veraltet)
description: Die DRM-Kernelkomponente (veraltet)
ms.assetid: 016899fb-6d0a-4529-8649-5e8f29c89253
keywords:
- Windows Media Format SDK, Microsoft Secure Audio Path (SAP)
- Digital Rights Management (DRM), Microsoft Secure Audio Path (SAP)
- DRM (Digital Rights Management), Microsoft Secure Audio Path (SAP)
- Windows Medienformat-SDK, Sicherer Audiopfad (SAP)
- Digital Rights Management (DRM), Sicherer Audiopfad (SAP)
- DRM (Digital Rights Management), Sicherer Audiopfad (SAP)
- Windows Medienformat-SDK, DRM-Kernelkomponente
- Digital Rights Management (DRM), Kernelkomponente
- DRM (Digital Rights Management), Kernelkomponente
- Microsoft Secure Audio Path (SAP), DRM-Kernelkomponente
- Sicherer Audiopfad (SAP), DRM-Kernelkomponente
- SAP (Sicherer Audiopfad), DRM-Kernelkomponente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8db4389d9156ef13d9e87983a4ae433e6028805268f3cbd55690d4d0d8144b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845757"
---
# <a name="the-drm-kernel-component-deprecated"></a>Die DRM-Kernelkomponente (veraltet)

Auf dieser Seite wird ein Feature dokumentiert, das in zukünftigen Versionen von mit einer anderen technischen Lösung unterstützt Windows.

Im SAP-Modell (Microsoft Secure Audio Path) bietet die DRM-Kernelkomponente zwei grundlegende Features, die die Integrität verschlüsselter Musik schützen.

Zunächst werden die DRM-Clientkomponente und die DRM-Kernelkomponente kommunizieren, wenn eine Musikdatei abgespielt wird. Diese Kommunikation zwischen Komponenten verhindert, dass das verschlüsselte Signal manipuliert oder falsche Informationen eingefügt werden.

Zweitens entschlüsselt die DRM-Kernelkomponente das Musiksignal erst, wenn alle verbleibenden Komponenten authentifiziert sind. Das bedeutet, dass die DRM-Kernelkomponente vor dem Entschlüsseln von Inhalt und der Übergabe an die nächste Systemkomponente jede Komponente überprüft, die im Pfad zur Soundkarte verbleibt (jede Komponente, die auf den Inhalt zugreifen kann) und überprüft, ob diese Komponenten mit einem Zertifikat von Microsoft signiert sind. Eine komponente ohne Vorzeichen kann auf eine verdächtige Komponente oder einen schädlichen Treiber hinweisen. Wenn also die DRM-Kernelkomponente verbleibende Komponenten überprüft und eine Komponente diesen Test nicht besteht, wird das Signal angehalten und kann nicht abgespielt werden. Andernfalls entschlüsselt die DRM-Kernelkomponente die Musik und übergibt sie an die nächste Komponente, wenn alle Komponenten die Validierung bestehen.

Microsoft signiert Treiber, die die Windows® Hardware Quality Lab (WHQL)-Tests bestehen, digital, um sicherzustellen, dass Benutzer die treibern mit der höchsten Qualität verwenden. Diese Vorgehensweise ist Standard und garantiert die Authentizität von Komponenten, da die Signatur nicht gefälscht werden kann und der Code auch nicht geändert werden kann, ohne die Signatur zu zerstören. Treiber, die für Secure Audio Path zertifiziert sind, müssen die Audiodaten, die sie verarbeiten, vor dem Zugriff durch nicht vertrauenswürdige Komponenten schützen. 

Treiber, die in Windows Edition und Windows XP enthalten sind, werden für Secure Audio Path aktualisiert und signiert. Treiber, die nicht für die Verwendung mit Windows Me oder Windows XP signiert sind, können keine geschützte Musik wieder geben. Treiberhersteller können aktualisierte Versionen ihrer Treiber, die von WHQL signiert sind, erneut veröffentlichen und im Internet veröffentlichen, damit sie von Kunden heruntergeladen werden können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Sicherer Audiopfad von Microsoft**](microsoft-secure-audio-path--deprecated.md)
</dt> </dl>

 

 




