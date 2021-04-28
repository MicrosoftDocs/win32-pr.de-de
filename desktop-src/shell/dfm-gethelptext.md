---
description: 'DFM_GETHELPTEXT Meldung: Ermöglicht dem Rückrufobjekt das Angeben einer Hilfetextzeichenfolge.'
title: DFM_GETHELPTEXT (Shlobj.h)
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
ms.openlocfilehash: 2428fe6696ff5949a0b25487437c8f3408b95f65
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097068"
---
# <a name="dfm_gethelptext-message"></a><span data-ttu-id="c73ea-103">DFM \_ GETHELPTEXT-Nachricht</span><span class="sxs-lookup"><span data-stu-id="c73ea-103">DFM\_GETHELPTEXT message</span></span>

<span data-ttu-id="c73ea-104">Ermöglicht dem Rückrufobjekt das Angeben einer Hilfetextzeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="c73ea-104">Allows the callback object to specify a help text string.</span></span>


```C++
DFM_GETHELPTEXT 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a><span data-ttu-id="c73ea-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="c73ea-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c73ea-106">*idCmd \_ cchMax* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c73ea-106">*idCmd\_cchMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c73ea-107">Das niedrige Wort dieses Parameters enthält die Befehls-ID.</span><span class="sxs-lookup"><span data-stu-id="c73ea-107">The low-order word of this parameter holds the command ID.</span></span> <span data-ttu-id="c73ea-108">Das obere Wort enthält die Anzahl der Zeichen im *pszText-Puffer.*</span><span class="sxs-lookup"><span data-stu-id="c73ea-108">The high-order word holds the number of characters in the *pszText* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="c73ea-109">*pszText* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c73ea-109">*pszText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c73ea-110">Eine AUF NULL beendete ANSI-Zeichenfolge, die den Hilfetext enthält.</span><span class="sxs-lookup"><span data-stu-id="c73ea-110">A null-terminated ANSI string containing the help text.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c73ea-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c73ea-111">Remarks</span></span>

<span data-ttu-id="c73ea-112">Diese Meldung wird entweder an die Rückruffunktion oder das Rückrufobjekt gesendet, je nachdem, wie das Standardkontextmenüobjekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c73ea-112">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="c73ea-113">Es gibt zwei APIs für die Erstellung: [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="c73ea-113">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="c73ea-114">[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) ist eine erweiterte Version dieser Nachricht und stellt weitere Informationen für den Rückruf zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="c73ea-114">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="c73ea-115">Verwenden **Sie DFM \_ INVOKECOMMANDEX,** wenn die zusätzlichen Informationen, die von dieser Schnittstelle bereitgestellt werden, in Ihrer Implementierung benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="c73ea-115">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="c73ea-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c73ea-116">Requirements</span></span>



| <span data-ttu-id="c73ea-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c73ea-117">Requirement</span></span> | <span data-ttu-id="c73ea-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c73ea-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c73ea-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c73ea-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c73ea-120">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c73ea-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="c73ea-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c73ea-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c73ea-122">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c73ea-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c73ea-123">Header</span><span class="sxs-lookup"><span data-stu-id="c73ea-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c73ea-124"><dt>Shlobj.h</dt></span><span class="sxs-lookup"><span data-stu-id="c73ea-124"><dt>Shlobj.h</dt></span></span> </dl> |
| <span data-ttu-id="c73ea-125">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="c73ea-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c73ea-126">**DFM \_ GETHELPTEXT** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c73ea-126">**DFM\_GETHELPTEXT** (ANSI)</span></span><br/>                                              |



 

 




