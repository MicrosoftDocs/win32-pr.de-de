---
description: Beschreibt einen vollständigen Satz von Werten, die einem Auftrag zugeordnet sind, und unterstützt große Spooldateien mit Größen, die mit 64 Bits ausgedrückt werden.
ms.assetid: 90932ae2-ea9e-43bc-9a1d-c68223f6d0ee
title: JOB_INFO_4-Struktur (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_4
- _JOB_INFO_4A
- _JOB_INFO_4W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: dd338b4e6e486c59bfdac705b68c72c56eafb96c9f4e1899e9b4cb3b294791de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091920"
---
# <a name="job_info_4-structure"></a>JOB \_ INFO \_ 4-Struktur

Beschreibt einen vollständigen Satz von Werten, die einem Auftrag zugeordnet sind, und unterstützt große Spooldateien mit Größen, die mit 64 Bits ausgedrückt werden.

## <a name="syntax"></a>Syntax


```C++
typedef struct _JOB_INFO_4 {
  DWORD                JobId;
  LPTSTR               pPrinterName;
  LPTSTR               pMachineName;
  LPTSTR               pUserName;
  LPTSTR               pDocument;
  LPTSTR               pNotifyName;
  LPTSTR               pDatatype;
  LPTSTR               pPrintProcessor;
  LPTSTR               pParameters;
  LPTSTR               pDriverName;
  LPDEVMODE            pDevMode;
  LPTSTR               pStatus;
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
  DWORD                Status;
  DWORD                Priority;
  DWORD                Position;
  DWORD                StartTime;
  DWORD                UntilTime;
  DWORD                TotalPages;
  DWORD                Size;
  SYSTEMTIME           Submitted;
  DWORD                Time;
  DWORD                PagesPrinted;
  LONG                 SizeHigh;
} JOB_INFO_4, *PJOB_INFO_4;
```



## <a name="members"></a>Member

<dl> <dt>

**Jobid**
</dt> <dd>

Ein Auftragsbezeichnerwert.

</dd> <dt>

**pPrinterName**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Druckers angibt, für den der Auftrag gespoolt wird.

</dd> <dt>

**pMachineName**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Computers angibt, der den Druckauftrag erstellt hat.

</dd> <dt>

**pUserName**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Benutzers angibt, der der Eigentümer des Druckauftrags ist.

</dd> <dt>

**pDocument**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Druckauftrags angibt (z. B. "MS-WORD: Review.doc").

</dd> <dt>

**pNotifyName**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Benutzers angibt, der benachrichtigt werden soll, wenn der Auftrag gedruckt wurde oder wenn beim Drucken des Auftrags ein Fehler auftritt.

</dd> <dt>

**pDatatype**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Datentyp angibt, der zum Aufzeichnen des Druckauftrags verwendet wird.

</dd> <dt>

**pPrintProcessor**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Druckprozessors angibt, der zum Drucken des Auftrags verwendet werden soll.

</dd> <dt>

**pParameters**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die Druckprozessorparameter angibt.

</dd> <dt>

**pDriverName**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Druckertreibers angibt, der zum Verarbeiten des Druckauftrags verwendet werden soll.

</dd> <dt>

**pDevMode**
</dt> <dd>

Ein Zeiger auf eine [**DEVMODE-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-devmodea) die Geräteinitialisierungs- und Umgebungsdaten für den Druckertreiber enthält.

</dd> <dt>

**pStatus**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Status des Druckauftrags angibt. Dieser Member sollte vor **Status** überprüft werden. Wenn **pStatus** **NULL** ist, wird der Status durch den Inhalt des Statusmembers definiert.

</dd> <dt>

**pSecurityDescriptor**
</dt> <dd>

Der Wert dieses Members ist **NULL.** Das Abrufen und Festlegen von Dokumentsicherheitsbeschreibungen wird in dieser Version nicht unterstützt.

</dd> <dt>

**Status**
</dt> <dd>

Der Auftragsstatus. Bei diesem Member kann es sich um einen oder mehrere der folgenden Werte handelt:

| Wert                           | Bedeutung                                                      |
|---------------------------------|--------------------------------------------------------------|
| \_ \_ AUFTRAGSSTATUS BLOCKIERT \_ DEVQ      | Der Treiber kann den Auftrag nicht drucken.                             |
| AUFTRAGSSTATUS \_ \_ GELÖSCHT            | Der Auftrag wurde gelöscht.                                        |
| \_LÖSCHEN DES AUFTRAGSSTATUS \_           | Der Auftrag wird gelöscht.                                        |
| \_ \_ AUFTRAGSSTATUSFEHLER              | Dem Auftrag wird ein Fehler zugeordnet.                         |
| AUFTRAGSSTATUS \_ \_ OFFLINE            | Der Drucker ist offline.                                          |
| JOB \_ STATUS \_ PAPEROUT           | Der Drucker ist nicht mehr auf Papier.                                     |
| AUFTRAGSSTATUS \_ \_ ANGEHALTEN             | Der Auftrag wird angehalten.                                               |
| AUFTRAGSSTATUS \_ \_ GEDRUCKT            | Der Auftrag wurde gedruckt.                                             |
| \_DRUCKEN DES AUFTRAGSSTATUS \_           | Der Auftrag wird gedruckt.                                             |
| \_ \_ AUFTRAGSSTATUSNEUSTART            | Der Auftrag wurde neu gestartet.                                      |
| \_ \_ AUFTRAGSSTATUSSPOOLING           | Der Auftrag wird gespoolt.                                             |
| \_BENUTZEREINGRIFF BEIM AUFTRAGSSTATUS \_ \_ | Drucker weist einen Fehler auf, der erfordert, dass der Benutzer etwas tut. |



 

In Windows XP und neueren Versionen von Windows können auch die folgenden Werte verwendet werden:

| Wert                 | Bedeutung                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------|
| AUFTRAGSSTATUS \_ \_ ABGESCHLOSSEN | Der Auftrag wird an den Drucker gesendet, ist aber möglicherweise noch nicht gedruckt. Weitere Informationen finden Sie unter Hinweise. |
| AUFTRAGSSTATUS \_ \_ BEIBEHALTEN | Der Auftrag wurde nach dem Drucken in der Druckwarteschlange beibehalten.                              |



 

</dd> <dt>

**Priority**
</dt> <dd>

Die Auftragspriorität. Dieser Member kann einer der folgenden Werte oder im Bereich zwischen 1 und 99 (MIN \_ PRIORITY bis MAX \_ PRIORITY) sein.



| Wert         | Bedeutung           |
|---------------|-------------------|
| MIN \_ PRIORITY | Mindestpriorität. |
| MAX \_ PRIORITY | Maximale Priorität. |
| DEF \_ PRIORITY | Standardpriorität. |



 

</dd> <dt>

**Position**
</dt> <dd>

Die Position des Auftrags in der Druckwarteschlange.

</dd> <dt>

**StartTime**
</dt> <dd>

Der früheste Zeitpunkt, zu dem der Auftrag gedruckt werden kann.

</dd> <dt>

**UntilTime**
</dt> <dd>

Die letzte Zeit, zu der der Auftrag gedruckt werden kann.

</dd> <dt>

**TotalPages**
</dt> <dd>

Die Anzahl der seiten, die für den Auftrag erforderlich sind. Dieser Wert kann 0 (null) sein, wenn der Druckauftrag keine Seitentrenninformationen enthält.

</dd> <dt>

**Größe**
</dt> <dd>

Die unteren vier Bytes der Größe des Auftrags in Bytes. Siehe auch das **SizeHigh-Element** weiter unten.

</dd> <dt>

**Gesendet**
</dt> <dd>

Eine [**SYSTEMTIME-Struktur,**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) die den Zeitpunkt angibt, zu dem der Auftrag übermittelt wurde.

Dieser Zeitwert liegt im UTC-Format (Universal Time Coordinate) vor. Sie sollten ihn in einen Lokalen Zeitwert konvertieren, bevor Sie ihn anzeigen. Sie können die [**FileTimeToLocalFileTime-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) verwenden, um die Konvertierung durchzuführen.

</dd> <dt>

**Time**
</dt> <dd>

Die Gesamtzeit in Millisekunden, die seit beginn des Drucks des Auftrags verstrichen ist.

</dd> <dt>

**PagesPrinted**
</dt> <dd>

Die Anzahl der seiten, die gedruckt wurden. Dieser Wert kann 0 (null) sein, wenn der Druckauftrag keine Informationen zum Seitentrennzeichen enthält.

</dd> <dt>

**SizeHigh**
</dt> <dd>

Die höheren vier Bytes der Größe des Auftrags in Bytes. Siehe auch das **oben genannte Size-Member.**

</dd> </dl>

## <a name="remarks"></a>Hinweise

Portmonitore, die TrueEndOfJob nicht unterstützen, legen den Auftrag sofort nach dem Senden des Auftrags an den Drucker auf JOB \_ STATUS \_ PRINTED fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Winspool.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ JOB \_ INFO \_ 4W** (Unicode) und **\_ JOB INFO \_ \_ 4A** (ANSI)<br/>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Devmode**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**EnumJobs**](enumjobs.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

