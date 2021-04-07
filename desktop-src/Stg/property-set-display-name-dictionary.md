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
# <a name="property-set-display-name-dictionary"></a>Eigenschaften Satz Anzeige Name-Wörterbuch

Mit einem Wörterbuch von Eigenschaften Anzeige Namen können Benutzer festlegen, dass die Bedeutung von Eigenschaften festgelegt werden soll, die über die des typindikators hinausgehen.

## <a name="dictionary-structure"></a>Wörterbuch Struktur

Das Wörterbuch enthält die Anzahl der Einträge in der Liste, gefolgt von einer Liste der Wörterbucheinträge.

``` syntax
typedef struct tagDICTIONARY 
{ 
    DWORD  cEntries ;               // Count of entries in the list 
    ENTRY  rgEntry[ cEntries ] ;    // Property ID/String pair 
} DICTIONARY ;
```

## <a name="dictionary-entry-structure"></a>Struktur der Wörterbucheinträge

Jeder Wörterbucheintrag in der Liste ist ein Eigenschaften Bezeichner/Zeichen folgen Paar. Im folgenden finden Sie eine Pseudo Struktur Definition für einen Wörterbucheintrag. Es handelt sich um eine Pseudo Struktur, da der SZ- \[ \] Member eine Variable Größe hat.

``` syntax
typedef struct tagENTRY 
{ 
    DWORD  propid ;    // Property ID 
    DWORD  cch ;       // Count of characters in the string 
    char  sz[cch];     // Zero-terminated string 
} ENTRY ;
```

## <a name="sample-dictionary"></a>Beispiel Wörterbuch

Das folgende Beispiel für einen Börsendaten Transfer kann einen anzeigbaren Namen "Aktienkurs" für den gesamten Satz und "Ticker Symbol" für das PID- \_ Symbol enthalten. Wenn ein Eigenschaften Satz nur ein Symbol und das Wörterbuch enthielt, hat der Eigenschaften Satz Abschnitt einen Bytestream, der wie folgt aussieht.

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

Beachten Sie die folgenden Aspekte bezüglich der Eigenschaften Satz Wörterbücher:

-   Die eigen schafts-ID 0 weist keinen Typindikator auf. Der **DWORD** -Datentyp, der die Anzahl der Einträge angibt, die an der Typindikator Position liegen.
-   Die Anzahl der Zeichen in der *CCH* -Zeichenfolge enthält das NULL Zeichen, das die Zeichenfolge beendet. Wenn die Codepage des Eigenschaften Satzes nicht Unicode ist, ist dieses Feld tatsächlich eine **Byte** Anzahl. Bei Eigenschafts Sätzen mit der Format Version 0 darf diese Anzahl 256 nicht überschreiten. Bei Eigenschafts Sätzen mit der Format Version 1 kann diese Anzahl so groß sein, wie Sie für die gesamte Eigenschaften Satz Größe zulässig ist.
-   Das Wörterbuch ist optional. Nicht alle Namen von Eigenschaften in der Gruppe müssen im Wörterbuch angezeigt werden. Umgekehrt sind nicht alle Namen im Wörterbuch erforderlich, um den Eigenschaften in der Menge zu entsprechen. Das Wörterbuch sollte Einträge für Eigenschaften weglassen, die von Anwendungen universell erkannt werden, die den Eigenschaften Satz ändern. In der Regel werden Namen für die Basis Eigenschaften Sätze für allgemein akzeptierte Standards ausgelassen, aber spezielle Eigenschaften Sätze können Wörterbücher für die Verwendung durch Browser enthalten.
-   Eigenschaftsnamen im Wörterbuch werden in der durch die eigen [schafts-ID 1](/windows/desktop/Stg/reserved-property-identifiers)aufgeführten Codepage gespeichert. Bei ANSI-Codepages wird jeder Wörterbucheintrag Byte bündig ausgerichtet. Folglich gibt es keinen Abstand zwischen den Eigenschaftsnamen mit der Eigenschaften-ID 0. Dies ist der einzige Fall, in dem Werte von **DWORD** -Datentypen (die Eigenschaften-ID und die Eigenschafts Länge **DWORD** s) nicht an 32-Bit-Grenzen ausgerichtet werden müssen. Bei Unicode-Seiten ist jeder Wörterbucheintrag 32-Bit-ausgerichtet.
-   Eigenschaften Namen, die mit den binären Unicode-Zeichen 0x0001 bis 0x001F beginnen, sind für die zukünftige Verwendung reserviert.
-   Der Eigenschaftsname, der der Eigenschaften-ID 0 zugeordnet ist, stellt den Namen des gesamten Eigenschaften Satzes dar.

 

 