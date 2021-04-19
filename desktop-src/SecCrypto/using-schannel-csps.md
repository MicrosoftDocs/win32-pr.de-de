---
description: Die SSL-Protokoll-Engine (SChannel) verwendet bei der Durchführung kryptografischer Vorgänge einen Kryptografiedienstanbieter (CSP). Kryptografische Anwendungen können CryptAcquireContext mithilfe der Prov \_ RSA \_ SChannel-und Prov \_ dh \_ SChannel-Anbieter aufrufen.
ms.assetid: ad1eabf1-23bc-4d23-8f8b-13f0bda95120
title: Verwenden von SChannel-CSPs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 289ed57d9f312ee1ef57aecf7534a8d585859126
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348471"
---
# <a name="using-schannel-csps"></a>Verwenden von SChannel-CSPs

Die SSL-Protokoll-Engine ([*SChannel*](../secgloss/s-gly.md)) verwendet bei der Durchführung kryptografischer Vorgänge einen [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (CSP). Kryptografische Anwendungen können [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) mithilfe der Prov \_ RSA \_ SChannel-und Prov \_ dh \_ SChannel-Anbieter aufrufen.

In diesem Abschnitt werden die RSA-und Diffie-Hellman SChannel- [*CSP-Typen*](../secgloss/c-gly.md) definiert. Darüber hinaus werden die Funktionen beschrieben, die ein CSP unterstützen muss, damit er mit Schannel.dll kompatibel ist Bei einer Protokoll-Engine handelt es sich um ein Programm, das einen sicheren Kommunikationskanal zwischen einer Client-und einer Serveranwendung herstellt.

Anwendungen sollten nicht versuchen, Informationen in dieser Dokumentation zu verwenden, um Prov \_ RSA \_ SChannel oder Prov \_ dh \_ SChannel direkt zu verwenden. In dieser Dokumentation wird erläutert, wie CSP-Entwickler und-Anbieter SChannel-CSPs schreiben müssen, die mit Microsoft SChannel-Anbietern kompatibel sind.

Diese Dokumentation soll CSP-Entwicklern bei der Implementierung kompatibler RSA-oder Diffie-Hellman SChannel-CSPs unterstützen. Entwickler werden davon ausgegangen, dass Sie mit dem SSL-Protokoll ( [*Secure Socket Layer*](../secgloss/s-gly.md) ), Version 3,0, Kryptografie mit [*öffentlichem Schlüssel*](../secgloss/p-gly.md) , [*digitalen Zertifikaten*](../secgloss/d-gly.md)und dem CryptoAPI-Funktions Satz vertraut sind. Entwickler, die sich mit diesen Themen vertraut machen, werden empfohlen, die Spezifikation SSL-Protokoll 3,0 und die Dokumentation zu [Cryptography Essentials](cryptography-essentials.md) in diesem SDK zu lesen. Außerdem müssen RSA-und Diffie-Hellman CSP-Entwickler [*Transport Layer Security*](../secgloss/t-gly.md) (TLS)-Protokoll Spezifikationen zusammen mit den entsprechenden RSA [*-und Diffie-Hellman-Algorithmen*](../secgloss/d-gly.md)kennen.

Ein Beispiel, das von einer Microsoft-Protokoll-Engine verwendet wird, finden Sie unter [Erstellen des Haupt Schlüssels](creating-the-master-key.md). Die Aufrufe von Kryptografiefunktionen in diesem Beispiel führen zu Aufrufen von CP-Funktionen, die von einem CSP implementiert werden müssen. Um einen kompatiblen CSP zu schreiben, muss ein Entwickler die Spezifikation für SSL 3,0 verstehen und dieses Wissen mit einem Verständnis des Protokoll-Engine-Codes kombinieren, der der in diesem Beispiel verwendeten ähnelt.

Da die Verwendung des Protokolls für die private Kommunikationstechnologie in Zukunft voraussichtlich minimal ist, müssen Entwickler neuer CSPs dieses Protokoll nicht unterstützen. Die SChannel-Protokoll-Engine unterstützt diese strikt aus Gründen der Abwärtskompatibilität.

 

 
