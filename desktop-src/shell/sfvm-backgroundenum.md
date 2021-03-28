---
description: 'Ermöglicht dem Rückruf Objekt, Enumeration in einem Hintergrund Thread anzufordern. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
title: SFVM_BACKGROUNDENUM Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8428179c-2ec9-4979-9281-c2439e58beb6
api_name:
- SFVM_BACKGROUNDENUM
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: cb0b85abb3ca6830610a35502f55c0867a5ffbf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994919"
---
# <a name="sfvm_backgroundenum-message"></a><span data-ttu-id="f5a63-104">Sfvm- \_ backgroundenum-Meldung</span><span class="sxs-lookup"><span data-stu-id="f5a63-104">SFVM\_BACKGROUNDENUM message</span></span>

<span data-ttu-id="f5a63-105">Ermöglicht dem Rückruf Objekt, Enumeration in einem Hintergrund Thread anzufordern.</span><span class="sxs-lookup"><span data-stu-id="f5a63-105">Allows the callback object to request enumeration on a background thread.</span></span> <span data-ttu-id="f5a63-106">Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f5a63-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++

                SFVM_BACKGROUNDENUM

            
```



## <a name="parameters"></a><span data-ttu-id="f5a63-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5a63-107">Parameters</span></span>

<span data-ttu-id="f5a63-108">Diese Nachricht weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="f5a63-108">This message has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5a63-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f5a63-109">Remarks</span></span>

<span data-ttu-id="f5a63-110">Geben Sie als Antwort auf diese Benachrichtigung S \_ OK ein, um die hintergrundenumeration zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="f5a63-110">In response to this notification, return S\_OK to enable background enumeration.</span></span> <span data-ttu-id="f5a63-111">Standardmäßig wird das Systemordner Objekt die Animation "Taschenlampe" anzeigen, während die Enumeration stattfindet.</span><span class="sxs-lookup"><span data-stu-id="f5a63-111">By default, the system folder object will display the "flashlight" animation while the enumeration is taking place.</span></span> <span data-ttu-id="f5a63-112">Um eine benutzerdefinierte Animation anzugeben, behandeln Sie [**sfvm \_ getanimation**](sfvm-getanimation.md).</span><span class="sxs-lookup"><span data-stu-id="f5a63-112">To specify a custom animation, handle [**SFVM\_GETANIMATION**](sfvm-getanimation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f5a63-113">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="f5a63-113">Requirements</span></span>



| <span data-ttu-id="f5a63-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f5a63-114">Requirement</span></span> | <span data-ttu-id="f5a63-115">Wert</span><span class="sxs-lookup"><span data-stu-id="f5a63-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f5a63-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f5a63-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f5a63-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5a63-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f5a63-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f5a63-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f5a63-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5a63-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f5a63-120">Header</span><span class="sxs-lookup"><span data-stu-id="f5a63-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5a63-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5a63-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
