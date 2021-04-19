---
description: Stellt Drucker Funktions Informationen dar.
ms.assetid: 70120739-a4e0-4b87-ac7a-40a42fb509ee
title: PRINTPROCESSOR_CAPS_2 Struktur (winspool. h)
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
ms.openlocfilehash: 1847ffa1912a8638476ce80dfbdb71c40fc376d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364120"
---
# <a name="printprocessor_caps_2-structure"></a>PrintProcessor \_ Caps \_ 2-Struktur

Stellt Drucker Funktions Informationen dar.

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

**dwlevel**
</dt> <dd>

Ein-Wert, der die Versionsnummer der-Struktur angibt.

</dd> <dt>

**dwnupoptions**
</dt> <dd>

Eine Bitmaske, die die verschiedenen Anzahl von Dokument Seiten darstellt, die der Drucker auf einer einzelnen Seite eines physischen Blatts drucken kann. Das unwichtigste Bit stellt eine Dokument Seite pro Seite dar, das nächste Bit stellt 2 Dokument Seiten pro Seite dar usw. Beispielsweise gibt 0x0000810b an, dass der Drucker jeweils 1, 2, 4, 9 und 16 Dokument Seiten pro physischer Seite unterstützt.

</dd> <dt>

**dwpaargeorderflags**
</dt> <dd>

Ein Flagwert, der die Reihenfolge angibt, in der Seiten gedruckt werden. Dabei kann es sich um einen **normalen \_ Druck**, einen **umgekehrten \_ Druck** **oder einen Druck Druck \_** handeln.

</dd> <dt>

**dwnumofkopien**
</dt> <dd>

Die maximale Anzahl von Kopien, die der Drucker verarbeiten kann.

</dd> <dt>

**dwnupdirectioncaps**
</dt> <dd>

Die verfügbaren Muster, wenn mehrere Dokument Seiten auf derselben Seite eines Papier Blatts gedruckt werden. Folgende Flags sind möglich:



| Wert                     | Bedeutung                                                                                             |
|---------------------------|-----------------------------------------------------------------------------------------------------|
| ppcaps \_ direkt \_ \_ nach unten | Die Seiten werden in Zeilen von rechts nach links angezeigt, und jede nachfolgende Zeile unter dem Vorgänger.                 |
| ppcaps \_ nach \_ \_ Rechts | Seiten werden in Spalten von oben nach unten angezeigt, wobei jede nachfolgende Spalte rechts neben dem Vorgänger angezeigt wird. |
| ppcaps \_ Links \_ \_ unten  | Die Seiten werden in Zeilen von links nach rechts angezeigt, und jede nachfolgende Zeile unter dem Vorgänger.                 |
| ppcaps \_ nach \_ \_ Links  | Seiten werden in Spalten von oben nach unten angezeigt, wobei jede nachfolgende Spalte links vom Vorgänger angezeigt wird.  |



 

</dd> <dt>

**dwnupbordercaps**
</dt> <dd>

Kann nur ein ppcaps-Rahmen \_ \_ Druck sein, was bedeutet, dass beim Drucken mehrerer Dokument Seiten auf einer einzelnen Seite eines physischen Blatts der Drucker informiert werden kann, ob ein Rahmen um den Druckbereich der einzelnen Dokument Seiten gedruckt werden soll.

</dd> <dt>

**dwbooklethandlingcaps**
</dt> <dd>

Es kann nur ein ppcaps-Formatierungs \_ \_ Rand angegeben werden, der angibt, dass der Drucker den Schrift Schnitt drucken kann

</dd> <dt>**dwduplexhandlingcaps**</dt> <dd> 

| Wert                                         | Bedeutung                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ppcaps \_ umgekehrter \_ Seiten \_ für \_ Reverse- \_ Duplex  | Beim Drucken in umgekehrter Reihenfolge und Duplexing kann der Prozessor die Reihenfolge der einzelnen Seiten Paare austauschen, sodass Sie nicht in der Reihenfolge 4, 3, 2, 1 gedruckt werden, sondern in der Reihenfolge 3, 4, 1, 2.                                                                                                       |
| ppcaps \_ \_ senden keine \_ zusätzlichen \_ Seiten \_ für \_ Duplex | Beim Duplexing kann dem Druck Prozessor mitgeteilt werden, dass keine zusätzliche Seite gesendet wird, wenn eine ungerade Anzahl von Dokument Seiten vorhanden ist. Der Prozessor berücksichtigt den Wert so gut wie möglich. in Fällen, in denen das verhindern einer zusätzlichen leeren Seite zu einer unsachgemäßen Ausgabe führen würde, werden die zusätzlichen Seiten möglicherweise dennoch gesendet. |



 

</dd> <dt>

**dwscalingcaps**
</dt> <dd>

Kann nur eine quadratische Skalierung mit ppcaps sein \_ \_ , was darauf hinweist, dass der Drucker das Seitenbild skalieren kann.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Werte für alle Strukturmember werden von der Funktion **getprintprocessorfunctions** bereitgestellt, die im Windows-Treiberkit dokumentiert ist.

Wenn eine Anwendung [**getprinterdata**](getprinterdata.md)aufruft, ruft der Spooler die **getprintprocessorfunctions** -Funktion eines Druck Prozessors auf und gibt einen Wertnamen an, der das Format **printproccaps \_**_Datentyp_ hat, wobei *Datentyp* der Name eines Eingabe Datentyps ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Getprinterdata**](getprinterdata.md)
</dt> </dl>

 

 




