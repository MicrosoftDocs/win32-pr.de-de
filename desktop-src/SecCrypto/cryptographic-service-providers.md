---
description: 'Wichtig: Diese API ist veraltet.'
ms.assetid: 4e6eb2df-a917-4533-b9f1-8da39598d0b8
title: Kryptografiedienstanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec7ef58122e47594b195700241b936b8985cd88137c52841976495b195d7e4c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876190"
---
# <a name="cryptographic-service-providers"></a>Kryptografiedienstanbieter

> [!IMPORTANT]
> Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung [Cryptography Next Generation-APIs beginnen.](/windows/desktop/SecCNG/cng-portal) Microsoft kann diese API in zukünftigen Versionen entfernen.

 

Ein [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (Cryptographic Service Provider, CSP) enthält Implementierungen kryptografischer Standards und Algorithmen. Ein CSP besteht mindestens aus einer Dll [*(Dynamic Link Library),*](../secgloss/d-gly.md) die die Funktionen in [*CryptoSPI*](../secgloss/c-gly.md) (einer [*Systemprogrammschnittstelle) implementiert.*](../secgloss/s-gly.md) Die meisten CSPs enthalten die Implementierung aller ihrer eigenen Funktionen. Einige CSPs implementieren ihre Funktionen jedoch hauptsächlich in einem Windows-basierten Dienstprogramm, das vom Windows Service Control Manager verwaltet wird. Andere implementieren Funktionen in Hardware, z. B. eine [*Smartcard oder*](../secgloss/s-gly.md) einen sicheren Coprozessor. Wenn ein CSP keine eigenen Funktionen implementiert, fungiert die DLL als Pass-Through-Schicht, die die Kommunikation zwischen dem Betriebssystem und der tatsächlichen CSP-Implementierung vereinfacht.

In diesem Abschnitt werden folgende Themen behandelt.



| Thema                                                                                      | Inhalte                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Kryptografieanbietertypen](cryptographic-provider-types.md)                           | Kryptografieanbietertypen sind Familien von Kryptografiedienstanbietern, die Datenformate und kryptografische Protokolle gemeinsam nutzen. Zu den Datenformaten gehören Algorithmen [*zum Aufpadding*](../secgloss/p-gly.md) von [*Schemas, Schlüssellängen*](../secgloss/k-gly.md)und Standardmodi. |
| [Microsoft Cryptographic Service Providers](microsoft-cryptographic-service-providers.md) | Ausführliche Informationen zu CSPs, die derzeit von Microsoft verfügbar sind.                                                                                                                                                                                                                                                                                       |



 

 

 
