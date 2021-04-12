---
description: Die autoreconnetct-Eigenschaft des-Objekts "Swap-Aktualisierungs Programm" ist ein boolescher Wert, der angibt, ob das Aktualisierungs Programm automatisch erneut eine Verbindung mit einem Remote Anbieter herstellt, wenn die Verbindung getrennt ist.
ms.assetid: 3be24128-8a35-44b0-befd-8b8937eff1b7
ms.tgt_platform: multiple
title: Taubemaktusher. autoreconnetct-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.AutoReconnect
- ISWbemRefresher.AutoReconnect
- ISWbemRefresher.get_AutoReconnect
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4faa02a4a77409bb8b1813ee433c326d1c45d1bd
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351319"
---
# <a name="swbemrefresherautoreconnect-property"></a><span data-ttu-id="c2838-103">' Swap. autoreconnetct '-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c2838-103">SWbemRefresher.AutoReconnect property</span></span>

<span data-ttu-id="c2838-104">Die **autoreconnetct** -Eigenschaft des-Objekts " [**Swap**](swbemrefresher.md) -Aktualisierungs Programm" ist ein boolescher Wert, der angibt, ob das Aktualisierungs Programm automatisch erneut eine Verbindung mit einem Remote Anbieter herstellt, wenn die Verbindung getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="c2838-104">The **AutoReconnect** property of the [**SWbemRefresher**](swbemrefresher.md) object is a Boolean value that indicates whether the refresher automatically reconnects to a remote provider if the connection is broken.</span></span>

<span data-ttu-id="c2838-105">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="c2838-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="c2838-106">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c2838-106">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2838-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2838-107">Syntax</span></span>


```VB
SWbemRefresher.AutoReconnect As Boolean
```



## <a name="property-value"></a><span data-ttu-id="c2838-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c2838-108">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="c2838-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2838-109">Remarks</span></span>

<span data-ttu-id="c2838-110">Das Ändern dieser Eigenschaft wirkt sich nur auf Objekte im Aktualisierungs Programm aus, die von einem Hochleistungs Anbieter unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="c2838-110">Modifying this property affects only objects in the refresher that are backed by a high-performance provider.</span></span> <span data-ttu-id="c2838-111">Wenn es sich bei dem Anbieter nicht um einen Hochleistungs Anbieter handelt, hat das Festlegen der **autoreconnetct** -Eigenschaft auf **true** keine Auswirkung, da das Objekt " [**Swap**](swbemrefresher.md) -Aktualisierungs Programm" nie erneut eine Verbindung herstellt.</span><span class="sxs-lookup"><span data-stu-id="c2838-111">If the provider is not a high-performance provider, then setting the **AutoReconnect** property to **TRUE** has no effect because the [**SWbemRefresher**](swbemrefresher.md) object never reconnects.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2838-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2838-112">Requirements</span></span>



| <span data-ttu-id="c2838-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2838-113">Requirement</span></span> | <span data-ttu-id="c2838-114">Wert</span><span class="sxs-lookup"><span data-stu-id="c2838-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2838-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c2838-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c2838-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c2838-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c2838-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c2838-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c2838-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c2838-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c2838-119">Header</span><span class="sxs-lookup"><span data-stu-id="c2838-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2838-120"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2838-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c2838-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="c2838-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="c2838-122"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c2838-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c2838-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c2838-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2838-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2838-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c2838-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="c2838-125">CLSID</span></span><br/>                    | <span data-ttu-id="c2838-126">CLSID- \_ Austauschprogramm</span><span class="sxs-lookup"><span data-stu-id="c2838-126">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="c2838-127">IID</span><span class="sxs-lookup"><span data-stu-id="c2838-127">IID</span></span><br/>                      | <span data-ttu-id="c2838-128">IID \_ iswbemfreshsher</span><span class="sxs-lookup"><span data-stu-id="c2838-128">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="c2838-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2838-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2838-130">**Swap-Aktualisierungs Programm**</span><span class="sxs-lookup"><span data-stu-id="c2838-130">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




