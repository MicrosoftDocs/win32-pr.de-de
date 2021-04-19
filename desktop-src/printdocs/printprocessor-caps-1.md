---
description: Die PrintProcessor \_ Caps \_ 1-Struktur ist das Format für die Drucker Funktions Informationen, die von der getprinterdata-Funktion in dem Puffer zurückgegeben werden, der von der pData-Variablen angegeben wird.
ms.assetid: 43c568ff-ccc9-4873-b159-ede09b4a7e51
title: PRINTPROCESSOR_CAPS_1 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_CAPS_1
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 131b5ecf874554c3642808570a53ee8b20ad0e68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364149"
---
# <a name="printprocessor_caps_1-structure"></a>PrintProcessor-Ober \_ Grenzen \_ 1-Struktur

Die **PrintProcessor \_ Caps \_ 1** -Struktur ist das Format für die Drucker Funktions Informationen, die von der [**getprinterdata**](getprinterdata.md) -Funktion in dem Puffer zurückgegeben werden, der von der *pData* -Variablen angegeben wird.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PRINTPROCESSOR_CAPS_1 {
  DWORD dwLevel;
  DWORD dwNupOptions;
  DWORD dwPageOrderFlags;
  DWORD dwNumberOfCopies;
} PRINTPROCESSOR_CAPS_1, *PPRINTPROCESSOR_CAPS_1;
```



## <a name="members"></a>Member

<dl> <dt>

**dwlevel**
</dt> <dd>

Die Versionsnummer der-Struktur. Dieser Wert muss 1 sein.

</dd> <dt>

**dwnupoptions**
</dt> <dd>

Eine Bitmaske, die die verschiedenen Anzahl von Dokument Seiten darstellt, die der Drucker auf einer physischen Seite drucken kann. Das unwichtigste Bit stellt eine Dokument Seite pro Seite dar, das nächste Bit stellt 2 Dokument Seiten pro Seite dar usw. Beispielsweise gibt 0x0000810b an, dass der Drucker jeweils 1, 2, 4, 9 und 16 Dokument Seiten pro physischer Seite unterstützt.

</dd> <dt>

**dwpaargeorderflags**
</dt> <dd>

Die Reihenfolge, in der Seiten gedruckt werden. Bei diesem Wert kann es sich um einen normalen \_ Druck, einen umgekehrten \_ Druck oder einen \_ Drucker Druck handeln.

</dd> <dt>

**dwnumofkopien**
</dt> <dd>

Die maximale Anzahl von Kopien, die der Drucker verarbeiten kann.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Werte für alle Strukturmember werden von der Funktion [**getprintprocessorfunctions**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) bereitgestellt, die im Windows-Treiberkit (WDK) dokumentiert ist.

Der Spooler Ruft die [**getprintprocessorfunctions**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) -Funktion eines Druck Prozessors auf, wenn eine Anwendung [**getprinterdata**](getprinterdata.md)aufruft und einen Wertnamen mit dem Format printproccaps \_ *Datentyp* angibt, wobei *Datentyp* der Name eines Eingabe Datentyps ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Getprinterdata**](getprinterdata.md)
</dt> </dl>

 

