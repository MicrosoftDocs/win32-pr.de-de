---
description: Die mxdc \_ S0PAGE \_ Data \_ T-Struktur enthält eine XPS-Dokument Seite, die ohne Verarbeitung an die Microsoft XPS Document Converter-Ausgabedatei (mxdc) übermittelt werden soll.
ms.assetid: 3dc8e0b9-cf63-4345-93d2-3b60dac42546
title: MXDC_S0PAGE_DATA_T-Struktur (mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 2da9df454b8741f2203072fd25856118407ef5c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757741"
---
# <a name="mxdc_s0page_data_t-structure"></a><span data-ttu-id="4dbdd-103">Mxdc \_ S0PAGE \_ Data \_ T-Struktur</span><span class="sxs-lookup"><span data-stu-id="4dbdd-103">MXDC\_S0PAGE\_DATA\_T structure</span></span>

<span data-ttu-id="4dbdd-104">Die **mxdc \_ S0PAGE \_ Data \_ T** -Struktur enthält eine XPS-Dokument Seite, die ohne Verarbeitung an die Microsoft XPS Document Converter-Ausgabedatei (mxdc) übermittelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4dbdd-104">The **MXDC\_S0PAGE\_DATA\_T** structure holds an XPS document page to be passed to the Microsoft XPS Document Converter (MXDC) output file without any processing.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dbdd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4dbdd-105">Syntax</span></span>


```C++
typedef struct tagMxdcS0PageData {
  ULONG dwSize;
  BYTE  bData[1];
} MXDC_S0PAGE_DATA_T, *P_MXDC_S0PAGE_DATA_T;
```



## <a name="members"></a><span data-ttu-id="4dbdd-106">Member</span><span class="sxs-lookup"><span data-stu-id="4dbdd-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4dbdd-107">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="4dbdd-107">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="4dbdd-108">Die Größe des Ausgabepuffers, **bdata**.</span><span class="sxs-lookup"><span data-stu-id="4dbdd-108">The size of the output buffer, **bData**.</span></span>

</dd> <dt>

<span data-ttu-id="4dbdd-109">**bData**</span><span class="sxs-lookup"><span data-stu-id="4dbdd-109">**bData**</span></span>
</dt> <dd>

<span data-ttu-id="4dbdd-110">Die XPS-Dokument Seite.</span><span class="sxs-lookup"><span data-stu-id="4dbdd-110">The XPS document page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4dbdd-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4dbdd-111">Remarks</span></span>

<span data-ttu-id="4dbdd-112">Diese Struktur wird an eine [**mxdc- \_ \_ escapeheader- \_ t**](mxdcescapeheader.md) -Struktur angehängt (deren **Opcode** auf mxdcop Set S0PAGE festgelegt ist \_ \_ ), um eine [**mxdc \_ S0PAGE \_ Passthrough- \_ Escape \_ t**](mxdcs0pagepassthroughescape.md) -Struktur zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4dbdd-112">This structure is appended to an [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure (which has its **opCode** set to MXDCOP\_SET\_S0PAGE) to make an [**MXDC\_S0PAGE\_PASSTHROUGH\_ESCAPE\_T**](mxdcs0pagepassthroughescape.md) structure.</span></span> <span data-ttu-id="4dbdd-113">Diese Struktur wird dann an den *lpszindata* -Parameter der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Funktion übergeben, wenn Sie mit [**mxdc \_ Escape**](mxdc-escape.md) als Escapezeichen aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4dbdd-113">That structure is then passed to the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function when it is called with [**MXDC\_ESCAPE**](mxdc-escape.md) as the escape.</span></span> <span data-ttu-id="4dbdd-114">Das Ergebnis ist, dass der mxdc die Seite an die Ausgabe übergibt, ohne Sie zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="4dbdd-114">The result is that the MXDC passes the page through to the output without processing it.</span></span>

<span data-ttu-id="4dbdd-115">Der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -aufrufsausdruck muss zwischen einem Aufrufen von [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) und einem Aufrufen von [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)liegen.</span><span class="sxs-lookup"><span data-stu-id="4dbdd-115">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must be between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span>

<span data-ttu-id="4dbdd-116">Die aufrufende Anwendung ist für die Validierung des XML-Codes der XPS-Dokument Seite verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="4dbdd-116">The calling application is responsible for validating the XML of the XPS document page.</span></span>

<span data-ttu-id="4dbdd-117">Der Streamingverbrauch ist effizienter, wenn Sie [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) mit **mxdcop \_ Set \_ S0PAGE \_ Resource** als **Opcode** für jede Ressource auf der Seite aufruft, bevor Sie Sie mit **mxdcop \_ Set \_ S0PAGE** aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="4dbdd-117">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with **MXDCOP\_SET\_S0PAGE\_RESOURCE** as **opCode** for each resource on the page before you call it with **MXDCOP\_SET\_S0PAGE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4dbdd-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4dbdd-118">Requirements</span></span>



| <span data-ttu-id="4dbdd-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4dbdd-119">Requirement</span></span> | <span data-ttu-id="4dbdd-120">Wert</span><span class="sxs-lookup"><span data-stu-id="4dbdd-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="4dbdd-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4dbdd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4dbdd-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4dbdd-122">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4dbdd-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4dbdd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4dbdd-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4dbdd-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4dbdd-125">Header</span><span class="sxs-lookup"><span data-stu-id="4dbdd-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4dbdd-126"><dt>Mxdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="4dbdd-126"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4dbdd-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4dbdd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dbdd-128">Drucken</span><span class="sxs-lookup"><span data-stu-id="4dbdd-128">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="4dbdd-129">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="4dbdd-129">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="4dbdd-130">[Escapefunktionen für GDI-Drucker](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4dbdd-130">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4dbdd-131">**Extescape**</span><span class="sxs-lookup"><span data-stu-id="4dbdd-131">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="4dbdd-132">**mxdc-Escapezeichen \_**</span><span class="sxs-lookup"><span data-stu-id="4dbdd-132">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

