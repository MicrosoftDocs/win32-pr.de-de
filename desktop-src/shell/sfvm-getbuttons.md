---
description: 'Ermöglicht dem Rückruf Objekt die Angabe der Schaltflächen, die der Symbolleiste hinzugefügt werden sollen. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
ms.assetid: 0c0dbf61-9da9-4bcc-bad9-92c3f78db78f
title: SFVM_GETBUTTONS Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ad4ced86909c37ec77bf0470b46a40954f5b61c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866780"
---
# <a name="sfvm_getbuttons-message"></a><span data-ttu-id="6e2ca-104">Sfvm \_ getButtons-Meldung</span><span class="sxs-lookup"><span data-stu-id="6e2ca-104">SFVM\_GETBUTTONS message</span></span>

<span data-ttu-id="6e2ca-105">Ermöglicht dem Rückruf Objekt die Angabe der Schaltflächen, die der Symbolleiste hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6e2ca-105">Allows the callback object to specify the buttons to be added to the toolbar.</span></span> <span data-ttu-id="6e2ca-106">Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.</span><span class="sxs-lookup"><span data-stu-id="6e2ca-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETBUTTONS 

    wParam = (WPARAM)(DWORD) idCmdFirst,cbtnMax;

    lParam = (LPARAM)(LPTBBUTTON) pbtn;

            
```



## <a name="parameters"></a><span data-ttu-id="6e2ca-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e2ca-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e2ca-108">*idcmdfirst \_ cbtnmax* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6e2ca-108">*idCmdFirst\_cbtnMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e2ca-109">Enthält 2 16-Bit-Werte, die mit dem [**makewparam**](/windows/win32/api/winuser/nf-winuser-makewparam) -Makro in den-Parameter gepackt wurden.</span><span class="sxs-lookup"><span data-stu-id="6e2ca-109">Contains two 16-bit values packed into the parameter with the [**MAKEWPARAM**](/windows/win32/api/winuser/nf-winuser-makewparam) macro.</span></span> <span data-ttu-id="6e2ca-110">Das nieder wertige Wort enthält die anfängliche Befehls-ID.</span><span class="sxs-lookup"><span data-stu-id="6e2ca-110">The low-order word contains the initial command ID.</span></span> <span data-ttu-id="6e2ca-111">Das höchst wertige Wort enthält die Anzahl der hinzu zufügenden Schaltflächen, wie in der vorstehenden [**sfvm \_ getbuttoninfo**](sfvm-getbuttoninfo.md) -Meldung angegeben.</span><span class="sxs-lookup"><span data-stu-id="6e2ca-111">The high-order word contains the number of buttons to be added, as specified in the preceding [**SFVM\_GETBUTTONINFO**](sfvm-getbuttoninfo.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="6e2ca-112">*pbtn* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6e2ca-112">*pbtn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e2ca-113">Die Adresse eines Arrays von [**TBBUTTON**](/windows/win32/api/commctrl/ns-commctrl-tbbutton) -Strukturen, eines für jede Schaltfläche, die der Symbolleiste hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6e2ca-113">The address of an array of [**TBBUTTON**](/windows/win32/api/commctrl/ns-commctrl-tbbutton) structures, one for each button to be added to the toolbar.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6e2ca-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6e2ca-114">Remarks</span></span>

<span data-ttu-id="6e2ca-115">Dieser Nachricht wird eine [**sfvm \_ getbuttoninfo**](sfvm-getbuttoninfo.md) -Meldung vorangestellt.</span><span class="sxs-lookup"><span data-stu-id="6e2ca-115">This message is preceded by a [**SFVM\_GETBUTTONINFO**](sfvm-getbuttoninfo.md) message.</span></span> <span data-ttu-id="6e2ca-116">Das Rückruf Objekt muss diese Nachricht verarbeiten, um die Anzahl der Schaltflächen und die Position anzugeben, an der Sie auf der Symbolleiste platziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6e2ca-116">The callback object must handle that message to specify the number of buttons and where they are to be placed on the toolbar.</span></span> <span data-ttu-id="6e2ca-117">Abhängig davon, wie das Rückruf Objekt auf die **sfvm \_ getbuttoninfo** -Nachricht antwortet, werden die durch den *pbtn* -Parameter angegebenen Schaltflächen den Standard Schaltflächen des Systemordner Ansichts Objekts angefügt oder der Standardgruppe ersetzt.</span><span class="sxs-lookup"><span data-stu-id="6e2ca-117">Depending on how the callback object responds to the **SFVM\_GETBUTTONINFO** message, the buttons specified by *pbtn* parameter will be appended or prepended to the system folder view object's standard buttons, or replace the standard set.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e2ca-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="6e2ca-118">Requirements</span></span>



| <span data-ttu-id="6e2ca-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6e2ca-119">Requirement</span></span> | <span data-ttu-id="6e2ca-120">Wert</span><span class="sxs-lookup"><span data-stu-id="6e2ca-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6e2ca-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6e2ca-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6e2ca-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6e2ca-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6e2ca-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6e2ca-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6e2ca-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6e2ca-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6e2ca-125">Header</span><span class="sxs-lookup"><span data-stu-id="6e2ca-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e2ca-126"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e2ca-126"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
