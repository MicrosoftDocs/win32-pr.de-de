---
description: Stellt ein Handle für eine OCSP-Antwort dar, die einer Serverzertifikat Kette zugeordnet ist.
ms.assetid: baf173f1-99dc-49f9-9a17-fee79b393db7
title: HCERT_SERVER_OCSP_RESPONSE (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceab319b5d8370dd15ef3dcd288124e4f2adf9ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867415"
---
# <a name="hcert_server_ocsp_response"></a><span data-ttu-id="933d0-103">hcert- \_ Server- \_ OCSP- \_ Antwort</span><span class="sxs-lookup"><span data-stu-id="933d0-103">HCERT\_SERVER\_OCSP\_RESPONSE</span></span>

<span data-ttu-id="933d0-104">Der Datentyp der **\_ \_ OCSP- \_ Antwort des hcert-Servers** stellt ein Handle für eine OCSP-Antwort dar, die einer Server Zertifikat Kette zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="933d0-104">The **HCERT\_SERVER\_OCSP\_RESPONSE** data type represents a handle to an OCSP response associated with a server certificate chain.</span></span>

<span data-ttu-id="933d0-105">Dieser Typ wird von den folgenden APIs verwendet.</span><span class="sxs-lookup"><span data-stu-id="933d0-105">This type is used by the following APIs.</span></span>

-   [<span data-ttu-id="933d0-106">**Certoptserverocspresponse**</span><span class="sxs-lookup"><span data-stu-id="933d0-106">**CertOpenServerOcspResponse**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenserverocspresponse)
-   [<span data-ttu-id="933d0-107">**Certadresssserverocspresponse**</span><span class="sxs-lookup"><span data-stu-id="933d0-107">**CertAddRefServerOcspResponse**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddrefserverocspresponse)
-   [<span data-ttu-id="933d0-108">**Certcloseserverocspresponse**</span><span class="sxs-lookup"><span data-stu-id="933d0-108">**CertCloseServerOcspResponse**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certcloseserverocspresponse)
-   [<span data-ttu-id="933d0-109">**Certgetserverocspresponsecontext**</span><span class="sxs-lookup"><span data-stu-id="933d0-109">**CertGetServerOcspResponseContext**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetserverocspresponsecontext)


```C++
typedef VOID* HCERT_SERVER_OCSP_RESPONSE;
```



## <a name="requirements"></a><span data-ttu-id="933d0-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="933d0-110">Requirements</span></span>



| <span data-ttu-id="933d0-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="933d0-111">Requirement</span></span> | <span data-ttu-id="933d0-112">Wert</span><span class="sxs-lookup"><span data-stu-id="933d0-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="933d0-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="933d0-113">Minimum supported client</span></span><br/> | <span data-ttu-id="933d0-114">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="933d0-114">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="933d0-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="933d0-115">Minimum supported server</span></span><br/> | <span data-ttu-id="933d0-116">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="933d0-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="933d0-117">Header</span><span class="sxs-lookup"><span data-stu-id="933d0-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="933d0-118"><dt>WinCrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="933d0-118"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 




