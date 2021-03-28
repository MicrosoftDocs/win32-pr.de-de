---
description: Sfvm \_ GetDetailsOf kann geändert werden oder ist nicht verfügbar.
ms.assetid: 46a81a7b-527c-4d41-8d25-ce65fd87416e
title: SFVM_GETDETAILSOF Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6170c0fc8dc29435b2c6f2bb033f30706ccb7b33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980217"
---
# <a name="sfvm_getdetailsof-message"></a><span data-ttu-id="c68f8-103">Sfvm \_ GetDetailsOf-Meldung</span><span class="sxs-lookup"><span data-stu-id="c68f8-103">SFVM\_GETDETAILSOF message</span></span>

<span data-ttu-id="c68f8-104">\[**Sfvm \_ "GetDetailsOf** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="c68f8-104">\[**SFVM\_GETDETAILSOF** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c68f8-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="c68f8-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="c68f8-106">Ermöglicht dem Rückruf Objekt, die Details für ein Element in einem Shellordner bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c68f8-106">Allows the callback object to provide the details for an item in a Shell folder.</span></span> <span data-ttu-id="c68f8-107">Verwenden Sie nur, wenn ein Rückruf [**von IShellFolder2:: GetDetailsOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsof) fehlschlägt und keine [**ishelldetails:: GetDetailsOf**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishelldetails-getdetailsof) -Methode zum Aufrufen verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="c68f8-107">Use only if a call to [**IShellFolder2::GetDetailsOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsof) fails and there is no [**IShellDetails::GetDetailsOf**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishelldetails-getdetailsof) method available to call.</span></span> <span data-ttu-id="c68f8-108">Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.</span><span class="sxs-lookup"><span data-stu-id="c68f8-108">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETDETAILSOF
    wParam = (WPARAM)(int) iColumn;
    lParam = (LPARAM)(DETAILSINFO*) pDi;
            
```



## <a name="parameters"></a><span data-ttu-id="c68f8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c68f8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c68f8-110">*icolumn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c68f8-110">*iColumn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c68f8-111">Die null basierte ID der Spalte.</span><span class="sxs-lookup"><span data-stu-id="c68f8-111">The zero-based ID of the column.</span></span>

</dd> <dt>

<span data-ttu-id="c68f8-112">*PDI* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c68f8-112">*pDi* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c68f8-113">Ein Zeiger auf eine [**detailsinfo**](/windows/desktop/api/shlobj_core/ns-shlobj_core-detailsinfo) -Struktur, die mit den angeforderten Informationen gefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="c68f8-113">A pointer to a [**DETAILSINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-detailsinfo) structure filled with the requested information.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c68f8-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c68f8-114">Requirements</span></span>



| <span data-ttu-id="c68f8-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c68f8-115">Requirement</span></span> | <span data-ttu-id="c68f8-116">Wert</span><span class="sxs-lookup"><span data-stu-id="c68f8-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c68f8-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c68f8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c68f8-118">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c68f8-118">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c68f8-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c68f8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c68f8-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c68f8-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c68f8-121">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="c68f8-121">End of client support</span></span><br/>    | <span data-ttu-id="c68f8-122">Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="c68f8-122">Windows XP with SP2</span></span><br/>                                                      |
| <span data-ttu-id="c68f8-123">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="c68f8-123">End of server support</span></span><br/>    | <span data-ttu-id="c68f8-124">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c68f8-124">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="c68f8-125">Header</span><span class="sxs-lookup"><span data-stu-id="c68f8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c68f8-126"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="c68f8-126"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
