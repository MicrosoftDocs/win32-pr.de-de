---
description: Wird an eine Erweiterungs-DLL gesendet, wenn der Datei-Manager die dll lädt.
ms.assetid: 9d673ab8-c468-4b46-b96e-1adfaa9f85fb
title: FMEVENT_LOAD Meldung (WF. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_LOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.openlocfilehash: de7a950e3f17c9b2cee2b66a047d289ca29b6b56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979705"
---
# <a name="fmevent_load-message"></a><span data-ttu-id="534ad-103">Meldung zum Laden des Ereignisses \_</span><span class="sxs-lookup"><span data-stu-id="534ad-103">FMEVENT\_LOAD message</span></span>

<span data-ttu-id="534ad-104">Wird an eine Erweiterungs-DLL gesendet, wenn der Datei-Manager die dll lädt.</span><span class="sxs-lookup"><span data-stu-id="534ad-104">Sent to an extension DLL when File Manager is loading the DLL.</span></span>

## <a name="parameters"></a><span data-ttu-id="534ad-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="534ad-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="534ad-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="534ad-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="534ad-107">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="534ad-107">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="534ad-108">*lpfmsld*</span><span class="sxs-lookup"><span data-stu-id="534ad-108">*lpfmsld*</span></span> 
</dt> <dd>

<span data-ttu-id="534ad-109">Die Adresse einer [**Lom- \_ Lade**](fms-load.md) Struktur, die den Delta Wert für das Menü Element angibt.</span><span class="sxs-lookup"><span data-stu-id="534ad-109">The address of an [**FMS\_LOAD**](fms-load.md) structure that specifies the menu item delta value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="534ad-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="534ad-110">Return value</span></span>

<span data-ttu-id="534ad-111">Eine Erweiterungs-DLL muss **true** zurückgeben, um das Laden der dll fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="534ad-111">An extension DLL must return **TRUE** to continue loading the DLL.</span></span> <span data-ttu-id="534ad-112">Wenn die DLL **false** zurückgibt, ruft der Datei-Manager die [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) -Funktion auf und beendet jegliche Kommunikation mit der Erweiterungs-DLL.</span><span class="sxs-lookup"><span data-stu-id="534ad-112">If the DLL returns **FALSE**, File Manager calls the [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) function and ends any communication with the extension DLL.</span></span>

## <a name="remarks"></a><span data-ttu-id="534ad-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="534ad-113">Remarks</span></span>

<span data-ttu-id="534ad-114">Eine Anwendung sollte die Member " **dwSize**", " **szmenuname**" und " **HMENU** " in der [**FMS- \_ Lade**](fms-load.md) Struktur ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="534ad-114">An application should fill the **dwSize**, **szMenuName**, and **hMenu** members in the [**FMS\_LOAD**](fms-load.md) structure.</span></span> <span data-ttu-id="534ad-115">Außerdem sollte Sie den Wert des **wmenudelta** -Members speichern und verwenden, um Menü Elemente bei der Menü Änderung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="534ad-115">It should also save the value of the **wMenuDelta** member and use it to identify menu items when modifying the menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="534ad-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="534ad-116">Requirements</span></span>



| <span data-ttu-id="534ad-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="534ad-117">Requirement</span></span> | <span data-ttu-id="534ad-118">Wert</span><span class="sxs-lookup"><span data-stu-id="534ad-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="534ad-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="534ad-119">Minimum supported client</span></span><br/> | <span data-ttu-id="534ad-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="534ad-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="534ad-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="534ad-121">Minimum supported server</span></span><br/> | <span data-ttu-id="534ad-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="534ad-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="534ad-123">Header</span><span class="sxs-lookup"><span data-stu-id="534ad-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="534ad-124"><dt>WF. h</dt></span><span class="sxs-lookup"><span data-stu-id="534ad-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="534ad-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="534ad-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="534ad-126">**"F"**</span><span class="sxs-lookup"><span data-stu-id="534ad-126">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 
