---
description: Der Basis Anbieter erstellt symmetrische 40-Bit-Schlüssel, die mit elf Bytes mit einem Salt-Wert von 0 Bytes erstellt wurden, bei Angabe von "Crypt Salt Salt" \_ \_ oder "kein Salt-Wert".
ms.assetid: f1af0af7-c64e-435a-aef0-7c4ed7bd1199
title: Salt-Wert-Funktionalität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd8e3049c431cf909c1008acac26925cd1fa9e6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344348"
---
# <a name="salt-value-functionality"></a>Salt-Wert-Funktionalität

Der Basis Anbieter erstellt [*symmetrische*](../secgloss/s-gly.md) 40-Bit-Schlüssel, die mit elf Bytes mit einem [*Salt*](../secgloss/s-gly.md)-Wert von 0 Bytes erstellt wurden, bei Angabe von "Crypt Salt Salt" \_ oder " \_ kein Salt-Wert". Ein symmetrischer 40-Bit-Schlüssel mit einem Salt-Wert von 0 (null) ist jedoch nicht mit 40 einem symmetrischen 32-Bit-Schlüssel ohne Salt identisch. Für die Interoperabilität müssen Schlüssel ohne Salt erstellt werden. Dieses Problem ergibt sich aus einer Standard Bedingung, die nur mit Schlüsseln von exakt 40 Bits auftritt. Allen anderen [*Schlüssellängen*](../secgloss/k-gly.md) ist standardmäßig kein Salt zugeordnet.

Sowohl der Basis Anbieter als auch der erweiterte Anbieter können das Crypt \_ No \_ Salt-Flag verwenden, um anzugeben, dass kein Salt-Wert für einen symmetrischen 40-Bit-Schlüssel zugeordnet ist. Die Funktionen, die dieses Flag akzeptieren, sind [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey), [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey)und [**cryptimportkey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey). Standardmäßig sorgen diese Funktionen für die Abwärtskompatibilität des 40-Bit-symmetrischen Schlüssels, indem Sie die Verwendung des elf-Byte-langen Salt-Werts mit der Länge 0 (null) fortsetzen.

 

 
