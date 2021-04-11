---
description: Die Informationen in diesem Thema gelten für Windows Server 2003 und Windows XP.
ms.assetid: 45536902-af80-4dca-b3ce-207086844763
title: Secure Sockets Layer-Protokoll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3ed2555c854a6cc25948abe0dc83043ee632170
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959634"
---
# <a name="secure-sockets-layer-protocol"></a>Secure Sockets Layer-Protokoll

Die Informationen in diesem Thema gelten für Windows Server 2003 und Windows XP. Informationen zu Verschlüsselungs Sammlungen für Windows Server 2008 und Windows Vista finden Sie unter Verschlüsselungs Sammlungen [in Schannel](cipher-suites-in-schannel.md).

SChannel unterstützt die Versionen 2,0 und 3,0 des [*Secure Sockets Layer (SSL)-Protokolls*](../secgloss/s-gly.md).

> [!Note]  
> Ab Windows 10, Version 1607 und Windows Server 2016, wurde SSL 2,0 entfernt und wird nicht mehr unterstützt.

 

## <a name="ssl-30"></a>SSL 3.0

SSL 3,0 ist der Vorgänger des [Transport Layer Security Protokolls](transport-layer-security-protocol.md).

SChannel unterstützt die Verschlüsselungs Sammlungen, die unter [TLS Chiffre Suites](tls-cipher-suites.md) for SSL 3,0 aufgelistet sind. SSL 3,0 unterstützt alle Verschlüsselungs Sammlungen, die unter TLS-Verschlüsselungs Sammlungen aufgeführt sind, sowie SSL- \_ Fortezza \_ KEA \_ mit \_ Fortezza \_ CBC \_ SHA.

## <a name="ssl-20"></a>SSL 2.0

SSL 2,0 wurde durch TLS abgelöst und sollte nicht für die neue Entwicklung verwendet werden.

SChannel unterstützt die folgenden Verschlüsselungs Sammlungen für SSL 2,0. Die Auflistungen werden in der Reihenfolge von den sichersten bis zum geringsten sicher aufgelistet.

-   SSL \_ RC4 \_ 128 \_ mit \_ MD5
-   SSL \_ des \_ 192 \_ EDE3 \_ CBC \_ mit \_ MD5
-   SSL \_ RC2 \_ CBC \_ 128 \_ CBC \_ mit \_ MD5
-   SSL \_ des \_ 64 \_ CBC \_ mit \_ MD5
-   SSL \_ RC4 \_ 128 \_ EXPORT40 \_ mit \_ MD5

 

 
