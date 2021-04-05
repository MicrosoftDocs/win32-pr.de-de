---
title: DRM-Versionen
description: DRM-Versionen
ms.assetid: ac802547-a3cc-4b30-a8e6-62b679326486
keywords:
- Windows Media-Format-SDK, DRM-Versionen
- Digital Rights Management (DRM), Versionen
- DRM (Digital Rights Management), Versionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be792554e553ccc35dbec71d40ff304af76fafd0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947573"
---
# <a name="drm-versions"></a>DRM-Versionen

Es gibt mehrere Versionen von Windows Media Digital Rights Management (DRM). DRM-Version 1 wird häufig von den anderen Versionen in dieser Dokumentation getrennt, da Sie mithilfe von Verfahren implementiert wird, die sich von den neueren Versionen unterscheiden. Die zweite Generation von Windows Media DRM heißt DRM-Version 7, da Sie als Teil des Windows Media-Formats 7 SDK eingeführt wurde. Sie wird manchmal als DRM-Version 2 bezeichnet. Bei den neueren Versionen von Windows Media DRM, DRM Version 9 und den neuen Windows Media DRM 10 handelt es sich um Erweiterungen der DRM-Version 7, und die gleichen Prozeduren werden für die Implementierung verwendet. Alle Versionen von Windows Media DRM verwenden dieselben Verschlüsselungs Routinen. die Unterschiede zwischen den Versionen müssen mit Lizenz Features durchzuführen sein.

Wenn Sie geschützte Dateien mithilfe der Objekte des Windows Media Format SDK erstellen, sollten Sie sowohl Version 1 als auch die aktuellste Version unterstützen. Dateien, die von DRM-Version 1 geschützt werden, unterscheiden sich von Dateien, die durch höhere Versionen geschützt sind, nur im Inhalt des Headers Neuere Dateien, die die zusätzlichen Header Informationen enthalten, können weiterhin auf Clients verwendet werden, die nur Inhalt der Version 1 darstellen. Obwohl spätere Versionen von DRM ein höheres Maß an Sicherheit und zusätzliche Features bieten, gibt es immer noch viele Spieler, die nur Version 1 verwenden.

Weitere Informationen zu DRM-Versionen finden Sie in der Dokumentation zum Windows Media Rights Manager SDK.

> [!Note]  
> DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Features digitaler Rights Management**](digital-rights-management-features.md)
</dt> <dt>

[**Aktivieren DRM-Unterstützung**](enabling-drm-support.md)
</dt> </dl>

 

 




