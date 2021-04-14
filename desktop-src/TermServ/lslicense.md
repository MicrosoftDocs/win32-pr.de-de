---
title: Lslicense-Struktur
description: Enthält Informationen zu einer bestimmten Remotedesktopdienste Lizenz.
ms.assetid: 2c7f7b7a-e3b5-4f84-b49f-5f1d6960652d
ms.tgt_platform: multiple
keywords:
- Lslicense-Struktur Remotedesktopdienste
- Lplslicense-Struktur Zeiger Remotedesktopdienste
topic_type:
- apiref
api_name:
- LSLicense
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dcb8551c1d1edfd9486d42df63de9a76fab38433
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476440"
---
# <a name="lslicense-structure"></a><span data-ttu-id="8302a-105">Lslicense-Struktur</span><span class="sxs-lookup"><span data-stu-id="8302a-105">LSLicense structure</span></span>

<span data-ttu-id="8302a-106">Enthält Informationen zu einer bestimmten Remotedesktopdienste Lizenz.</span><span class="sxs-lookup"><span data-stu-id="8302a-106">Contains information about a specific Remote Desktop Services license.</span></span>

> [!Note]  
> <span data-ttu-id="8302a-107">Diese Struktur ist nicht in einer Header Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="8302a-107">This structure is not defined in any header file.</span></span> <span data-ttu-id="8302a-108">Um diese Struktur verwenden zu können, müssen Sie Sie selbst definieren, wie in diesem Thema gezeigt.</span><span class="sxs-lookup"><span data-stu-id="8302a-108">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="8302a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8302a-109">Syntax</span></span>


```C++
typedef struct _LSLicense {
  DWORD dwVersion;
  DWORD dwLicenseId;
  DWORD dwKeyPackId;
  TCHAR szHWID[GUID_MAX_SIZE];
  TCHAR szMachineName[MAXCOMPUTERNAMELENGTH];
  TCHAR szUserName[MAXUSERNAMELENGTH];
  DWORD dwCertSerialLicense;
  DWORD dwLicenseSerialNumber;
  DWORD ftIssueDate;
  DWORD ftExpireDate;
  UCHAR ucLicenseStatus;
} LSLicense, *LPLSLicense;
```



## <a name="members"></a><span data-ttu-id="8302a-110">Member</span><span class="sxs-lookup"><span data-stu-id="8302a-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="8302a-111">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="8302a-111">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="8302a-112">Version der Lizenz.</span><span class="sxs-lookup"><span data-stu-id="8302a-112">Version of the license.</span></span>

</dd> <dt>

<span data-ttu-id="8302a-113">**dwlicenseid**</span><span class="sxs-lookup"><span data-stu-id="8302a-113">**dwLicenseId**</span></span>
</dt> <dd>

<span data-ttu-id="8302a-114">Die ID der Lizenz.</span><span class="sxs-lookup"><span data-stu-id="8302a-114">ID of the license.</span></span>

</dd> <dt>

<span data-ttu-id="8302a-115">**dwkeypackid**</span><span class="sxs-lookup"><span data-stu-id="8302a-115">**dwKeyPackId**</span></span>
</dt> <dd>

<span data-ttu-id="8302a-116">ID des [**lschräypack-Pakets**](lskeypack.md) , das die Lizenz enthält.</span><span class="sxs-lookup"><span data-stu-id="8302a-116">ID of the [**LSKeyPack**](lskeypack.md) that contains the license.</span></span>

</dd> <dt>

<span data-ttu-id="8302a-117">**szhwid**</span><span class="sxs-lookup"><span data-stu-id="8302a-117">**szHWID**</span></span>
</dt> <dd>

<span data-ttu-id="8302a-118">Die Hardware-ID des Remotedesktopverbindung (RDC)-Clients, für den die Lizenz ausgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="8302a-118">Hardware ID of the Remote Desktop Connection (RDC) client that was issued the license.</span></span>

</dd> <dt>

<span data-ttu-id="8302a-119">**szmachinename**</span><span class="sxs-lookup"><span data-stu-id="8302a-119">**szMachineName**</span></span>
</dt> <dd>

<span data-ttu-id="8302a-120">Der Name des Remotedesktopverbindung (RDC)-Clients, für den die Lizenz ausgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="8302a-120">Name of the Remote Desktop Connection (RDC) client that was issued the license.</span></span>

</dd> <dt>

<span data-ttu-id="8302a-121">**szusername**</span><span class="sxs-lookup"><span data-stu-id="8302a-121">**szUserName**</span></span>
</dt> <dd>

<span data-ttu-id="8302a-122">Der Name des Benutzers, der die Lizenz ausgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="8302a-122">Name of the user who was issued the license.</span></span>

</dd> <dt>

<span data-ttu-id="8302a-123">**dwcertseriallicense**</span><span class="sxs-lookup"><span data-stu-id="8302a-123">**dwCertSerialLicense**</span></span>
</dt> <dd>

<span data-ttu-id="8302a-124">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="8302a-124">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="8302a-125">**dwlicenseserialnumber**</span><span class="sxs-lookup"><span data-stu-id="8302a-125">**dwLicenseSerialNumber**</span></span>
</dt> <dd>

<span data-ttu-id="8302a-126">Seriennummer der Lizenz.</span><span class="sxs-lookup"><span data-stu-id="8302a-126">Serial number of the license.</span></span>

</dd> <dt>

<span data-ttu-id="8302a-127">**ftIssueDate**</span><span class="sxs-lookup"><span data-stu-id="8302a-127">**ftIssueDate**</span></span>
</dt> <dd>

<span data-ttu-id="8302a-128">Datum, an dem die Lizenz ausgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="8302a-128">Date that the license was issued.</span></span>

</dd> <dt>

<span data-ttu-id="8302a-129">**ftexpiredate**</span><span class="sxs-lookup"><span data-stu-id="8302a-129">**ftExpireDate**</span></span>
</dt> <dd>

<span data-ttu-id="8302a-130">Datum, an dem die Lizenz abläuft.</span><span class="sxs-lookup"><span data-stu-id="8302a-130">Date that the license will expire.</span></span>

</dd> <dt>

<span data-ttu-id="8302a-131">**uclicenstatusstatus**</span><span class="sxs-lookup"><span data-stu-id="8302a-131">**ucLicenseStatus**</span></span>
</dt> <dd>

<span data-ttu-id="8302a-132">Aktueller Status der Lizenz.</span><span class="sxs-lookup"><span data-stu-id="8302a-132">Current status of the license.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8302a-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8302a-133">Requirements</span></span>



| <span data-ttu-id="8302a-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8302a-134">Requirement</span></span> | <span data-ttu-id="8302a-135">Wert</span><span class="sxs-lookup"><span data-stu-id="8302a-135">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="8302a-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8302a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8302a-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8302a-137">Windows Vista</span></span><br/>       |
| <span data-ttu-id="8302a-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8302a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8302a-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8302a-139">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8302a-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8302a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8302a-141">**Lschräypack**</span><span class="sxs-lookup"><span data-stu-id="8302a-141">**LSKeyPack**</span></span>](lskeypack.md)
</dt> <dt>

[<span data-ttu-id="8302a-142">**Tlslicenseenumbegin**</span><span class="sxs-lookup"><span data-stu-id="8302a-142">**TLSLicenseEnumBegin**</span></span>](tlslicenseenumbegin.md)
</dt> <dt>

[<span data-ttu-id="8302a-143">**Tlslicensitztenenumnext**</span><span class="sxs-lookup"><span data-stu-id="8302a-143">**TLSLicenseEnumNext**</span></span>](tlslicenseenumnext.md)
</dt> <dt>

[<span data-ttu-id="8302a-144">**Tlslicenabenumend**</span><span class="sxs-lookup"><span data-stu-id="8302a-144">**TLSLicenseEnumEnd**</span></span>](tlslicenseenumend.md)
</dt> </dl>

 

 





