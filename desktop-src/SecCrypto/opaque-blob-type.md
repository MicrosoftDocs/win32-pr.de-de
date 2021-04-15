---
description: Nicht transparente BLOB-(auch als "opaquekeyblob" bezeichnet) werden zum Speichern von Sitzungs Schlüsseln in einem herstellerspezifischen Format verwendet, z. b. Schannel.
ms.assetid: a0756c03-0c27-41ff-9b74-8af462e09675
title: Nicht transparenter BLOB-Typ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e45cf8899d5cc63fb360a6b5e4177733de3880f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393769"
---
# <a name="opaque-blob-type"></a><span data-ttu-id="07396-103">Nicht transparenter BLOB-Typ</span><span class="sxs-lookup"><span data-stu-id="07396-103">Opaque BLOB Type</span></span>

<span data-ttu-id="07396-104">Nicht transparente [*BLOB*](../secgloss/o-gly.md)-(auch als "opaquekeyblob" bezeichnet) werden zum Speichern von [*Sitzungs Schlüsseln*](../secgloss/s-gly.md) in einem herstellerspezifischen Format verwendet, z. b. [*SChannel*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="07396-104">[*Opaque BLOBs*](../secgloss/o-gly.md), also known as OPAQUEKEYBLOBs, are used to store [*session keys*](../secgloss/s-gly.md) in a vendor-specific format, such as [*Schannel*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="07396-105">Sie enthalten das Basis Schlüsselmaterial und alle aktuellen [*Zustands*](../secgloss/s-gly.md) Informationen.</span><span class="sxs-lookup"><span data-stu-id="07396-105">They contain the base key material and all current [*state*](../secgloss/s-gly.md) information.</span></span> <span data-ttu-id="07396-106">Dies schließt Informationen wie den [*Salt-Wert*](../secgloss/s-gly.md), den [*Initialisierungs Vektor*](../secgloss/i-gly.md)und die Schlüssel Tabelle ein.</span><span class="sxs-lookup"><span data-stu-id="07396-106">This includes information such as the [*salt value*](../secgloss/s-gly.md), the [*initialization vector*](../secgloss/i-gly.md), and the key table.</span></span> <span data-ttu-id="07396-107">Das Format von nicht transparenten blobbden ist nicht veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="07396-107">The format of opaque BLOBs is unpublished.</span></span> <span data-ttu-id="07396-108">Jeder CSP-Anbieter bestimmt sein eigenes BLOB-Format.</span><span class="sxs-lookup"><span data-stu-id="07396-108">Each CSP vendor determines its own BLOB format.</span></span>

<span data-ttu-id="07396-109">Da ein Schlüssel in ein nicht transparentes BLOB im CSP-spezifischen Format exportiert wird, kann er nur in den CSP importiert werden, von dem er ursprünglich exportiert wurde.</span><span class="sxs-lookup"><span data-stu-id="07396-109">Because a key is exported into an opaque BLOB in CSP-specific format, it can only be imported into the CSP from which it was originally exported.</span></span>

<span data-ttu-id="07396-110">Wenn zwei Prozesse beteiligt sind, ruft [](../secgloss/p-gly.md) jeder Prozess [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) unabhängig auf.</span><span class="sxs-lookup"><span data-stu-id="07396-110">When two processes are involved, each [*process*](../secgloss/p-gly.md) calls [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) independently.</span></span> <span data-ttu-id="07396-111">Jeder Prozess erhält ein Handle für einen Schlüssel Container.</span><span class="sxs-lookup"><span data-stu-id="07396-111">Each process gets a handle to a key container.</span></span> <span data-ttu-id="07396-112">Beide Prozesse können über Handles für denselben Schlüssel Container verfügen.</span><span class="sxs-lookup"><span data-stu-id="07396-112">It is possible for both processes to have handles to the same key container.</span></span> <span data-ttu-id="07396-113">Ein Prozess erstellt die Schlüssel und exportiert Sie in nicht transparente blobwerte und übergibt dann die blobwerte an den zweiten Prozess.</span><span class="sxs-lookup"><span data-stu-id="07396-113">One process creates the keys and exports them into opaque BLOBs, then passes the BLOBs to the second process.</span></span> <span data-ttu-id="07396-114">Der zweite Prozess importiert die Schlüssel aus dem BLOB in den [*Schlüssel Container*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="07396-114">The second process imports the keys from the BLOB into its [*key container*](../secgloss/k-gly.md).</span></span>

<span data-ttu-id="07396-115">Wenn ein Hardware-CSP den Export von Schlüsseln nicht unterstützt, enthält das BLOB möglicherweise nur den Index eines Schlüssel Registers oder etwas ähnliches.</span><span class="sxs-lookup"><span data-stu-id="07396-115">If a hardware CSP does not support exporting keys, the BLOB might only contain the index of a key register, or something similar.</span></span> <span data-ttu-id="07396-116">In diesem Fall wird der restliche Vorgang ignoriert.</span><span class="sxs-lookup"><span data-stu-id="07396-116">In this case, the rest of the procedure is ignored.</span></span>

``` syntax
<secure process>
cbBlob = sizeof(rgbBlob);
CryptExportKey(
          hKey, 
          0, 
          OPAQUEKEYBLOB, 
          0, 
          rgbBlob, 
          &cbBlob);
hKey = 0;

<BLOB is transferred to other process>

<user process>
CryptImportKey(
            hProv, 
            pbBlob, 
            cbBlob, 
            0, 
            0, 
            &hKey);
```

 

 
