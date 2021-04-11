---
description: Die mxdc \_ S0PAGE \_ Resource \_ Escape \_ t-Struktur ist eine mxdc-Escape-Header-t-Struktur, die \_ \_ \_ mit einer mxdc \_ XPS \_ S0PAGE \_ Resource \_ T-Struktur verkettet ist.
ms.assetid: e5caa280-f0a5-4a89-b4f1-4f195a537dc6
title: MXDC_S0PAGE_RESOURCE_ESCAPE_T-Struktur (mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_RESOURCE_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: ed1d78aad1ede2a318dcde2d3a2d39fd8e666ddc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215970"
---
# <a name="mxdc_s0page_resource_escape_t-structure"></a><span data-ttu-id="830d8-103">Mxdc \_ S0PAGE \_ Resource \_ Escape- \_ T-Struktur</span><span class="sxs-lookup"><span data-stu-id="830d8-103">MXDC\_S0PAGE\_RESOURCE\_ESCAPE\_T structure</span></span>

<span data-ttu-id="830d8-104">Die **mxdc \_ S0PAGE \_ Resource \_ Escape \_ t** -Struktur ist eine [**mxdc- \_ Escape-Header- \_ \_ t**](mxdcescapeheader.md) -Struktur, die mit einer [**mxdc \_ XPS \_ S0PAGE \_ Resource \_ T**](mxdcxpss0pageresource.md) -Struktur verkettet ist.</span><span class="sxs-lookup"><span data-stu-id="830d8-104">The **MXDC\_S0PAGE\_RESOURCE\_ESCAPE\_T** structure is an [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure concatenated with an [**MXDC\_XPS\_S0PAGE\_RESOURCE\_T**](mxdcxpss0pageresource.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="830d8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="830d8-105">Syntax</span></span>


```C++
typedef struct tagMxdcS0PageResourceEscape {
  MXDC_ESCAPE_HEADER_T       mxdcEscape;
  MXDC_XPS_S0PAGE_RESOURCE_T xpsS0PageResourcePassthrough;
} MXDC_S0PAGE_RESOURCE_ESCAPE_T, *P_MXDC_S0PAGE_RESOURCE_ESCAPE_T;
```



## <a name="members"></a><span data-ttu-id="830d8-106">Member</span><span class="sxs-lookup"><span data-stu-id="830d8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="830d8-107">**mxdcescape**</span><span class="sxs-lookup"><span data-stu-id="830d8-107">**mxdcEscape**</span></span>
</dt> <dd>

<span data-ttu-id="830d8-108">Eine [**mxdc- \_ Escape- \_ Header- \_ T**](mxdcescapeheader.md) -Struktur, deren **Opcode** -Member auf mxdcop \_ Set S0PAGE Resource festgelegt ist \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="830d8-108">An [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure with its **opCode** member set to MXDCOP\_SET\_S0PAGE\_RESOURCE.</span></span>

</dd> <dt>

<span data-ttu-id="830d8-109">**xpsS0PageResourcePassthrough**</span><span class="sxs-lookup"><span data-stu-id="830d8-109">**xpsS0PageResourcePassthrough**</span></span>
</dt> <dd>

<span data-ttu-id="830d8-110">Eine [**mxdc \_ XPS \_ S0PAGE \_ Resource \_ T**](mxdcxpss0pageresource.md) -Struktur, die eine Ressource (z. b. eine Schriftart oder Bilddatei) auf einer XPS-Dokument Seite darstellt.</span><span class="sxs-lookup"><span data-stu-id="830d8-110">An [**MXDC\_XPS\_S0PAGE\_RESOURCE\_T**](mxdcxpss0pageresource.md) structure representing a resource, such as a font or image file, on an XPS document page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="830d8-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="830d8-111">Remarks</span></span>

<span data-ttu-id="830d8-112">Diese Struktur wird in den *lpszindata* -Parameter der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Funktion übergeben, wenn diese Funktion mit dem Escapezeichen " [**mxdc \_**](mxdc-escape.md) " aufgerufen wird und der **Opcode** -Member der [**mxdc- \_ Escape-Header- \_ \_ T**](mxdcescapeheader.md) -Struktur **mxdcop \_ Set \_ S0PAGE \_ Resource** ist.</span><span class="sxs-lookup"><span data-stu-id="830d8-112">This structure is passed in the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function when that function is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape, and the **opCode** member of the [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure is **MXDCOP\_SET\_S0PAGE\_RESOURCE**.</span></span> <span data-ttu-id="830d8-113">Das Ergebnis ist eine Seiten Ressource, die an den mxdc gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="830d8-113">The result is a page resource to send to the MXDC.</span></span>

<span data-ttu-id="830d8-114">Weisen Sie der Escapesequenz wie unten gezeigt den Speicher zu, legen Sie die Felder nach Bedarf fest, und nennen Sie dann [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span><span class="sxs-lookup"><span data-stu-id="830d8-114">Allocate memory for the escape as shown below, set the fields as needed, and then call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span></span>


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_S0PAGE_RESOURCE_ESCAPE_T) + 
                        iS0PageResourceDataSize - 1;

// Allocate the memory buffer.
P_MXDC_S0PAGE_RESOURCE_ESCAPE_T pS0PageResourceEscapeData = 
                        (P_MXDC_S0PAGE_RESOURCE_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



<span data-ttu-id="830d8-115">Der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -aufrufsausdruck muss zwischen einem Aufrufen von [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) und einem Aufrufen von " [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage);" liegen. zwischen den Aufrufen von **Startpage** und **EndPage** können jedoch mehr als einer dieser Aufrufe vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="830d8-115">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must be between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage); however, there can be more than one of these calls between the calls to **StartPage** and **EndPage**.</span></span>

<span data-ttu-id="830d8-116">Der Streamingverbrauch ist effizienter, wenn [**Sie extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) mit dem **mxdcop \_ Set \_ S0PAGE \_ Resource** **Opcode** für jede Ressource auf der Seite aufruft, bevor Sie **extescape** mit dem **mxdcop \_ Set \_ S0PAGE**  **Opcode** aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="830d8-116">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with the **MXDCOP\_SET\_S0PAGE\_RESOURCE** **opCode** for each resource on the page before you call **ExtEscape** with the **MXDCOP\_SET\_S0PAGE**  **opCode**.</span></span>

## <a name="requirements"></a><span data-ttu-id="830d8-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="830d8-117">Requirements</span></span>



| <span data-ttu-id="830d8-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="830d8-118">Requirement</span></span> | <span data-ttu-id="830d8-119">Wert</span><span class="sxs-lookup"><span data-stu-id="830d8-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="830d8-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="830d8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="830d8-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="830d8-121">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="830d8-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="830d8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="830d8-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="830d8-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="830d8-124">Header</span><span class="sxs-lookup"><span data-stu-id="830d8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="830d8-125"><dt>Mxdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="830d8-125"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="830d8-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="830d8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="830d8-127">Drucken</span><span class="sxs-lookup"><span data-stu-id="830d8-127">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="830d8-128">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="830d8-128">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="830d8-129">[Escapefunktionen für GDI-Drucker](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="830d8-129">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="830d8-130">**Extescape**</span><span class="sxs-lookup"><span data-stu-id="830d8-130">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="830d8-131">**mxdc-Escapezeichen \_**</span><span class="sxs-lookup"><span data-stu-id="830d8-131">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

