---
description: Der ursprüngliche Basis Anbieter hat fälschlicherweise gemeldet, dass der SHA-Hash Algorithmus Algorithmen durch Aufrufe von "CryptGetProvParam" mit dem angegebenen Parameter "PP \_ enumalgs" auflistet.
ms.assetid: 75128a4f-273a-4195-b206-30fc8bc589e9
title: SHA-Funktionalität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad8a06ce5c11dfaa00e2ec7ee3427dfda2f8b3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749560"
---
# <a name="sha-functionality"></a><span data-ttu-id="c3fc4-103">SHA-Funktionalität</span><span class="sxs-lookup"><span data-stu-id="c3fc4-103">SHA Functionality</span></span>

<span data-ttu-id="c3fc4-104">Der ursprüngliche Basis Anbieter hat fälschlicherweise gemeldet, dass der [*SHA*](../secgloss/s-gly.md) -Hash Algorithmus Algorithmen durch Aufrufe von " [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) " mit dem angegebenen Parameter "PP \_ enumalgs" auflistet.</span><span class="sxs-lookup"><span data-stu-id="c3fc4-104">The original Base Provider incorrectly reported that the [*SHA*](../secgloss/s-gly.md) hash algorithm enumerating algorithms by calls to [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) with parameter PP\_ENUMALGS specified.</span></span> <span data-ttu-id="c3fc4-105">Dies wurde im Basis Anbieter behoben.</span><span class="sxs-lookup"><span data-stu-id="c3fc4-105">This has been fixed in the Base Provider.</span></span> <span data-ttu-id="c3fc4-106">Der überarbeitete Basis Anbieter und der erweiterte Anbieter melden nun SHA-1 ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="c3fc4-106">Both the revised Base Provider and the Extended Provider and now correctly report SHA-1.</span></span>

<span data-ttu-id="c3fc4-107">Eine definierte calg \_ SHA1-Konstante wurde Wincrypt. h mit dem gleichen Wert wie calg SHA hinzugefügt \_ .</span><span class="sxs-lookup"><span data-stu-id="c3fc4-107">A defined CALG\_SHA1 constant has been added to Wincrypt.h with the same value as CALG\_SHA.</span></span>

 

 
