---
title: WMDRM_ENCRYPT_SCATTER_INFO Struktur (wmdrmsdk. h)
description: Die WMDRM- \_ Verschlüsselungs Punkt \_ \_ Info Struktur enthält Informationen, die erforderlich sind, um die zu verwendende iwmdrmencryptscatter-Schnittstelle zu konfigurieren.
ms.assetid: 25e19511-56ac-441b-b521-5097dd792ead
keywords:
- WMDRM_ENCRYPT_SCATTER_INFO Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- WMDRM_ENCRYPT_SCATTER_INFO
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 500012231f6860fd94038b240355eda9aa2aee44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364892"
---
# <a name="wmdrm_encrypt_scatter_info-structure"></a><span data-ttu-id="aa3bd-105">WMDRM- \_ Verschlüsselungs Punkt \_ Info- \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="aa3bd-105">WMDRM\_ENCRYPT\_SCATTER\_INFO structure</span></span>

<span data-ttu-id="aa3bd-106">Die **WMDRM- \_ Verschlüsselungs Punkt \_ \_ Info** Struktur enthält Informationen, die erforderlich sind, um die zu verwendende [**iwmdrmencryptscatter**](iwmdrmencryptscatter.md) -Schnittstelle zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="aa3bd-106">The **WMDRM\_ENCRYPT\_SCATTER\_INFO** structure contains information needed to configure the [**IWMDRMEncryptScatter**](iwmdrmencryptscatter.md) interface for use.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa3bd-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa3bd-107">Syntax</span></span>


```C++
typedef struct WMDRM_ENCRYPT_SCATTER_INFO {
  DWORD dwStreamID;
  DWORD dwSampleProtectionVersion;
  DWORD cbProtectionInfo;
  BYTE  *pbProtectionInfo;
} ;
```



## <a name="members"></a><span data-ttu-id="aa3bd-108">Member</span><span class="sxs-lookup"><span data-stu-id="aa3bd-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="aa3bd-109">**dwstreamid**</span><span class="sxs-lookup"><span data-stu-id="aa3bd-109">**dwStreamID**</span></span>
</dt> <dd>

<span data-ttu-id="aa3bd-110">Der Bezeichner des zu verschlüsselnden Streams.</span><span class="sxs-lookup"><span data-stu-id="aa3bd-110">Identifier of the stream to be encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="aa3bd-111">**dwsampleschutzversion**</span><span class="sxs-lookup"><span data-stu-id="aa3bd-111">**dwSampleProtectionVersion**</span></span>
</dt> <dd>

<span data-ttu-id="aa3bd-112">Die Beispiel Schutz Version, die zum Codieren von Daten aus dem angegebenen Stream verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="aa3bd-112">Sample protection version to be used to encode data from the specified stream.</span></span>

</dd> <dt>

<span data-ttu-id="aa3bd-113">**cbschutzinfo**</span><span class="sxs-lookup"><span data-stu-id="aa3bd-113">**cbProtectionInfo**</span></span>
</dt> <dd>

<span data-ttu-id="aa3bd-114">Größe des **pbschutzinfo** -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="aa3bd-114">Size of the **pbProtectionInfo** buffer in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="aa3bd-115">**pbschutzinfo**</span><span class="sxs-lookup"><span data-stu-id="aa3bd-115">**pbProtectionInfo**</span></span>
</dt> <dd>

<span data-ttu-id="aa3bd-116">Puffer mit zusätzlichen Schutz Informationen.</span><span class="sxs-lookup"><span data-stu-id="aa3bd-116">Buffer containing additional protection information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aa3bd-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aa3bd-117">Remarks</span></span>

<span data-ttu-id="aa3bd-118">Diese Struktur wird von der [**iwmdrmencryptscatter:: initencryptscatter**](iwmdrmencryptscatter-initencryptscatter.md) -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="aa3bd-118">This structure is used by the [**IWMDRMEncryptScatter::InitEncryptScatter**](iwmdrmencryptscatter-initencryptscatter.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa3bd-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa3bd-119">Requirements</span></span>



| <span data-ttu-id="aa3bd-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa3bd-120">Requirement</span></span> | <span data-ttu-id="aa3bd-121">Wert</span><span class="sxs-lookup"><span data-stu-id="aa3bd-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aa3bd-122">Header</span><span class="sxs-lookup"><span data-stu-id="aa3bd-122">Header</span></span><br/> | <dl> <span data-ttu-id="aa3bd-123"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa3bd-123"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa3bd-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa3bd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa3bd-125">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="aa3bd-125">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





