---
description: Anbieter implementieren kryptografische Algorithmen, generieren Schlüssel, stellen Schlüsselspeicher zur Verfügung und authentifizieren Benutzer. Anbieter können in Hardware, Software oder beidem implementiert werden.
ms.assetid: 42f76d22-1f0e-4e20-a19e-e5e926ab27f9
title: Grundlegendes zu Kryptografieanbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f167f186ed4da1ac5e97aba8a3c4659f13f29f253de3f489981fc6b32810015f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127220"
---
# <a name="understanding-cryptographic-providers"></a>Grundlegendes zu Kryptografieanbietern

Das Konzept des Kryptografieanbieters, das in der Kryptografie-API [*(CryptoAPI)*](/windows/desktop/SecGloss/c-gly)eingeführt wurde und sich in [*Cryptography API: Next Generation*](/windows/desktop/SecGloss/c-gly) (CNG) etwas weiterentwickelt hat, ist für die sichere Implementierung kryptografischer Funktionen auf Microsoft-Betriebssystemen von zentraler Bedeutung. Diese beiden SDKs wurden zum Erstellen vieler Anwendungen verwendet und werden intern von anderen SDKs aufgerufen. Beispielsweise basieren Active Directory-Zertifikatdienste und die Zertifikatregistrierungs-API auf CryptoAPI und CNG.

Im Allgemeinen implementieren Anbieter kryptografische Algorithmen, generieren Schlüssel, stellen Schlüsselspeicher zur Verfügung und authentifizieren Benutzer. Anbieter können in Hardware, Software oder beidem implementiert werden. Anwendungen, die mit CryptoAPI oder CNG erstellt wurden, können die von Anbietern erstellten Schlüssel nicht ändern, und sie können die Kryptografiealgorithmusimplementierung nicht ändern. Die von Microsoft erstellten Anbieter werden mit den Betriebssystemen verteilt. Andere Anbieter wurden von Drittanbietern erstellt und verteilt.

In den folgenden Themen werden die Unterschiede zwischen Anbietern, die CryptoAPI zugeordnet sind, und CNG-Anbietern behandelt. In der Regel bezieht sich diese Dokumentation auf Anbieter ohne Verweis auf das SDK, dem sie zugeordnet sind. Die Zuordnung wird nur dann bezeichnet, wenn sie relevant ist.

-   [Kryptografiedienstanbieter für CryptoAPI](cryptoapi-cryptographic-service-providers.md)
-   [CNG-Kryptografiealgorithmusanbieter](cng-cryptographic-algorithm-providers.md)
-   [CNG-Storage Anbieter](cng-key-storage-providers.md)
-   [Aufzählen installierter Anbieter](enumerating-installed-providers.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Zertifikatregistrierungs-API](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 
