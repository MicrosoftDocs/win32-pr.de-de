---
description: 'Ermöglicht dem Rückruf Objekt anzugeben, dass eine Animation angezeigt werden soll, während Elemente in einem Hintergrund Thread aufgelistet werden. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
ms.assetid: 6f8b3894-f08f-4ebf-a645-87869e7d1b20
title: SFVM_GETANIMATION Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60e4281689556e8315da7a9550fd69acc1a327a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131949"
---
# <a name="sfvm_getanimation-message"></a><span data-ttu-id="c7037-104">Sfvm- \_ getanimationsmeldung</span><span class="sxs-lookup"><span data-stu-id="c7037-104">SFVM\_GETANIMATION message</span></span>

<span data-ttu-id="c7037-105">Ermöglicht dem Rückruf Objekt anzugeben, dass eine Animation angezeigt werden soll, während Elemente in einem Hintergrund Thread aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="c7037-105">Allows the callback object to specify that an animation be displayed while items are enumerated on a background thread.</span></span> <span data-ttu-id="c7037-106">Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.</span><span class="sxs-lookup"><span data-stu-id="c7037-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETANIMATION 

    wParam = (WPARAM)(HINSTANCE*) phinst;

    lParam = (LPARAM)(WCHAR*) pwszName;

            
```



## <a name="parameters"></a><span data-ttu-id="c7037-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7037-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7037-108">*phinst* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c7037-108">*phinst* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7037-109">Der Instanzhandle des Moduls, aus dem die Ressource geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c7037-109">The instance handle of the module that the resource should be loaded from.</span></span>

</dd> <dt>

<span data-ttu-id="c7037-110">*pwszName* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c7037-110">*pwszName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7037-111">Ein Zeiger auf eine NULL-terminierte Unicode-Zeichenfolge, die den Pfad der AVI-Datei oder den Namen einer AVI-Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="c7037-111">A pointer to a null-terminated Unicode string containing the path of the .avi file or the name of an AVI resource.</span></span> <span data-ttu-id="c7037-112">Alternativ kann dieser Parameter aus dem Ressourcen Bezeichner im nieder wertigen Wort und 0 im höherwertigen Wort bestehen.</span><span class="sxs-lookup"><span data-stu-id="c7037-112">Alternatively, this parameter can consist of the resource identifier in the low-order word and 0 in the high-order word.</span></span> <span data-ttu-id="c7037-113">Verwenden Sie das [**makeintresource**](/windows/win32/api/winuser/nf-winuser-makeintresourcea) -Makro, um diesen Wert zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c7037-113">To create this value, use the [**MAKEINTRESOURCE**](/windows/win32/api/winuser/nf-winuser-makeintresourcea) macro.</span></span> <span data-ttu-id="c7037-114">Das-Steuerelement lädt die Ressource aus dem durch hInst angegebenen Modul.</span><span class="sxs-lookup"><span data-stu-id="c7037-114">The control loads the resource from the module specified by hinst.</span></span> <span data-ttu-id="c7037-115">Eine AVI-Ressource muss den Typ "AVI" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c7037-115">An AVI resource must have the "AVI" type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7037-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7037-116">Remarks</span></span>

<span data-ttu-id="c7037-117">Standardmäßig zeigt das Systemordner Ansicht-Objekt während einer hintergrundenumeration die "Taschen Taschen"-Animation an.</span><span class="sxs-lookup"><span data-stu-id="c7037-117">By default, the system folder view object displays the "flashlight" animation during a background enumeration.</span></span>

<span data-ttu-id="c7037-118">*phinst* und *pwszName* werden mit einer [**\_ geöffneten ACM**](../controls/acm-open.md) -Meldung an das [Animations Steuer](../controls/animation-control-overview.md) Element übergeben.</span><span class="sxs-lookup"><span data-stu-id="c7037-118">*phinst* and *pwszName* will be passed to the [animation control](../controls/animation-control-overview.md) with an [**ACM\_OPEN**](../controls/acm-open.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7037-119">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c7037-119">Requirements</span></span>



| <span data-ttu-id="c7037-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c7037-120">Requirement</span></span> | <span data-ttu-id="c7037-121">Wert</span><span class="sxs-lookup"><span data-stu-id="c7037-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c7037-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c7037-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c7037-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c7037-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c7037-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c7037-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c7037-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c7037-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c7037-126">Header</span><span class="sxs-lookup"><span data-stu-id="c7037-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7037-127"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7037-127"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
