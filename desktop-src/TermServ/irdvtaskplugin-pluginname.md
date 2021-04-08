---
title: "\"Undvtaskplugin PluginName\"-Eigenschaft (tspubplugincom. h)"
description: Enthält den anzeigen amen des Task-Agents.
ms.assetid: 6f414270-e90b-4075-80fe-f918acbdd205
ms.tgt_platform: multiple
keywords:
- PluginName-Eigenschaft Remotedesktopdienste
- PluginName-Eigenschaft Remotedesktopdienste, undvtaskplugin-Schnittstelle
- Undvtaskplugin-Schnittstelle Remotedesktopdienste, PluginName-Eigenschaft
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.PluginName
- IRDVTaskPlugin.get_PluginName
api_location:
- tspubplugincom.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0262472e37a8ff3e5b9bb153d2e94f4e52029b14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742073"
---
# <a name="irdvtaskpluginpluginname-property"></a><span data-ttu-id="d7f44-106">Undvtaskplugin::P luginname-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d7f44-106">IRDVTaskPlugin::PluginName property</span></span>

<span data-ttu-id="d7f44-107">Enthält den anzeigen amen des Task-Agents.</span><span class="sxs-lookup"><span data-stu-id="d7f44-107">Contains the display name of the task agent.</span></span> <span data-ttu-id="d7f44-108">Dieser Name wird nur zu Protokollierungs Zwecken verwendet.</span><span class="sxs-lookup"><span data-stu-id="d7f44-108">This name is used for logging purposes only.</span></span>

<span data-ttu-id="d7f44-109">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d7f44-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7f44-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7f44-110">Syntax</span></span>


```C++
HRESULT get_PluginName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="d7f44-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="d7f44-111">Property value</span></span>

<span data-ttu-id="d7f44-112">Der Anzeige Name des Task-Agents.</span><span class="sxs-lookup"><span data-stu-id="d7f44-112">The display name of the task agent.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7f44-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d7f44-113">Requirements</span></span>



| <span data-ttu-id="d7f44-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d7f44-114">Requirement</span></span> | <span data-ttu-id="d7f44-115">Wert</span><span class="sxs-lookup"><span data-stu-id="d7f44-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7f44-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d7f44-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d7f44-117">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="d7f44-117">Windows 7 Enterprise</span></span><br/>                                                             |
| <span data-ttu-id="d7f44-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d7f44-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d7f44-119">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d7f44-119">Windows Server 2008 R2</span></span><br/>                                                           |
| <span data-ttu-id="d7f44-120">Header</span><span class="sxs-lookup"><span data-stu-id="d7f44-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7f44-121"><dt>Tspubplugincom. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7f44-121"><dt>Tspubplugincom.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7f44-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d7f44-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7f44-123">**"Undvtaskplugin"**</span><span class="sxs-lookup"><span data-stu-id="d7f44-123">**IRDVTaskPlugin**</span></span>](irdvtaskplugin.md)
</dt> </dl>

 

 





