---
title: Lschräypack-Struktur
description: Enthält Informationen zu einem bestimmten Remotedesktopdienste Licensing Key Pack.
ms.assetid: c26d27ee-7dd3-49f0-a79c-752d23693a2a
ms.tgt_platform: multiple
keywords:
- Lschräypack-Struktur Remotedesktopdienste
- Lplschräypack-Struktur Zeiger Remotedesktopdienste
topic_type:
- apiref
api_name:
- LSKeyPack
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b1ac1f51e66a0a3c15c33f2535bc02f1fd3528f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957059"
---
# <a name="lskeypack-structure"></a><span data-ttu-id="d2e45-105">Lschräypack-Struktur</span><span class="sxs-lookup"><span data-stu-id="d2e45-105">LSKeyPack structure</span></span>

<span data-ttu-id="d2e45-106">Enthält Informationen zu einem bestimmten Remotedesktopdienste Licensing Key Pack.</span><span class="sxs-lookup"><span data-stu-id="d2e45-106">Contains information about a specific Remote Desktop Services licensing key pack.</span></span>

> [!Note]  
> <span data-ttu-id="d2e45-107">Diese Struktur ist nicht in einer Header Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="d2e45-107">This structure is not defined in any header file.</span></span> <span data-ttu-id="d2e45-108">Um diese Struktur verwenden zu können, müssen Sie Sie selbst definieren, wie in diesem Thema gezeigt.</span><span class="sxs-lookup"><span data-stu-id="d2e45-108">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d2e45-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2e45-109">Syntax</span></span>


```C++
typedef struct _LSKeyPack {
  DWORD dwVersion;
  UCHAR ucKeyPackType;
  TCHAR szCompanyName[256];
  TCHAR szKeyPackId[256];
  TCHAR szProductName[256];
  TCHAR szProductId[256];
  TCHAR szProductDesc[256];
  WORD  wMajorVersion;
  WORD  wMinorVersion;
  DWORD dwPlatformType;
  UCHAR ucLicenseType;
  DWORD dwLanguageId;
  UCHAR ucChannelOfPurchase;
  TCHAR szBeginSerialNumber[256];
  DWORD dwTotalLicenseInKeyPack;
  DWORD dwProductFlags;
  DWORD dwKeyPackId;
  UCHAR ucKeyPackStatus;
  DWORD dwActivateDate;
  DWORD dwExpirationDate;
  DWORD dwNumberOfLicenses;
} LSKeyPack, *LPLSKeyPack;
```



## <a name="members"></a><span data-ttu-id="d2e45-110">Member</span><span class="sxs-lookup"><span data-stu-id="d2e45-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="d2e45-111">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="d2e45-111">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="d2e45-112">Version des Schlüssel Pakets.</span><span class="sxs-lookup"><span data-stu-id="d2e45-112">Version of the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="d2e45-113">**uckeypacktype**</span><span class="sxs-lookup"><span data-stu-id="d2e45-113">**ucKeyPackType**</span></span>
</dt> <dd>

<span data-ttu-id="d2e45-114">Der Typ des Schlüssel Pakets.</span><span class="sxs-lookup"><span data-stu-id="d2e45-114">Type of key pack.</span></span>

</dd> <dt>

<span data-ttu-id="d2e45-115">**szcompanyname**</span><span class="sxs-lookup"><span data-stu-id="d2e45-115">**szCompanyName**</span></span>
</dt> <dd>

<span data-ttu-id="d2e45-116">Name des Unternehmens, von dem das Schlüssel Paket ausgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d2e45-116">Name of the company that issued the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="d2e45-117">**szkeypackid**</span><span class="sxs-lookup"><span data-stu-id="d2e45-117">**szKeyPackId**</span></span>
</dt> <dd>

<span data-ttu-id="d2e45-118">ID des Schlüssel Pakets.</span><span class="sxs-lookup"><span data-stu-id="d2e45-118">ID of the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="d2e45-119">**szproductname**</span><span class="sxs-lookup"><span data-stu-id="d2e45-119">**szProductName**</span></span>
</dt> <dd>

<span data-ttu-id="d2e45-120">Der Name des Produkts, zu dem dieses Schlüssel Paket gehört.</span><span class="sxs-lookup"><span data-stu-id="d2e45-120">Name of the product to which this key pack belongs.</span></span>

</dd> <dt>

<span data-ttu-id="d2e45-121">**szproductid**</span><span class="sxs-lookup"><span data-stu-id="d2e45-121">**szProductId**</span></span>
</dt> <dd>

<span data-ttu-id="d2e45-122">ID des Produkts, zu dem dieses Schlüssel Paket gehört.</span><span class="sxs-lookup"><span data-stu-id="d2e45-122">ID of the product to which this key pack belongs.</span></span>

</dd> <dt>

<span data-ttu-id="d2e45-123">**szproductde**</span><span class="sxs-lookup"><span data-stu-id="d2e45-123">**szProductDesc**</span></span>
</dt> <dd>

<span data-ttu-id="d2e45-124">Die Beschreibung des Produkts, zu dem dieses Schlüssel Paket gehört.</span><span class="sxs-lookup"><span data-stu-id="d2e45-124">Description of the product to which this key pack belongs.</span></span>

</dd> <dt>

<span data-ttu-id="d2e45-125">**wmajorversion**</span><span class="sxs-lookup"><span data-stu-id="d2e45-125">**wMajorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="d2e45-126">Hauptversion des Produkts, zu dem dieses Schlüssel Paket gehört.</span><span class="sxs-lookup"><span data-stu-id="d2e45-126">Major version of the product to which this key pack belongs.</span></span>

</dd> <dt>

<span data-ttu-id="d2e45-127">**wminorversion**</span><span class="sxs-lookup"><span data-stu-id="d2e45-127">**wMinorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="d2e45-128">Neben Version des Produkts, zu dem dieses Schlüssel Paket gehört.</span><span class="sxs-lookup"><span data-stu-id="d2e45-128">Minor version of the product to which this key pack belongs.</span></span>

</dd> <dt>

<span data-ttu-id="d2e45-129">**dwplatformtype**</span><span class="sxs-lookup"><span data-stu-id="d2e45-129">**dwPlatformType**</span></span>
</dt> <dd>

<span data-ttu-id="d2e45-130">Plattformtyp.</span><span class="sxs-lookup"><span data-stu-id="d2e45-130">Platform type.</span></span>

</dd> <dt>

<span data-ttu-id="d2e45-131">**uclicensertyp**</span><span class="sxs-lookup"><span data-stu-id="d2e45-131">**ucLicenseType**</span></span>
</dt> <dd>

<span data-ttu-id="d2e45-132">Der Typ der Lizenzen im Schlüssel Paket.</span><span class="sxs-lookup"><span data-stu-id="d2e45-132">Type of licenses in the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="d2e45-133">**dwLanguageId**</span><span class="sxs-lookup"><span data-stu-id="d2e45-133">**dwLanguageId**</span></span>
</dt> <dd>

<span data-ttu-id="d2e45-134">Sprach-ID.</span><span class="sxs-lookup"><span data-stu-id="d2e45-134">Language ID.</span></span>

</dd> <dt>

<span data-ttu-id="d2e45-135">**ucchannelofpurchase**</span><span class="sxs-lookup"><span data-stu-id="d2e45-135">**ucChannelOfPurchase**</span></span>
</dt> <dd>

<span data-ttu-id="d2e45-136">Kanal des Kaufs.</span><span class="sxs-lookup"><span data-stu-id="d2e45-136">Channel of purchase.</span></span>

</dd> <dt>

<span data-ttu-id="d2e45-137">**szbeginserialnumber**</span><span class="sxs-lookup"><span data-stu-id="d2e45-137">**szBeginSerialNumber**</span></span>
</dt> <dd>

<span data-ttu-id="d2e45-138">Seriennummer für die erste Lizenz.</span><span class="sxs-lookup"><span data-stu-id="d2e45-138">Serial number for the first license.</span></span>

</dd> <dt>

<span data-ttu-id="d2e45-139">**dwtotallicenseingekeypack**</span><span class="sxs-lookup"><span data-stu-id="d2e45-139">**dwTotalLicenseInKeyPack**</span></span>
</dt> <dd>

<span data-ttu-id="d2e45-140">Die Gesamtanzahl der Lizenzen im Schlüssel Paket.</span><span class="sxs-lookup"><span data-stu-id="d2e45-140">Total number of licenses in the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="d2e45-141">**dwproductflags**</span><span class="sxs-lookup"><span data-stu-id="d2e45-141">**dwProductFlags**</span></span>
</dt> <dd>

<span data-ttu-id="d2e45-142">Fahren.</span><span class="sxs-lookup"><span data-stu-id="d2e45-142">Flags.</span></span>

</dd> <dt>

<span data-ttu-id="d2e45-143">**dwkeypackid**</span><span class="sxs-lookup"><span data-stu-id="d2e45-143">**dwKeyPackId**</span></span>
</dt> <dd>

<span data-ttu-id="d2e45-144">ID des Schlüssel Pakets.</span><span class="sxs-lookup"><span data-stu-id="d2e45-144">ID of the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="d2e45-145">**uckeypackstatus**</span><span class="sxs-lookup"><span data-stu-id="d2e45-145">**ucKeyPackStatus**</span></span>
</dt> <dd>

<span data-ttu-id="d2e45-146">Der Status des Schlüssel Pakets.</span><span class="sxs-lookup"><span data-stu-id="d2e45-146">Status of the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="d2e45-147">**dwactivatedate**</span><span class="sxs-lookup"><span data-stu-id="d2e45-147">**dwActivateDate**</span></span>
</dt> <dd>

<span data-ttu-id="d2e45-148">Aktivierungsdatum für das Schlüssel Paket.</span><span class="sxs-lookup"><span data-stu-id="d2e45-148">Activation date for the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="d2e45-149">**dwexpirationdate**</span><span class="sxs-lookup"><span data-stu-id="d2e45-149">**dwExpirationDate**</span></span>
</dt> <dd>

<span data-ttu-id="d2e45-150">Das Ablaufdatum für das Schlüssel Paket.</span><span class="sxs-lookup"><span data-stu-id="d2e45-150">Expiration date for the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="d2e45-151">**dwnumoflicenses**</span><span class="sxs-lookup"><span data-stu-id="d2e45-151">**dwNumberOfLicenses**</span></span>
</dt> <dd>

<span data-ttu-id="d2e45-152">Anzahl der Lizenzen.</span><span class="sxs-lookup"><span data-stu-id="d2e45-152">Number of licenses.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d2e45-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2e45-153">Requirements</span></span>



| <span data-ttu-id="d2e45-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2e45-154">Requirement</span></span> | <span data-ttu-id="d2e45-155">Wert</span><span class="sxs-lookup"><span data-stu-id="d2e45-155">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="d2e45-156">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d2e45-156">Minimum supported client</span></span><br/> | <span data-ttu-id="d2e45-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d2e45-157">Windows Vista</span></span><br/>       |
| <span data-ttu-id="d2e45-158">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d2e45-158">Minimum supported server</span></span><br/> | <span data-ttu-id="d2e45-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2e45-159">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d2e45-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2e45-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2e45-161">**Tlskeypackenumbegin**</span><span class="sxs-lookup"><span data-stu-id="d2e45-161">**TLSKeyPackEnumBegin**</span></span>](tlskeypackenumbegin.md)
</dt> <dt>

[<span data-ttu-id="d2e45-162">**Tlskeypackenumnext**</span><span class="sxs-lookup"><span data-stu-id="d2e45-162">**TLSKeyPackEnumNext**</span></span>](tlskeypackenumnext.md)
</dt> <dt>

[<span data-ttu-id="d2e45-163">**Tlskeypackenumend**</span><span class="sxs-lookup"><span data-stu-id="d2e45-163">**TLSKeyPackEnumEnd**</span></span>](tlskeypackenumend.md)
</dt> </dl>

 

 





