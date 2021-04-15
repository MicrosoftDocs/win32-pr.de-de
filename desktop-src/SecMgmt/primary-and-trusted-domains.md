---
description: Die folgenden Begriffe beschreiben Domänen, die auf Remote Systemen vorhanden sind.
ms.assetid: a6ce5356-682a-46ae-a101-15227c3b8d1e
title: Primäre und vertrauenswürdige Domänen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d69a8bf5f5a8363f8de726c6183fd4de820665
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525718"
---
# <a name="primary-and-trusted-domains"></a>Primäre und vertrauenswürdige Domänen

Die folgenden Begriffe beschreiben Domänen, die auf Remote Systemen vorhanden sind.

-   [Primäre Domäne](#primary-domain)
-   [Vertrauenswürdige Domäne](#primary-and-trusted-domains)

## <a name="primary-domain"></a>Primäre Domäne

Eine primäre Domäne ist die Domäne, die für die Einrichtung weiterer Vertrauens Stellungen und die Durchführung der Authentifizierung (oder für die Übergabe einer Authentifizierungsanforderung an eine entsprechende vertrauenswürdige Domäne) zuständig ist. Die Domänen Controller in der primären Domäne verarbeiten oder übergeben Authentifizierungsanforderungen, die von der Arbeitsstation stammen.

Wenn die Anmeldung erfolgt, überprüft die LSA die integrierten Domänen und die Konto Domänen auf Authentifizierungsinformationen. Wenn sich das Konto, bei dem angemeldet wird, nicht in einer dieser Domänen befindet, wird die Anmelde Anforderung an die primäre Domäne des Systems übergeben.

## <a name="trusted-domain"></a>Vertrauenswürdige Domäne

Eine vertrauenswürdige Domäne ist eine Domäne, der das lokale System vertraut, um Benutzer zu authentifizieren. Anders ausgedrückt: Wenn ein Benutzer oder eine Anwendung von einer vertrauenswürdigen Domäne authentifiziert wird, wird diese Authentifizierung von allen Domänen akzeptiert, die der authentifizier enden Domäne vertrauen.

Jede untergeordnete Domäne verfügt automatisch über eine bidirektionale Vertrauensstellung mit der Hauptdomäne. Standardmäßig ist diese Vertrauensstellung transitiv, d. h., wenn ein System Domäne a vertraut, vertraut Sie auch allen Domänen, denen eine Domäne vertraut. Unidirektionale Vertrauens Stellungen werden auch für ältere Betriebssysteme als Windows 2000 unterstützt, die keine transitiven bidirektionalen Vertrauens Stellungen unterstützen.

Die [*Lokale Sicherheits Autorität (Local Security Authority*](/windows/desktop/SecGloss/l-gly) , LSA) verfügt über den Objekttyp " [**Treuhänder Domäne**](the-trusteddomain-object-type.md)", der zum Speichern von Informationen über Vertrauens Stellungen verwendet wird, einschließlich des Namens und der [*Sicherheits*](/windows/desktop/SecGloss/s-gly) -ID (SID) der vertrauenswürdigen Domäne, des Kontos in der Domäne, das für Authentifizierungsanforderungen verwendet werden soll

Auf Domänen Controllern erstellt die LSA eine Instanz eines vertrauenswürdigen [**Domänen**](the-trusteddomain-object-type.md) Objekts für jede Domäne, die vom lokalen System als vertrauenswürdig eingestuft wird.

Wenn z. b. eine Windows XP-Arbeitsstation einem Windows 2000-Domänen Controller vertraut, der wiederum vier andere Systeme als vertrauenswürdig einstuft, erhält die Arbeitsstation, die über transitiv Vertrauensstellung verbunden ist, fünf vertrauenswürdige [**Domänen**](the-trusteddomain-object-type.md) Objekte auf dem lokalen System.

 

 
