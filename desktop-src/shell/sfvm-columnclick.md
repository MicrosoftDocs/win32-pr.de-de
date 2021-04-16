---
description: 'Benachrichtigt das Rückruf Objekt, dass der Benutzer auf einen Spaltenheader geklickt hat, um die Liste der Objekte in der Ordneransicht zu sortieren. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
title: SFVM_COLUMNCLICK Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 351be842-6ea5-4223-8162-0e6c4e6a5afb
api_name:
- SFVM_COLUMNCLICK
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bca80554e25378af1c078a36a02222390b771874
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485515"
---
# <a name="sfvm_columnclick-message"></a><span data-ttu-id="e6303-104">Sfvm- \_ ColumnClick-Nachricht</span><span class="sxs-lookup"><span data-stu-id="e6303-104">SFVM\_COLUMNCLICK message</span></span>

<span data-ttu-id="e6303-105">Benachrichtigt das Rückruf Objekt, dass der Benutzer auf einen Spaltenheader geklickt hat, um die Liste der Objekte in der Ordneransicht zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="e6303-105">Notifies the callback object that the user has clicked a column header to sort the list of objects in the folder view.</span></span> <span data-ttu-id="e6303-106">Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.</span><span class="sxs-lookup"><span data-stu-id="e6303-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_COLUMNCLICK 

    wParam = (WPARAM)(UINT)iColumn;

            
```



## <a name="parameters"></a><span data-ttu-id="e6303-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6303-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6303-108">*icolumn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e6303-108">*iColumn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6303-109">Der Index der Spalte, auf die geklickt wurde.</span><span class="sxs-lookup"><span data-stu-id="e6303-109">The index of the column that was clicked.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e6303-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6303-110">Remarks</span></span>

<span data-ttu-id="e6303-111">Als Antwort auf diese Benachrichtigung sollten Sie S OK zurückgeben, \_ um die Liste selbst neu anzuordnen.</span><span class="sxs-lookup"><span data-stu-id="e6303-111">In response to this notification, you should return S\_OK to rearrange the list yourself.</span></span> <span data-ttu-id="e6303-112">Wenn das Ansichts Objekt des System Ordners die Liste neu anordnen soll, geben Sie "false" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="e6303-112">To have the system folder view object rearrange the list, return S\_FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6303-113">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="e6303-113">Requirements</span></span>



| <span data-ttu-id="e6303-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6303-114">Requirement</span></span> | <span data-ttu-id="e6303-115">Wert</span><span class="sxs-lookup"><span data-stu-id="e6303-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e6303-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e6303-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e6303-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6303-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e6303-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e6303-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e6303-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6303-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e6303-120">Header</span><span class="sxs-lookup"><span data-stu-id="e6303-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6303-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6303-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
