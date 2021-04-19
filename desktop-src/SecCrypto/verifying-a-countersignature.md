---
description: Erläutert, wie eine gegen Signatur mithilfe von cryptmsgverifycountersignaturecodiert überprüft wird.
ms.assetid: b7be0d4c-338f-4319-bd82-5cf3d158d6fe
title: Überprüfen einer gegen Signatur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711e15388144fbf674cbb0c42ff41883edbb5af0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348836"
---
# <a name="verifying-a-countersignature"></a><span data-ttu-id="3944f-103">Überprüfen einer gegen Signatur</span><span class="sxs-lookup"><span data-stu-id="3944f-103">Verifying a Countersignature</span></span>

<span data-ttu-id="3944f-104">**So überprüfen Sie eine gegen Signatur**</span><span class="sxs-lookup"><span data-stu-id="3944f-104">**To verify a countersignature**</span></span>

1.  <span data-ttu-id="3944f-105">Aufrufen von [**cryptmsgopentodecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) , um ein Handle für die signierte Nachricht zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3944f-105">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) to get a handle to the signed message.</span></span>
2.  <span data-ttu-id="3944f-106">Verschaffen Sie sich einen Zeiger auf das Zertifikat des gegen Signatur Gebers ( [**CERT \_ Info**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info)).</span><span class="sxs-lookup"><span data-stu-id="3944f-106">Get a pointer to the countersigner's certificate ( [**CERT\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info)).</span></span>
3.  <span data-ttu-id="3944f-107">Rufen Sie [**cryptmsggetparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) auf, um die Signatur Geber Informationen aus der Nachricht abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3944f-107">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) to retrieve the signer information from the message.</span></span>
4.  <span data-ttu-id="3944f-108">Rufen Sie [**cryptmsggetparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) auf, um die [*gegen Signatur*](../secgloss/c-gly.md) aus der Nachricht abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3944f-108">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) to retrieve the [*countersignature*](../secgloss/c-gly.md) from the message.</span></span>
5.  <span data-ttu-id="3944f-109">Sie können [**cryptmsgverifycountersignaturecodierer**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) aufrufen, um die gegen Signatur zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="3944f-109">Call [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) to verify the countersignature.</span></span>

<span data-ttu-id="3944f-110">Wenn der [**cryptmsgverifycountersignaturecodierte**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) Funktions Aufrufvorgang erfolgreich ist, wird die [*gegen Signatur*](../secgloss/c-gly.md) überprüft.</span><span class="sxs-lookup"><span data-stu-id="3944f-110">If the [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) function call succeeds, the [*countersignature*](../secgloss/c-gly.md) is verified.</span></span>

 

 
