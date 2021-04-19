---
title: Itspubplugin-PluginName-Eigenschaft
description: Ruft den Namen des Plug-ins ab.
ms.assetid: c1ea46b6-fac6-4140-a278-cb04ee9af739
ms.tgt_platform: multiple
keywords:
- PluginName-Eigenschaft Remotedesktopdienste
- PluginName-Eigenschaft Remotedesktopdienste, itspubplugin-Schnittstelle
- Itspubplugin-Schnittstelle Remotedesktopdienste, PluginName-Eigenschaft
topic_type:
- apiref
api_name:
- ItsPubPlugin.pluginName
- ItsPubPlugin.get_pluginName
api_location:
- Cpubplugin.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f5aa6ff6659047e9be48fd7b7a41f652c5cfd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339993"
---
# <a name="itspubpluginpluginname-property"></a><span data-ttu-id="6c476-106">Itspubplugin::p luginname-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6c476-106">ItsPubPlugin::pluginName property</span></span>

<span data-ttu-id="6c476-107">Ruft den Namen des Plug-ins ab.</span><span class="sxs-lookup"><span data-stu-id="6c476-107">Retrieves the name of the plug-in.</span></span>

<span data-ttu-id="6c476-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="6c476-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c476-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c476-109">Syntax</span></span>


```C++
HRESULT get_pluginName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="6c476-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="6c476-110">Property value</span></span>

<span data-ttu-id="6c476-111">Ein Zeiger auf eine **BSTR** -Variable, die den Namen des Plug-ins erhält.</span><span class="sxs-lookup"><span data-stu-id="6c476-111">A pointer to a **BSTR** variable to receive the name of the plug-in.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c476-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c476-112">Requirements</span></span>



| <span data-ttu-id="6c476-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c476-113">Requirement</span></span> | <span data-ttu-id="6c476-114">Wert</span><span class="sxs-lookup"><span data-stu-id="6c476-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c476-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6c476-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6c476-116">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6c476-116">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="6c476-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6c476-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6c476-118">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6c476-118">Windows Server 2008 R2</span></span><br/>                                                         |
| <span data-ttu-id="6c476-119">IDL</span><span class="sxs-lookup"><span data-stu-id="6c476-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6c476-120"><dt>Cpubplugin. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6c476-120"><dt>Cpubplugin.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c476-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c476-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c476-122">**Itspubplugin**</span><span class="sxs-lookup"><span data-stu-id="6c476-122">**ItsPubPlugin**</span></span>](/windows/desktop/api/tspubplugincom/nn-tspubplugincom-itspubplugin)
</dt> </dl>

 

 





