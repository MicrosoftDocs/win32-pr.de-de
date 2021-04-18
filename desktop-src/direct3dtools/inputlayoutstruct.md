---
description: Stellt die Eingabe Layout-Felder eines Scheitelpunkt Puffers dar, einen pro Feld im Scheitelpunkt Puffer.
MS-HAID: vspixengine.InputLayoutStruct
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Inputlayoutstruct-Struktur
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CC7AAC2F-FDB1-4AD8-9B87-A97EE557FEAC
api_name:
- InputLayoutStruct
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1369d80d202682b67eacbb184b215d9da1711874
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106340070"
---
# <a name="span-idvspixengineinputlayoutstructspaninputlayoutstruct-structure"></a><span data-ttu-id="f4018-103"><span id="vspixengine.inputlayoutstruct"></span>Inputlayoutstruct-Struktur</span><span class="sxs-lookup"><span data-stu-id="f4018-103"><span id="vspixengine.inputlayoutstruct"></span>InputLayoutStruct structure</span></span>

<span data-ttu-id="f4018-104">Stellt die Eingabe Layout-Felder eines Scheitelpunkt Puffers dar, einen pro Feld im Scheitelpunkt Puffer.</span><span class="sxs-lookup"><span data-stu-id="f4018-104">Represents the input layout fields of a vertex buffer, one per field in the vertex buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4018-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4018-105">Syntax</span></span>


```C++
} InputLayoutStruct;
```

## <a name="members"></a><span data-ttu-id="f4018-106">Member</span><span class="sxs-lookup"><span data-stu-id="f4018-106">Members</span></span>

<span data-ttu-id="f4018-107">**Semanticname**</span><span class="sxs-lookup"><span data-stu-id="f4018-107">**SemanticName**</span></span>  
<span data-ttu-id="f4018-108">Eine com-Zeichenfolge, die den Namen der zugeordneten Semantik enthält.</span><span class="sxs-lookup"><span data-stu-id="f4018-108">A COM string containing the name of the associated semantic.</span></span>

<span data-ttu-id="f4018-109">**Semanticindex**</span><span class="sxs-lookup"><span data-stu-id="f4018-109">**SemanticIndex**</span></span>  
<span data-ttu-id="f4018-110">Der Index der zugeordneten Semantik.</span><span class="sxs-lookup"><span data-stu-id="f4018-110">The index of the associated semantic.</span></span>

<span data-ttu-id="f4018-111">**Format**</span><span class="sxs-lookup"><span data-stu-id="f4018-111">**Format**</span></span>  
<span data-ttu-id="f4018-112">Das Format des Felds.</span><span class="sxs-lookup"><span data-stu-id="f4018-112">The format of the field.</span></span> <span data-ttu-id="f4018-113">Weitere Informationen finden Sie in der DXGI- \_ formatenumeration.</span><span class="sxs-lookup"><span data-stu-id="f4018-113">For more information see the DXGI\_FORMAT enumeration.</span></span>

<span data-ttu-id="f4018-114">**Input Slot**</span><span class="sxs-lookup"><span data-stu-id="f4018-114">**InputSlot**</span></span>  
<span data-ttu-id="f4018-115">Der zugeordnete Eingabe Slot.</span><span class="sxs-lookup"><span data-stu-id="f4018-115">The associated input slot.</span></span>

<span data-ttu-id="f4018-116">**Alignedbyteoffset**</span><span class="sxs-lookup"><span data-stu-id="f4018-116">**AlignedByteOffset**</span></span>  

<span data-ttu-id="f4018-117">**Inputslotclass**</span><span class="sxs-lookup"><span data-stu-id="f4018-117">**InputSlotClass**</span></span>  

<span data-ttu-id="f4018-118">**Instancedatasteprate**</span><span class="sxs-lookup"><span data-stu-id="f4018-118">**InstanceDataStepRate**</span></span>  

## <a name="requirements"></a><span data-ttu-id="f4018-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4018-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f4018-120">Header</span><span class="sxs-lookup"><span data-stu-id="f4018-120">Header</span></span></p></td><td><span data-ttu-id="f4018-121">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="f4018-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



