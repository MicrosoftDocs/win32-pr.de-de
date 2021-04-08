---
title: Die DRM-Kernel Komponente (veraltet)
description: Die DRM-Kernel Komponente (veraltet)
ms.assetid: 016899fb-6d0a-4529-8649-5e8f29c89253
keywords:
- Windows Media-Format-SDK, Microsoft Secure-Audiopfad (SAP)
- Digital Rights Management (DRM), Microsoft Secure-Audiopfad (SAP)
- DRM (Digital Rights Management), Microsoft Secure-Audiopfad (SAP)
- Windows Media-Format-SDK, sicherer Audiopfad (SAP)
- Digital Rights Management (DRM), sicherer Audiopfad (SAP)
- DRM (Digital Rights Management), sicherer Audiopfad (SAP)
- Windows Media-Format-SDK, DRM-Kernel Komponente
- Digital Rights Management (DRM), Kernel Komponente
- DRM (Digital Rights Management), Kernel Komponente
- Microsoft Secure-Audiopfad (SAP), DRM-Kernel Komponente
- Secure-Audiopfad (SAP), DRM-Kernel Komponente
- SAP (sicherer Audiopfad), DRM-Kernel Komponente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacc0074fdf390ca478ed41b59188ad42ec193c1
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104039822"
---
# <a name="the-drm-kernel-component-deprecated"></a>Die DRM-Kernel Komponente (veraltet)

Diese Seite dokumentiert eine Funktion, die in zukünftigen Versionen von Windows mit einer anderen technischen Lösung unterstützt wird.

Im SAP-Modell (Secure audiopath) von Microsoft bietet die DRM-Kernel Komponente zwei grundlegende Features, mit denen die Integrität verschlüsselter Musik geschützt wird.

Zuerst werden die DRM-Client Komponente und die DRM-Kernel Komponente bei der Wiedergabe einer Musikdatei kommuniziert. Diese Kommunikation zwischen Komponenten verhindert, dass jemand das verschlüsselte Signal manipuliert oder falsche Informationen einfügt.

Zweitens entschlüsselt die DRM-Kernel Komponente das Musiksignal erst, wenn alle verbleibenden Komponenten authentifiziert wurden. Das heißt, vor dem Entschlüsseln von Inhalten und der Übergabe an die nächste Systemkomponente überprüft die DRM-Kernel Komponente jede Komponente, die im Pfad zur Audiokarte verbleibt (jede Komponente, die auf den Inhalt zugreifen kann) und überprüft, ob diese Komponenten mit einem Zertifikat von Microsoft signiert sind. Eine nicht signierte Komponente weist möglicherweise auf eine verdächtige Komponente oder einen bösartigen Treiber hin. Wenn also die DRM-Kernel Komponente die verbleibenden Komponenten überprüft, wird das Signal angehalten und kann nicht wiedergegeben werden, wenn eine Komponente den Test nicht bestanden hat. Wenn alle Komponenten die Überprüfung bestehen, entschlüsselt die DRM-Kernel Komponente andernfalls die Musik und übergibt sie an die nächste Komponente.

Microsoft signiert Treiber, die die Tests der Windows®-Hardware Qualität (WHQL) bestanden haben, Digital, um Benutzern zu gewährleisten, dass Sie die Treiber mit der höchsten Qualität verwenden. Diese Vorgehensweise ist Standard und garantiert die Authentizität von Komponenten, da die Signatur nicht gefälscht werden kann, und der Code kann nicht geändert werden, ohne die Signatur zu zerstören. Treiber, die für einen sicheren Audiopfad zertifiziert sind, müssen die Audiodaten, die Sie verarbeiten, vor dem Zugriff durch nicht vertrauenswürdige Komponenten schützen. 

Treiber, die in der Windows Millennium Edition und Windows XP enthalten sind, werden für einen sicheren Audiopfad aktualisiert und signiert. Treiber, die nicht für die Verwendung mit Windows Me oder Windows XP signiert sind, können geschützte Musik nicht wiedergeben. Treiber Hersteller können aktualisierte Versionen ihrer von WHQL signierten Treiber neu ausstellen und im Internet veröffentlichen, damit Consumer Sie herunterladen können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Microsoft Secure-Audiopfad**](microsoft-secure-audio-path--deprecated.md)
</dt> </dl>

 

 




