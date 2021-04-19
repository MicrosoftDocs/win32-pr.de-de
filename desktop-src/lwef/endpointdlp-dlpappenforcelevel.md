---
description: Gibt die Erzwingungsebene eines Endpunkt-DLP-Vorgangs (Data Loss Prevention) an.
title: DlpAppEnforceLevel-Enumeration (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpAppEnforceLevel
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: d0ccc8d0d39bc4022899deaeb9e8a81eae1f720f
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495773"
---
# <a name="dlpappenforcelevel-enumeration"></a><span data-ttu-id="45854-103">DlpAppEnforceLevel-Enumeration</span><span class="sxs-lookup"><span data-stu-id="45854-103">DlpAppEnforceLevel enumeration</span></span>

<span data-ttu-id="45854-104">Gibt die Erzwingungsebene eines Endpunkt-DLP-Vorgangs (Data Loss Prevention, Verhinderung von Datenverlust) an.</span><span class="sxs-lookup"><span data-stu-id="45854-104">Specifies the enforcement level of an endpoint Data Loss Prevention (DLP) operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="45854-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="45854-105">Syntax</span></span>


```C++
typedef enum _DlpAppEnforceLevel {
    DlpAppEnforceLevelNone = 0, 
    DlpAppEnforceLevelNotify,   
    DlpAppEnforceLevelPrevent,   
    DlpAppEnforceLevelFull, 
    DlpAppEnforceLevelCount,
}DlpAppEnforceLevel;
```


## <a name="constants"></a><span data-ttu-id="45854-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="45854-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="45854-107">*DlpAppEnforceLevelNone* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="45854-107">*DlpAppEnforceLevelNone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45854-108">Keine Erzwingung durch die App.</span><span class="sxs-lookup"><span data-stu-id="45854-108">No enforcement by the app.</span></span> <span data-ttu-id="45854-109">Das DLP-System erzwingt den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="45854-109">The DLP system will enforce the operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="45854-110">*DlpAppEnforceLevelNotify* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="45854-110">*DlpAppEnforceLevelNotify* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45854-111">Die Tne-App verwendet die DLP-APIs, um das DLP-System über den Vorgang zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="45854-111">Tne app will use the DLP APIs to notify the DLP system about the operation.</span></span> <span data-ttu-id="45854-112">Das DLP-System erzwingt den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="45854-112">The DLP system will enforce the operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="45854-113">*DlpAppEnforceLevelPrevent* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="45854-113">*DlpAppEnforceLevelPrevent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45854-114">Wird in der aktuellen Version nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="45854-114">Not supported in the current version.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="45854-115">*DlpAppEnforceLevelFull* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="45854-115">*DlpAppEnforceLevelFull* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45854-116">Wird in der aktuellen Version nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="45854-116">Not supported in the current version.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="45854-117">*DlpAppEnforceLevelCount* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="45854-117">*DlpAppEnforceLevelCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45854-118">Der Höchstwert der Enumeration.</span><span class="sxs-lookup"><span data-stu-id="45854-118">The maximum value of the enumeration.</span></span>

</dd> </dl>



## <a name="remarks"></a><span data-ttu-id="45854-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="45854-119">Remarks</span></span>

<span data-ttu-id="45854-120">Werte aus dieser Enumeration werden von der [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="45854-120">Values from this enumeration are used by the [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) structure.</span></span>


## <a name="requirements"></a><span data-ttu-id="45854-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="45854-121">Requirements</span></span>



| <span data-ttu-id="45854-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="45854-122">Requirement</span></span>          |    <span data-ttu-id="45854-123">Wert</span><span class="sxs-lookup"><span data-stu-id="45854-123">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="45854-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="45854-124">Minimum supported client</span></span><br/> | <span data-ttu-id="45854-125">Windows 10, Version 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="45854-125">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |

