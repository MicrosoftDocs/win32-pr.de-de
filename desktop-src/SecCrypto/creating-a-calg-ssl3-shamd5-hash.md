---
description: Erläutert, wie ein calg \_ SSL3 SHAMD5-Hash erstellt wird \_ .
ms.assetid: dad6fc7f-8abd-4f90-b3e4-8d0169e95087
title: Erstellen eines CALG_SSL3_SHAMD5 Hash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f38b5939dc64467ef813b354f33a90f009619f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358559"
---
# <a name="creating-a-calg_ssl3_shamd5-hash"></a><span data-ttu-id="6a21f-103">Erstellen eines calg- \_ SSL3 \_ SHAMD5 Hash</span><span class="sxs-lookup"><span data-stu-id="6a21f-103">Creating a CALG\_SSL3\_SHAMD5 Hash</span></span>

<span data-ttu-id="6a21f-104">**So erstellen Sie einen calg- \_ SSL3 \_ SHAMD5-Hash**</span><span class="sxs-lookup"><span data-stu-id="6a21f-104">**To create a CALG\_SSL3\_SHAMD5 hash**</span></span>

1.  <span data-ttu-id="6a21f-105">Erstellen Sie mithilfe der standardmäßigen kryptoapi-Methodik sowohl einen MD5-als auch einen [*SHA*](../secgloss/s-gly.md) - [*Hash*](../secgloss/h-gly.md) der Zieldaten.</span><span class="sxs-lookup"><span data-stu-id="6a21f-105">Using standard CryptoAPI methodology, create both a MD5 and a [*SHA*](../secgloss/s-gly.md) [*hash*](../secgloss/h-gly.md) of the target data.</span></span>
2.  <span data-ttu-id="6a21f-106">Verketten Sie die beiden Hashwerte mit dem MD5-Wert ganz links und dem SHA-Wert ganz rechts.</span><span class="sxs-lookup"><span data-stu-id="6a21f-106">Concatenate the two hashes, with the MD5 value leftmost and the SHA value rightmost.</span></span> <span data-ttu-id="6a21f-107">Dies führt zu einem Wert von 36 Byte (16 Bytes + 20 Bytes).</span><span class="sxs-lookup"><span data-stu-id="6a21f-107">This results in a 36-byte value (16 bytes + 20 bytes).</span></span>
3.  <span data-ttu-id="6a21f-108">Rufen Sie ein Handle für ein [*Hash Objekt*](../secgloss/h-gly.md) durch Aufrufen von " [**cryptcreatehash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) with calg SSL3 SHAMD5" ab, \_ \_ das im *algid* -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="6a21f-108">Get a handle to a [*hash object*](../secgloss/h-gly.md) by calling [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) with CALG\_SSL3\_SHAMD5 passed in the *Algid* parameter.</span></span>
4.  <span data-ttu-id="6a21f-109">Legen Sie den Hashwert mit einem Rückruf von [**cryptsethashparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam)fest.</span><span class="sxs-lookup"><span data-stu-id="6a21f-109">Set the hash value with a call to [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam).</span></span> <span data-ttu-id="6a21f-110">Die verketteten Hashwerte werden als **Byte** \* im *pbData* -Parameter übergeben, und der HP \_ hashval-Wert muss im *dwparam* -Parameter übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="6a21f-110">The concatenated hash values are passed as a **BYTE**\* in the *pbData* parameter, and the HP\_HASHVAL value must be passed in the *dwParam* parameter.</span></span> <span data-ttu-id="6a21f-111">Das Aufrufen von [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) mithilfe des Handles, das von [**cryptcreatehash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) in Schritt 3 zurückgegeben wird, schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="6a21f-111">Calling [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) using the handle returned by [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) in step 3 will fail.</span></span>
5.  <span data-ttu-id="6a21f-112">Rufen Sie [**cryptsignhash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) auf, um die Signatur zu generieren.</span><span class="sxs-lookup"><span data-stu-id="6a21f-112">Call [**CryptSignHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) to generate the signature.</span></span>
6.  <span data-ttu-id="6a21f-113">Nennen Sie [**cryptdestroyhash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) , um das Hash Objekt zu zerstören.</span><span class="sxs-lookup"><span data-stu-id="6a21f-113">Call [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) to destroy the hash object.</span></span>

 

 
