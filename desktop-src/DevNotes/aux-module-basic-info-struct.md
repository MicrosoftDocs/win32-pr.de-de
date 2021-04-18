---
description: Enthält grundlegende Modul Informationen.
ms.assetid: 5cdb0b11-8bd3-46d2-b214-85cdb2f274a7
title: AUX_MODULE_BASIC_INFO Struktur (AUX \_ KLIB. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AUX_MODULE_BASIC_INFO
api_type:
- HeaderDef
api_location:
- Aux_klib.h
ms.openlocfilehash: 1ee7300ec2c2d84e1ddadc4149135dab53d2336b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365694"
---
# <a name="aux_module_basic_info-structure"></a><span data-ttu-id="21919-103">\_ \_ Grundlegende \_ Informationsstruktur des aux-Moduls</span><span class="sxs-lookup"><span data-stu-id="21919-103">AUX\_MODULE\_BASIC\_INFO structure</span></span>

<span data-ttu-id="21919-104">Enthält grundlegende Modul Informationen.</span><span class="sxs-lookup"><span data-stu-id="21919-104">Contains basic module information.</span></span>

## <a name="syntax"></a><span data-ttu-id="21919-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="21919-105">Syntax</span></span>


```C++
typedef struct _AUX_MODULE_BASIC_INFO {
  PVOID ImageBase;
} AUX_MODULE_BASIC_INFO, *PAUX_MODULE_BASIC_INFO;
```



## <a name="members"></a><span data-ttu-id="21919-106">Member</span><span class="sxs-lookup"><span data-stu-id="21919-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="21919-107">**ImageBase**</span><span class="sxs-lookup"><span data-stu-id="21919-107">**ImageBase**</span></span>
</dt> <dd>

<span data-ttu-id="21919-108">Die Basisadresse des Moduls innerhalb des Adressraums des Kernels.</span><span class="sxs-lookup"><span data-stu-id="21919-108">The base address of the module within the kernel's address space.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="21919-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="21919-109">Remarks</span></span>

<span data-ttu-id="21919-110">Die Objektbibliothek, die diese API implementiert, kann [hier](https://www.microsoft.com/?ref=go)heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="21919-110">The object library that implements this API can be downloaded from [here](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="21919-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21919-111">Requirements</span></span>



| <span data-ttu-id="21919-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21919-112">Requirement</span></span> | <span data-ttu-id="21919-113">Wert</span><span class="sxs-lookup"><span data-stu-id="21919-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="21919-114">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="21919-114">Redistributable</span></span><br/> | <span data-ttu-id="21919-115">Windows-Erweiterungs-API-Bibliothek, Version 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="21919-115">Windows Auxiliary API library version 1.0 or later</span></span><br/>                          |
| <span data-ttu-id="21919-116">Header</span><span class="sxs-lookup"><span data-stu-id="21919-116">Header</span></span><br/>          | <dl> <span data-ttu-id="21919-117"><dt>AUX \_ KLIB. h</dt></span><span class="sxs-lookup"><span data-stu-id="21919-117"><dt>Aux\_klib.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21919-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21919-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21919-119">**"Auxklibquerymoduleinformation"**</span><span class="sxs-lookup"><span data-stu-id="21919-119">**AuxKlibQueryModuleInformation**</span></span>](auxklibquerymoduleinformation-func.md)
</dt> </dl>

 

 




