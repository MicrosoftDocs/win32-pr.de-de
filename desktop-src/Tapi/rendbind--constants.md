---
description: 'Die "rendbind"-Konstanten sind Flags, die von der itdirectory:: Bind-Methode verwendet werden, um Typen der angegebenen Authentifizierung anzugeben.'
ms.assetid: 27bcf36a-1826-4603-9821-22fcc5c1e186
title: RENDBIND_ Konstanten (rend. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: badd2a48b2ae0632e317522533c664d4f74a6c77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371665"
---
# <a name="rendbind_-constants"></a><span data-ttu-id="b81e7-103">Rendbind- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="b81e7-103">RENDBIND\_ Constants</span></span>

<span data-ttu-id="b81e7-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b81e7-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b81e7-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="b81e7-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b81e7-106">Die "rendbind"-Konstanten sind Flags, die von der [**itdirectory:: Bind**](/windows/desktop/api/Rend/nf-rend-itdirectory-bind) -Methode verwendet werden, um Typen der angegebenen Authentifizierung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b81e7-106">The RENDBIND constants are flags used by the [**ITDirectory::Bind**](/windows/desktop/api/Rend/nf-rend-itdirectory-bind) method to indicate types of authentication supplied.</span></span>

<dl> <dt>

<span data-ttu-id="b81e7-107"><span id="RENDBIND_AUTHENTICATE"></span><span id="rendbind_authenticate"></span>**"rendbind"- \_ Authentifizierung**</span><span class="sxs-lookup"><span data-stu-id="b81e7-107"><span id="RENDBIND_AUTHENTICATE"></span><span id="rendbind_authenticate"></span>**RENDBIND\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="b81e7-108">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b81e7-108">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="b81e7-109">Authentifizieren Sie den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="b81e7-109">Authenticate user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b81e7-110"><span id="RENDBIND_DEFAULTDOMAINNAME"></span><span id="rendbind_defaultdomainname"></span>**rendbind \_ DefaultDomainName**</span><span class="sxs-lookup"><span data-stu-id="b81e7-110"><span id="RENDBIND_DEFAULTDOMAINNAME"></span><span id="rendbind_defaultdomainname"></span>**RENDBIND\_DEFAULTDOMAINNAME**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="b81e7-111">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b81e7-111">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="b81e7-112">Verwenden Sie den Standard Domänen Namen.</span><span class="sxs-lookup"><span data-stu-id="b81e7-112">Use default domain name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b81e7-113"><span id="RENDBIND_DEFAULTUSERNAME"></span><span id="rendbind_defaultusername"></span>**rendbind \_ DefaultUserName**</span><span class="sxs-lookup"><span data-stu-id="b81e7-113"><span id="RENDBIND_DEFAULTUSERNAME"></span><span id="rendbind_defaultusername"></span>**RENDBIND\_DEFAULTUSERNAME**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="b81e7-114">0x00000004</span><span class="sxs-lookup"><span data-stu-id="b81e7-114">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="b81e7-115">Standardbenutzer Namen verwenden.</span><span class="sxs-lookup"><span data-stu-id="b81e7-115">Use default user name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b81e7-116"><span id="RENDBIND_DEFAULTPASSWORD"></span><span id="rendbind_defaultpassword"></span>**rendbind \_ DefaultPassword**</span><span class="sxs-lookup"><span data-stu-id="b81e7-116"><span id="RENDBIND_DEFAULTPASSWORD"></span><span id="rendbind_defaultpassword"></span>**RENDBIND\_DEFAULTPASSWORD**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="b81e7-117">0x00000008</span><span class="sxs-lookup"><span data-stu-id="b81e7-117">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="b81e7-118">Standard Kennwort verwenden.</span><span class="sxs-lookup"><span data-stu-id="b81e7-118">Use default password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b81e7-119"><span id="RENDBIND_DEFAULTCREDENTIALS"></span><span id="rendbind_defaultcredentials"></span>**rendbind \_ default-Anmelde Informationen**</span><span class="sxs-lookup"><span data-stu-id="b81e7-119"><span id="RENDBIND_DEFAULTCREDENTIALS"></span><span id="rendbind_defaultcredentials"></span>**RENDBIND\_DEFAULTCREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="b81e7-120">0x0000000e</span><span class="sxs-lookup"><span data-stu-id="b81e7-120">0x0000000e</span></span>
</dt> <dt>



<span data-ttu-id="b81e7-121">Die vorherigen drei ORed sind aus Gründen der leichteren Arbeit.</span><span class="sxs-lookup"><span data-stu-id="b81e7-121">The previous three ORed together for convenience.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b81e7-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b81e7-122">Requirements</span></span>



| <span data-ttu-id="b81e7-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b81e7-123">Requirement</span></span> | <span data-ttu-id="b81e7-124">Wert</span><span class="sxs-lookup"><span data-stu-id="b81e7-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b81e7-125">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="b81e7-125">TAPI version</span></span><br/> | <span data-ttu-id="b81e7-126">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="b81e7-126">Requires TAPI 3.0 or later</span></span><br/>                                             |
| <span data-ttu-id="b81e7-127">Header</span><span class="sxs-lookup"><span data-stu-id="b81e7-127">Header</span></span><br/>       | <dl> <span data-ttu-id="b81e7-128"><dt>Rend. h</dt></span><span class="sxs-lookup"><span data-stu-id="b81e7-128"><dt>Rend.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b81e7-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b81e7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b81e7-130">**Itdirectory**</span><span class="sxs-lookup"><span data-stu-id="b81e7-130">**ITDirectory**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectory)
</dt> <dt>

[<span data-ttu-id="b81e7-131">**Itdirectory:: Bind**</span><span class="sxs-lookup"><span data-stu-id="b81e7-131">**ITDirectory::Bind**</span></span>](/windows/desktop/api/Rend/nf-rend-itdirectory-bind)
</dt> </dl>

 

 




