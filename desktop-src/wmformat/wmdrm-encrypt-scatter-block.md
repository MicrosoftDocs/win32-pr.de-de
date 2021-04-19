---
title: WMDRM_ENCRYPT_SCATTER_BLOCK Struktur (wmdrmsdk. h)
description: Die WMDRM- \_ Verschlüsselungs Punkt \_ \_ Blockstruktur enthält einen Daten Block, der verschlüsselt werden soll.
ms.assetid: 73c871f0-3d0d-480f-856c-0f7d5dde5895
keywords:
- WMDRM_ENCRYPT_SCATTER_BLOCK Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- WMDRM_ENCRYPT_SCATTER_BLOCK
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8911ba1822b146de4a99ff1fe144afcfd8e212e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353821"
---
# <a name="wmdrm_encrypt_scatter_block-structure"></a><span data-ttu-id="e48b2-105">WMDRM-Verschlüsselungs Punkt- \_ \_ \_ Block Struktur</span><span class="sxs-lookup"><span data-stu-id="e48b2-105">WMDRM\_ENCRYPT\_SCATTER\_BLOCK structure</span></span>

<span data-ttu-id="e48b2-106">Die **WMDRM- \_ Verschlüsselungs Punkt \_ \_ Block** Struktur enthält einen Daten Block, der verschlüsselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e48b2-106">The **WMDRM\_ENCRYPT\_SCATTER\_BLOCK** structure contains a block of data to be encrypted.</span></span>

## <a name="syntax"></a><span data-ttu-id="e48b2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e48b2-107">Syntax</span></span>


```C++
typedef struct WMDRM_ENCRYPT_SCATTER_BLOCK {
  DWORD dwStreamID;
  DWORD cbBlock;
  BYTE  *pbBlock;
} ;
```



## <a name="members"></a><span data-ttu-id="e48b2-108">Member</span><span class="sxs-lookup"><span data-stu-id="e48b2-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e48b2-109">**dwstreamid**</span><span class="sxs-lookup"><span data-stu-id="e48b2-109">**dwStreamID**</span></span>
</dt> <dd>

<span data-ttu-id="e48b2-110">Der Bezeichner des Streams, zu dem der Datenblock gehört.</span><span class="sxs-lookup"><span data-stu-id="e48b2-110">Identifier of the stream to which the data block belongs.</span></span>

</dd> <dt>

<span data-ttu-id="e48b2-111">**cbblock**</span><span class="sxs-lookup"><span data-stu-id="e48b2-111">**cbBlock**</span></span>
</dt> <dd>

<span data-ttu-id="e48b2-112">Blockgröße in Bytes.</span><span class="sxs-lookup"><span data-stu-id="e48b2-112">Size of block in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e48b2-113">**pbblock**</span><span class="sxs-lookup"><span data-stu-id="e48b2-113">**pbBlock**</span></span>
</dt> <dd>

<span data-ttu-id="e48b2-114">Zeiger auf einen Puffer, der den Datenblock enthält.</span><span class="sxs-lookup"><span data-stu-id="e48b2-114">Pointer to a buffer containing the data block.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e48b2-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e48b2-115">Remarks</span></span>

<span data-ttu-id="e48b2-116">Diese Struktur wird von der [**iwmdrmencryptscatter:: verschlüsseltscatter**](iwmdrmencryptscatter-encryptscatter.md) -Methode verwendet, um Datenblöcke zu identifizieren, die verschlüsselt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e48b2-116">This structure is used by the [**IWMDRMEncryptScatter::EncryptScatter**](iwmdrmencryptscatter-encryptscatter.md) method to identify blocks of data to encrypt.</span></span>

## <a name="requirements"></a><span data-ttu-id="e48b2-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e48b2-117">Requirements</span></span>



| <span data-ttu-id="e48b2-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e48b2-118">Requirement</span></span> | <span data-ttu-id="e48b2-119">Wert</span><span class="sxs-lookup"><span data-stu-id="e48b2-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e48b2-120">Header</span><span class="sxs-lookup"><span data-stu-id="e48b2-120">Header</span></span><br/> | <dl> <span data-ttu-id="e48b2-121"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="e48b2-121"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e48b2-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e48b2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e48b2-123">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="e48b2-123">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





