---
description: Ermöglicht dem Rückruf, dem Menü Elemente hinzuzufügen.
title: DFM_MERGECONTEXTMENU Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2fd779ac-7dd6-4b81-86dc-8930db27ae59
api_name:
- DFM_MERGECONTEXTMENU
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d469f9764b5e377e5f47227d3414f246441d3505
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977273"
---
# <a name="dfm_mergecontextmenu-message"></a><span data-ttu-id="4a6dc-103">DFM- \_ mergecontextmenu-Meldung</span><span class="sxs-lookup"><span data-stu-id="4a6dc-103">DFM\_MERGECONTEXTMENU message</span></span>

<span data-ttu-id="4a6dc-104">Ermöglicht dem Rückruf, dem Menü Elemente hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4a6dc-104">Allows the callback to add items to the menu.</span></span>


```C++
DFM_MERGECONTEXTMENU

    lParam = (LPARAM)(LPQCMINFO) pqcminfo;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a><span data-ttu-id="4a6dc-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a6dc-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a6dc-106">*pqcminfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a6dc-106">*pqcminfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a6dc-107">Ein Zeiger auf eine [**qcminfo**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) -Struktur, die die Informationen enthält, die in der Zusammenführung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a6dc-107">A pointer to a [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) structure containing the information used in the merge.</span></span>

</dd> <dt>

<span data-ttu-id="4a6dc-108">*uFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a6dc-108">*uFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a6dc-109">Flags, die angeben, wie das Kontextmenü geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="4a6dc-109">Flags specifying how the context menu can be changed.</span></span> <span data-ttu-id="4a6dc-110">Dieser Parameter verwendet die CMF-Werte, die \_ \* in [**IContextMenu:: querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="4a6dc-110">This parameter uses the CMF\_\* values described in [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4a6dc-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a6dc-111">Remarks</span></span>

<span data-ttu-id="4a6dc-112">Wenn dem Kontextmenü Elemente hinzugefügt werden, müssen Sie mit Routinen unterstützt werden, die entsprechend reagieren, wenn eines dieser Elemente mithilfe von [**DFM \_ InvokeCommand**](dfm-invokecommand.md)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4a6dc-112">If items are added to the context menu, they must be supported with routines that respond appropriately when one of those items is invoked using [**DFM\_INVOKECOMMAND**](dfm-invokecommand.md).</span></span>

<span data-ttu-id="4a6dc-113">Diese Nachricht wird entweder an die Rückruffunktion oder an das Rückruf Objekt gesendet, je nachdem, wie das Standardkontext Menü-Objekt implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="4a6dc-113">This message is sent to either the callback function or the callback object depending on how the default context menu object is implemented.</span></span> <span data-ttu-id="4a6dc-114">Es gibt zwei APIs für die Implementierung, [**cdeffoldermenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**shkreatedefaultcontextmenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="4a6dc-114">There are two APIs for its implementation, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="4a6dc-115">[**DFM \_ Invokecommandex**](dfm-invokecommandex.md) ist eine erweiterte Version dieser Nachricht und bietet weitere Informationen für den Rückruf.</span><span class="sxs-lookup"><span data-stu-id="4a6dc-115">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="4a6dc-116">Verwenden Sie **DFM \_ invokecommandex** , wenn die zusätzlichen Informationen, die von dieser Schnittstelle bereitgestellt werden, in der Implementierung benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="4a6dc-116">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a6dc-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="4a6dc-117">Requirements</span></span>



| <span data-ttu-id="4a6dc-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a6dc-118">Requirement</span></span> | <span data-ttu-id="4a6dc-119">Wert</span><span class="sxs-lookup"><span data-stu-id="4a6dc-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4a6dc-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4a6dc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4a6dc-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4a6dc-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4a6dc-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4a6dc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4a6dc-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4a6dc-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4a6dc-124">Header</span><span class="sxs-lookup"><span data-stu-id="4a6dc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a6dc-125"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a6dc-125"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




