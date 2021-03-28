---
description: Wird von der Standard Implementierung des Kontextmenüs gesendet, um einem Menübefehl einen Namen zuzuweisen.
title: DFM_MAPCOMMANDNAME Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8aa764f7-d5d4-4a84-94d2-993265e1eb5a
api_name:
- DFM_MAPCOMMANDNAME
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 312817e5c530078b906af63e4e8c3d00595d3a04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525358"
---
# <a name="dfm_mapcommandname-message"></a><span data-ttu-id="55bbb-103">DFM- \_ mapcommandname-Meldung</span><span class="sxs-lookup"><span data-stu-id="55bbb-103">DFM\_MAPCOMMANDNAME message</span></span>

<span data-ttu-id="55bbb-104">Wird von der Standard Implementierung des Kontextmenüs gesendet, um einem Menübefehl einen Namen zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="55bbb-104">Sent by the default context menu implementation to assign a name to a menu command.</span></span>


```C++
DFM_MAPCOMMANDNAME

    lParam = (LPARAM)(int*) defaultID;

    wparam = (WPARAM)(LPTSTR) pszCommandName;

            
```



## <a name="parameters"></a><span data-ttu-id="55bbb-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="55bbb-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55bbb-106">*DefaultID* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="55bbb-106">*defaultID* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="55bbb-107">Ein Zeiger auf die ID des ausgewählten Menübefehls.</span><span class="sxs-lookup"><span data-stu-id="55bbb-107">A pointer to the ID of the selected menu command.</span></span>

</dd> <dt>

<span data-ttu-id="55bbb-108">*pszcommandname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55bbb-108">*pszCommandName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55bbb-109">Ein Zeiger auf eine Unicode-Zeichenfolge, die den Namen des Befehls enthält.</span><span class="sxs-lookup"><span data-stu-id="55bbb-109">A pointer to a Unicode string containing the name of the command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55bbb-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55bbb-110">Remarks</span></span>

<span data-ttu-id="55bbb-111">Diese Nachricht wird entweder an die Rückruffunktion oder an das Rückruf Objekt gesendet, je nachdem, wie das Standardkontext Menü-Objekt implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="55bbb-111">This message is sent to either the callback function or the callback object depending on how the default context menu object is implemented.</span></span> <span data-ttu-id="55bbb-112">Es gibt zwei APIs für die Implementierung, [**cdeffoldermenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**shkreatedefaultcontextmenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="55bbb-112">There are two APIs for its implementation, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="55bbb-113">[**DFM \_ Invokecommandex**](dfm-invokecommandex.md) ist eine erweiterte Version dieser Nachricht und bietet weitere Informationen für den Rückruf.</span><span class="sxs-lookup"><span data-stu-id="55bbb-113">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="55bbb-114">Verwenden Sie **DFM \_ invokecommandex** , wenn die zusätzlichen Informationen, die von dieser Schnittstelle bereitgestellt werden, in der Implementierung benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="55bbb-114">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="55bbb-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="55bbb-115">Requirements</span></span>



| <span data-ttu-id="55bbb-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="55bbb-116">Requirement</span></span> | <span data-ttu-id="55bbb-117">Wert</span><span class="sxs-lookup"><span data-stu-id="55bbb-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="55bbb-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="55bbb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="55bbb-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55bbb-119">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="55bbb-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="55bbb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="55bbb-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55bbb-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="55bbb-122">Header</span><span class="sxs-lookup"><span data-stu-id="55bbb-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="55bbb-123"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="55bbb-123"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




