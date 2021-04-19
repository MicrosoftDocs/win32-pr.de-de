---
title: WMDRM_LICENSE_FILTER Struktur (wmdrmsdk. h)
description: Die WMDRM- \_ Lizenz \_ Filter Struktur definiert Filter Parameter, die beim Erstellen einer Lizenzierungs Enumeration verwendet werden.
ms.assetid: 43bbbfdc-1ec4-44a6-8245-96853bbeea86
keywords:
- WMDRM_LICENSE_FILTER Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- WMDRM_LICENSE_FILTER
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9200bea0d74b7c9a84c5731072e2e65bca81b6cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356408"
---
# <a name="wmdrm_license_filter-structure"></a><span data-ttu-id="58c5f-105">WMDRM- \_ Lizenz \_ Filter Struktur</span><span class="sxs-lookup"><span data-stu-id="58c5f-105">WMDRM\_LICENSE\_FILTER structure</span></span>

<span data-ttu-id="58c5f-106">Die **WMDRM- \_ Lizenz \_ Filter** Struktur definiert Filter Parameter, die beim Erstellen einer Lizenzierungs Enumeration verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="58c5f-106">The **WMDRM\_LICENSE\_FILTER** structure defines filtering parameters for use when creating a license enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="58c5f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="58c5f-107">Syntax</span></span>


```C++
typedef struct WMDRM_LICENSE_FILTER {
  DWORD dwVersion;
  BSTR  bstrKID;
  BSTR  bstrRights;
  BSTR  bstrAllowedSourceIDs;
} ;
```



## <a name="members"></a><span data-ttu-id="58c5f-108">Member</span><span class="sxs-lookup"><span data-stu-id="58c5f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="58c5f-109">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="58c5f-109">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="58c5f-110">Gibt eine minimale Versionsnummer für die zurückgegebenen Lizenzen an.</span><span class="sxs-lookup"><span data-stu-id="58c5f-110">Specifies a minimum version number for the returned licenses.</span></span>

</dd> <dt>

<span data-ttu-id="58c5f-111">**bstrinkid**</span><span class="sxs-lookup"><span data-stu-id="58c5f-111">**bstrKID**</span></span>
</dt> <dd>

<span data-ttu-id="58c5f-112">Gibt eine Schlüssel-ID zum Filtern von Lizenzen an.</span><span class="sxs-lookup"><span data-stu-id="58c5f-112">Specifies a key ID to filter licenses for.</span></span> <span data-ttu-id="58c5f-113">Nur Lizenzen mit der angegebenen Schlüssel-ID werden in die-Enumeration eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="58c5f-113">Only licenses with the specified key ID will be included in the enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="58c5f-114">**bstraurights**</span><span class="sxs-lookup"><span data-stu-id="58c5f-114">**bstrRights**</span></span>
</dt> <dd>

<span data-ttu-id="58c5f-115">Gibt einen Satz von Rechten zum Filtern von Lizenzen an.</span><span class="sxs-lookup"><span data-stu-id="58c5f-115">Specifies a set of rights to filter licenses for.</span></span> <span data-ttu-id="58c5f-116">Nur Lizenzen, die alle angegebenen Rechte bereitstellen, sind in der-Enumeration enthalten.</span><span class="sxs-lookup"><span data-stu-id="58c5f-116">Only licenses that provide all of the specified rights will be included in the enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="58c5f-117">**bstrauzuweisung-sourceids**</span><span class="sxs-lookup"><span data-stu-id="58c5f-117">**bstrAllowedSourceIDs**</span></span>
</dt> <dd>

<span data-ttu-id="58c5f-118">Gibt die Quellen geschützter Inhalte an, die in der Lizenz Suche enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="58c5f-118">Specifies the sources of protected content to include in the license search.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="58c5f-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58c5f-119">Remarks</span></span>

<span data-ttu-id="58c5f-120">Diese Struktur wird von der [**iwmdrmlicenaberation**](iwmdrmlicensemanagement-createlicenseenumeration.md) -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="58c5f-120">This structure is used by the [**IWMDRMLicenseManagement::CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="58c5f-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58c5f-121">Requirements</span></span>



| <span data-ttu-id="58c5f-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="58c5f-122">Requirement</span></span> | <span data-ttu-id="58c5f-123">Wert</span><span class="sxs-lookup"><span data-stu-id="58c5f-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="58c5f-124">Header</span><span class="sxs-lookup"><span data-stu-id="58c5f-124">Header</span></span><br/> | <dl> <span data-ttu-id="58c5f-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="58c5f-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58c5f-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58c5f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58c5f-127">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="58c5f-127">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





