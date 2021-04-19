---
description: Erläutert, wie eine Nachricht mithilfe von cryptmsgcountersign gegen signiert werden kann.
ms.assetid: e1969b43-f50e-4c7d-a7e5-b22db4e05be2
title: Gegen Signieren einer Nachricht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02091d25e7ee22f986a26b8f07abff68ebb8c11c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353574"
---
# <a name="countersigning-a-message"></a><span data-ttu-id="2c44f-103">Gegen Signieren einer Nachricht</span><span class="sxs-lookup"><span data-stu-id="2c44f-103">Countersigning a Message</span></span>

<span data-ttu-id="2c44f-104">**So setzen Sie eine signierte Nachricht mithilfe von cryptmsgcountersign gegen Signieren**</span><span class="sxs-lookup"><span data-stu-id="2c44f-104">**To countersign a signed message by using CryptMsgCountersign**</span></span>

1.  <span data-ttu-id="2c44f-105">Aufrufen von [**cryptmsgopentodecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) , um ein Handle für die signierte Nachricht zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2c44f-105">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) to get a handle to the signed message.</span></span>
2.  <span data-ttu-id="2c44f-106">Initialisieren Sie eine [**CMSG-Signatur Geber- \_ \_ \_ Informations**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) Struktur für den gegen Signatur Geber.</span><span class="sxs-lookup"><span data-stu-id="2c44f-106">Initialize a [**CMSG\_SIGNER\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) structure for the countersigner.</span></span>
3.  <span data-ttu-id="2c44f-107">Fügen Sie die Struktur der [**CMSG-Signatur Geber- \_ \_ \_ Info**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) einem Array von gegen Signatur Bezeichnern hinzu (derzeit wird nur ein gegen Signatur Geber unterstützt).</span><span class="sxs-lookup"><span data-stu-id="2c44f-107">Add the [**CMSG\_SIGNER\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) structure to an array of countersigners (only one countersigner is currently supported).</span></span>
4.  <span data-ttu-id="2c44f-108">Aufrufen von [**cryptmsgcountersign**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersign) zum Hinzufügen der gegen Signatur oder der gegen Signaturen.</span><span class="sxs-lookup"><span data-stu-id="2c44f-108">Call [**CryptMsgCountersign**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersign) to add the countersignature or countersignatures.</span></span>

<span data-ttu-id="2c44f-109">Wenn alle Funktionsaufrufe erfolgreich sind, verfügt die ursprüngliche Nachricht nun über eine [*gegen Signatur*](../secgloss/c-gly.md) , die als nicht authentifiziertes Attribut enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="2c44f-109">If all of the function calls succeed, the original message now has a [*countersignature*](../secgloss/c-gly.md) included as an unauthenticated attribute.</span></span>

<span data-ttu-id="2c44f-110">**So setzen Sie eine signierte Nachricht mithilfe von cryptmsgcountersignencoded gegen Signieren**</span><span class="sxs-lookup"><span data-stu-id="2c44f-110">**To countersign a signed message by using CryptMsgCountersignEncoded**</span></span>

1.  <span data-ttu-id="2c44f-111">Aufrufen von [**cryptmsgopentodecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) , um ein Handle für die signierte Nachricht zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2c44f-111">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) to get a handle to the signed message.</span></span>
2.  <span data-ttu-id="2c44f-112">Rufen Sie [**cryptmsggetparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) auf, um die codierten Signatur Geber Informationen der signierten Nachricht abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2c44f-112">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) to retrieve the encoded signer information of the signed message.</span></span>
3.  <span data-ttu-id="2c44f-113">Initialisieren Sie eine [**CMSG-Signatur Geber- \_ \_ \_ Informations**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) Struktur für den gegen Signatur Geber.</span><span class="sxs-lookup"><span data-stu-id="2c44f-113">Initialize a [**CMSG\_SIGNER\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) structure for the countersigner.</span></span>
4.  <span data-ttu-id="2c44f-114">Fügen Sie die Struktur der [**CMSG-Signatur Geber- \_ \_ \_ Info**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) einem Array von gegen Signatur Bezeichnern hinzu (derzeit wird nur ein gegen Signatur Geber unterstützt).</span><span class="sxs-lookup"><span data-stu-id="2c44f-114">Add the [**CMSG\_SIGNER\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) structure to an array of countersigners (only one countersigner is currently supported).</span></span>
5.  <span data-ttu-id="2c44f-115">Rufen Sie [**cryptmsgcountersignencoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersignencoded) auf, um das codierte gegen Signatur-Attribut zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2c44f-115">Call [**CryptMsgCountersignEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersignencoded) to create the encoded countersignature attribute.</span></span>
6.  <span data-ttu-id="2c44f-116">Bitten Sie [**cryptmsgcontrol**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol) , das gegen Signatur-Attribut der ursprünglichen Nachricht als nicht authentifiziertes Attribut hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="2c44f-116">Call [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol) to add the countersignature attribute to the original message as an unauthenticated attribute.</span></span>

<span data-ttu-id="2c44f-117">Wenn alle Funktionsaufrufe erfolgreich sind, wird der ursprünglichen Nachricht ein [*gegen Signatur*](../secgloss/c-gly.md) -Attribut hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2c44f-117">If all of the function calls succeed, a [*countersignature*](../secgloss/c-gly.md) attribute is added to the original message.</span></span>

 

 
