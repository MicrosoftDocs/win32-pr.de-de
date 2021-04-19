---
title: Iremotedesktopclienttouchpointer-aktivierte Eigenschaft
description: Gibt an, ob die Funktion für den Fingerabdruck für das Client Steuerelement der RDP-App aktiviert ist.
ms.assetid: f1e2f2f2-1b96-4c5a-b0dd-fd57627c5ec3
ms.tgt_platform: multiple
keywords:
- Aktivierte Eigenschaften Remotedesktopdienste
- Aktivierte Eigenschaften Remotedesktopdienste, iremotedesktopclienttouchpointer-Schnittstelle
- Iremotedesktopclienttouchpointer-Schnittstelle Remotedesktopdienste, aktivierte Eigenschaft
topic_type:
- apiref
api_name:
- IRemoteDesktopClientTouchPointer.Enabled
- IRemoteDesktopClientTouchPointer.get_Enabled
- IRemoteDesktopClientTouchPointer.put_Enabled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdd534a9f8ec77903f196bbdfa10e1823a18dff4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342636"
---
# <a name="iremotedesktopclienttouchpointerenabled-property"></a><span data-ttu-id="b6eca-106">Iremotedesktopclienttouchpointer:: aktivierte Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b6eca-106">IRemoteDesktopClientTouchPointer::Enabled property</span></span>

<span data-ttu-id="b6eca-107">Gibt an, ob die Funktion für den Fingerabdruck für das Client Steuerelement der RDP-App aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b6eca-107">Whether the touch pointer feature is enabled on the RDP app container client control.</span></span>

<span data-ttu-id="b6eca-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="b6eca-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6eca-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6eca-109">Syntax</span></span>


```C++
HRESULT put_Enabled(
  [in]          VARIANT_BOOL Enabled
);

HRESULT get_Enabled(
  [out, retval] VARIANT_BOOL *Enabled
);
```



## <a name="property-value"></a><span data-ttu-id="b6eca-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b6eca-110">Property value</span></span>

<span data-ttu-id="b6eca-111">**true** , wenn die Berührungs Zeiger Funktion aktiviert ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="b6eca-111">**true** if the touch pointer feature is enabled; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6eca-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6eca-112">Requirements</span></span>



| <span data-ttu-id="b6eca-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6eca-113">Requirement</span></span> | <span data-ttu-id="b6eca-114">Wert</span><span class="sxs-lookup"><span data-stu-id="b6eca-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6eca-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b6eca-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b6eca-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b6eca-116">Windows 8</span></span><br/>                                                                                |
| <span data-ttu-id="b6eca-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b6eca-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b6eca-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b6eca-118">Windows Server 2012</span></span><br/>                                                                      |
| <span data-ttu-id="b6eca-119">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="b6eca-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="b6eca-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6eca-120"><dt>MsTscAx.dll</dt></span></span> </dl>              |
| <span data-ttu-id="b6eca-121">DLL</span><span class="sxs-lookup"><span data-stu-id="b6eca-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6eca-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6eca-122"><dt>MsTscAx.dll</dt></span></span> </dl>              |
| <span data-ttu-id="b6eca-123">IID</span><span class="sxs-lookup"><span data-stu-id="b6eca-123">IID</span></span><br/>                      | <span data-ttu-id="b6eca-124">IID \_ iremotedesktopclienttouchpointer ist als 260ec22d-8cbc-44b5-9e88-2a37f 6c93ae9 definiert.</span><span class="sxs-lookup"><span data-stu-id="b6eca-124">IID\_IRemoteDesktopClientTouchPointer is defined as 260EC22D-8CBC-44B5-9E88-2A37F6C93AE9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b6eca-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6eca-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6eca-126">**Iremotedesktopclienttouchpointer**</span><span class="sxs-lookup"><span data-stu-id="b6eca-126">**IRemoteDesktopClientTouchPointer**</span></span>](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclienttouchpointer)
</dt> </dl>

 

