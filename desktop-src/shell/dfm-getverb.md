---
description: Wird von der standardmäßigen Kontextmenü Implementierung gesendet, um das Verb für die angegebene Befehls-ID im Kontextmenü zu erhalten.
title: DFM_GETVERB Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bd12a38e-4d50-43ad-9d1f-8fefa90b44f9
api_name:
- DFM_GETVERB
- DFM_GETVERBA
- DFM_GETVERBW
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bbb1b2fb54aa2b0e4b66cf8fc559c56eb279504d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214430"
---
# <a name="dfm_getverb-message"></a><span data-ttu-id="91e90-103">DFM \_ getverb-Nachricht</span><span class="sxs-lookup"><span data-stu-id="91e90-103">DFM\_GETVERB message</span></span>

<span data-ttu-id="91e90-104">Wird von der standardmäßigen Kontextmenü Implementierung gesendet, um das Verb für die angegebene Befehls-ID im Kontextmenü zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="91e90-104">Sent by the default context menu implementation to get the verb for the given command ID in the context menu.</span></span>


```C++

                DFM_GETVERB 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a><span data-ttu-id="91e90-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="91e90-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91e90-106">*idcmd \_ cchmax* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91e90-106">*idCmd\_cchMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91e90-107">Das nieder wertige Wort dieses Parameters enthält die Befehls-ID.</span><span class="sxs-lookup"><span data-stu-id="91e90-107">The low-order word of this parameter holds the command ID.</span></span> <span data-ttu-id="91e90-108">Das höchst wertige Wort enthält die Anzahl der Zeichen im *pszText* -Puffer.</span><span class="sxs-lookup"><span data-stu-id="91e90-108">The high-order word holds the number of characters in the *pszText* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="91e90-109">*pszText* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="91e90-109">*pszText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91e90-110">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Verb Text enthält.</span><span class="sxs-lookup"><span data-stu-id="91e90-110">A pointer to a null-terminated string that contains the verb text.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="91e90-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91e90-111">Remarks</span></span>

<span data-ttu-id="91e90-112">Diese Nachricht wird entweder an die Rückruffunktion oder an das Rückruf Objekt gesendet, je nachdem, wie das standardmäßige Kontextmenü Objekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="91e90-112">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="91e90-113">Es gibt zwei APIs für die Erstellung, [**cdeffoldermenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**shkreatedefaultcontextmenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="91e90-113">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="91e90-114">[**DFM \_ Invokecommandex**](dfm-invokecommandex.md) ist eine erweiterte Version dieser Nachricht und bietet weitere Informationen für den Rückruf.</span><span class="sxs-lookup"><span data-stu-id="91e90-114">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="91e90-115">Verwenden Sie **DFM \_ invokecommandex** , wenn die zusätzlichen Informationen, die von dieser Schnittstelle bereitgestellt werden, in der Implementierung benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="91e90-115">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="91e90-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="91e90-116">Requirements</span></span>



| <span data-ttu-id="91e90-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="91e90-117">Requirement</span></span> | <span data-ttu-id="91e90-118">Wert</span><span class="sxs-lookup"><span data-stu-id="91e90-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="91e90-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="91e90-119">Minimum supported client</span></span><br/> | <span data-ttu-id="91e90-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91e90-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="91e90-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="91e90-121">Minimum supported server</span></span><br/> | <span data-ttu-id="91e90-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91e90-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="91e90-123">Header</span><span class="sxs-lookup"><span data-stu-id="91e90-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="91e90-124"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="91e90-124"><dt>Shlobj.h</dt></span></span> </dl> |
| <span data-ttu-id="91e90-125">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="91e90-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="91e90-126">**DFM \_ Getverbw** (Unicode) und **DFM \_ getverba** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="91e90-126">**DFM\_GETVERBW** (Unicode) and **DFM\_GETVERBA** (ANSI)</span></span><br/>                 |



 

 




