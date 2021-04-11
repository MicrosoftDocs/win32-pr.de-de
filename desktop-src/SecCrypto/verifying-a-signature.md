---
description: Erstellen Sie ein Hash Objekt mithilfe von "cryptkreatehash", um eine Signatur zu überprüfen. Dieses Hash Objekt sammelt die zu überprüfenden Daten. Die Daten werden dann mit der CryptHashData-Funktion dem Hash Objekt hinzugefügt.
ms.assetid: 3779f83b-0d87-4f47-949b-9eb39690adfb
title: Überprüfen einer Signatur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9a416dc2c3f7523af781e68fe78b066accbe6d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130225"
---
# <a name="verifying-a-signature"></a><span data-ttu-id="5e287-105">Überprüfen einer Signatur</span><span class="sxs-lookup"><span data-stu-id="5e287-105">Verifying a Signature</span></span>

<span data-ttu-id="5e287-106">Erstellen Sie ein [*Hash Objekt*](../secgloss/h-gly.md) mithilfe von " [**cryptkreatehash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash)", um eine Signatur zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5e287-106">To verify a signature, create a [*hash object*](../secgloss/h-gly.md) using [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash).</span></span> <span data-ttu-id="5e287-107">Dieses Hash Objekt sammelt die zu überprüfenden Daten.</span><span class="sxs-lookup"><span data-stu-id="5e287-107">This hash object accumulates the data to be verified.</span></span> <span data-ttu-id="5e287-108">Die Daten werden dann mit der [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) -Funktion dem Hash Objekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5e287-108">The data is then added to the hash object with the [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) function.</span></span>

<span data-ttu-id="5e287-109">Nachdem der letzte Datenblock dem Hash hinzugefügt wurde, überprüfen Sie die Signatur mit [**cryptverifysignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea) .</span><span class="sxs-lookup"><span data-stu-id="5e287-109">After the last block of data is added to the hash, use [**CryptVerifySignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea) to verify the signature.</span></span> <span data-ttu-id="5e287-110">Die Adresse der Signatur Daten, ein Handle für das Hash Objekt und das Handle der öffentlichen Schlüssel werden an **cryptverifysignature** übermittelt.</span><span class="sxs-lookup"><span data-stu-id="5e287-110">The address of the signature data, a handle to the hash object, and the handle of the public keys are passed to **CryptVerifySignature**.</span></span>

<span data-ttu-id="5e287-111">Nachdem die Signatur überprüft wurde (oder die Überprüfung nicht bestanden hat), zerstören Sie das Hash Objekt mithilfe der [**cryptdestroyhash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="5e287-111">After the signature has been verified (or has failed the verification), destroy the hash object using the [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) function.</span></span>

 

 
