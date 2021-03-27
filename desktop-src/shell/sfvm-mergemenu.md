---
description: 'Ermöglicht dem Rückruf Objekt das Zusammenführen von Menü Elementen in den Windows-Explorer-Menüs. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
title: SFVM_MERGEMENU Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 59bb99a3-9a5a-4ea5-9830-b04d7d886b3f
api_name:
- SFVM_MERGEMENU
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5cf95a7576c15ab1c3e64ebe55e244feffa6d86d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980832"
---
# <a name="sfvm_mergemenu-message"></a><span data-ttu-id="3e116-104">Sfvm \_ MergeMenu-Meldung</span><span class="sxs-lookup"><span data-stu-id="3e116-104">SFVM\_MERGEMENU message</span></span>

<span data-ttu-id="3e116-105">Ermöglicht dem Rückruf Objekt das Zusammenführen von Menü Elementen in den Windows-Explorer-Menüs.</span><span class="sxs-lookup"><span data-stu-id="3e116-105">Allows the callback object to merge menu items into the Windows Explorer menus.</span></span> <span data-ttu-id="3e116-106">Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.</span><span class="sxs-lookup"><span data-stu-id="3e116-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_MERGEMENU 

    lParam = (LPARAM)(LPQCMINFO) pInfo;

            
```



## <a name="parameters"></a><span data-ttu-id="3e116-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e116-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e116-108">*pinfo* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3e116-108">*pInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e116-109">Eine [**qcminfo**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) -Struktur, die die Informationen enthält, die erforderlich sind, um die Elemente im Menü zusammenzuführen.</span><span class="sxs-lookup"><span data-stu-id="3e116-109">A [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) structure containing the information needed to merge the items into the menu.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e116-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3e116-110">Remarks</span></span>

<span data-ttu-id="3e116-111">Diese Nachricht dient im Wesentlichen dem gleichen Zweck wie [**ishellbrowser:: insertmenussb**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb) und [**ishellbrowser:: setmenusb**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) in einer benutzerdefinierten Ordneransicht.</span><span class="sxs-lookup"><span data-stu-id="3e116-111">This message serves essentially the same purpose as the [**IShellBrowser::InsertMenusSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb) and [**IShellBrowser::SetMenuSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) in a custom folder view.</span></span> <span data-ttu-id="3e116-112">Weitere Informationen finden Sie im Abschnitt *Verwenden von ishellbrowser zum kommunizieren mit Windows-Explorer* unter [Implementieren einer Ordneransicht](../lwef/nse-folderview.md) .</span><span class="sxs-lookup"><span data-stu-id="3e116-112">See the *Using IShellBrowser to Communicate with Windows Explorer* section of [Implementing a Folder View](../lwef/nse-folderview.md) for further discussion.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e116-113">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="3e116-113">Requirements</span></span>



| <span data-ttu-id="3e116-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3e116-114">Requirement</span></span> | <span data-ttu-id="3e116-115">Wert</span><span class="sxs-lookup"><span data-stu-id="3e116-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3e116-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3e116-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3e116-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3e116-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3e116-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3e116-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3e116-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3e116-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3e116-120">Header</span><span class="sxs-lookup"><span data-stu-id="3e116-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e116-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e116-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
