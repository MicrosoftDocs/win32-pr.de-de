---
description: Enthält Informationen zu erweiterten Modulen.
ms.assetid: 705769de-0aeb-4a28-b174-8620efa74baf
title: AUX_MODULE_EXTENDED_INFO Struktur (AUX \_ KLIB. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AUX_MODULE_EXTENDED_INFO
api_type:
- HeaderDef
api_location:
- Aux_klib.h
ms.openlocfilehash: 9faa706ca3603a1796d70e2f208e9b3b2e518c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354740"
---
# <a name="aux_module_extended_info-structure"></a><span data-ttu-id="ac834-103">\_ \_ Erweiterte \_ Informationsstruktur des aux-Moduls</span><span class="sxs-lookup"><span data-stu-id="ac834-103">AUX\_MODULE\_EXTENDED\_INFO structure</span></span>

<span data-ttu-id="ac834-104">Enthält Informationen zu erweiterten Modulen.</span><span class="sxs-lookup"><span data-stu-id="ac834-104">Contains extended module information.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac834-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac834-105">Syntax</span></span>


```C++
typedef struct _AUX_MODULE_EXTENDED_INFO {
  AUX_MODULE_BASIC_INFO BasicInfo;
  ULONG                 ImageSize;
  USHORT                FileNameOffset;
  UCHAR                 FullPathName[AUX_KLIB_MODULE_PATH_LEN];
} AUX_MODULE_EXTENDED_INFO, *PAUX_MODULE_EXTENDED_INFO;
```



## <a name="members"></a><span data-ttu-id="ac834-106">Member</span><span class="sxs-lookup"><span data-stu-id="ac834-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ac834-107">**BasicInfo**</span><span class="sxs-lookup"><span data-stu-id="ac834-107">**BasicInfo**</span></span>
</dt> <dd>

<span data-ttu-id="ac834-108">Eine [**\_ \_ grundlegende \_ Informationsstruktur von aux Module**](aux-module-basic-info-struct.md) .</span><span class="sxs-lookup"><span data-stu-id="ac834-108">An [**AUX\_MODULE\_BASIC\_INFO**](aux-module-basic-info-struct.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ac834-109">**ImageSize**</span><span class="sxs-lookup"><span data-stu-id="ac834-109">**ImageSize**</span></span>
</dt> <dd>

<span data-ttu-id="ac834-110">Die Größe (in Bytes) des geladenen Moduls.</span><span class="sxs-lookup"><span data-stu-id="ac834-110">The size, in bytes, of the loaded module.</span></span>

</dd> <dt>

<span data-ttu-id="ac834-111">**Dateinameoffset**</span><span class="sxs-lookup"><span data-stu-id="ac834-111">**FileNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="ac834-112">Der Offset des Datei namens innerhalb des **fullpathname** -Puffers.</span><span class="sxs-lookup"><span data-stu-id="ac834-112">The offset of the file name within the **FullPathName** buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ac834-113">**Fullpathname**</span><span class="sxs-lookup"><span data-stu-id="ac834-113">**FullPathName**</span></span>
</dt> <dd>

<span data-ttu-id="ac834-114">Der vollständige Pfad des Moduls.</span><span class="sxs-lookup"><span data-stu-id="ac834-114">The full path of the module.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ac834-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac834-115">Remarks</span></span>

<span data-ttu-id="ac834-116">Die Objektbibliothek, die diese API implementiert, kann [hier](https://www.microsoft.com/?ref=go)heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="ac834-116">The object library that implements this API can be downloaded from [here](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="ac834-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac834-117">Requirements</span></span>



| <span data-ttu-id="ac834-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac834-118">Requirement</span></span> | <span data-ttu-id="ac834-119">Wert</span><span class="sxs-lookup"><span data-stu-id="ac834-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac834-120">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="ac834-120">Redistributable</span></span><br/> | <span data-ttu-id="ac834-121">Windows-Erweiterungs-API-Bibliothek, Version 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="ac834-121">Windows Auxiliary API library version 1.0 or later</span></span><br/>                          |
| <span data-ttu-id="ac834-122">Header</span><span class="sxs-lookup"><span data-stu-id="ac834-122">Header</span></span><br/>          | <dl> <span data-ttu-id="ac834-123"><dt>AUX \_ KLIB. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac834-123"><dt>Aux\_klib.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac834-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac834-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac834-125">**"Auxklibquerymoduleinformation"**</span><span class="sxs-lookup"><span data-stu-id="ac834-125">**AuxKlibQueryModuleInformation**</span></span>](auxklibquerymoduleinformation-func.md)
</dt> <dt>

[<span data-ttu-id="ac834-126">**\_ \_ grundlegende \_ Informationen zu aux-Modulen**</span><span class="sxs-lookup"><span data-stu-id="ac834-126">**AUX\_MODULE\_BASIC\_INFO**</span></span>](aux-module-basic-info-struct.md)
</dt> </dl>

 

 




