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
# <a name="names-in-istorage"></a>Namen in IStorage

Ein Eigenschaften Satz wird in der [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) -Schnittstelle mit einem Format Bezeichner (fmtid) identifiziert. In der [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Schnittstelle wird ein Eigenschaften Satz mit einer null-terminierten Unicode-Zeichenfolge mit einer maximalen Länge von 32 Zeichen benannt. Um die Interoperabilität zu aktivieren, muss eine Zuordnung zwischen einer fmtid und einer entsprechenden mit NULL endenden Unicode-Zeichenfolge eingerichtet werden.

## <a name="converting-a-property-set-from-a-fmtid-to-a-string-name"></a>Wandeln Sie einen Eigenschaften Satz von einer fmtid in einen Zeichen folgen Namen um.

Wenn Sie von einer fmtid in einen entsprechenden Unicode-Zeichen folgen Namen umrechnen, überprüfen Sie zunächst, ob fmtid ein bekannter Wert ist, der in der folgenden Tabelle aufgeführt ist. Wenn dies der Fall ist, verwenden Sie den entsprechenden bekannten Zeichen folgen Namen.

| FMTID                                                                                | Zeichenfolgenname                       | Tischer                                                         |
|--------------------------------------------------------------------------------------|-----------------------------------|------------------------------------------------------------------|
| F29F85E0-4FF9-1068-AB91-08002B27B3D9                                                 | " \\ 005summaryinformation"         | COM2 Zusammenfassungs Informationen                                         |
| D5CDD502-2E9C-101B-9397-08002B2CF9AE D5CDD505-2E9C-101B-9397-08002B2CF9AE<br/> | " \\ 005documentsummaryinformation" | Zusammenfassende Informationen zu Office-Dokumenten und benutzerdefinierte Eigenschaften. |



 

> [!Note]  
> Die Eigenschaften Sätze " **documentsummaryinformation** " und " **UserDefined** " sind insofern eindeutig, als Sie zwei Abschnitte enthalten. In keinem anderen Eigenschaften Satz sind mehrere Abschnitte zulässig. Weitere Informationen finden Sie unter [Format des serialisierten genserialisierten Speichers](structured-storage-serialized-property-set-format.md)und [der Eigenschaften Sätze "documentsummaryinformation" und "UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md)". Der erste Abschnitt wurde als Teil von com definiert. die zweite wurde durch Microsoft Office definiert.

 

Wenn die fmtid kein bekannter Wert ist, verwenden Sie das folgende Verfahren, um einen Zeichen folgen Namen algorithmisch zu bilden.

**So bilden Sie einen Zeichen folgen Namen algorithmisch**

1.  Konvertieren Sie ggf. die fmtid in eine Little-Endian-Byte Reihenfolge.
2.  Nehmen Sie die 128 Bits der fmtid, und betrachten Sie Sie als eine lange Bitzeichenfolge, indem Sie die einzelnen Bytes miteinander verketten. Das erste Bit des 128-Bit-Werts ist das am wenigsten bedeutende Bit des ersten Bytes im Arbeitsspeicher der fmtid. das letzte Bit des 128-Bit-Werts ist das signifikanteste Bit des letzten Bytes im Arbeitsspeicher der fmtid. Erweitern Sie diese 128 Bits auf 130 Bits, indem Sie zwei Bits am Ende hinzufügen.
3.  Dividieren Sie die 130 Bits in Gruppen mit fünf Bits. Es gibt 26 solche Gruppen. Stellen Sie jede Gruppe als ganze Zahl mit umgekehrter bitrangfolge in Erwägung. Beispielsweise ist das erste der 128 Bits das am wenigsten bedeutende Bit der ersten Gruppe von fünf Bits. das fünfte der 128 Bits ist das signifikanteste Bit der ersten Gruppe.
4.  Ordnen Sie die einzelnen ganzen Zahlen als Index dem Array von 32 Zeichen zu: ABCDEFGHIJKLMNOPQRSTUVWXYZ012345. Dies ergibt eine Sequenz von 26 Unicode-Zeichen, die nur Großbuchstaben und Ziffern verwendet. Überlegungen zur Groß-/Kleinschreibung sollten nicht beachtet werden, sodass jedes Zeichen in jedem Gebiets Schema eindeutig ist.
5.  Erstellen Sie die endgültige Zeichenfolge, indem Sie die Zeichenfolge " \\ 005" an der Vorderseite dieser 26 Zeichen mit einer Gesamtlänge von 27 Zeichen verketten.

Der folgende Beispielcode zeigt, wie Sie eine Zuordnung von einer fmtid zu einer Eigenschaften Zeichenfolge durch sehen.


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



## <a name="converting-a-property-set-from-a-string-name-to-a-fmtid"></a>Wandeln eines Eigenschaften Satzes von einem Zeichen folgen Namen in eine fmtid

Konverter von Eigenschafts Zeichenfolgen-Namen an GUIDs sollten Kleinbuchstaben als Synonym mit ihren Großbuchstaben akzeptieren.

Der folgende Beispielcode zeigt, wie Sie eine Zuordnung von einer Eigenschafts Zeichenfolge zu einer fmtid durch sehen.


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



Wenn Sie versuchen, einen vorhandenen Eigenschaften Satz zu öffnen, wird in [IPropertySetStorage:: Open](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)die (root) fmtid wie oben beschrieben in eine Zeichenfolge konvertiert. Wenn ein [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Element mit diesem Namen vorhanden ist, wird es verwendet. Andernfalls schlägt das Öffnen fehl.

Wenn Sie einen neuen Eigenschaften Satz erstellen, bestimmt die oben genannte Zuordnung den verwendeten Zeichen folgen Namen.

 

 





