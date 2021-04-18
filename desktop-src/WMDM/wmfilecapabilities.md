---
title: Wmfilefunktionen-Struktur
description: Die wmfilefunktionalitäten-Struktur beschreibt den MIME-Typ.
ms.assetid: 30307343-f55e-4695-9ae8-b938617d749d
keywords:
- Wmfilefunktionen-Struktur Windows Media Device Manager
topic_type:
- apiref
api_name:
- WMFILECAPABILITIES
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7657ddd15a4219a0d5f56dbadeffba2a9547bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357529"
---
# <a name="wmfilecapabilities-structure"></a><span data-ttu-id="2b9e5-104">Wmfilefunktionen-Struktur</span><span class="sxs-lookup"><span data-stu-id="2b9e5-104">WMFILECAPABILITIES structure</span></span>

<span data-ttu-id="2b9e5-105">Die **wmfilefunktionalitäten** -Struktur beschreibt den MIME-Typ.</span><span class="sxs-lookup"><span data-stu-id="2b9e5-105">The **WMFILECAPABILITIES** structure describes the MIME type.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b9e5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b9e5-106">Syntax</span></span>


```C++
typedef struct _tagWMFILECAPABILITIES {
  LPWSTR pwszMimeType;
  DWORD  dwReserved;
} WMFILECAPABILITIES;
```



## <a name="members"></a><span data-ttu-id="2b9e5-107">Member</span><span class="sxs-lookup"><span data-stu-id="2b9e5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="2b9e5-108">**pwszmimetype**</span><span class="sxs-lookup"><span data-stu-id="2b9e5-108">**pwszMimeType**</span></span>
</dt> <dd>

<span data-ttu-id="2b9e5-109">MIME-Typ.</span><span class="sxs-lookup"><span data-stu-id="2b9e5-109">MIME type.</span></span>

</dd> <dt>

<span data-ttu-id="2b9e5-110">**dwReserved**</span><span class="sxs-lookup"><span data-stu-id="2b9e5-110">**dwReserved**</span></span>
</dt> <dd>

<span data-ttu-id="2b9e5-111">**DWORD** ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="2b9e5-111">**DWORD** reserved for future use.</span></span> <span data-ttu-id="2b9e5-112">Auf NULL (0) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2b9e5-112">Set to zero (0).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2b9e5-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b9e5-113">Requirements</span></span>



| <span data-ttu-id="2b9e5-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b9e5-114">Requirement</span></span> | <span data-ttu-id="2b9e5-115">Wert</span><span class="sxs-lookup"><span data-stu-id="2b9e5-115">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2b9e5-116">Header</span><span class="sxs-lookup"><span data-stu-id="2b9e5-116">Header</span></span><br/> | <dl> <span data-ttu-id="2b9e5-117"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2b9e5-117"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b9e5-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b9e5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b9e5-119">**IWMDMDevice2::GetFormatSupport2**</span><span class="sxs-lookup"><span data-stu-id="2b9e5-119">**IWMDMDevice2::GetFormatSupport2**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2)
</dt> <dt>

[<span data-ttu-id="2b9e5-120">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="2b9e5-120">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





