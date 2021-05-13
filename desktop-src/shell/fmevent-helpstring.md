---
description: Wird an eine DATEI-Manager-Erweiterungs-DLL-Prozedur gesendet, wenn der Datei-Manager eine Hilfezeichenfolge für ein Menü- oder Symbolleistenbefehlselement benötigt.
title: FMEVENT_HELPSTRING (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_HELPSTRING
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 55fb5bfe-2889-40e5-9798-85f63727e31f
ms.openlocfilehash: 6fe187330e27f7e246c9bbd68005f68f346bbc90
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841281"
---
# <a name="fmevent_helpstring-message"></a><span data-ttu-id="d1b9e-103">FMEVENT \_ HELPSTRING-Meldung</span><span class="sxs-lookup"><span data-stu-id="d1b9e-103">FMEVENT\_HELPSTRING message</span></span>

<span data-ttu-id="d1b9e-104">Wird an eine DATEI-Manager-Erweiterungs-DLL-Prozedur gesendet, wenn der Datei-Manager eine Hilfezeichenfolge für ein Menü- oder Symbolleistenbefehlselement benötigt.</span><span class="sxs-lookup"><span data-stu-id="d1b9e-104">Sent to a File Manager extension DLL procedure when File Manager wants a Help string for a menu or toolbar command item.</span></span>

## <a name="parameters"></a><span data-ttu-id="d1b9e-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1b9e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1b9e-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d1b9e-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d1b9e-107">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="d1b9e-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d1b9e-108">*lpfmshs*</span><span class="sxs-lookup"><span data-stu-id="d1b9e-108">*lpfmshs*</span></span> 
</dt> <dd>

<span data-ttu-id="d1b9e-109">Die Adresse einer [**FMS \_ HELPSTRING-Struktur,**](fms-helpstring.md) die Hilfezeichenfolgendaten des Befehlselements kommuniziert.</span><span class="sxs-lookup"><span data-stu-id="d1b9e-109">The address of an [**FMS\_HELPSTRING**](fms-helpstring.md) structure that communicates command item Help string data.</span></span> <span data-ttu-id="d1b9e-110">Die **FMS \_ HELPSTRING-Struktur** identifiziert das Befehlselement, für das eine Hilfezeichenfolge gewünscht ist, zusammen mit einem Handle für das Menü.</span><span class="sxs-lookup"><span data-stu-id="d1b9e-110">The **FMS\_HELPSTRING** structure identifies the command item for which a Help string is wanted, along with a handle to its menu.</span></span> <span data-ttu-id="d1b9e-111">Eine Anwendung schreibt dann die entsprechende Hilfezeichenfolge in das **szHelp-Member** der **FMS \_ HELPSTRING-Struktur.**</span><span class="sxs-lookup"><span data-stu-id="d1b9e-111">An application then writes the appropriate Help string to the **FMS\_HELPSTRING** structure's **szHelp** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1b9e-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d1b9e-112">Return value</span></span>

<span data-ttu-id="d1b9e-113">Eine DLL-Erweiterungsprozedur sollte 0 (null) zurückgeben, wenn diese Meldung verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="d1b9e-113">An extension DLL procedure should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1b9e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1b9e-114">Requirements</span></span>



| <span data-ttu-id="d1b9e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1b9e-115">Requirement</span></span> | <span data-ttu-id="d1b9e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d1b9e-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d1b9e-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d1b9e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d1b9e-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d1b9e-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="d1b9e-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d1b9e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d1b9e-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d1b9e-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d1b9e-121">Header</span><span class="sxs-lookup"><span data-stu-id="d1b9e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1b9e-122"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="d1b9e-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1b9e-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1b9e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1b9e-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="d1b9e-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="d1b9e-125">**FMEVENT \_ HELPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="d1b9e-125">**FMEVENT\_HELPMENUITEM**</span></span>](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




