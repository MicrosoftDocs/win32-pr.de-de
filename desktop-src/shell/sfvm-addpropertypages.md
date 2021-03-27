---
description: 'Ermöglicht dem Rückruf Objekt, eine Seite bereitzustellen, die dem Eigenschaften Blatt Eigenschaften des ausgewählten Objekts hinzugefügt werden kann. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
title: SFVM_ADDPROPERTYPAGES Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 54f67d0e-6089-4e75-a547-5313794e1512
api_name:
- SFVM_ADDPROPERTYPAGES
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e5f3e1f39b457bce105a8ac2b4be8b5939435615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994886"
---
# <a name="sfvm_addpropertypages-message"></a><span data-ttu-id="9eb58-104">Sfvm \_ addpropertypages-Meldung</span><span class="sxs-lookup"><span data-stu-id="9eb58-104">SFVM\_ADDPROPERTYPAGES message</span></span>

<span data-ttu-id="9eb58-105">Ermöglicht dem Rückruf Objekt, eine Seite bereitzustellen, die dem **Eigenschaften Blatt Eigenschaften** des ausgewählten Objekts hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="9eb58-105">Allows the callback object to provide a page to add to the **Properties** property sheet of the selected object.</span></span> <span data-ttu-id="9eb58-106">Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.</span><span class="sxs-lookup"><span data-stu-id="9eb58-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_ADDPROPERTYPAGES 

    lParam = (LPARAM)(SFVM_PROPPAGE_DATA*) pData;

            
```



## <a name="parameters"></a><span data-ttu-id="9eb58-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9eb58-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9eb58-108">*pData* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9eb58-108">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9eb58-109">Die Adresse einer [**sfvm- \_ PropPage- \_ Daten**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_proppage_data) Struktur.</span><span class="sxs-lookup"><span data-stu-id="9eb58-109">The address of a [**SFVM\_PROPPAGE\_DATA**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_proppage_data) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9eb58-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9eb58-110">Remarks</span></span>

<span data-ttu-id="9eb58-111">Diese Meldung dient im wesentlichen derselben Funktion wie [**ishellpropsheetext:: addPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages).</span><span class="sxs-lookup"><span data-stu-id="9eb58-111">This message serves essentially the same function as [**IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages).</span></span> <span data-ttu-id="9eb58-112">Weitere Erläuterungen finden Sie unter [Erstellen von Eigenschaften Blatt Handlern](propsheet-handlers.md) .</span><span class="sxs-lookup"><span data-stu-id="9eb58-112">See [Creating Property Sheet Handlers](propsheet-handlers.md) for further discussion.</span></span>

## <a name="requirements"></a><span data-ttu-id="9eb58-113">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="9eb58-113">Requirements</span></span>



| <span data-ttu-id="9eb58-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9eb58-114">Requirement</span></span> | <span data-ttu-id="9eb58-115">Wert</span><span class="sxs-lookup"><span data-stu-id="9eb58-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9eb58-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9eb58-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9eb58-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9eb58-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9eb58-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9eb58-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9eb58-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9eb58-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9eb58-120">Header</span><span class="sxs-lookup"><span data-stu-id="9eb58-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9eb58-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="9eb58-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
