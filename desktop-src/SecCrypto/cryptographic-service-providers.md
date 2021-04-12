---
description: Wichtig diese API ist veraltet.
ms.assetid: 4e6eb2df-a917-4533-b9f1-8da39598d0b8
title: Kryptografiedienstanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5431d8ddda1be977e2a33297613633343fc2f9c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393509"
---
# <a name="cryptographic-service-providers"></a>Kryptografiedienstanbieter

> [!IMPORTANT]
> Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von [Cryptography Next Generation-APIs beginnen.](/windows/desktop/SecCNG/cng-portal) Microsoft kann diese API in zukünftigen Versionen entfernen.

 

Ein [*Kryptografiedienstanbieter (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP) enthält Implementierungen kryptografischer Standards und Algorithmen. Ein CSP besteht mindestens aus einer DLL ( [*Dynamic Link Library*](../secgloss/d-gly.md) ), die die Funktionen in [*cryptospi*](../secgloss/c-gly.md) (einer [*Systemprogramm Schnittstelle*](../secgloss/s-gly.md)) implementiert. Die meisten CSPs enthalten die Implementierung aller ihrer eigenen Funktionen. Einige CSPs implementieren ihre Funktionen jedoch hauptsächlich in einem Windows-basierten Dienstprogramm, das vom Windows-Dienststeuerungs-Manager verwaltet wird. Andere implementieren Funktionen in Hardware, z. b. eine [*Smartcard*](../secgloss/s-gly.md) oder einen sicheren Coprozessor. Wenn ein CSP seine eigenen Funktionen nicht implementiert, fungiert die dll als Pass-Through-Schicht und ermöglicht die Kommunikation zwischen dem Betriebssystem und der eigentlichen CSP-Implementierung.

In diesem Abschnitt werden folgende Themen behandelt.



| Thema                                                                                      | Inhalte                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Typen von Kryptografieanbietern](cryptographic-provider-types.md)                           | Kryptografieanbiettypen sind Familien von Kryptografiedienstanbietern, die Datenformate und Kryptografieprotokolle gemeinsam nutzen. Zu den Datenformaten gehören Algorithmen zum [*Auffüllen*](../secgloss/p-gly.md) von Auffüll Schemata, [*Schlüssellängen*](../secgloss/k-gly.md)und Standard Modi. |
| [Kryptografiedienstanbieter von Microsoft](microsoft-cryptographic-service-providers.md) | Ausführliche Informationen zu den derzeit von Microsoft verfügbaren CSPs.                                                                                                                                                                                                                                                                                       |



 

 

 
