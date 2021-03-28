---
description: Ermöglicht dem Rückruf Objekt, eine Hilfe Text Zeichenfolge anzugeben.
title: DFM_GETHELPTEXT Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 40ed981b-6d03-4c4f-9e70-1a01d49edcb0
api_name:
- DFM_GETHELPTEXT
- DFM_GETHELPTEXT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b9aefb1c3a12ff00294ccc536464794a17fccfc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525364"
---
# <a name="dfm_gethelptext-message"></a><span data-ttu-id="3253f-103">DFM- \_ GetHelpText-Nachricht</span><span class="sxs-lookup"><span data-stu-id="3253f-103">DFM\_GETHELPTEXT message</span></span>

<span data-ttu-id="3253f-104">Ermöglicht dem Rückruf Objekt, eine Hilfe Text Zeichenfolge anzugeben.</span><span class="sxs-lookup"><span data-stu-id="3253f-104">Allows the callback object to specify a help text string.</span></span>


```C++
DFM_GETHELPTEXT 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a><span data-ttu-id="3253f-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="3253f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3253f-106">*idcmd \_ cchmax* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3253f-106">*idCmd\_cchMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3253f-107">Das nieder wertige Wort dieses Parameters enthält die Befehls-ID.</span><span class="sxs-lookup"><span data-stu-id="3253f-107">The low-order word of this parameter holds the command ID.</span></span> <span data-ttu-id="3253f-108">Das höchst wertige Wort enthält die Anzahl der Zeichen im *pszText* -Puffer.</span><span class="sxs-lookup"><span data-stu-id="3253f-108">The high-order word holds the number of characters in the *pszText* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="3253f-109">*pszText* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3253f-109">*pszText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3253f-110">Eine mit NULL endende ANSI-Zeichenfolge, die den Hilfe Text enthält.</span><span class="sxs-lookup"><span data-stu-id="3253f-110">A null-terminated ANSI string containing the help text.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3253f-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3253f-111">Remarks</span></span>

<span data-ttu-id="3253f-112">Diese Nachricht wird entweder an die Rückruffunktion oder an das Rückruf Objekt gesendet, je nachdem, wie das standardmäßige Kontextmenü Objekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3253f-112">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="3253f-113">Es gibt zwei APIs für die Erstellung, [**cdeffoldermenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**shkreatedefaultcontextmenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="3253f-113">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="3253f-114">[**DFM \_ Invokecommandex**](dfm-invokecommandex.md) ist eine erweiterte Version dieser Nachricht und bietet weitere Informationen für den Rückruf.</span><span class="sxs-lookup"><span data-stu-id="3253f-114">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="3253f-115">Verwenden Sie **DFM \_ invokecommandex** , wenn die zusätzlichen Informationen, die von dieser Schnittstelle bereitgestellt werden, in der Implementierung benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="3253f-115">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="3253f-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="3253f-116">Requirements</span></span>



| <span data-ttu-id="3253f-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3253f-117">Requirement</span></span> | <span data-ttu-id="3253f-118">Wert</span><span class="sxs-lookup"><span data-stu-id="3253f-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3253f-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3253f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3253f-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3253f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="3253f-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3253f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3253f-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3253f-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3253f-123">Header</span><span class="sxs-lookup"><span data-stu-id="3253f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3253f-124"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="3253f-124"><dt>Shlobj.h</dt></span></span> </dl> |
| <span data-ttu-id="3253f-125">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="3253f-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3253f-126">**DFM \_ GetHelpText** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3253f-126">**DFM\_GETHELPTEXT** (ANSI)</span></span><br/>                                              |



 

 




