---
title: Namen in IStorage
description: Ein Eigenschaftensatz wird mit einem Formatbezeichner (FMTID) in der IPropertySetStorage-Schnittstelle identifiziert.
ms.assetid: 5f8eba37-c589-413e-9971-7ecb01dc6734
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e17b1125f642d3f24e24fa6040bc5e55ca3d48b2384aac551680b84c1496900f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662380"
---
# <a name="names-in-istorage"></a>Namen in IStorage

Ein Eigenschaftensatz wird mit einem Formatbezeichner (FMTID) in der [**IPropertySetStorage-Schnittstelle**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) identifiziert. In der [**IStorage-Schnittstelle**](/windows/desktop/api/Objidl/nn-objidl-istorage) wird ein Eigenschaftensatz mit einer unicode-Zeichenfolge mit NULL-Terminierung und einer maximalen Länge von 32 Zeichen benannt. Um die Interoperabilität zu ermöglichen, muss eine Zuordnung zwischen einer FMTID und einer entsprechenden auf NULL terminierten Unicode-Zeichenfolge eingerichtet werden.

## <a name="converting-a-property-set-from-a-fmtid-to-a-string-name"></a>Konvertieren eines Eigenschaftensets aus einer FMTID in einen Zeichenfolgennamen

Wenn Sie eine FMTID-Datei in einen entsprechenden Unicode-Zeichenfolgennamen konvertieren, überprüfen Sie zunächst, ob fmtid ein bekannter Wert ist, der in der folgenden Tabelle aufgeführt ist. Wenn dies der Wert ist, verwenden Sie den entsprechenden bekannten Zeichenfolgennamen.

| FMTID                                                                                | Zeichenfolgenname                       | Semantische                                                         |
|--------------------------------------------------------------------------------------|-----------------------------------|------------------------------------------------------------------|
| F29F85E0-4FF9-1068-AB91-08002B27B3D9                                                 | " \\ 005SummaryInformation"         | COM2-Zusammenfassungsinformationen                                         |
| D5CDD502-2E9C-101B-9397-08002B2CF9AE D5CDD505-2E9C-101B-9397-08002B2CF9AE<br/> | " \\ 005DocumentSummaryInformation" | Office Dokumentzusammenfassungsinformationen und benutzerdefinierte Eigenschaften. |



 

> [!Note]  
> Der **Eigenschaftensatz DocumentSummaryInformation** **und UserDefined** ist eindeutig, da er zwei Abschnitte enthält. Mehrere Abschnitte sind in einem anderen Eigenschaftensatz nicht zulässig. Weitere Informationen finden Sie unter [Structured Storage Serialized Property Set Format](structured-storage-serialized-property-set-format.md)und The [DocumentSummaryInformation and UserDefined Property Sets](the-documentsummaryinformation-and-userdefined-property-sets.md). Der erste Abschnitt wurde als Teil von COM definiert. die zweite wurde durch Microsoft Office.

 

Wenn fmtid kein bekannter Wert ist, verwenden Sie das folgende Verfahren, um einen Zeichenfolgennamen algorithmusisch zu bilden.

**So bilden Sie einen Zeichenfolgennamen algorithmisch**

1.  Konvertieren Sie die FMTID bei Bedarf in die Little-Endian-Byte reihenfolge.
2.  Nehmen Sie die 128 Bits des FMTID, und betrachten Sie sie als eine Long-Bit-Zeichenfolge, indem Sie jedes der Bytes miteinander verketten. Das erste Bit des 128-Bit-Werts ist das am wenigsten signifikante Bit des ersten Byte im Arbeitsspeicher des FMTID. Das letzte Bit des 128-Bit-Werts ist das wichtigste Bit des letzten Byte im Arbeitsspeicher der FMTID. Erweitern Sie diese 128 Bits auf 130 Bit, indem Sie am Ende zwei Nullbits hinzufügen.
3.  Teilen Sie die 130 Bits in Gruppen von fünf Bits auf. Es werden 26 solcher Gruppen verwendet. Betrachten Sie jede Gruppe als ganze Zahl mit umgekehrter Bit-Rangfolge. Beispielsweise ist das erste der 128 Bits das am wenigsten signifikante Bit der ersten Gruppe von fünf Bits. das fünfte der 128 Bits ist das wichtigste Bit der ersten Gruppe.
4.  Ordnen Sie jede dieser ganzen Zahlen als Index dem Array mit 32 Zeichen zu: ABCDEFGHLMNOPQRSTUVWXYZ012345. Dies ergibt eine Sequenz von 26 Unicode-Zeichen, die nur Großbuchstaben und Ziffern verwendet. Überlegungen zur Groß-/Kleinschreibung und zur Berücksichtigung der Groß-/Kleinschreibung sind nicht zu berücksichtigen, sodass jedes Zeichen in einem beliebigen Locale eindeutig ist.
5.  Erstellen Sie die endgültige Zeichenfolge, indem Sie die Zeichenfolge "005" mit einer Gesamtlänge von 27 Zeichen an den Front dieser \\ 26 Zeichen verketten.

Der folgende Beispielcode zeigt, wie eine FMTID einer Eigenschaftenzeichenfolge zuordnt.


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



## <a name="converting-a-property-set-from-a-string-name-to-a-fmtid"></a>Konvertieren eines Eigenschaftensets von einem Zeichenfolgennamen in eine FMTID

Konverter von Eigenschaftszeichenfolgennamen zu GUIDs sollten Kleinbuchstaben als Synonyme mit ihren Entsprechungen in Großbuchstaben akzeptieren.

Der folgende Beispielcode zeigt, wie sie eine Zuordnung von einer Eigenschaftenzeichenfolge zu einer FMTID ausführen.


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



Beim Versuch, einen vorhandenen Eigenschaftensatz zu öffnen, wird in [IPropertySetStorage::Open](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)der FMTID -Wert (root) in eine Zeichenfolge konvertiert, wie oben beschrieben. Wenn ein Element des [**IStorage-Elements**](/windows/desktop/api/Objidl/nn-objidl-istorage) dieses Namens vorhanden ist, wird es verwendet. Andernfalls schlägt das Öffnen fehl.

Beim Erstellen eines neuen Eigenschaftensets bestimmt die obige Zuordnung den verwendeten Zeichenfolgennamen.

 

 





