---
description: Anbieter implementieren kryptografische Algorithmen, generieren Schlüssel, stellen Schlüsselspeicher bereit und authentifizieren Benutzer. Anbieter können in Hardware, Software oder beidem implementiert werden.
ms.assetid: 42f76d22-1f0e-4e20-a19e-e5e926ab27f9
title: Grundlegendes zu Kryptografieanbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11861b99dc8a19fc4300be2c9707462235f4a792
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960310"
---
# <a name="understanding-cryptographic-providers"></a>Grundlegendes zu Kryptografieanbietern

Das kryptografieanbieterkonzept, das in Cryptography API ([*CryptoAPI*](/windows/desktop/SecGloss/c-gly)) eingeführt wurde und etwas in [*Cryptography API: Next Generation*](/windows/desktop/SecGloss/c-gly) (CNG) entwickelt wurde, ist für die sichere Implementierung von Kryptografiefunktionen auf Microsoft-Betriebssystemen von zentraler Bedeutung. Diese beiden sdche wurden verwendet, um viele Anwendungen zu erstellen und werden intern von anderen sdert aufgerufen. Beispielsweise basieren Active Directory Zertifikat Dienste und die Zertifikatregistrierungs-API auf CryptoAPI und CNG.

Im Allgemeinen implementieren Anbieter Kryptografiealgorithmen, generieren Schlüssel, stellen Schlüsselspeicher bereit und authentifizieren Benutzer. Anbieter können in Hardware, Software oder beidem implementiert werden. Anwendungen, die mithilfe von CryptoAPI oder CNG erstellt wurden, können die von Anbietern erstellten Schlüssel nicht ändern, und Sie können die Implementierung von Kryptografiealgorithmen nicht ändern. Die von Microsoft erstellten verschiedenen Anbieter werden mit den Betriebssystemen verteilt. Andere Anbieter wurden von Drittanbietern erstellt und verteilt.

In den folgenden Themen werden die Unterschiede zwischen den Anbietern der kryptografieapi und den mit CNG zugeordneten Anbietern hervorgehoben. In der Regel bezieht sich diese Dokumentation auf Anbieter ohne Verweis auf das SDK, mit dem Sie verknüpft sind. die Zuordnung erfolgt nur, wenn Sie relevant ist.

-   [Kryptografiedienstanbieter von CryptoAPI](cryptoapi-cryptographic-service-providers.md)
-   [CNG-kryptografiealgorithmusanbieter](cng-cryptographic-algorithm-providers.md)
-   [CNG-Schlüsselspeicher Anbieter](cng-key-storage-providers.md)
-   [Auflisten installierter Anbieter](enumerating-installed-providers.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Zertifikatregistrierungs-API](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 
