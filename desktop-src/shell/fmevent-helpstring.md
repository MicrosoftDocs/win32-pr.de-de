---
description: Wird an eine DLL-Prozedur für Datei-Manager-Erweiterungen gesendet, wenn der Datei-Manager eine Hilfe Zeichenfolge für ein Menü oder Symbolleisten-Befehls
title: FMEVENT_HELPSTRING Meldung (WF. h)
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
ms.openlocfilehash: ae3be1953d4c8bbf70f8f17fcf34fcfb1ac583f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215955"
---
# <a name="fmevent_helpstring-message"></a><span data-ttu-id="8f7b9-103">Meldung zu "Meldungs \_ Meldung"</span><span class="sxs-lookup"><span data-stu-id="8f7b9-103">FMEVENT\_HELPSTRING message</span></span>

<span data-ttu-id="8f7b9-104">Wird an eine DLL-Prozedur für Datei-Manager-Erweiterungen gesendet, wenn der Datei-Manager eine Hilfe Zeichenfolge für ein Menü oder Symbolleisten-Befehls</span><span class="sxs-lookup"><span data-stu-id="8f7b9-104">Sent to a File Manager extension DLL procedure when File Manager wants a Help string for a menu or toolbar command item.</span></span>

## <a name="parameters"></a><span data-ttu-id="8f7b9-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f7b9-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f7b9-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8f7b9-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8f7b9-107">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="8f7b9-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8f7b9-108">*lpfmshs*</span><span class="sxs-lookup"><span data-stu-id="8f7b9-108">*lpfmshs*</span></span> 
</dt> <dd>

<span data-ttu-id="8f7b9-109">Die Adresse einer [**f- \_ HelpString**](fms-helpstring.md) -Struktur, die Befehls Element-hilfezeichen folgen Daten kommuniziert.</span><span class="sxs-lookup"><span data-stu-id="8f7b9-109">The address of an [**FMS\_HELPSTRING**](fms-helpstring.md) structure that communicates command item Help string data.</span></span> <span data-ttu-id="8f7b9-110">Die **FMS \_ HelpString** -Struktur identifiziert das Befehls Element, für das eine Hilfe Zeichenfolge gewünscht wird, sowie ein Handle für das Menü.</span><span class="sxs-lookup"><span data-stu-id="8f7b9-110">The **FMS\_HELPSTRING** structure identifies the command item for which a Help string is wanted, along with a handle to its menu.</span></span> <span data-ttu-id="8f7b9-111">Eine Anwendung schreibt dann die entsprechende Hilfe Zeichenfolge in den **szhelp** -Member der **FMS- \_ HelpString** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="8f7b9-111">An application then writes the appropriate Help string to the **FMS\_HELPSTRING** structure's **szHelp** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f7b9-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8f7b9-112">Return value</span></span>

<span data-ttu-id="8f7b9-113">Eine Erweiterungs-DLL-Prozedur sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="8f7b9-113">An extension DLL procedure should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f7b9-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="8f7b9-114">Requirements</span></span>



| <span data-ttu-id="8f7b9-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8f7b9-115">Requirement</span></span> | <span data-ttu-id="8f7b9-116">Wert</span><span class="sxs-lookup"><span data-stu-id="8f7b9-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8f7b9-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8f7b9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8f7b9-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8f7b9-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="8f7b9-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8f7b9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8f7b9-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8f7b9-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8f7b9-121">Header</span><span class="sxs-lookup"><span data-stu-id="8f7b9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f7b9-122"><dt>WF. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f7b9-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f7b9-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8f7b9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f7b9-124">**"F"**</span><span class="sxs-lookup"><span data-stu-id="8f7b9-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="8f7b9-125">**"helpmenuitem" für "f" \_**</span><span class="sxs-lookup"><span data-stu-id="8f7b9-125">**FMEVENT\_HELPMENUITEM**</span></span>](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




