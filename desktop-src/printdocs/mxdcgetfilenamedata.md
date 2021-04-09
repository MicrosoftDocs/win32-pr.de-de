---
description: Die mxdc \_ get \_ filename \_ Data \_ T-Struktur enthält den vollständigen Pfad und den Dateinamen einer Microsoft XPS Document Converter (mxdc)-Ausgabedatei.
ms.assetid: 070bce2e-5055-47e8-9412-2094a636635f
title: MXDC_GET_FILENAME_DATA_T-Struktur (mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_GET_FILENAME_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: dd29696ae21924f245e508469acfbb88c78b034b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864963"
---
# <a name="mxdc_get_filename_data_t-structure"></a><span data-ttu-id="f088c-103">Mxdc \_ get \_ filename \_ Data \_ T-Struktur</span><span class="sxs-lookup"><span data-stu-id="f088c-103">MXDC\_GET\_FILENAME\_DATA\_T structure</span></span>

<span data-ttu-id="f088c-104">Die **mxdc \_ get \_ filename \_ Data \_ T** -Struktur enthält den vollständigen Pfad und den Dateinamen einer Microsoft XPS Document Converter (mxdc)-Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="f088c-104">The **MXDC\_GET\_FILENAME\_DATA\_T** structure holds the full path and file name of a Microsoft XPS Document Converter (MXDC) output file.</span></span>

## <a name="syntax"></a><span data-ttu-id="f088c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f088c-105">Syntax</span></span>


```C++
typedef struct _tagMxdcGetFileNameData {
  ULONG   cbOutput;
  wchar_t wszData[1];
} MXDC_GET_FILENAME_DATA_T, *P_MXDC_GET_FILENAME_DATA_T;
```



## <a name="members"></a><span data-ttu-id="f088c-106">Member</span><span class="sxs-lookup"><span data-stu-id="f088c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f088c-107">**cboutput**</span><span class="sxs-lookup"><span data-stu-id="f088c-107">**cbOutput**</span></span>
</dt> <dd>

<span data-ttu-id="f088c-108">Die Größe des Ausgabepuffers, **wszdata**.</span><span class="sxs-lookup"><span data-stu-id="f088c-108">The size of the output buffer, **wszData**.</span></span>

</dd> <dt>

<span data-ttu-id="f088c-109">**wszdata**</span><span class="sxs-lookup"><span data-stu-id="f088c-109">**wszData**</span></span>
</dt> <dd>

<span data-ttu-id="f088c-110">Der voll qualifizierte Pfad und Dateiname der Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="f088c-110">The fully qualified path and file name of the output file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f088c-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f088c-111">Remarks</span></span>

<span data-ttu-id="f088c-112">Diese Struktur wird von [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) zurückgegeben, wenn Sie mit dem Escapezeichen für [**\_ mxdc**](mxdc-escape.md) aufgerufen wird und die im *lpszindata* -Parameter übergebenen [**mxdc- \_ escapeheader- \_ \_ T**](mxdcescapeheader.md) -Struktur den **Opcode** auf **mxdcop \_ get \_ filename** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f088c-112">This structure is returned by [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) when it is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape and the [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure that is passed in the *lpszInData* parameter has its **opCode** set to **MXDCOP\_GET\_FILENAME**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f088c-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f088c-113">Requirements</span></span>



| <span data-ttu-id="f088c-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f088c-114">Requirement</span></span> | <span data-ttu-id="f088c-115">Wert</span><span class="sxs-lookup"><span data-stu-id="f088c-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f088c-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f088c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f088c-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f088c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f088c-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f088c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f088c-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f088c-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f088c-120">Header</span><span class="sxs-lookup"><span data-stu-id="f088c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f088c-121"><dt>Mxdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="f088c-121"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f088c-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f088c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f088c-123">Drucken</span><span class="sxs-lookup"><span data-stu-id="f088c-123">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f088c-124">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="f088c-124">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="f088c-125">[Escapefunktionen für GDI-Drucker](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f088c-125">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f088c-126">**Extescape**</span><span class="sxs-lookup"><span data-stu-id="f088c-126">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="f088c-127">**mxdc-Escapezeichen \_**</span><span class="sxs-lookup"><span data-stu-id="f088c-127">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

