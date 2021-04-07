---
title: Eigenschaften Satz Anzeige Name-Wörterbuch
description: Mit einem Wörterbuch von Eigenschaften Anzeige Namen können Benutzer festlegen, dass die Bedeutung von Eigenschaften festgelegt werden soll, die über die des typindikators hinausgehen.
ms.assetid: b6813a86-39d3-4754-86e4-51035a7c91d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd844b4d37d4f10434fc5b73f936b4b6565c1506
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729072"
---
# <a name="property-set-display-name-dictionary"></a><span data-ttu-id="d24e6-103">Eigenschaften Satz Anzeige Name-Wörterbuch</span><span class="sxs-lookup"><span data-stu-id="d24e6-103">Property Set Display Name Dictionary</span></span>

<span data-ttu-id="d24e6-104">Mit einem Wörterbuch von Eigenschaften Anzeige Namen können Benutzer festlegen, dass die Bedeutung von Eigenschaften festgelegt werden soll, die über die des typindikators hinausgehen.</span><span class="sxs-lookup"><span data-stu-id="d24e6-104">A dictionary of property display names enables property set users to attach meaning to properties - beyond those provided by the type indicator.</span></span>

## <a name="dictionary-structure"></a><span data-ttu-id="d24e6-105">Wörterbuch Struktur</span><span class="sxs-lookup"><span data-stu-id="d24e6-105">Dictionary Structure</span></span>

<span data-ttu-id="d24e6-106">Das Wörterbuch enthält die Anzahl der Einträge in der Liste, gefolgt von einer Liste der Wörterbucheinträge.</span><span class="sxs-lookup"><span data-stu-id="d24e6-106">The dictionary contains a count of entries in the list, followed by a list of dictionary entries.</span></span>

``` syntax
typedef struct tagDICTIONARY 
{ 
    DWORD  cEntries ;               // Count of entries in the list 
    ENTRY  rgEntry[ cEntries ] ;    // Property ID/String pair 
} DICTIONARY ;
```

## <a name="dictionary-entry-structure"></a><span data-ttu-id="d24e6-107">Struktur der Wörterbucheinträge</span><span class="sxs-lookup"><span data-stu-id="d24e6-107">Dictionary Entry Structure</span></span>

<span data-ttu-id="d24e6-108">Jeder Wörterbucheintrag in der Liste ist ein Eigenschaften Bezeichner/Zeichen folgen Paar.</span><span class="sxs-lookup"><span data-stu-id="d24e6-108">Each dictionary entry in the list is a Property Identifier/String pair.</span></span> <span data-ttu-id="d24e6-109">Im folgenden finden Sie eine Pseudo Struktur Definition für einen Wörterbucheintrag.</span><span class="sxs-lookup"><span data-stu-id="d24e6-109">The following is a pseudo-structure definition for a dictionary entry.</span></span> <span data-ttu-id="d24e6-110">Es handelt sich um eine Pseudo Struktur, da der SZ- \[ \] Member eine Variable Größe hat.</span><span class="sxs-lookup"><span data-stu-id="d24e6-110">It's a pseudo-structure because the sz\[\] member is variable in size.</span></span>

``` syntax
typedef struct tagENTRY 
{ 
    DWORD  propid ;    // Property ID 
    DWORD  cch ;       // Count of characters in the string 
    char  sz[cch];     // Zero-terminated string 
} ENTRY ;
```

## <a name="sample-dictionary"></a><span data-ttu-id="d24e6-111">Beispiel Wörterbuch</span><span class="sxs-lookup"><span data-stu-id="d24e6-111">Sample Dictionary</span></span>

<span data-ttu-id="d24e6-112">Das folgende Beispiel für einen Börsendaten Transfer kann einen anzeigbaren Namen "Aktienkurs" für den gesamten Satz und "Ticker Symbol" für das PID- \_ Symbol enthalten.</span><span class="sxs-lookup"><span data-stu-id="d24e6-112">The following stock market data transfer example might include a displayable name "Stock Quote" for the entire set, and "Ticker Symbol" for PID\_SYMBOL.</span></span> <span data-ttu-id="d24e6-113">Wenn ein Eigenschaften Satz nur ein Symbol und das Wörterbuch enthielt, hat der Eigenschaften Satz Abschnitt einen Bytestream, der wie folgt aussieht.</span><span class="sxs-lookup"><span data-stu-id="d24e6-113">If a property set contained just a symbol and the dictionary, the property set section would have a byte stream that looked like the following.</span></span>

``` syntax
Offset     Bytes 
; Start of section 
0000    5C 01 00 00    ; DWORD size of section 
0004    04 00 00 00    ; DWORD number of properties in section 
 
; Start of PropID/Offset pairs 
0008    01 00 00 00    ; DWORD Property ID (1 == code page) 
000C    28 00 00 00    ; DWORD offset to property ID 
0010    00 00 00 80    ; DWORD Property ID (0x80000000 == locale
                                                 ID) 
0014    30 00 00 00    ; DWORD offset to property ID 
0018    00 00 00 00    ; DWORD Property ID (0 == dictionary) 
001C    38 00 00 00    ; DWORD offset to property ID 
0020    07 00 00 00    ; DWORD Property ID (7 == PID_SYMBOL)
0024    5C 01 00 00    ; DWORD offset to property ID
 
; Start of Property 1 (code page)
0028    01 00 00 00    ; DWORD type indicator (VT_12)
002C    B0 04          ; USHORT codepage (0x04b0 == 1200 ==
                                                 unicode)
002E    00 00          ; Pad to 32-bit boundary
 
; Start of Property 0x80000000 (Local ID)
0030    13 00 00 00    ; DWORD type indicator (VT_U14)
0034    09 04 00 00    ; ULONG locale ID (0x0409 == American 
                                                 English)
 
; Start of Property 0 (the dictionary)
0038    08 00 00 00    ; DWORD number of entries in dictionary
                             (Note:  No type indicator)
003C    00 00 00 00    ; DWORD propid == 0 (the dictionary)
0040    0C 00 00 00    ; DWORD cch == wcslen(L"Stock Quote") +
                                                 sizeof(L'\0') == 12
0044    L"Stock Quote" ; wchar_t wsz(12)
005C    05 00 00 00    ; DWORD propid == 5 (PID_HIGH)
0060    0B 00 00 00    ; DWORD cch == wcslen(L"High Price") + 
                                                 sizeof(L'\0') == 11
0064    L"High Price\0"; wchar_t wsz(11)
007A    00 00          ; padding for 32-bit alignment (necessary
                             because the codepage is unicode)
007C    07 00 00 00    ; DWORD propid == 7 (PID_SYMBOL)
0080    0E 00 00 00    ; DWORD cch - wcslen(L"Ticker Symbol\0") 
                             == 14
0084    L"Ticker Symbol\0" ; wchar_t wsz(14)
 
    // The dictionary would continue, but may not contain entries 
    // for every possible property, and may contain entries for 
    // properties that are not present. Entries are not required  
    // to be in order.
```

<span data-ttu-id="d24e6-114">Beachten Sie die folgenden Aspekte bezüglich der Eigenschaften Satz Wörterbücher:</span><span class="sxs-lookup"><span data-stu-id="d24e6-114">Be aware of the following issues regarding property set dictionaries:</span></span>

-   <span data-ttu-id="d24e6-115">Die eigen schafts-ID 0 weist keinen Typindikator auf.</span><span class="sxs-lookup"><span data-stu-id="d24e6-115">Property ID 0 does not have a type indicator.</span></span> <span data-ttu-id="d24e6-116">Der **DWORD** -Datentyp, der die Anzahl der Einträge angibt, die an der Typindikator Position liegen.</span><span class="sxs-lookup"><span data-stu-id="d24e6-116">The **DWORD** data type that indicates the count of entries sits in the type-indicator position.</span></span>
-   <span data-ttu-id="d24e6-117">Die Anzahl der Zeichen in der *CCH* -Zeichenfolge enthält das NULL Zeichen, das die Zeichenfolge beendet.</span><span class="sxs-lookup"><span data-stu-id="d24e6-117">The count of characters in the *cch* string includes the zero character that terminates the string.</span></span> <span data-ttu-id="d24e6-118">Wenn die Codepage des Eigenschaften Satzes nicht Unicode ist, ist dieses Feld tatsächlich eine **Byte** Anzahl.</span><span class="sxs-lookup"><span data-stu-id="d24e6-118">When the codepage of the property set is not Unicode, this field is actually a **byte** count.</span></span> <span data-ttu-id="d24e6-119">Bei Eigenschafts Sätzen mit der Format Version 0 darf diese Anzahl 256 nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="d24e6-119">For property sets with a format version of 0, this count may not exceed 256.</span></span> <span data-ttu-id="d24e6-120">Bei Eigenschafts Sätzen mit der Format Version 1 kann diese Anzahl so groß sein, wie Sie für die gesamte Eigenschaften Satz Größe zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="d24e6-120">For property sets with a format version of 1, this count may be as large as is allowed by the total property set size.</span></span>
-   <span data-ttu-id="d24e6-121">Das Wörterbuch ist optional.</span><span class="sxs-lookup"><span data-stu-id="d24e6-121">The dictionary is optional.</span></span> <span data-ttu-id="d24e6-122">Nicht alle Namen von Eigenschaften in der Gruppe müssen im Wörterbuch angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d24e6-122">Not all the names of properties in the set are required to appear in the dictionary.</span></span> <span data-ttu-id="d24e6-123">Umgekehrt sind nicht alle Namen im Wörterbuch erforderlich, um den Eigenschaften in der Menge zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d24e6-123">Conversely, not all names in the dictionary are required to correspond to properties in the set.</span></span> <span data-ttu-id="d24e6-124">Das Wörterbuch sollte Einträge für Eigenschaften weglassen, die von Anwendungen universell erkannt werden, die den Eigenschaften Satz ändern.</span><span class="sxs-lookup"><span data-stu-id="d24e6-124">The dictionary should omit entries for properties assumed to be universally recognized by applications manipulating the property set.</span></span> <span data-ttu-id="d24e6-125">In der Regel werden Namen für die Basis Eigenschaften Sätze für allgemein akzeptierte Standards ausgelassen, aber spezielle Eigenschaften Sätze können Wörterbücher für die Verwendung durch Browser enthalten.</span><span class="sxs-lookup"><span data-stu-id="d24e6-125">Typically, names for the base property sets for widely-accepted standards are omitted, but special-purpose property sets may include dictionaries for use by browsers.</span></span>
-   <span data-ttu-id="d24e6-126">Eigenschaftsnamen im Wörterbuch werden in der durch die eigen [schafts-ID 1](/windows/desktop/Stg/reserved-property-identifiers)aufgeführten Codepage gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d24e6-126">Property names in the dictionary are stored in the code page indicated by [Property ID 1](/windows/desktop/Stg/reserved-property-identifiers).</span></span> <span data-ttu-id="d24e6-127">Bei ANSI-Codepages wird jeder Wörterbucheintrag Byte bündig ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="d24e6-127">For ANSI code pages, each dictionary entry is byte-aligned.</span></span> <span data-ttu-id="d24e6-128">Folglich gibt es keinen Abstand zwischen den Eigenschaftsnamen mit der Eigenschaften-ID 0.</span><span class="sxs-lookup"><span data-stu-id="d24e6-128">Thus, there is no spacing between property names with Property ID 0.</span></span> <span data-ttu-id="d24e6-129">Dies ist der einzige Fall, in dem Werte von **DWORD** -Datentypen (die Eigenschaften-ID und die Eigenschafts Länge **DWORD** s) nicht an 32-Bit-Grenzen ausgerichtet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d24e6-129">This is the only case where values of **DWORD** data types (the property ID and property name-length **DWORD** s) are not required to be aligned on 32-bit boundaries.</span></span> <span data-ttu-id="d24e6-130">Bei Unicode-Seiten ist jeder Wörterbucheintrag 32-Bit-ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="d24e6-130">For Unicode pages, each dictionary entry is 32-bit aligned.</span></span>
-   <span data-ttu-id="d24e6-131">Eigenschaften Namen, die mit den binären Unicode-Zeichen 0x0001 bis 0x001F beginnen, sind für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="d24e6-131">Property names that begin with the binary Unicode characters 0x0001 through 0x001F are reserved for future use.</span></span>
-   <span data-ttu-id="d24e6-132">Der Eigenschaftsname, der der Eigenschaften-ID 0 zugeordnet ist, stellt den Namen des gesamten Eigenschaften Satzes dar.</span><span class="sxs-lookup"><span data-stu-id="d24e6-132">The property name associated with Property ID 0 represents the name of the entire property set.</span></span>

 

 