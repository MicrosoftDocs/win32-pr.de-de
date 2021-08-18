---
description: Die folgenden Begriffe beschreiben Domänen, die auf Remotesystemen vorhanden sind.
ms.assetid: a6ce5356-682a-46ae-a101-15227c3b8d1e
title: Primäre und vertrauenswürdige Domänen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d80f1bd4983a17725de1bac9c55aae0f7d64e85bc2768bfaea2ca1469ed3d3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005064"
---
# <a name="primary-and-trusted-domains"></a>Primäre und vertrauenswürdige Domänen

Die folgenden Begriffe beschreiben Domänen, die auf Remotesystemen vorhanden sind.

-   [Primäre Domäne](#primary-domain)
-   [Vertrauenswürdige Domäne](#primary-and-trusted-domains)

## <a name="primary-domain"></a>Primäre Domäne

Eine primäre Domäne ist die Domäne, die für die Einrichtung weiterer Vertrauensstellungen und die Durchführung der Authentifizierung (oder für die Übergabe einer Authentifizierungsanforderung an eine geeignete vertrauenswürdige Domäne) verantwortlich ist. Die Domänencontroller in der primären Domäne verarbeiten oder übergeben Authentifizierungsanforderungen, die von der Arbeitsstation stammen.

Wenn die Anmeldung erfolgt, überprüft das LSA die integrierte Domäne und die Kontodomäne auf Authentifizierungsinformationen. Wenn sich das Konto, bei dem angemeldet ist, nicht in einer dieser Domänen befindet, wird die Anmeldeanforderung an die primäre Domäne des Systems übergeben.

## <a name="trusted-domain"></a>Vertrauenswürdige Domäne

Eine vertrauenswürdige Domäne ist eine Domäne, der das lokale System vertraut, um Benutzer zu authentifizieren. Anders ausgedrückt: Wenn ein Benutzer oder eine Anwendung von einer vertrauenswürdigen Domäne authentifiziert wird, wird diese Authentifizierung von allen Domänen akzeptiert, die der authentifizierenden Domäne vertrauen.

Jede untergeordnete Domäne verfügt automatisch über eine gegenseitige Vertrauensstellung mit der Hauptdomäne. Standardmäßig ist diese Vertrauensstellung transitiv, d. h., wenn ein System Domäne A vertraut, wird auch allen Domänen vertraut, denen Domäne A vertraut. One-Way-Vertrauensstellungen werden auch für Betriebssysteme vor Windows 2000 unterstützt, die keine transitiven, zweigefängten Vertrauensstellungen unterstützen.

Die lokale Sicherheitsstelle (Local [*Security Authority,*](/windows/desktop/SecGloss/l-gly) LSA) verfügt über den Objekttyp [**TrustedDomain,**](the-trusteddomain-object-type.md)der zum Speichern von Informationen zu Vertrauensstellungen verwendet wird, einschließlich des Namens und der Sicherheits-ID [*(SID)*](/windows/desktop/SecGloss/s-gly) der vertrauenswürdigen Domäne, des Kontos in der Domäne, das für Authentifizierungsanforderungen verwendet werden soll, des Namens und der SID-Übersetzungsanforderungen sowie der Namen von Domänencontrollern in der vertrauenswürdigen Domäne.

Auf Domänencontrollern erstellt das LSA eine Instanz eines [**TrustedDomain-Objekts**](the-trusteddomain-object-type.md) für jede Domäne, die vom lokalen System als vertrauenswürdig eingestuft wird.

Wenn beispielsweise eine Windows XP-Arbeitsstation einem Windows 2000-Domänencontroller vertraut, der wiederum vier anderen Systemen vertraut, hat die Arbeitsstation, die über transitive Vertrauensstellung verbunden ist, fünf [**TrustedDomain-Objekte**](the-trusteddomain-object-type.md) auf ihrem lokalen System.

 

 
