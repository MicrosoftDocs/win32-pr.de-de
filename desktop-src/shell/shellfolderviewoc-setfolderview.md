---
description: Leitet die Ereignisse des angegebenen shellfolderview-Objekts an den entsprechenden shellfolderviewoc-Ereignishandler weiter.
ms.assetid: 44a2a0a5-aa87-43ae-b4ea-0d301fcb8464
title: Shellfolderviewoc. setfolderview-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderViewOC.SetFolderView
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 7d331fadbd8abae62ee896caec772d84d079f88d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980424"
---
# <a name="shellfolderviewocsetfolderview-method"></a><span data-ttu-id="6d973-103">Shellfolderviewoc. setfolderview-Methode</span><span class="sxs-lookup"><span data-stu-id="6d973-103">ShellFolderViewOC.SetFolderView method</span></span>

<span data-ttu-id="6d973-104">Leitet die Ereignisse des angegebenen [**shellfolderview**](shellfolderview.md) -Objekts an den entsprechenden [**shellfolderviewoc**](shellfolderviewoc-object.md) -Ereignishandler weiter.</span><span class="sxs-lookup"><span data-stu-id="6d973-104">Forwards the events of the specified [**ShellFolderView**](shellfolderview.md) object to the corresponding [**ShellFolderViewOC**](shellfolderviewoc-object.md) event handler.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d973-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d973-105">Syntax</span></span>


```JScript
iRetVal = ShellFolderViewOC.SetFolderView(
  oShellFolderView
)
```



## <a name="parameters"></a><span data-ttu-id="6d973-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d973-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d973-107">*oshellfolderview* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6d973-107">*oShellFolderView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d973-108">Typ: \**[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) \** _</span><span class="sxs-lookup"><span data-stu-id="6d973-108">Type: \**[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\** _</span></span>

<span data-ttu-id="6d973-109">Ein [_ *shellfolderview* \*](shellfolderview.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="6d973-109">A [_ *ShellFolderView*\*](shellfolderview.md) object.</span></span> <span data-ttu-id="6d973-110">Die [**enumdone**](shellfolderviewoc-enumdone.md) -und [**SelectionChanged**](shellfolderview-selectionchanged.md) -Ereignisse werden an den entsprechenden [**shellfolderviewoc**](shellfolderviewoc-object.md) -Ereignishandler weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="6d973-110">Its [**EnumDone**](shellfolderviewoc-enumdone.md) and [**SelectionChanged**](shellfolderview-selectionchanged.md) events will be forwarded to the corresponding [**ShellFolderViewOC**](shellfolderviewoc-object.md) event handler.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6d973-111">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="6d973-111">Requirements</span></span>



| <span data-ttu-id="6d973-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6d973-112">Requirement</span></span> | <span data-ttu-id="6d973-113">Wert</span><span class="sxs-lookup"><span data-stu-id="6d973-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d973-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6d973-114">Minimum supported client</span></span><br/> | <span data-ttu-id="6d973-115">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6d973-115">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6d973-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6d973-116">Minimum supported server</span></span><br/> | <span data-ttu-id="6d973-117">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6d973-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="6d973-118">Header</span><span class="sxs-lookup"><span data-stu-id="6d973-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d973-119"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d973-119"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="6d973-120">IDL</span><span class="sxs-lookup"><span data-stu-id="6d973-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6d973-121"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6d973-121"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="6d973-122">DLL</span><span class="sxs-lookup"><span data-stu-id="6d973-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d973-123"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="6d973-123"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
