---
description: Die folgenden global eindeutigen Bezeichner (GUIDs) werden von Windows Journal verwendet, um benutzerdefinierte Eigenschaften für Striche oder Zeichnungs Attribute zu identifizieren.
ms.assetid: a7488c26-b61f-47d8-a19b-d630a8c00875
title: GUIDs der benutzerdefinierten Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb1d9069f2c655f658752a6ae3891910ff68103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362642"
---
# <a name="custom-property-guids"></a><span data-ttu-id="c065c-103">GUIDs der benutzerdefinierten Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c065c-103">Custom Property GUIDs</span></span>

<span data-ttu-id="c065c-104">Die folgenden global eindeutigen Bezeichner (GUIDs) werden von Windows Journal verwendet, um benutzerdefinierte Eigenschaften für Striche oder Zeichnungs Attribute zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c065c-104">The following globally unique identifiers (GUIDs) are used by Windows Journal to identify custom properties on strokes or drawing attributes.</span></span>

## <a name="guid_stroke_timestamp"></a><span data-ttu-id="c065c-105">GUID- \_ Strich \_ Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="c065c-105">GUID\_STROKE\_TIMESTAMP</span></span>


```C++
GUID_STROKE_TIMESTAMP = {4EA66C4-F33A-461B-B8FE-68070D9C7575}
```



<span data-ttu-id="c065c-106">Dies ist eine [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) -Struktur, die die Uhrzeit angibt, zu der der Strich erstellt oder dem Dokument hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="c065c-106">This is a [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure that indicates the time at which the stroke was created or added to the document.</span></span>


```C++
typedef struct _FILETIME {
    DWORD dwLowDateTime;
    DWORD dwHighDateTime;
} FILETIME, *PFILETIME;
```



## <a name="guid_stroke_timeid"></a><span data-ttu-id="c065c-107">GUID \_ \_ -Strich-TimeID</span><span class="sxs-lookup"><span data-stu-id="c065c-107">GUID\_STROKE\_TIMEID</span></span>


```C++
GUID_STROKE_TIMEID = {50B6BC8-3B7D-4816-8C61-BC7E905B2132}
```



<span data-ttu-id="c065c-108">Dies ist eine **TimeID-** Struktur.</span><span class="sxs-lookup"><span data-stu-id="c065c-108">This is a **TIMEID** structure.</span></span> <span data-ttu-id="c065c-109">Sie ermöglicht die Beibehaltung der Stroke-Reihenfolge über Einfüge-und Löschvorgänge.</span><span class="sxs-lookup"><span data-stu-id="c065c-109">It allows stroke order to be maintained across paste and drop operations.</span></span> <span data-ttu-id="c065c-110">Ohne die **TimeID-** Struktur ist der Zeitstempel für alle [**IInkStrokeDisp-Schnittstellen**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) Objekte, die in einer [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung ausgeschnitten und eingefügt werden, identisch.</span><span class="sxs-lookup"><span data-stu-id="c065c-110">Without the **TIMEID** structure, the timestamp for all [**IInkStrokeDisp Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects cut and pasted in a [InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) will be the same.</span></span>


```C++
typedef struct tagTIMEID {
    FILETIME  tmFiletime;
    ULONG     uiOrder;
} TIMEID;
```



## <a name="guid_highlighter"></a><span data-ttu-id="c065c-111">GUID- \_ highheller</span><span class="sxs-lookup"><span data-stu-id="c065c-111">GUID\_HIGHLIGHTER</span></span>

<span data-ttu-id="c065c-112">Dies ist ein **boolescher** Wert, bei dem **true**= highheller Ink, **false**= reguläre Freihand ist.</span><span class="sxs-lookup"><span data-stu-id="c065c-112">This is a **BOOL**, where **TRUE**=highlighter ink, **FALSE**=regular ink.</span></span> <span data-ttu-id="c065c-113">Dies wird auf Zeichnungs Attribute angewendet.</span><span class="sxs-lookup"><span data-stu-id="c065c-113">This is applied to drawing attributes.</span></span>


```C++
GUID_HIGHLIGHTER = {9B6267B8-3968-4048-AB74-F490406A2DFA}
```



## <a name="guid_ink_style_bold"></a><span data-ttu-id="c065c-114">GUID- \_ Ink- \_ Stil \_ Fett</span><span class="sxs-lookup"><span data-stu-id="c065c-114">GUID\_INK\_STYLE\_BOLD</span></span>

<span data-ttu-id="c065c-115">Dabei handelt es sich um einen **booleschen** Wert, bei dem **true**= Bold Ink, **false**= normal ist.</span><span class="sxs-lookup"><span data-stu-id="c065c-115">This is a **BOOL**, where **TRUE**=bold ink, **FALSE**=normal.</span></span> <span data-ttu-id="c065c-116">Dies wird auf Zeichnungs Attribute angewendet.</span><span class="sxs-lookup"><span data-stu-id="c065c-116">This is applied to drawing attributes.</span></span>


```C++
GUID_INK_STYLE_BOLD = {E02FB5C1-9693-4312-A434-00DE7F3AD493}
```



## <a name="guid_ink_style_italics"></a><span data-ttu-id="c065c-117">GUID-Freihand- \_ \_ \_ stilkursiv</span><span class="sxs-lookup"><span data-stu-id="c065c-117">GUID\_INK\_STYLE\_ITALICS</span></span>

<span data-ttu-id="c065c-118">Dabei handelt es sich um einen **booleschen** Wert ( **true**= Italicized Ink, **false**= normal).</span><span class="sxs-lookup"><span data-stu-id="c065c-118">This is a **BOOL**, where **TRUE**=italicized ink, **FALSE**=normal.</span></span> <span data-ttu-id="c065c-119">Dies wird auf Zeichnungs Attribute angewendet.</span><span class="sxs-lookup"><span data-stu-id="c065c-119">This is applied to drawing attributes.</span></span>


```C++
GUID_INK_STYLE_ITALICS = {05253B51-49C6-4A04-8993-64DD9ABD842A}
```



## <a name="related-topics"></a><span data-ttu-id="c065c-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c065c-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c065c-121">**Ijournalreader-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c065c-121">**IJournalReader Interface**</span></span>](ijournalreader.md)
</dt> </dl>

 

 
