---
description: Wird gesendet, um zu überprüfen, ob ein Menübefehl vorhanden ist.
title: DFM_VALIDATECMD Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 97ff3cdf-ed0c-4813-8d5a-b5141636d32c
api_name:
- DFM_VALIDATECMD
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5aa171f19d4d08c3ba3088676a4ae5364f0826f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128453"
---
# <a name="dfm_validatecmd-message"></a><span data-ttu-id="b5dca-103">DFM- \_ validatecmd-Meldung</span><span class="sxs-lookup"><span data-stu-id="b5dca-103">DFM\_VALIDATECMD message</span></span>

<span data-ttu-id="b5dca-104">Wird gesendet, um zu überprüfen, ob ein Menübefehl vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b5dca-104">Sent to verify the existence of a menu command.</span></span>


```C++
DFM_INVOKECOMMAND

    wParam = (WPARAM)(WPARAM) idCmd;            

    lParam = (LPARAM)(LPARAM) lParam = 0;

            
```



## <a name="parameters"></a><span data-ttu-id="b5dca-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5dca-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5dca-106">*idcmd*</span><span class="sxs-lookup"><span data-stu-id="b5dca-106">*idCmd*</span></span> 
</dt> <dd><span data-ttu-id="b5dca-107">Der Offset des Menübefehls Bezeichners.</span><span class="sxs-lookup"><span data-stu-id="b5dca-107">The menu command identifier offset.</span></span></dd> <dt>

<span data-ttu-id="b5dca-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b5dca-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b5dca-109">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b5dca-109">Not used.</span></span> <span data-ttu-id="b5dca-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="b5dca-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5dca-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b5dca-111">Return value</span></span>

<span data-ttu-id="b5dca-112">Gibt "s OK" zurück \_ , wenn der Befehl vorhanden ist, \_ andernfalls "false".</span><span class="sxs-lookup"><span data-stu-id="b5dca-112">Returns S\_OK if the command exists, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5dca-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b5dca-113">Remarks</span></span>

<span data-ttu-id="b5dca-114">Diese Nachricht wird entweder an die Rückruffunktion oder an das Rückruf Objekt gesendet, je nachdem, wie das standardmäßige Kontextmenü Objekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b5dca-114">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="b5dca-115">Es gibt zwei APIs für die Erstellung, [**cdeffoldermenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**shkreatedefaultcontextmenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="b5dca-115">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="b5dca-116">[**DFM \_ Invokecommandex**](dfm-invokecommandex.md) ist eine erweiterte Version dieser Nachricht und bietet weitere Informationen für den Rückruf.</span><span class="sxs-lookup"><span data-stu-id="b5dca-116">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="b5dca-117">Verwenden Sie **DFM \_ invokecommandex** , wenn die zusätzlichen Informationen, die von dieser Schnittstelle bereitgestellt werden, in der Implementierung benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="b5dca-117">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5dca-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b5dca-118">Requirements</span></span>



| <span data-ttu-id="b5dca-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5dca-119">Requirement</span></span> | <span data-ttu-id="b5dca-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b5dca-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b5dca-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b5dca-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b5dca-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5dca-122">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b5dca-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b5dca-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b5dca-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5dca-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b5dca-125">Header</span><span class="sxs-lookup"><span data-stu-id="b5dca-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5dca-126"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5dca-126"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




