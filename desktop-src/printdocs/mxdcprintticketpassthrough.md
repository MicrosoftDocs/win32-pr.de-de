---
description: Die mxdc \_ PrintTicket \_ Data \_ T-Struktur enthält ein XPS-Dokument-Druck Ticket, das Drucker-und Druckauftrags Einstellungen enthält, die an die Microsoft XPS Document Converter (mxdc)-Ausgabedatei ohne Verarbeitung übergeben werden.
ms.assetid: d30ba8bb-f429-49d5-963c-b770c3086e97
title: MXDC_PRINTTICKET_DATA_T-Struktur (mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_PRINTTICKET_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 94308527437316dda75fc5a50a6a7829e9315c3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864960"
---
# <a name="mxdc_printticket_data_t-structure"></a><span data-ttu-id="f9dd9-103">Mxdc- \_ PrintTicket- \_ Daten \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="f9dd9-103">MXDC\_PRINTTICKET\_DATA\_T structure</span></span>

<span data-ttu-id="f9dd9-104">Die **mxdc \_ PrintTicket \_ Data \_ T** -Struktur enthält ein XPS-Dokument-Druck Ticket, das Drucker-und Druckauftrags Einstellungen enthält, die an die Microsoft XPS Document Converter (mxdc)-Ausgabedatei ohne Verarbeitung übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="f9dd9-104">The **MXDC\_PRINTTICKET\_DATA\_T** structure holds an XPS document print ticket, which contains printer and print job settings, to pass to the Microsoft XPS Document Converter (MXDC) output file without any processing.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9dd9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9dd9-105">Syntax</span></span>


```C++
typedef struct tagMxdcPrintTicketData {
  DWORD dwDataSize;
  BYTE  bData[1];
} MXDC_PRINTTICKET_DATA_T, *P_MXDC_PRINTTICKET_DATA_T;
```



## <a name="members"></a><span data-ttu-id="f9dd9-106">Member</span><span class="sxs-lookup"><span data-stu-id="f9dd9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f9dd9-107">**dwDataSize**</span><span class="sxs-lookup"><span data-stu-id="f9dd9-107">**dwDataSize**</span></span>
</dt> <dd>

<span data-ttu-id="f9dd9-108">Die Größe des Druck Tickets in Bytes.</span><span class="sxs-lookup"><span data-stu-id="f9dd9-108">The size of the print ticket in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="f9dd9-109">**bData**</span><span class="sxs-lookup"><span data-stu-id="f9dd9-109">**bData**</span></span>
</dt> <dd>

<span data-ttu-id="f9dd9-110">Das XPS-Dokument-Druck Ticket.</span><span class="sxs-lookup"><span data-stu-id="f9dd9-110">The XPS document print ticket.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f9dd9-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9dd9-111">Remarks</span></span>

<span data-ttu-id="f9dd9-112">Diese Struktur wird an eine [**mxdc- \_ Escape- \_ Header- \_ T**](mxdcescapeheader.md) -Struktur angehängt, bei der der **Opcode** -Member auf **mxdcop \_ PrintTicket \_ Fixed \_ Page**, **mxdcop \_ PrintTicket \_ Fixed \_ doc** oder **mxdcop \_ PrintTicket Fixed \_ \_ doc \_** festgelegt ist, um eine [**mxdc \_ PrintTicket \_ Escape- \_ t**](mxdcprintticketescape.md) -Struktur zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f9dd9-112">This structure is appended to an [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure that has the **opCode** member set to **MXDCOP\_PRINTTICKET\_FIXED\_PAGE**, **MXDCOP\_PRINTTICKET\_FIXED\_DOC**, or **MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ** to make an [**MXDC\_PRINTTICKET\_ESCAPE\_T**](mxdcprintticketescape.md) structure.</span></span> <span data-ttu-id="f9dd9-113">Die **mxdc \_ PrintTicket \_ Escape \_ T** -Struktur wird dann an den *lpszindata* -Parameter der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Funktion übergeben, wenn Sie mit dem Escapezeichen " [**mxdc \_**](mxdc-escape.md) " aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f9dd9-113">The **MXDC\_PRINTTICKET\_ESCAPE\_T** structure is then passed to the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function when it is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape.</span></span> <span data-ttu-id="f9dd9-114">Der Effekt besteht darin, das Druck Ticket in die XPS-Dokument Datei zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="f9dd9-114">The effect is to write the print ticket to the XPS document file.</span></span>

<span data-ttu-id="f9dd9-115">Wenn **Opcode** auf **mxdcop \_ PrintTicket \_ Fixed \_ Page** festgelegt ist, muss der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Aufrufe zwischen einem Aufrufen von [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) und einem Aufrufen von [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)erfolgen.</span><span class="sxs-lookup"><span data-stu-id="f9dd9-115">If the **opCode** is set to **MXDCOP\_PRINTTICKET\_FIXED\_PAGE**, the call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span> <span data-ttu-id="f9dd9-116">Wenn der **Opcode** entweder auf **mxdcop \_ PrintTicket \_ Fixed \_ doc** oder **mxdcop \_ PrintTicket \_ Fixed \_ doc \_** festgelegt ist, muss der **extescape** -Befehl zwischen einem [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) -Befehl und einem- [**Endpunkt**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f9dd9-116">If the **opCode** set to either **MXDCOP\_PRINTTICKET\_FIXED\_DOC** or **MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ**, the call to **ExtEscape** must occur between a call to [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) and a call to [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).</span></span>

## <a name="requirements"></a><span data-ttu-id="f9dd9-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9dd9-117">Requirements</span></span>



| <span data-ttu-id="f9dd9-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9dd9-118">Requirement</span></span> | <span data-ttu-id="f9dd9-119">Wert</span><span class="sxs-lookup"><span data-stu-id="f9dd9-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f9dd9-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f9dd9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f9dd9-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9dd9-121">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f9dd9-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f9dd9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f9dd9-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9dd9-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f9dd9-124">Header</span><span class="sxs-lookup"><span data-stu-id="f9dd9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9dd9-125"><dt>Mxdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9dd9-125"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9dd9-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9dd9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9dd9-127">Drucken</span><span class="sxs-lookup"><span data-stu-id="f9dd9-127">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f9dd9-128">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="f9dd9-128">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="f9dd9-129">[Escapefunktionen für GDI-Drucker](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f9dd9-129">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f9dd9-130">**Extescape**</span><span class="sxs-lookup"><span data-stu-id="f9dd9-130">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="f9dd9-131">**mxdc-Escapezeichen \_**</span><span class="sxs-lookup"><span data-stu-id="f9dd9-131">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

