---
description: Die PRINTER \_ NOTIFY \_ INFO-Struktur enthält Druckerinformationen, die von der FindNextPrinterChangeNotification-Funktion zurückgegeben werden. Die Funktion gibt diese Informationen zurück, nachdem ein Wartevorgang für ein Druckeränderungsbenachrichtigungsobjekt erfüllt wurde.
ms.assetid: c104fabe-edf5-426e-859b-694811975623
title: PRINTER_NOTIFY_INFO -Struktur (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_INFO
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 26c7fca07eda8638bf657055691d72c78bccdbec6ef2b9a8c76ee7cf830bc767
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091850"
---
# <a name="printer_notify_info-structure"></a>PRINTER \_ NOTIFY \_ INFO-Struktur

Die **PRINTER \_ NOTIFY \_ INFO-Struktur** enthält Druckerinformationen, die von der [**FindNextPrinterChangeNotification-Funktion zurückgegeben**](findnextprinterchangenotification.md) werden. Die Funktion gibt diese Informationen zurück, nachdem ein Wartevorgang für ein Druckeränderungsbenachrichtigungsobjekt erfüllt wurde.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PRINTER_NOTIFY_INFO {
  DWORD                    Version;
  DWORD                    Flags;
  DWORD                    Count;
  PRINTER_NOTIFY_INFO_DATA aData[1];
} PRINTER_NOTIFY_INFO, *PPRINTER_NOTIFY_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**Version**
</dt> <dd>

Die Version dieser -Struktur. Legen Sie diesen Member auf 2 fest.

</dd> <dt>

**Flags**
</dt> <dd>

Ein Bitflag, das den Status der Benachrichtigungsstruktur angibt. Wenn das Bit PRINTER NOTIFY INFO DISCARDED festgelegt ist, bedeutet \_ \_ dies, dass einige \_ Benachrichtigungen verworfen werden mussten.

</dd> <dt>

**Count**
</dt> <dd>

Die Anzahl der [**PRINTER \_ NOTIFY INFO \_ \_ DATA-Elemente**](printer-notify-info-data.md) im **aData-Array.**

</dd> <dt>

**Adata**
</dt> <dd>

Ein Array von [**PRINTER \_ NOTIFY INFO \_ \_ DATA-Strukturen.**](printer-notify-info-data.md) Jedes Element des Arrays identifiziert einen einzelnen Auftrag oder ein Druckerinformationsfeld und stellt die aktuellen Daten für dieses Feld zur Verfügung.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn für **das Flags-Member** das Bit PRINTER NOTIFY INFO DISCARDED festgelegt ist, deutet dies darauf hin, dass ein Überlauf oder Fehler aufgetreten ist und Benachrichtigungen \_ möglicherweise verloren gegangen \_ \_ sind. In diesem Fall müssen Sie [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) aufrufen und das FLAG PRINTER NOTIFY OPTIONS REFRESH angeben, um \_ alle aktuellen Informationen \_ \_ abzurufen. Bis Sie diesen Aktualisierungsvorgang anfordern, sendet das System keine zusätzlichen Benachrichtigungen für dieses Änderungsbenachrichtigungsobjekt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> <dt>

[**\_ \_ BENACHRICHTIGUNGSINFORMATIONSDATEN DES \_ DRUCKERS**](printer-notify-info-data.md)
</dt> </dl>

 

 




