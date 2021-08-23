---
description: Stellt Druckerfunktionsinformationen dar.
ms.assetid: 70120739-a4e0-4b87-ac7a-40a42fb509ee
title: PRINTPROCESSOR_CAPS_2-Struktur (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_CAPS_2
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 3425f9477b153721980e3bb44b919b0baea37aa645caea6a3ee328a9ff923eb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824731"
---
# <a name="printprocessor_caps_2-structure"></a>PRINTPROCESSOR \_ CAPS \_ 2-Struktur

Stellt Druckerfunktionsinformationen dar.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PRINTPROCESSOR_CAPS_2 {
  DWORD dwLevel;
  DWORD dwNupOptions;
  DWORD dwPageOrderFlags;
  DWORD dwNumberOfCopies;
  DWORD dwNupDirectionCaps;
  DWORD dwNupBorderCaps;
  DWORD dwBookletHandlingCaps;
  DWORD dwDuplexHandlingCaps;
  DWORD dwScalingCaps;
} PRINTPROCESSOR_CAPS_2, *PPRINTPROCESSOR_CAPS_2;
```



## <a name="members"></a>Member

<dl> <dt>

**dwLevel**
</dt> <dd>

Ein -Wert, der die Versionsnummer der Struktur angibt.

</dd> <dt>

**dwNupOptions**
</dt> <dd>

Eine Bitmaske, die die verschiedenen Dokumentseiten darstellt, die der Drucker auf einer einzelnen Seite eines physischen Blatts drucken kann. Das am wenigsten signifikante Bit stellt eine Dokumentseite pro Seite dar, das nächste Bit stellt 2 Dokumentseiten pro Seite dar usw. Beispielsweise gibt 0x0000810B an, dass der Drucker 1, 2, 4, 9 und 16 Dokumentseiten pro physischer Seite unterstützt.

</dd> <dt>

**dwPageOrderFlags**
</dt> <dd>

Ein Flagwert, der die Reihenfolge angibt, in der Seiten gedruckt werden. Dies kann **NORMAL \_ PRINT,** **REVERSE \_ PRINT** oder **PRINT \_ PRINT** sein.

</dd> <dt>

**dwNumberOfCopies**
</dt> <dd>

Die maximale Anzahl von Kopien, die der Drucker verarbeiten kann.

</dd> <dt>

**dwNupDirectionCaps**
</dt> <dd>

Die verfügbaren Muster, wenn mehrere Dokumentseiten auf der gleichen Seite eines Papierblatts gedruckt werden. Folgende Flags sind möglich:



| Wert                     | Bedeutung                                                                                             |
|---------------------------|-----------------------------------------------------------------------------------------------------|
| PPCAPS \_ RECHTS UND DANN NACH \_ \_ UNTEN | Seiten werden in Zeilen von rechts nach links angezeigt, jede nachfolgende Zeile unterhalb ihres Vorgängers.                 |
| PPCAPS \_ NACH UNTEN UND \_ RECHTS \_ | Seiten werden in Spalten von oben nach unten angezeigt, jede nachfolgende Spalte rechts neben ihrem Vorgänger. |
| PPCAPS \_ NACH LINKS UND \_ \_ UNTEN  | Seiten werden in Zeilen von links nach rechts angezeigt, jede nachfolgende Zeile unterhalb ihres Vorgängers.                 |
| PPCAPS \_ NACH UNTEN UND DANN \_ \_ LINKS  | Seiten werden in Spalten von oben nach unten angezeigt, jede nachfolgende Spalte links neben ihrem Vorgänger.  |



 

</dd> <dt>

**dwNupBorderCaps**
</dt> <dd>

Kann nur PPCAPS BORDER PRINT sein. Dies bedeutet, dass dem Drucker mitgeteilt \_ \_ werden kann, ob ein Rahmen um den bildbaren Bereich der einzelnen Dokumentseiten gedruckt werden soll, wenn mehrere Dokumentseiten auf einer einzelnen Seite eines physischen Blatts gedruckt werden.

</dd> <dt>

**dwBookletHandlingCaps**
</dt> <dd>

Kann nur PPCAPS \_ PRINTER \_ EDGE sein, was darauf hinweist, dass der Drucker Druckstile drucken kann.

</dd> <dt>**dwDuplexHandlingCaps**</dt> <dd> 

| Wert                                         | Bedeutung                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PPCAPS \_ REVERSE PAGES FÜR REVERSE \_ \_ \_ \_ DUPLEX  | Beim Drucken in umgekehrter Reihenfolge und beim Duplexing kann der Prozessor die Reihenfolge der einzelnen Seitenpaare austauschen. Anstatt also in der Reihenfolge 4,3,2,1 zu drucken, werden sie in der Reihenfolge 3,4,1,2 gedruckt.                                                                                                       |
| PPCAPS \_ SENDEN KEINE \_ \_ \_ ZUSÄTZLICHEN SEITEN FÜR \_ \_ DUPLEX | Beim Duplexing kann der Druckprozessor angewiesen werden, keine zusätzliche Seite zu senden, wenn eine ungerade Anzahl von Dokumentseiten vorhanden ist. Der Prozessor berücksichtigt den Wert so gut wie es geht. In Fällen, in denen das Verhindern einer zusätzlichen leeren Seite zu einer falschen Ausgabe führen würde, werden die zusätzlichen Seiten möglicherweise trotzdem gesendet. |



 

</dd> <dt>

**dwScalingCaps**
</dt> <dd>

Kann nur PPCAPS \_ SQUARE \_ SCALING sein, was angibt, dass der Drucker das Seitenbild skalieren kann.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Werte für alle Strukturmember werden von der **GetPrintProcessorCapabilities-Funktion** bereitgestellt, die im Windows Driver Kit dokumentiert ist.

Wenn eine Anwendung [**GetPrinterData**](getprinterdata.md)aufruft, ruft der Spooler die **GetPrintProcessorCapabilities-Funktion** eines Druckprozessors auf und gibt einen Wertnamen mit dem Format **\_ PrintProcCaps-Datentyp** an, wobei *datatype* der Name eines Eingabedatentyps ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**GetPrinterData**](getprinterdata.md)
</dt> </dl>

 

 




