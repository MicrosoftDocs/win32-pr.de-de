---
description: Die mxdc \_ PrintTicket \_ Escape \_ t-Struktur ist eine mxdc-Escape-Header-t-Struktur, die \_ \_ \_ mit einer mxdc \_ PrintTicket \_ Data T-Struktur verkettet ist \_ .
ms.assetid: 79b4f830-3e3f-4c6f-9e61-98e8bf6e2824
title: MXDC_PRINTTICKET_ESCAPE_T-Struktur (mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_PRINTTICKET_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 158ee2038c83b74077d00e6922b2c7050b76bc62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369843"
---
# <a name="mxdc_printticket_escape_t-structure"></a><span data-ttu-id="03006-103">Mxdc \_ PrintTicket \_ Escape- \_ T-Struktur</span><span class="sxs-lookup"><span data-stu-id="03006-103">MXDC\_PRINTTICKET\_ESCAPE\_T structure</span></span>

<span data-ttu-id="03006-104">Die **mxdc \_ PrintTicket \_ Escape \_ t** -Struktur ist eine [**mxdc- \_ Escape-Header- \_ \_ t**](mxdcescapeheader.md) -Struktur, die mit einer [**mxdc \_ PrintTicket \_ Data \_ T**](mxdcprintticketpassthrough.md) -Struktur verkettet ist.</span><span class="sxs-lookup"><span data-stu-id="03006-104">The **MXDC\_PRINTTICKET\_ESCAPE\_T** structure is a [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure concatenated with a [**MXDC\_PRINTTICKET\_DATA\_T**](mxdcprintticketpassthrough.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="03006-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="03006-105">Syntax</span></span>


```C++
typedef struct tagMxdcPrintTicketEscape {
  MXDC_ESCAPE_HEADER_T    mxdcEscape;
  MXDC_PRINTTICKET_DATA_T printTicketData;
} MXDC_PRINTTICKET_ESCAPE_T, *P_MXDC_PRINTTICKET_ESCAPE_T;
```



## <a name="members"></a><span data-ttu-id="03006-106">Member</span><span class="sxs-lookup"><span data-stu-id="03006-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="03006-107">**mxdcescape**</span><span class="sxs-lookup"><span data-stu-id="03006-107">**mxdcEscape**</span></span>
</dt> <dd>

<span data-ttu-id="03006-108">Eine [**mxdc- \_ Escape- \_ Header- \_ T**](mxdcescapeheader.md) -Struktur, deren **Opcode** -Member auf mxdcop \_ PrintTicket \_ Fixed \_ Page, mxdcop \_ PrintTicket \_ Fixed \_ doc oder mxdcop \_ PrintTicket \_ Fixed doc (Fixed \_ doc \_ ) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="03006-108">A [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure with its **opCode** member set to MXDCOP\_PRINTTICKET\_FIXED\_PAGE, MXDCOP\_PRINTTICKET\_FIXED\_DOC, or MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ.</span></span>

</dd> <dt>

<span data-ttu-id="03006-109">**printticketdata**</span><span class="sxs-lookup"><span data-stu-id="03006-109">**printTicketData**</span></span>
</dt> <dd>

<span data-ttu-id="03006-110">Eine [**mxdc \_ PrintTicket \_ Data \_ T**](mxdcprintticketpassthrough.md) -Struktur, die das Druck Ticket enthält.</span><span class="sxs-lookup"><span data-stu-id="03006-110">A [**MXDC\_PRINTTICKET\_DATA\_T**](mxdcprintticketpassthrough.md) structure containing the print ticket.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="03006-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03006-111">Remarks</span></span>

<span data-ttu-id="03006-112">Diese Struktur wird in den *lpszindata* -Parameter der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Funktion übergeben, wenn diese Funktion mit der escapeescapezeichen [**mxdc \_**](mxdc-escape.md) aufgerufen wird und das **Opcode** -Element der [**mxdc- \_ Escape-Header- \_ \_ T**](mxdcescapeheader.md) -Struktur **mxdcop \_ PrintTicket \_ Fixed \_ Page**, **mxdcop \_ PrintTicket Fixed \_ \_ doc** oder **mxdcop \_ PrintTicket \_ Fixed \_ doc \_**</span><span class="sxs-lookup"><span data-stu-id="03006-112">This structure is passed in the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function when that function is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape and the **opCode** member of the [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure is **MXDCOP\_PRINTTICKET\_FIXED\_PAGE**, **MXDCOP\_PRINTTICKET\_FIXED\_DOC**, or **MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ**.</span></span> <span data-ttu-id="03006-113">Das Ergebnis ist, das Druck Ticket in die XPS-Dokument Datei zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="03006-113">The result is to write the print ticket to the XPS document file.</span></span>

<span data-ttu-id="03006-114">Weisen Sie der Escapesequenz wie unten gezeigt den Speicher zu, legen Sie die Felder nach Bedarf fest, und nennen Sie dann [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span><span class="sxs-lookup"><span data-stu-id="03006-114">Allocate memory for the escape as shown below, set the fields as needed, and then call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span></span>


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_PRINTTICKET_ESCAPE_T) + 
                        iS0PageDataSize - 1;

// Allocate the memory buffer.
P_MXDC_PRINTTICKET_ESCAPE_T pS0PageEscapeData = 
                        (P_MXDC_PRINTTICKET_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



<span data-ttu-id="03006-115">Wenn **Opcode** auf **mxdcop \_ PrintTicket \_ Fixed \_ Page** festgelegt ist, muss der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Aufrufe zwischen einem Aufrufen von [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) und einem Aufrufen von [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)erfolgen.</span><span class="sxs-lookup"><span data-stu-id="03006-115">If the **opCode** is set to **MXDCOP\_PRINTTICKET\_FIXED\_PAGE**, the call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span> <span data-ttu-id="03006-116">Wenn der **Opcode** entweder auf **mxdcop \_ PrintTicket \_ Fixed \_ doc** oder **mxdcop \_ PrintTicket \_ Fixed \_ doc \_** festgelegt ist, muss der **extescape** -Befehl zwischen einem [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) -Befehl und einem- [**Endpunkt**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="03006-116">If the **opCode** set to either **MXDCOP\_PRINTTICKET\_FIXED\_DOC** or **MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ**, the call to **ExtEscape** must occur between a call to [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) and a call to [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).</span></span>

## <a name="requirements"></a><span data-ttu-id="03006-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03006-117">Requirements</span></span>



| <span data-ttu-id="03006-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03006-118">Requirement</span></span> | <span data-ttu-id="03006-119">Wert</span><span class="sxs-lookup"><span data-stu-id="03006-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="03006-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="03006-120">Minimum supported client</span></span><br/> | <span data-ttu-id="03006-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="03006-121">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="03006-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="03006-122">Minimum supported server</span></span><br/> | <span data-ttu-id="03006-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="03006-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="03006-124">Header</span><span class="sxs-lookup"><span data-stu-id="03006-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="03006-125"><dt>Mxdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="03006-125"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03006-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03006-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03006-127">Drucken</span><span class="sxs-lookup"><span data-stu-id="03006-127">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="03006-128">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="03006-128">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="03006-129">[Escapefunktionen für GDI-Drucker](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="03006-129">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="03006-130">**Extescape**</span><span class="sxs-lookup"><span data-stu-id="03006-130">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="03006-131">**mxdc-Escapezeichen \_**</span><span class="sxs-lookup"><span data-stu-id="03006-131">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

