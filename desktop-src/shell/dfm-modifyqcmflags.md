---
description: 'Ermöglicht dem Rückruf das Ändern der \_ an IContextMenu:: querycontextmenu übergebenen cfm xxx-Werte.'
title: DFM_MODIFYQCMFLAGS Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2c87e14d-4cf4-425d-a5fe-9dc7530f0e59
api_name:
- DFM_MODIFYQCMFLAGS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ff90cfb0e0297e7d3276f00f314fce865920663a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862123"
---
# <a name="dfm_modifyqcmflags-message"></a><span data-ttu-id="a77b7-103">DFM- \_ modifyqcmflags-Meldung</span><span class="sxs-lookup"><span data-stu-id="a77b7-103">DFM\_MODIFYQCMFLAGS message</span></span>

<span data-ttu-id="a77b7-104">Ermöglicht dem Rückruf das Ändern der \_ an [**IContextMenu:: querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)übergebenen cfm xxx-Werte.</span><span class="sxs-lookup"><span data-stu-id="a77b7-104">Allows the callback to modify the CFM\_XXX values passed to [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span></span>


```C++
DFM_MODIFYQCMFLAGS

    lParam = (LPARAM)(UINT) *puNewFlags;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a><span data-ttu-id="a77b7-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="a77b7-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a77b7-106">*punewflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a77b7-106">*puNewFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a77b7-107">Ein Zeiger auf die neuen Flagwerte.</span><span class="sxs-lookup"><span data-stu-id="a77b7-107">A pointer to the new flag values.</span></span>

</dd> <dt>

<span data-ttu-id="a77b7-108">*uFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a77b7-108">*uFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a77b7-109">Flags, die angeben, wie das Kontextmenü geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a77b7-109">Flags that specify how the context menu can be changed.</span></span> <span data-ttu-id="a77b7-110">Dieser Parameter verwendet die CMF \_ xxx-Werte, die in [**IContextMenu:: querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="a77b7-110">This parameter uses the CMF\_XXX values described in [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a77b7-111">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a77b7-111">Requirements</span></span>



| <span data-ttu-id="a77b7-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a77b7-112">Requirement</span></span> | <span data-ttu-id="a77b7-113">Wert</span><span class="sxs-lookup"><span data-stu-id="a77b7-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a77b7-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a77b7-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a77b7-115">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a77b7-115">Windows 7 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a77b7-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a77b7-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a77b7-117">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a77b7-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a77b7-118">Header</span><span class="sxs-lookup"><span data-stu-id="a77b7-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="a77b7-119"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="a77b7-119"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




