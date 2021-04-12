---
description: Die mxdc \_ S0PAGE \_ Passthrough \_ - \_ escapestruktur ist eine mxdc-Escape-Header-t-Struktur, die \_ \_ \_ mit einer mxdc \_ S0PAGE \_ Data T-Struktur verkettet ist \_ .
ms.assetid: 949c1ed4-92d5-4c11-a7da-f9d94bafe3f8
title: MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T-Struktur (mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 7c1a8370d2cfa1ada9fda2d2d99b9fe500b79d31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346488"
---
# <a name="mxdc_s0page_passthrough_escape_t-structure"></a><span data-ttu-id="140b9-103">Mxdc \_ S0PAGE \_ Passthrough \_ - \_ escapestruktur</span><span class="sxs-lookup"><span data-stu-id="140b9-103">MXDC\_S0PAGE\_PASSTHROUGH\_ESCAPE\_T structure</span></span>

<span data-ttu-id="140b9-104">Die **mxdc \_ S0PAGE \_ Passthrough \_ \_** -escapestruktur ist eine [**mxdc- \_ Escape-Header- \_ \_ t**](mxdcescapeheader.md) -Struktur, die mit einer [**mxdc \_ S0PAGE \_ Data \_ T**](mxdcs0pagedata.md) -Struktur verkettet ist.</span><span class="sxs-lookup"><span data-stu-id="140b9-104">The **MXDC\_S0PAGE\_PASSTHROUGH\_ESCAPE\_T** structure is an [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure concatenated with an [**MXDC\_S0PAGE\_DATA\_T**](mxdcs0pagedata.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="140b9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="140b9-105">Syntax</span></span>


```C++
typedef struct tagMxdcS0PagePassthroughEscape {
  MXDC_ESCAPE_HEADER_T mxdcEscape;
  MXDC_S0PAGE_DATA_T   xpsS0PageData;
} MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T, *P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T;
```



## <a name="members"></a><span data-ttu-id="140b9-106">Member</span><span class="sxs-lookup"><span data-stu-id="140b9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="140b9-107">**mxdcescape**</span><span class="sxs-lookup"><span data-stu-id="140b9-107">**mxdcEscape**</span></span>
</dt> <dd>

<span data-ttu-id="140b9-108">Eine [**mxdc- \_ Escape- \_ Header- \_ T**](mxdcescapeheader.md) -Struktur, deren **Opcode** -Member auf **mxdcop \_ Set \_ S0PAGE** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="140b9-108">An [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure with its **opCode** member set to **MXDCOP\_SET\_S0PAGE**.</span></span>

</dd> <dt>

<span data-ttu-id="140b9-109">**xpsS0PageData**</span><span class="sxs-lookup"><span data-stu-id="140b9-109">**xpsS0PageData**</span></span>
</dt> <dd>

<span data-ttu-id="140b9-110">Eine [**MxdcS0PageData**](mxdcs0pagedata.md) -Struktur, die eine XPS-Dokument Seite darstellt.</span><span class="sxs-lookup"><span data-stu-id="140b9-110">An [**MxdcS0PageData**](mxdcs0pagedata.md) structure that represents an XPS-document page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="140b9-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="140b9-111">Remarks</span></span>

<span data-ttu-id="140b9-112">Diese Struktur wird in den *lpszindata* -Parameter der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Funktion übergeben, wenn Sie mit dem Escapezeichen für [**mxdc \_**](mxdc-escape.md) aufgerufen wird und der **Opcode** -Member der [**mxdc- \_ Escape-Header- \_ \_ T**](mxdcescapeheader.md) -Struktur **mxdcop \_ Set \_ S0PAGE** ist.</span><span class="sxs-lookup"><span data-stu-id="140b9-112">This structure is passed in the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function when it is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape and the **opCode** member of the [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure is **MXDCOP\_SET\_S0PAGE**.</span></span> <span data-ttu-id="140b9-113">Das Ergebnis ist, dass der Microsoft XML Document Converter (mxdc) die Seite an den Drucker übergibt, ohne Sie zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="140b9-113">The result is that the Microsoft XML Document Converter (MXDC) passes the page through to the printer without processing it.</span></span>

<span data-ttu-id="140b9-114">Weisen Sie der Escapesequenz wie unten gezeigt den Speicher zu, legen Sie die Felder nach Bedarf fest, und nennen Sie dann [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span><span class="sxs-lookup"><span data-stu-id="140b9-114">Allocate memory for the escape as shown below, set the fields as needed, and then call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span></span>


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T) + 
                        iS0PageDataSize - 1;

// Allocate the memory buffer.
P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T pS0PageEscapeData = 
                        (P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



<span data-ttu-id="140b9-115">Der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -aufrufsausdruck muss zwischen einem Aufrufen von [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) und einem Aufrufen von [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)liegen.</span><span class="sxs-lookup"><span data-stu-id="140b9-115">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must be between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span>

<span data-ttu-id="140b9-116">Die aufrufende Anwendung ist für die Validierung des XML-Codes der XPS-Dokument Seite verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="140b9-116">The calling application is responsible for validating the XML of the XPS document page.</span></span>

<span data-ttu-id="140b9-117">Der Streamingverbrauch ist effizienter, wenn Sie [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) mit **mxdcop \_ Set \_ S0PAGE \_ Resource** als **Opcode** für jede Ressource auf der Seite aufruft, bevor Sie Sie mit **mxdcop \_ Set \_ S0PAGE** aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="140b9-117">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with **MXDCOP\_SET\_S0PAGE\_RESOURCE** as **opCode** for each resource on the page before you call it with **MXDCOP\_SET\_S0PAGE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="140b9-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="140b9-118">Requirements</span></span>



| <span data-ttu-id="140b9-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="140b9-119">Requirement</span></span> | <span data-ttu-id="140b9-120">Wert</span><span class="sxs-lookup"><span data-stu-id="140b9-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="140b9-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="140b9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="140b9-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="140b9-122">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="140b9-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="140b9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="140b9-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="140b9-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="140b9-125">Header</span><span class="sxs-lookup"><span data-stu-id="140b9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="140b9-126"><dt>Mxdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="140b9-126"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="140b9-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="140b9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="140b9-128">Drucken</span><span class="sxs-lookup"><span data-stu-id="140b9-128">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="140b9-129">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="140b9-129">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="140b9-130">[Escapefunktionen für GDI-Drucker](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="140b9-130">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="140b9-131">**Extescape**</span><span class="sxs-lookup"><span data-stu-id="140b9-131">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="140b9-132">**mxdc-Escapezeichen \_**</span><span class="sxs-lookup"><span data-stu-id="140b9-132">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

