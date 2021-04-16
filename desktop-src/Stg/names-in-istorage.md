---
title: Namen in IStorage
description: Ein Eigenschaften Satz wird in der IPropertySetStorage-Schnittstelle mit einem Format Bezeichner (fmtid) identifiziert.
ms.assetid: 5f8eba37-c589-413e-9971-7ecb01dc6734
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cef9417f2f5fad7fd17dcc3d431f1d3565a3843
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516112"
---
# <a name="names-in-istorage"></a><span data-ttu-id="677cc-103">Namen in IStorage</span><span class="sxs-lookup"><span data-stu-id="677cc-103">Names in IStorage</span></span>

<span data-ttu-id="677cc-104">Ein Eigenschaften Satz wird in der [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) -Schnittstelle mit einem Format Bezeichner (fmtid) identifiziert.</span><span class="sxs-lookup"><span data-stu-id="677cc-104">A property set is identified with a format identifier (FMTID) in the [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interface.</span></span> <span data-ttu-id="677cc-105">In der [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Schnittstelle wird ein Eigenschaften Satz mit einer null-terminierten Unicode-Zeichenfolge mit einer maximalen Länge von 32 Zeichen benannt.</span><span class="sxs-lookup"><span data-stu-id="677cc-105">In the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface, a property set is named with a null-terminated Unicode string with a maximum length of 32 characters.</span></span> <span data-ttu-id="677cc-106">Um die Interoperabilität zu aktivieren, muss eine Zuordnung zwischen einer fmtid und einer entsprechenden mit NULL endenden Unicode-Zeichenfolge eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="677cc-106">To enable interoperability, a mapping between an FMTID and a corresponding null-terminated Unicode string must be established.</span></span>

## <a name="converting-a-property-set-from-a-fmtid-to-a-string-name"></a><span data-ttu-id="677cc-107">Wandeln Sie einen Eigenschaften Satz von einer fmtid in einen Zeichen folgen Namen um.</span><span class="sxs-lookup"><span data-stu-id="677cc-107">Converting a property set from a FMTID to a string name</span></span>

<span data-ttu-id="677cc-108">Wenn Sie von einer fmtid in einen entsprechenden Unicode-Zeichen folgen Namen umrechnen, überprüfen Sie zunächst, ob fmtid ein bekannter Wert ist, der in der folgenden Tabelle aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="677cc-108">When converting from an FMTID to a corresponding Unicode string name, first verify that the FMTID is a well-known value, listed in the following table.</span></span> <span data-ttu-id="677cc-109">Wenn dies der Fall ist, verwenden Sie den entsprechenden bekannten Zeichen folgen Namen.</span><span class="sxs-lookup"><span data-stu-id="677cc-109">If so, then use the corresponding well-known string name.</span></span>

| <span data-ttu-id="677cc-110">FMTID</span><span class="sxs-lookup"><span data-stu-id="677cc-110">FMTID</span></span>                                                                                | <span data-ttu-id="677cc-111">Zeichenfolgenname</span><span class="sxs-lookup"><span data-stu-id="677cc-111">String name</span></span>                       | <span data-ttu-id="677cc-112">Tischer</span><span class="sxs-lookup"><span data-stu-id="677cc-112">Semantic</span></span>                                                         |
|--------------------------------------------------------------------------------------|-----------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="677cc-113">F29F85E0-4FF9-1068-AB91-08002B27B3D9</span><span class="sxs-lookup"><span data-stu-id="677cc-113">F29F85E0-4FF9-1068-AB91-08002B27B3D9</span></span>                                                 | <span data-ttu-id="677cc-114">" \\ 005summaryinformation"</span><span class="sxs-lookup"><span data-stu-id="677cc-114">"\\005SummaryInformation"</span></span>         | <span data-ttu-id="677cc-115">COM2 Zusammenfassungs Informationen</span><span class="sxs-lookup"><span data-stu-id="677cc-115">COM2 summary information</span></span>                                         |
| <span data-ttu-id="677cc-116">D5CDD502-2E9C-101B-9397-08002B2CF9AE D5CDD505-2E9C-101B-9397-08002B2CF9AE</span><span class="sxs-lookup"><span data-stu-id="677cc-116">D5CDD502-2E9C-101B-9397-08002B2CF9AE D5CDD505-2E9C-101B-9397-08002B2CF9AE</span></span><br/> | <span data-ttu-id="677cc-117">" \\ 005documentsummaryinformation"</span><span class="sxs-lookup"><span data-stu-id="677cc-117">"\\005DocumentSummaryInformation"</span></span> | <span data-ttu-id="677cc-118">Zusammenfassende Informationen zu Office-Dokumenten und benutzerdefinierte Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="677cc-118">Office document summary information and user-defined properties.</span></span> |



 

> [!Note]  
> <span data-ttu-id="677cc-119">Die Eigenschaften Sätze " **documentsummaryinformation** " und " **UserDefined** " sind insofern eindeutig, als Sie zwei Abschnitte enthalten.</span><span class="sxs-lookup"><span data-stu-id="677cc-119">The **DocumentSummaryInformation** and **UserDefined** property set is unique in that it contains two sections.</span></span> <span data-ttu-id="677cc-120">In keinem anderen Eigenschaften Satz sind mehrere Abschnitte zulässig.</span><span class="sxs-lookup"><span data-stu-id="677cc-120">Multiple sections are not permitted in any other property set.</span></span> <span data-ttu-id="677cc-121">Weitere Informationen finden Sie unter [Format des serialisierten genserialisierten Speichers](structured-storage-serialized-property-set-format.md)und [der Eigenschaften Sätze "documentsummaryinformation" und "UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md)".</span><span class="sxs-lookup"><span data-stu-id="677cc-121">For more information, see [Structured Storage Serialized Property Set Format](structured-storage-serialized-property-set-format.md), and [The DocumentSummaryInformation and UserDefined Property Sets](the-documentsummaryinformation-and-userdefined-property-sets.md).</span></span> <span data-ttu-id="677cc-122">Der erste Abschnitt wurde als Teil von com definiert. die zweite wurde durch Microsoft Office definiert.</span><span class="sxs-lookup"><span data-stu-id="677cc-122">The first section was defined as part of COM; the second was defined by Microsoft Office.</span></span>

 

<span data-ttu-id="677cc-123">Wenn die fmtid kein bekannter Wert ist, verwenden Sie das folgende Verfahren, um einen Zeichen folgen Namen algorithmisch zu bilden.</span><span class="sxs-lookup"><span data-stu-id="677cc-123">If the FMTID is not a well-known value, then use the following procedure to algorithmically form a string name.</span></span>

<span data-ttu-id="677cc-124">**So bilden Sie einen Zeichen folgen Namen algorithmisch**</span><span class="sxs-lookup"><span data-stu-id="677cc-124">**To algorithmically form a string name**</span></span>

1.  <span data-ttu-id="677cc-125">Konvertieren Sie ggf. die fmtid in eine Little-Endian-Byte Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="677cc-125">Convert the FMTID to little-endian byte order, if necessary.</span></span>
2.  <span data-ttu-id="677cc-126">Nehmen Sie die 128 Bits der fmtid, und betrachten Sie Sie als eine lange Bitzeichenfolge, indem Sie die einzelnen Bytes miteinander verketten.</span><span class="sxs-lookup"><span data-stu-id="677cc-126">Take the 128 bits of the FMTID and consider them as one long bit string by concatenating each of the bytes together.</span></span> <span data-ttu-id="677cc-127">Das erste Bit des 128-Bit-Werts ist das am wenigsten bedeutende Bit des ersten Bytes im Arbeitsspeicher der fmtid. das letzte Bit des 128-Bit-Werts ist das signifikanteste Bit des letzten Bytes im Arbeitsspeicher der fmtid.</span><span class="sxs-lookup"><span data-stu-id="677cc-127">The first bit of the 128 bit value is the least significant bit of the first byte in memory of the FMTID; the last bit of the 128 bit value is the most significant bit of the last byte in memory of the FMTID.</span></span> <span data-ttu-id="677cc-128">Erweitern Sie diese 128 Bits auf 130 Bits, indem Sie zwei Bits am Ende hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="677cc-128">Extend these 128 bits to 130 bits by adding two zero bits to the end.</span></span>
3.  <span data-ttu-id="677cc-129">Dividieren Sie die 130 Bits in Gruppen mit fünf Bits. Es gibt 26 solche Gruppen.</span><span class="sxs-lookup"><span data-stu-id="677cc-129">Divide the 130 bits into groups of five bits; there will be 26 such groups.</span></span> <span data-ttu-id="677cc-130">Stellen Sie jede Gruppe als ganze Zahl mit umgekehrter bitrangfolge in Erwägung.</span><span class="sxs-lookup"><span data-stu-id="677cc-130">Consider each group as an integer with reversed bit precedence.</span></span> <span data-ttu-id="677cc-131">Beispielsweise ist das erste der 128 Bits das am wenigsten bedeutende Bit der ersten Gruppe von fünf Bits. das fünfte der 128 Bits ist das signifikanteste Bit der ersten Gruppe.</span><span class="sxs-lookup"><span data-stu-id="677cc-131">For example, the first of the 128 bits is the least significant bit of the first group of five bits; the fifth of the 128 bits is the most significant bit of the first group.</span></span>
4.  <span data-ttu-id="677cc-132">Ordnen Sie die einzelnen ganzen Zahlen als Index dem Array von 32 Zeichen zu: ABCDEFGHIJKLMNOPQRSTUVWXYZ012345.</span><span class="sxs-lookup"><span data-stu-id="677cc-132">Map each of these integers as an index into the array of thirty-two characters: ABCDEFGHIJKLMNOPQRSTUVWXYZ012345.</span></span> <span data-ttu-id="677cc-133">Dies ergibt eine Sequenz von 26 Unicode-Zeichen, die nur Großbuchstaben und Ziffern verwendet.</span><span class="sxs-lookup"><span data-stu-id="677cc-133">This yields a sequence of 26 Unicode characters that uses only uppercase characters and numerals.</span></span> <span data-ttu-id="677cc-134">Überlegungen zur Groß-/Kleinschreibung sollten nicht beachtet werden, sodass jedes Zeichen in jedem Gebiets Schema eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="677cc-134">Case sensitive and case insensitive considerations do not apply, causing each character to be unique in any locale.</span></span>
5.  <span data-ttu-id="677cc-135">Erstellen Sie die endgültige Zeichenfolge, indem Sie die Zeichenfolge " \\ 005" an der Vorderseite dieser 26 Zeichen mit einer Gesamtlänge von 27 Zeichen verketten.</span><span class="sxs-lookup"><span data-stu-id="677cc-135">Create the final string by concatenating the string "\\005" onto the front of these 26 characters, for a total length of 27 characters.</span></span>

<span data-ttu-id="677cc-136">Der folgende Beispielcode zeigt, wie Sie eine Zuordnung von einer fmtid zu einer Eigenschaften Zeichenfolge durch sehen.</span><span class="sxs-lookup"><span data-stu-id="677cc-136">The following example code shows how to map from an FMTID to a property string.</span></span>


```C++
#define CBIT_BYTE        8
#define CBIT_CHARMASK    5
#define CCH_MAP          (1 << CBIT_CHARMASK)    // 32
#define CHARMASK         (CCH_MAP - 1)           // 0x1f
 
CHAR awcMap[CCH_MAP + 1] = "abcdefghijklmnopqrstuvwxyz012345";
 
WCHAR MapChar(ULONG I) {
    return((WCHAR) awcMap[i & CHARMASK]);
    }
 
VOID GuidToPropertyStringName(GUID *pguid, WCHAR awcname[]) {
    BYTE *pb = (BYTE *) pguid;
    BYTE *pbEnd = pb + sizeof(*pguid);
    ULONG cbitRemain = CBIT_BYTE;
    WCHAR *pwc = awcname;
 
    *pwc++ = ((WCHAR) 0x0005);
    while (pb < pbEnd) {
        ULONG i = *pb >> (CBIT_BYTE - cbitRemain);
        if (cbitRemain >= CBIT_CHARMASK) {
            *pwc = MapChar(i);
            if (cbitRemain == CBIT_BYTE && 
                                    *pwc >= L'a' && *pwc <= L'z')
                {
                *pwc += (WCHAR) (L'A' - L'a');
                }
            pwc++;
            cbitRemain -= CBIT_CHARMASK;
            if (cbitRemain == 0) {
                pb++;
                cbitRemain = CBIT_BYTE;
                }
            }
        else {
            if (++pb < pbEnd) {
                i |= *pb << cbitRemain;
                }
            *pwc++ = MapChar(i);
            cbitRemain += CBIT_BYTE - CBIT_CHARMASK;
            }
        }
    *pwc = L'\0';
    }
```



## <a name="converting-a-property-set-from-a-string-name-to-a-fmtid"></a><span data-ttu-id="677cc-137">Wandeln eines Eigenschaften Satzes von einem Zeichen folgen Namen in eine fmtid</span><span class="sxs-lookup"><span data-stu-id="677cc-137">Converting a property set from a string name to a FMTID</span></span>

<span data-ttu-id="677cc-138">Konverter von Eigenschafts Zeichenfolgen-Namen an GUIDs sollten Kleinbuchstaben als Synonym mit ihren Großbuchstaben akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="677cc-138">Converters of property string names to GUIDs should accept lowercase letters as synonymous with their uppercase counterparts.</span></span>

<span data-ttu-id="677cc-139">Der folgende Beispielcode zeigt, wie Sie eine Zuordnung von einer Eigenschafts Zeichenfolge zu einer fmtid durch sehen.</span><span class="sxs-lookup"><span data-stu-id="677cc-139">The following example code shows how to map from a property string to an FMTID.</span></span>


```C++
#include "stdafx.h"
#define _INC_OLE
#include <windows.h>
#include <stdlib.h>
#include <stdio.h>
#include <string.h>
#include <ctype.h>
#define CBIT_CHARMASK 5
#define CBIT_BYTE     8
#define CBIT_GUID    (CBIT_BYTE * sizeof(GUID))
#define CWC_PROPSET  (1 + (CBIT_GUID + CBIT_CHARMASK-1)/CBIT_CHARMASK)
#define WC_PROPSET0  ((WCHAR) 0x0005)
#define CCH_MAP      (1 << CBIT_CHARMASK)        // 32
#define CHARMASK     (CCH_MAP - 1)            // 0x1f
CHAR awcMap[CCH_MAP + 1] = "abcdefghijklmnopqrstuvwxyz012345";
#define CALPHACHARS  ('z' - 'a' + 1)

GUID guidSummary =
{ 0xf29f85e0,0x4ff9, 0x1068,
{ 0xab, 0x91, 0x08, 0x00, 0x2b, 0x27, 0xb3, 0xd9 } };

WCHAR wszSummary[] = L"SummaryInformation";

GUID guidDocumentSummary =
    { 0xd5cdd502,
      0x2e9c, 0x101b,
      { 0x93, 0x97, 0x08, 0x00, 0x2b, 0x2c, 0xf9, 0xae } };

WCHAR wszDocumentSummary[] = L"DocumentSummaryInformation";
__inline WCHAR

MapChar(IN ULONG i)
{
    return((WCHAR) awcMap[i & CHARMASK]);
}

ULONG PropertySetNameToGuid(
    IN ULONG cwcname,
    IN WCHAR const awcname[],
    OUT GUID *pguid)
{
    ULONG Status = ERROR_INVALID_PARAMETER;
    WCHAR const *pwc = awcname;

    if (pwc[0] == WC_PROPSET0)
    {
        //Note: cwcname includes the WC_PROPSET0, and
        //sizeof(wsz...) includes the trailing L'\0', but
        //the comparison excludes both the leading
        //WC_PROPSET0 and the trailing L'\0'.
        if (cwcname == sizeof(wszSummary)/sizeof(WCHAR) &&
            wcsnicmp(&pwc[1], wszSummary, cwcname - 1) == 0)
        {
            *pguid = guidSummary;
            return(NO_ERROR);
        }
        if (cwcname == CWC_PROPSET)
        {
            ULONG cbit;
            BYTE *pb = (BYTE *) pguid - 1;
            ZeroMemory(pguid, sizeof(*pguid));
            for (cbit = 0; cbit < CBIT_GUID; cbit += 
            CBIT_CHARMASK)
            {
                ULONG cbitUsed = cbit % CBIT_BYTE;
                ULONG cbitStored;
                WCHAR wc;
                if (cbitUsed == 0)
                {
                    pb++;
                }
                wc = *++pwc - L'A';        //assume uppercase
                if (wc > CALPHACHARS)
                {
                    wc += (WCHAR) (L'A' - L'a'); //try lowercase
                    if (wc > CALPHACHARS)
                    {
                        wc += L'a' - L'0' + CALPHACHARS; 
                        if (wc > CHARMASK)
                        {
                            goto fail;       //invalid character
                        }
                    }
                }
                *pb |= (BYTE) (wc << cbitUsed);
                cbitStored = min(CBIT_BYTE - cbitUsed, 
                CBIT_CHARMASK);

                //If the translated bits will not fit in the 
                //current byte
                if (cbitStored < CBIT_CHARMASK)
                {
                    wc >>= CBIT_BYTE - cbitUsed;
                    if (cbit + cbitStored == CBIT_GUID)
                    {
                       if (wc != 0)
                       {
                           goto fail;        //extra bits
                       }
                       break;
                    }
                    pb++;
                    *pb |= (BYTE) wc;
                }
           }
           Status = NO_ERROR;
      }
    }
fail:
    return(Status);
}
```



<span data-ttu-id="677cc-140">Wenn Sie versuchen, einen vorhandenen Eigenschaften Satz zu öffnen, wird in [IPropertySetStorage:: Open](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)die (root) fmtid wie oben beschrieben in eine Zeichenfolge konvertiert.</span><span class="sxs-lookup"><span data-stu-id="677cc-140">When attempting to open an existing property set, in [IPropertySetStorage::Open](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open), the (root) FMTID is converted to a string as described above.</span></span> <span data-ttu-id="677cc-141">Wenn ein [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Element mit diesem Namen vorhanden ist, wird es verwendet.</span><span class="sxs-lookup"><span data-stu-id="677cc-141">If an element of the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) of that name exists, it is used.</span></span> <span data-ttu-id="677cc-142">Andernfalls schlägt das Öffnen fehl.</span><span class="sxs-lookup"><span data-stu-id="677cc-142">Otherwise, the open fails.</span></span>

<span data-ttu-id="677cc-143">Wenn Sie einen neuen Eigenschaften Satz erstellen, bestimmt die oben genannte Zuordnung den verwendeten Zeichen folgen Namen.</span><span class="sxs-lookup"><span data-stu-id="677cc-143">When creating a new property set, the above mapping determines the string name used.</span></span>

 

 





