---
title: CB_RESOURCE_TYPE-Enumeration (cbclient. h)
description: Gibt den Typ der Ressource an, mit der die eingehende Verbindung eine Verbindung herstellt.
ms.assetid: 80D921BF-2D84-4A18-9544-50087B81F177
ms.tgt_platform: multiple
keywords:
- CB_RESOURCE_TYPE Enumeration Remotedesktopdienste
topic_type:
- apiref
api_name:
- CB_RESOURCE_TYPE
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60561e4af54c6d27288d8df311693d51c0b9fc77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740584"
---
# <a name="cb_resource_type-enumeration"></a><span data-ttu-id="88923-104">CB \_ - \_ Ressourcentyp Enumeration</span><span class="sxs-lookup"><span data-stu-id="88923-104">CB\_RESOURCE\_TYPE enumeration</span></span>

<span data-ttu-id="88923-105">Gibt den Typ der Ressource an, mit der die eingehende Verbindung eine Verbindung herstellt.</span><span class="sxs-lookup"><span data-stu-id="88923-105">Specifies the type of resource that the incoming connection is connecting to.</span></span> <span data-ttu-id="88923-106">Diese Enumeration wird mit der [**CB- \_ Verbindungs \_ Informations**](cb-connection-info.md) Struktur verwendet.</span><span class="sxs-lookup"><span data-stu-id="88923-106">This enumeration is used with the [**CB\_CONNECTION\_INFO**](cb-connection-info.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="88923-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="88923-107">Syntax</span></span>


```C++
typedef enum _CB_RESOURCE_TYPE { 
  CB_RESOURCE_UNDEFINED  = 0,
  CB_RESOURCE_SESSION    = 1,
  CB_RESOURCE_VM
} CB_RESOURCE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="88923-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="88923-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="88923-109"><span id="CB_RESOURCE_UNDEFINED"></span><span id="cb_resource_undefined"></span>**CB- \_ Ressource nicht \_ definiert**</span><span class="sxs-lookup"><span data-stu-id="88923-109"><span id="CB_RESOURCE_UNDEFINED"></span><span id="cb_resource_undefined"></span>**CB\_RESOURCE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="88923-110">Der Ressourcentyp ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="88923-110">The resource type is not defined.</span></span>

</dd> <dt>

<span data-ttu-id="88923-111"><span id="CB_RESOURCE_SESSION"></span><span id="cb_resource_session"></span>**CB- \_ Ressourcen \_ Sitzung**</span><span class="sxs-lookup"><span data-stu-id="88923-111"><span id="CB_RESOURCE_SESSION"></span><span id="cb_resource_session"></span>**CB\_RESOURCE\_SESSION**</span></span>
</dt> <dd>

<span data-ttu-id="88923-112">Die Ressource ist eine Remote Sitzung.</span><span class="sxs-lookup"><span data-stu-id="88923-112">The resource is a remote session.</span></span>

</dd> <dt>

<span data-ttu-id="88923-113"><span id="CB_RESOURCE_VM"></span><span id="cb_resource_vm"></span>**CB- \_ Ressourcen- \_ VM**</span><span class="sxs-lookup"><span data-stu-id="88923-113"><span id="CB_RESOURCE_VM"></span><span id="cb_resource_vm"></span>**CB\_RESOURCE\_VM**</span></span>
</dt> <dd>

<span data-ttu-id="88923-114">Die Ressource ist ein virtueller Computer.</span><span class="sxs-lookup"><span data-stu-id="88923-114">The resource is a virtual machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="88923-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88923-115">Requirements</span></span>



| <span data-ttu-id="88923-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88923-116">Requirement</span></span> | <span data-ttu-id="88923-117">Wert</span><span class="sxs-lookup"><span data-stu-id="88923-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="88923-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="88923-118">Minimum supported client</span></span><br/> | <span data-ttu-id="88923-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="88923-119">Windows 8</span></span><br/>                                                                  |
| <span data-ttu-id="88923-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="88923-120">Minimum supported server</span></span><br/> | <span data-ttu-id="88923-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="88923-121">Windows Server 2012</span></span><br/>                                                        |
| <span data-ttu-id="88923-122">Header</span><span class="sxs-lookup"><span data-stu-id="88923-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="88923-123"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="88923-123"><dt>Cbclient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88923-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88923-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88923-125">**CB- \_ Verbindungs \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="88923-125">**CB\_CONNECTION\_INFO**</span></span>](cb-connection-info.md)
</dt> </dl>

 

 





