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
# <a name="salt-value-functionality"></a><span data-ttu-id="e9c99-103">Salt-Wert-Funktionalität</span><span class="sxs-lookup"><span data-stu-id="e9c99-103">Salt Value Functionality</span></span>

<span data-ttu-id="e9c99-104">Der Basis Anbieter erstellt [*symmetrische*](../secgloss/s-gly.md) 40-Bit-Schlüssel, die mit elf Bytes mit einem [*Salt*](../secgloss/s-gly.md)-Wert von 0 Bytes erstellt wurden, bei Angabe von "Crypt Salt Salt" \_ oder " \_ kein Salt-Wert".</span><span class="sxs-lookup"><span data-stu-id="e9c99-104">The Base Provider creates 40-bit [*symmetric keys*](../secgloss/s-gly.md) created with eleven bytes of zero-value [*salt*](../secgloss/s-gly.md), eleven bytes of nonzero salt if CRYPT\_CREATE\_SALT is specified, or no salt value.</span></span> <span data-ttu-id="e9c99-105">Ein symmetrischer 40-Bit-Schlüssel mit einem Salt-Wert von 0 (null) ist jedoch nicht mit 40 einem symmetrischen 32-Bit-Schlüssel ohne Salt identisch.</span><span class="sxs-lookup"><span data-stu-id="e9c99-105">A 40-bit symmetric key with zero-value salt, however, is not equivalent to a 40-bit symmetric key without salt.</span></span> <span data-ttu-id="e9c99-106">Für die Interoperabilität müssen Schlüssel ohne Salt erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e9c99-106">For interoperability, keys must be created without salt.</span></span> <span data-ttu-id="e9c99-107">Dieses Problem ergibt sich aus einer Standard Bedingung, die nur mit Schlüsseln von exakt 40 Bits auftritt.</span><span class="sxs-lookup"><span data-stu-id="e9c99-107">This problem results from a default condition that occurs only with keys of exactly 40 bits.</span></span> <span data-ttu-id="e9c99-108">Allen anderen [*Schlüssellängen*](../secgloss/k-gly.md) ist standardmäßig kein Salt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="e9c99-108">All other [*key lengths*](../secgloss/k-gly.md) do not have salt allocated by default.</span></span>

<span data-ttu-id="e9c99-109">Sowohl der Basis Anbieter als auch der erweiterte Anbieter können das Crypt \_ No \_ Salt-Flag verwenden, um anzugeben, dass kein Salt-Wert für einen symmetrischen 40-Bit-Schlüssel zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e9c99-109">Both the Base Providers and the Extended Provider can use the CRYPT\_NO\_SALT flag to specify that no salt value is allocated for a 40-bit symmetric key.</span></span> <span data-ttu-id="e9c99-110">Die Funktionen, die dieses Flag akzeptieren, sind [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey), [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey)und [**cryptimportkey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span><span class="sxs-lookup"><span data-stu-id="e9c99-110">The functions that accept this flag are [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey), [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey), and [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span></span> <span data-ttu-id="e9c99-111">Standardmäßig sorgen diese Funktionen für die Abwärtskompatibilität des 40-Bit-symmetrischen Schlüssels, indem Sie die Verwendung des elf-Byte-langen Salt-Werts mit der Länge 0 (null) fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="e9c99-111">By default, these functions provide backward compatibility for the 40-bit symmetric key case by continuing the use of the eleven-byte-long zero-value salt.</span></span>

 

 
