---
description: Wird an eine Erweiterungs-DLL gesendet, wenn der Datei-Manager Ihre Symbolleiste lädt. Diese Meldung ermöglicht der Erweiterungs-DLL, der Datei-Manager-Symbolleiste eine Schaltfläche hinzuzufügen.
title: FMEVENT_TOOLBARLOAD Meldung (WF. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_TOOLBARLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: c5daab49-4ed5-439b-b1b7-a87f70c379f0
ms.openlocfilehash: 5f04b524c8d44d987513b6605f9f827336078d02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215954"
---
# <a name="fmevent_toolbarload-message"></a><span data-ttu-id="927d3-104">Meldung für das Meldung "f" \_</span><span class="sxs-lookup"><span data-stu-id="927d3-104">FMEVENT\_TOOLBARLOAD message</span></span>

<span data-ttu-id="927d3-105">Wird an eine Erweiterungs-DLL gesendet, wenn der Datei-Manager Ihre Symbolleiste lädt.</span><span class="sxs-lookup"><span data-stu-id="927d3-105">Sent to an extension DLL when File Manager is loading its toolbar.</span></span> <span data-ttu-id="927d3-106">Diese Meldung ermöglicht der Erweiterungs-DLL, der Datei-Manager-Symbolleiste eine Schaltfläche hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="927d3-106">This message allows an extension DLL to add a button to the File Manager toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="927d3-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="927d3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="927d3-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="927d3-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="927d3-109">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="927d3-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="927d3-110">*lpfmstbl*</span><span class="sxs-lookup"><span data-stu-id="927d3-110">*lpfmstbl*</span></span> 
</dt> <dd>

<span data-ttu-id="927d3-111">Die Adresse einer [**f- \_ Load**](fms-toolbarload.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="927d3-111">The address of an [**FMS\_TOOLBARLOAD**](fms-toolbarload.md) structure.</span></span> <span data-ttu-id="927d3-112">Wenn die Erweiterungs-DLL der Symbolleiste im Datei-Manager eine Schaltfläche hinzufügt, sollte die dll die Struktur mit Informationen über die Schaltfläche Auffüllen.</span><span class="sxs-lookup"><span data-stu-id="927d3-112">If the extension DLL adds a button to the toolbar in File Manager, the DLL should fill the structure with information about the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="927d3-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="927d3-113">Return value</span></span>

<span data-ttu-id="927d3-114">Eine Erweiterungs-DLL muss **true** zurückgeben, um der Symbolleiste die Schaltfläche hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="927d3-114">An extension DLL must return **TRUE** to add the button to the toolbar.</span></span> <span data-ttu-id="927d3-115">Wenn die DLL **false** zurückgibt, fügt der Datei-Manager die Schaltfläche nicht hinzu.</span><span class="sxs-lookup"><span data-stu-id="927d3-115">If the DLL returns **FALSE**, File Manager does not add the button.</span></span>

## <a name="requirements"></a><span data-ttu-id="927d3-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="927d3-116">Requirements</span></span>



| <span data-ttu-id="927d3-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="927d3-117">Requirement</span></span> | <span data-ttu-id="927d3-118">Wert</span><span class="sxs-lookup"><span data-stu-id="927d3-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="927d3-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="927d3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="927d3-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="927d3-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="927d3-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="927d3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="927d3-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="927d3-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="927d3-123">Header</span><span class="sxs-lookup"><span data-stu-id="927d3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="927d3-124"><dt>WF. h</dt></span><span class="sxs-lookup"><span data-stu-id="927d3-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="927d3-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="927d3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="927d3-126">**"F"**</span><span class="sxs-lookup"><span data-stu-id="927d3-126">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




