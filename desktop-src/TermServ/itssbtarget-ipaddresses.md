---
title: Itssbtarget-IPADRESSEN (Eigenschaft)
description: Ruft die externen IP-Adressen des Ziels ab oder legt Sie fest.
ms.assetid: 938a753c-d541-4772-b41b-817324488685
ms.tgt_platform: multiple
keywords:
- Targetexternalipadressen-Eigenschaft Remotedesktopdienste
- Targetexternalipadressen-Eigenschaft Remotedesktopdienste, itssbtarget-Schnittstelle
- Targetexternalipadressen-Eigenschaft Remotedesktopdienste, itssbtarget-Schnittstelle
- IPADRESSEN-Eigenschaft Remotedesktopdienste
- IPADRESSEN-Eigenschaft Remotedesktopdienste, itssbtarget-Schnittstelle
- Itssbtarget-Schnittstelle Remotedesktopdienste, IPADRESSEN-Eigenschaft
- IPADRESSEN-Eigenschaft Remotedesktopdienste, itssbtargetex-Schnittstelle
- Itssbtargetex-Schnittstelle Remotedesktopdienste, IPADRESSEN-Eigenschaft
topic_type:
- apiref
api_name:
- ITsSbTarget.IpAddresses
- ITsSbTarget.get_IpAddresses
- ITsSbTarget.put_IpAddresses
- ITsSbTargetEx.IpAddresses
- ITsSbTargetEx.get_IpAddresses
- ITsSbTargetEx.put_IpAddresses
- TargetExternalIpAddresses
- ITsSbTarget.TargetExternalIpAddresses
- ITsSbTarget get_TargetExternalIpAddresses
- ITsSbTarget put_TargetExternalIpAddresses
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8b3902840b24bc49ae3bda0510c8355afb67810
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389125"
---
# <a name="itssbtargetipaddresses-property"></a><span data-ttu-id="9ff54-111">Itssbtarget:: IPADRESSEN-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9ff54-111">ITsSbTarget::IpAddresses property</span></span>

<span data-ttu-id="9ff54-112">Ruft die externen IP-Adressen des Ziels ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="9ff54-112">Retrieves or specifies the external IP addresses of the target.</span></span>

<span data-ttu-id="9ff54-113">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="9ff54-113">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ff54-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ff54-114">Syntax</span></span>


```C++
HRESULT put_IpAddresses(
  [in, size_is(numAddresses)]   TSSD_ConnectionPoint *sockaddr,
  [in]                          DWORD                numAddresses
);

HRESULT get_IpAddresses(
  [out, size_is(*numAddresses)] TSSD_ConnectionPoint *sockaddr,
  [in, out]                     DWORD                *numAddresses
);
```



## <a name="property-value"></a><span data-ttu-id="9ff54-115">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="9ff54-115">Property value</span></span>

<span data-ttu-id="9ff54-116">Ein Zeiger auf ein Array von [**Tssd- \_ ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) -Strukturen, die die externen IP-Adressen des Ziels empfangen.</span><span class="sxs-lookup"><span data-stu-id="9ff54-116">A pointer to an array of [**TSSD\_ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) structures that receive the external IP addresses of the target.</span></span>

<span data-ttu-id="9ff54-117">Ein Zeiger auf eine **DWORD** -Variable, die die Anzahl externer IP-Adressen im *sockaddr* -Parameter enthält.</span><span class="sxs-lookup"><span data-stu-id="9ff54-117">A pointer to a **DWORD** variable that contains the number of external IP addresses in the *sockaddr* parameter.</span></span> <span data-ttu-id="9ff54-118">Wenn die Anzahl der Adressen unbekannt ist, übergeben Sie *sockaddr* als **null**.</span><span class="sxs-lookup"><span data-stu-id="9ff54-118">If the number of addresses is unknown, pass *sockaddr* as **NULL**.</span></span> <span data-ttu-id="9ff54-119">Die-Methode gibt die Anzahl der [**Tssd- \_ ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) -Strukturen zurück, die erforderlich sind, um im Array zuzuordnen, auf das durch den *sockaddr* -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="9ff54-119">The method will return the number of [**TSSD\_ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) structures necessary to allocate in the array pointed to by the *sockaddr* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ff54-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ff54-120">Remarks</span></span>

<span data-ttu-id="9ff54-121">Diese Eigenschaft wurde früher als **targetexternalipadressen** in Windows Server 2008 R2 bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9ff54-121">This property was formerly known as **TargetExternalIpAddresses** in Windows Server 2008 R2.</span></span>

<span data-ttu-id="9ff54-122">Wenn die Anzahl externer IP-Adressen unbekannt ist, können Sie diese Methode mit *sockaddr* -Wert auf **null** festlegen.</span><span class="sxs-lookup"><span data-stu-id="9ff54-122">If the number of external IP addresses is unknown, you can call this method with *sockaddr* set to **NULL**.</span></span> <span data-ttu-id="9ff54-123">Die-Methode gibt dann im *numadkleidungs* -Parameter die Anzahl der [**Tssd- \_ ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) -Strukturen zurück, die erforderlich sind, um alle externen IP-Adressen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9ff54-123">The method will then return, in the *numAddresses* parameter, the number of [**TSSD\_ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) structures necessary to receive all the external IP addresses.</span></span> <span data-ttu-id="9ff54-124">Weisen Sie das Array für *sockaddr* auf Grundlage dieser Zahl zu, und klicken Sie dann erneut auf die Methode, und legen Sie *sockaddr* auf das neu zugewiesene Array und *numadcookiezeichen* auf die Zahl fest, die vom ersten-Befehl zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9ff54-124">Allocate the array for *sockaddr* based on this number, and then call the method again, setting *sockaddr* to the newly allocated array and *numAddresses* to the number returned by the first call.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ff54-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ff54-125">Requirements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9ff54-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9ff54-126">Minimum supported client</span></span><br/></td>
<td><span data-ttu-id="9ff54-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9ff54-127">None supported</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ff54-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9ff54-128">Minimum supported server</span></span><br/></td>
<td><span data-ttu-id="9ff54-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9ff54-129">Windows Server 2012</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ff54-130">IDL</span><span class="sxs-lookup"><span data-stu-id="9ff54-130">IDL</span></span><br/></td>
<td><dl> <span data-ttu-id="9ff54-131"><dt>Sbtsv. idl</dt> </span><span class="sxs-lookup"><span data-stu-id="9ff54-131"><dt>Sbtsv.idl</dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ff54-132">IID</span><span class="sxs-lookup"><span data-stu-id="9ff54-132">IID</span></span><br/></td>
<td><span data-ttu-id="9ff54-133">IID_ITsSbTarget ist definiert als:</span><span class="sxs-lookup"><span data-stu-id="9ff54-133">IID_ITsSbTarget is defined as:</span></span>
<ul>
<li><span data-ttu-id="9ff54-134">16616ecc-272d-411d-b324-126893033856</span><span class="sxs-lookup"><span data-stu-id="9ff54-134">16616ECC-272D-411D-B324-126893033856</span></span></li>
<li><span data-ttu-id="9ff54-135">e85e10ea-db0b-4752-b456-5sd5840901c0 unter Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9ff54-135">e85e10ea-db0b-4752-b456-5fd5840901c0 on Windows Server 2008 R2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="9ff54-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ff54-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ff54-137">**Itssbtargetex**</span><span class="sxs-lookup"><span data-stu-id="9ff54-137">**ITsSbTargetEx**</span></span>](itssbtargetex.md)
</dt> <dt>

[<span data-ttu-id="9ff54-138">**Itssbtarget**</span><span class="sxs-lookup"><span data-stu-id="9ff54-138">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dt>

[<span data-ttu-id="9ff54-139">**Tssd- \_ ConnectionPoint**</span><span class="sxs-lookup"><span data-stu-id="9ff54-139">**TSSD\_ConnectionPoint**</span></span>](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint)
</dt> </dl>

 

 





