---
description: 'Ermöglicht dem Rückruf Objekt das Hinzufügen von Schaltflächen zur Symbolleiste. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
title: SFVM_GETBUTTONINFO Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 983652ed-7309-46aa-a6c9-7516411ba5ac
api_name:
- SFVM_GETBUTTONINFO
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d0db40f7c1f54cd13d54765ba34a8eab31246809
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980225"
---
# <a name="sfvm_getbuttoninfo-message"></a><span data-ttu-id="248e8-104">Sfvm \_ getbuttoninfo-Meldung</span><span class="sxs-lookup"><span data-stu-id="248e8-104">SFVM\_GETBUTTONINFO message</span></span>

<span data-ttu-id="248e8-105">Ermöglicht dem Rückruf Objekt das Hinzufügen von Schaltflächen zur Symbolleiste.</span><span class="sxs-lookup"><span data-stu-id="248e8-105">Allows the callback object to add buttons to the toolbar.</span></span> <span data-ttu-id="248e8-106">Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.</span><span class="sxs-lookup"><span data-stu-id="248e8-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETBUTTONINFO 

    lParam = (LPARAM)(LPTBINFO) ptbinfo;

            
```



## <a name="parameters"></a><span data-ttu-id="248e8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="248e8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="248e8-108">*ptbinfo* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="248e8-108">*ptbinfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="248e8-109">Die Adresse einer [**tbinfo**](/windows/desktop/api/Shlobj/ns-shlobj-tbinfo) -Struktur, die die Anzahl der Schaltflächen angibt, und wie Sie der Symbolleiste hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="248e8-109">The address of a [**TBINFO**](/windows/desktop/api/Shlobj/ns-shlobj-tbinfo) structure that specifies the number of buttons and how they are to be added to the toolbar.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="248e8-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="248e8-110">Remarks</span></span>

<span data-ttu-id="248e8-111">Schaltflächen können den standardmäßigen Systemordner Ansichts Objekt-Schaltflächen angefügt oder vorangestellt werden oder anstelle der Standard Schaltflächen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="248e8-111">Buttons can be appended or prepended to the standard system folder view object buttons, or be displayed in place of the standard buttons.</span></span> <span data-ttu-id="248e8-112">Auf diese Nachricht folgt eine [**sfvm- \_ getButtons**](sfvm-getbuttons.md) -Meldung, die die Informationen zu den Details der Schaltfläche abruft.</span><span class="sxs-lookup"><span data-stu-id="248e8-112">This message is followed by a [**SFVM\_GETBUTTONS**](sfvm-getbuttons.md) message that retrieves the information concerning the button specifics.</span></span>

## <a name="requirements"></a><span data-ttu-id="248e8-113">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="248e8-113">Requirements</span></span>



| <span data-ttu-id="248e8-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="248e8-114">Requirement</span></span> | <span data-ttu-id="248e8-115">Wert</span><span class="sxs-lookup"><span data-stu-id="248e8-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="248e8-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="248e8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="248e8-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="248e8-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="248e8-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="248e8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="248e8-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="248e8-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="248e8-120">Header</span><span class="sxs-lookup"><span data-stu-id="248e8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="248e8-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="248e8-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
