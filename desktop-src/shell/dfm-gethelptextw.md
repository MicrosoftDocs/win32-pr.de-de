---
description: 'DFM_GETHELPTEXTW Meldung: Ermöglicht dem Rückrufobjekt das Angeben einer Hilfetextzeichenfolge.'
title: DFM_GETHELPTEXTW Nachricht (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 85bdd1d0-5b68-44a5-a1b0-4845b5be34d0
api_name:
- DFM_GETHELPTEXTW
- DFM_GETHELPTEXTW
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6271b150bead5be4715259c68711ee67417f6395
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097038"
---
# <a name="dfm_gethelptextw-message"></a><span data-ttu-id="f5b73-103">DFM \_ GETHELPTEXTW-Nachricht</span><span class="sxs-lookup"><span data-stu-id="f5b73-103">DFM\_GETHELPTEXTW message</span></span>

<span data-ttu-id="f5b73-104">Ermöglicht es dem Rückrufobjekt, eine Hilfetextzeichenfolge anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f5b73-104">Allows the callback object to specify a help text string.</span></span>


```C++
DFM_GETHELPTEXTW 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(WPTSTR) pszText;

            
```



## <a name="parameters"></a><span data-ttu-id="f5b73-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5b73-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5b73-106">*idCmd \_ cchMax* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f5b73-106">*idCmd\_cchMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5b73-107">Das Wort in niedriger Reihenfolge dieses Parameters enthält die Befehls-ID.</span><span class="sxs-lookup"><span data-stu-id="f5b73-107">The low-order word of this parameter holds the command ID.</span></span> <span data-ttu-id="f5b73-108">Das Wort in hoher Reihenfolge enthält die Anzahl der Zeichen im *pszText-Puffer.*</span><span class="sxs-lookup"><span data-stu-id="f5b73-108">The high-order word holds the number of characters in the *pszText* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f5b73-109">*pszText* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f5b73-109">*pszText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5b73-110">Eine auf NULL endende Unicode-Zeichenfolge, die den Hilfetext enthält.</span><span class="sxs-lookup"><span data-stu-id="f5b73-110">A null-terminated Unicode string containing the help text.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f5b73-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f5b73-111">Remarks</span></span>

<span data-ttu-id="f5b73-112">Diese Meldung wird entweder an die Rückruffunktion oder das Rückrufobjekt gesendet, je nachdem, wie das Standardkontextmenüobjekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f5b73-112">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="f5b73-113">Es gibt zwei APIs für die Erstellung: [**CDefFolderMenu \_ Create2,**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) [**SHCreateDefaultContextMenu.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu)</span><span class="sxs-lookup"><span data-stu-id="f5b73-113">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="f5b73-114">[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) ist eine erweiterte Version dieser Nachricht und stellt weitere Informationen zum Rückruf bereit.</span><span class="sxs-lookup"><span data-stu-id="f5b73-114">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="f5b73-115">Verwenden Sie **DFM \_ INVOKECOMMANDEX,** wenn die zusätzlichen Informationen, die von dieser Schnittstelle bereitgestellt werden, in Ihrer Implementierung benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="f5b73-115">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5b73-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5b73-116">Requirements</span></span>



| <span data-ttu-id="f5b73-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5b73-117">Requirement</span></span> | <span data-ttu-id="f5b73-118">Wert</span><span class="sxs-lookup"><span data-stu-id="f5b73-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f5b73-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f5b73-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f5b73-120">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5b73-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="f5b73-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f5b73-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f5b73-122">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5b73-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f5b73-123">Header</span><span class="sxs-lookup"><span data-stu-id="f5b73-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5b73-124"><dt>Shlobj.h</dt></span><span class="sxs-lookup"><span data-stu-id="f5b73-124"><dt>Shlobj.h</dt></span></span> </dl> |
| <span data-ttu-id="f5b73-125">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="f5b73-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f5b73-126">**DFM \_ GETHELPTEXTW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="f5b73-126">**DFM\_GETHELPTEXTW** (Unicode)</span></span><br/>                                          |



 

 




