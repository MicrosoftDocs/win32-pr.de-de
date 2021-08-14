---
description: Die Informationen in diesem Thema gelten für Windows Server 2003 und Windows XP.
ms.assetid: 45536902-af80-4dca-b3ce-207086844763
title: Secure Sockets Layer Protokoll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf8e6b7232db8bef98d5170887d6be75c9770927954a40b606450bf214efdf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918383"
---
# <a name="secure-sockets-layer-protocol"></a>Secure Sockets Layer Protokoll

Die Informationen in diesem Thema gelten für Windows Server 2003 und Windows XP. Verschlüsselungssammlungen für Windows Server 2008 und Windows Vista finden Sie unter [Cipher Suites in Schannel](cipher-suites-in-schannel.md).

Schannel unterstützt die Versionen 2.0 und 3.0 des Secure Sockets Layer [*-Protokolls (SSL).*](../secgloss/s-gly.md)

> [!Note]  
> Ab Windows 10 Version 1607 und Windows Server 2016 wurde SSL 2.0 entfernt und wird nicht mehr unterstützt.

 

## <a name="ssl-30"></a>SSL 3.0

SSL 3.0 ist der Vorgänger des Transport Layer Security [Protocol](transport-layer-security-protocol.md).

Schannel unterstützt die Verschlüsselungssammlungen, die unter [TLS-Verschlüsselungssammlungen für](tls-cipher-suites.md) SSL 3.0 aufgeführt sind. SSL 3.0 unterstützt alle Verschlüsselungssammlungen, die unter TLS-Verschlüsselungssammlungen aufgeführt sind, sowie SSL \_ FORTEZZA \_ KEA \_ WITH \_ FORTEZZA \_ CBC \_ SHA.

## <a name="ssl-20"></a>SSL 2.0

SSL 2.0 wurde durch TLS ersetzt und sollte nicht für neue Entwicklungen verwendet werden.

Schannel unterstützt die folgenden Verschlüsselungssammlungen für SSL 2.0. Die Sammlungen werden in der Reihenfolge von der sichersten zur am wenigsten sicheren listet.

-   SSL \_ RC4 \_ 128 \_ MIT \_ MD5
-   SSL \_ DES \_ 192 \_ EDE3 \_ CBC MIT \_ \_ MD5
-   SSL \_ RC2 \_ CBC \_ 128 \_ CBC \_ MIT \_ MD5
-   SSL \_ DES \_ 64 \_ CBC MIT \_ \_ MD5
-   SSL \_ RC4 \_ 128 \_ EXPORT40 \_ MIT \_ MD5

 

 
