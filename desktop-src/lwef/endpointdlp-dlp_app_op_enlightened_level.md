---
description: Ordnet eine DLP-Aktion (Data Loss Prevention) eines Endpunkts einer Erzwingungsebene zu.
title: DLP_APP_OP_ENLIGHTENED_LEVEL-Struktur (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_APP_OP_ENLIGHTENED_LEVEL
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 2d9c1aa8335078cad71832c6090cada1669641cb
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495789"
---
# <a name="dlp_app_op_enlightened_level-structure"></a><span data-ttu-id="aecd9-103">DLP_APP_OP_ENLIGHTENED_LEVEL-Struktur</span><span class="sxs-lookup"><span data-stu-id="aecd9-103">DLP_APP_OP_ENLIGHTENED_LEVEL structure</span></span>

<span data-ttu-id="aecd9-104">Ordnet eine DLP-Aktion (Data Loss Prevention) eines Endpunkts einer Erzwingungsebene zu.</span><span class="sxs-lookup"><span data-stu-id="aecd9-104">Associates an endpoint Data Loss Prevention (DLP) action with an enforcement level.</span></span>

## <a name="syntax"></a><span data-ttu-id="aecd9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aecd9-105">Syntax</span></span>


```C++
typedef struct _DLP_APP_OP_ENLIGHTENED_LEVEL{
    DlpActionType Operation;
    DlpAppEnforceLevel AppEnforcementLevel;
}DLP_APP_OP_ENLIGHTENED_LEVEL, *PDLP_APP_OP_ENLIGHTENED_LEVEL;
```


## <a name="members"></a><span data-ttu-id="aecd9-106">Members</span><span class="sxs-lookup"><span data-stu-id="aecd9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="aecd9-107">*Vorgang* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="aecd9-107">*Operation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aecd9-108">Ein Wert aus der [DlpActionType-Enumeration,](endpointdlp-dlpactiontype.md) der den DLP-Endpunktaktionstyp angibt.</span><span class="sxs-lookup"><span data-stu-id="aecd9-108">A value from the [DlpActionType](endpointdlp-dlpactiontype.md) enumeration specifying the endpoint DLP action type.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="aecd9-109">*AppEnforcementLevel* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="aecd9-109">*AppEnforcementLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aecd9-110">Ein Wert aus [DlpAppEnforceLevel,](endpointdlp-dlpappenforcelevel.md) der die Erzwingungsebene für den zugeordneten Endpunkt-DLP-Aktionstyp angibt.</span><span class="sxs-lookup"><span data-stu-id="aecd9-110">A value from the [DlpAppEnforceLevel](endpointdlp-dlpappenforcelevel.md) specifying the level of enforcement for the associated endpoint DLP action type.</span></span>

</dd> </dl>





## <a name="remarks"></a><span data-ttu-id="aecd9-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aecd9-111">Remarks</span></span>

<span data-ttu-id="aecd9-112">Übergeben Sie ein Array dieser Strukturen an [DlpInitializeEnforcementMode,](endpointdlp-dlpinitializeenforcementmode.md) um den Erzwingungsmodus für eine Reihe von Endpunkt-DLP-Vorgängen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="aecd9-112">Pass an array of these structures into [DlpInitializeEnforcementMode](endpointdlp-dlpinitializeenforcementmode.md) to set the enforcement mode for a set of endpoint DLP operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="aecd9-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aecd9-113">Requirements</span></span>



| <span data-ttu-id="aecd9-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aecd9-114">Requirement</span></span>          |    <span data-ttu-id="aecd9-115">Wert</span><span class="sxs-lookup"><span data-stu-id="aecd9-115">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aecd9-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aecd9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="aecd9-117">Windows 10, Version 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="aecd9-117">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |

