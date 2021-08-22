---
description: Die STRUKTUR PRINTER \_ NOTIFY INFO DATA identifiziert ein \_ \_ Auftrags- oder Druckerinformationsfeld und stellt die aktuellen Daten für dieses Feld bereit.
ms.assetid: 7a7b9e01-32e0-47f8-a5b1-5f7e6a663714
title: PRINTER_NOTIFY_INFO_DATA-Struktur (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_INFO_DATA,
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: e26f7ed7f002801d3bbdf60708d83234231fe3333675a1c211488431868a4236
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118731194"
---
# <a name="printer_notify_info_data-structure"></a>PRINTER \_ NOTIFY \_ INFO \_ DATA-Struktur

Die **STRUKTUR PRINTER NOTIFY INFO \_ \_ \_ DATA** identifiziert ein Auftrags- oder Druckerinformationsfeld und stellt die aktuellen Daten für dieses Feld bereit.

Die [**FindNextPrinterChangeNotification-Funktion**](findnextprinterchangenotification.md) gibt eine [**PRINTER NOTIFY \_ \_ INFO-Struktur**](printer-notify-info.md) zurück, die ein Array von **PRINTER NOTIFY INFO \_ \_ \_ DATA-Strukturen** enthält.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PRINTER_NOTIFY_INFO_DATA {
  WORD  Type;
  WORD  Field;
  DWORD Reserved;
  DWORD Id;
  union {
    DWORD  adwData[2];
    struct {
      DWORD  cbBuf;
      LPVOID pBuf;
    } Data;
  } NotifyData;
} PRINTER_NOTIFY_INFO_DATA, *PPRINTER_NOTIFY_INFO_DATA; ;
```



## <a name="members"></a>Member

<dl> <dt>

**Typ**
</dt> <dd>

Gibt den Typ der bereitgestellten Informationen an. Dieser Member kann einer der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                      | Bedeutung                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="JOB_NOTIFY_TYPE"></span><span id="job_notify_type"></span><dl> <dt>**JOB \_ NOTIFY \_ TYPE**</dt> <dt>0x01</dt> </dl>             | Gibt an, dass der **Field-Member** eine JOB \_ NOTIFY \_ FIELD-Konstante \_ \* angibt.<br/>     |
| <span id="PRINTER_NOTIFY_TYPE"></span><span id="printer_notify_type"></span><dl> <dt>**DRUCKER \_ NOTIFY \_ TYPE**</dt> <dt>0x00</dt> </dl> | Gibt an, dass der **Field-Member** eine PRINTER \_ NOTIFY \_ FIELD-Konstante \_ \* angibt.<br/> |



 

</dd> <dt>

**Feld**
</dt> <dd>

Gibt das geänderte Feld an. Eine Liste der möglichen Werte finden Sie im Abschnitt Hinweise.

</dd> <dt>

**Reserved**
</dt> <dd>

Reserviert.

</dd> <dt>

**Id**
</dt> <dd>

Gibt den Auftragsbezeichner an, wenn der **Type-Member** JOB \_ NOTIFY TYPE angibt. \_ Wenn der **Type-Member** PRINTER \_ NOTIFY TYPE angibt, ist dieser Member nicht \_ definiert.

</dd> <dt>

**NotifyData**
</dt> <dd>

Eine Vereinigung von Dateninformationen basierend auf den **Typ-** und **Feldmembern.** Eine Beschreibung des Datentyps, der jedem Feld zugeordnet ist, finden Sie im Abschnitt Hinweise.

<dl> <dt>

**adwData \[ 2\]**
</dt> <dd>

Ein Array von zwei **DWORD-Werten.** Für Informationsfelder, die nur ein einzelnes **DWORD** verwenden, sind die Daten in **adwData** \[ 0 \] enthalten.

</dd> <dt>

**Daten**
</dt> <dd> <dl> <dt>

**cbBuf**
</dt> <dd>

Gibt die Größe des Puffers in Bytes an, auf den **pBuf** zeigt.

</dd> <dt>

**pBuf**
</dt> <dd>

Zeiger auf einen Puffer, der die aktuellen Daten des Felds enthält.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn der **Type-Member** PRINTER \_ NOTIFY TYPE angibt, kann der \_ **Field-Member** einer der folgenden Werte sein.



<table>
<thead>
<tr class="header">
<th>Feld</th>
<th>Datentyp</th>
<th>Wert</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_SERVER_NAME</td>
<td>Wird nicht unterstützt.</td>
<td>0x00</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_PRINTER_NAME</td>
<td><strong>pBuf</strong> ist ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Druckers enthält.</td>
<td>0x01</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_SHARE_NAME</td>
<td><strong>pBuf</strong> ist ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Freigabepunkt für den Drucker identifiziert.</td>
<td>0x02</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_PORT_NAME</td>
<td><strong>pBuf</strong> ist ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Ports enthält, an dem die Druckaufträge gedruckt werden. Wenn &quot; Druckerpooling &quot; ausgewählt ist, ist dies eine durch Kommas getrennte Liste von Ports.</td>
<td>0x03</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_DRIVER_NAME</td>
<td><strong>pBuf</strong> ist ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Druckertreibers enthält.</td>
<td>0x04</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_COMMENT</td>
<td><strong>pBuf</strong> ist ein Zeiger auf eine auf NULL endende Zeichenfolge, die die neue Kommentarzeichenfolge enthält. Dies ist in der Regel eine kurze Beschreibung des Druckers.</td>
<td>0x05</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_LOCATION</td>
<td><strong>pBuf</strong> ist ein Zeiger auf eine auf NULL endende Zeichenfolge, die die neue physische Position des Druckers enthält (z. &quot; B. Bldg. 38, Raum 1164 &quot; ).</td>
<td>0x06</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_DEVMODE</td>
<td><strong>pBuf</strong> ist ein Zeiger auf eine <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea"><strong>DEVMODE-Struktur,</strong></a> die Standarddruckerdaten wie die Papierausrichtung und die Auflösung definiert.</td>
<td>0x07</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_SEPFILE</td>
<td><strong>pBuf</strong> ist ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen der Datei angibt, die zum Erstellen der Trennzeichenseite verwendet wird. Diese Seite dient zum Trennen von Druckaufträgen, die an den Drucker gesendet werden.</td>
<td>0x08</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_PRINT_PROCESSOR</td>
<td><strong>pBuf</strong> ist ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des vom Drucker verwendeten Druckprozessors angibt.</td>
<td>0x09</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_PARAMETERS</td>
<td><strong>pBuf</strong> ist ein Zeiger auf eine auf NULL endende Zeichenfolge, die die Standardparameter des Druckprozessors angibt.</td>
<td>0x0A</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_DATATYPE</td>
<td><strong>pBuf</strong> ist ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Datentyp angibt, der zum Aufzeichnen des Druckauftrags verwendet wird.</td>
<td>0x0B</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_SECURITY_DESCRIPTOR</td>
<td><strong>pBuf</strong> ist ein Zeiger auf eine <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> Struktur für den Drucker. Der Zeiger kann <strong>NULL</strong> sein, wenn kein Sicherheitsdeskriptor vorhanden ist.</td>
<td>0x0C</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_ATTRIBUTES</td>
<td><strong>adwData</strong> [0] gibt die Druckerattribute an, die einen der folgenden Werte aufweisen können:<dl> PRINTER_ATTRIBUTE_QUEUED<br />
PRINTER_ATTRIBUTE_DIRECT<br />
PRINTER_ATTRIBUTE_DEFAULT<br />
PRINTER_ATTRIBUTE_SHARED<br />
</dl></td>
<td>0x0D</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_PRIORITY</td>
<td><strong>adwData</strong> [0] gibt einen Prioritätswert an, den der Spooler zum Weiterleiten von Druckaufträgen verwendet.</td>
<td>0x0E</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_DEFAULT_PRIORITY</td>
<td><strong>adwData</strong> [0] gibt den Standardprioritätswert an, der jedem Druckauftrag zugewiesen ist.</td>
<td>0x0F</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_START_TIME</td>
<td><strong>adwData</strong> [0] gibt den frühesten Zeitpunkt an, zu dem der Drucker einen Auftrag ausgibt. (Dieser Wert wird in Minuten angegeben, die seit 12:00 Uhr verstrichen sind.)</td>
<td>0x10</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_UNTIL_TIME</td>
<td><strong>adwData</strong> [0] gibt den letzten Zeitpunkt an, zu dem der Drucker einen Auftrag druckt. (Dieser Wert wird in Minuten angegeben, die seit 12:00 Uhr verstrichen sind.)</td>
<td>0x11</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_STATUS</td>
<td><strong>adwData</strong> [0] gibt den Druckerstatus an. Eine Liste der möglichen Werte finden Sie in der <a href="printer-info-2.md"><strong>PRINTER_INFO_2</strong></a> Struktur.</td>
<td>0x12</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_STATUS_STRING</td>
<td>Wird nicht unterstützt.</td>
<td>0x13</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_CJOBS</td>
<td><strong>adwData</strong> [0] gibt die Anzahl der Druckaufträge an, die für den Drucker in die Warteschlange gestellt wurden.</td>
<td>0x14</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_AVERAGE_PPM</td>
<td><strong>adwData</strong> [0] gibt die durchschnittliche Anzahl von Seiten pro Minute an, die auf dem Drucker gedruckt wurden.</td>
<td>0x15</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_TOTAL_PAGES</td>
<td>Wird nicht unterstützt.</td>
<td>0x16</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_PAGES_PRINTED</td>
<td>Wird nicht unterstützt.</td>
<td>0x17</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_TOTAL_BYTES</td>
<td>Wird nicht unterstützt.</td>
<td>0x18</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_BYTES_PRINTED</td>
<td>Wird nicht unterstützt.</td>
<td>0x19</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_OBJECT_GUID</td>
<td>Dies wird festgelegt, wenn sich die Objekt-GUID ändert.</td>
<td>0x1A</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_FRIENDLY_NAME</td>
<td>Dies wird festgelegt, wenn die Druckerverbindung umbenannt wird.</td>
<td>0x1B</td>
</tr>
</tbody>
</table>



 

Wenn der **Type-Member** JOB \_ NOTIFY TYPE \_ angibt, kann **der Field-Member** einer der folgenden Werte sein.



| Feld                                    | Datentyp                                                                                                                                                                                                                                            | Wert |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| DRUCKERNAME \_ \_ DES \_ AUFTRAGSBENACHRICHTIGUNGSFELDS \_        | **pBuf ist** ein Zeiger auf eine auf NULL terminierte Zeichenfolge, die den Namen des Druckers enthält, für den der Auftrag gepoolt wird.                                                                                                                                      | 0x00  |
| NAME DES \_ \_ AUFTRAGSBENACHRICHTIGUNGSFELDCOMPUTERS \_ \_        | **pBuf ist** ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen des Computers angibt, der den Druckauftrag erstellt hat.                                                                                                                                    | 0x01  |
| PORTNAME \_ DES \_ FELDS \_ "AUFTRAGSBENACHRICHTIGUNG" \_           | **pBuf ist** ein Zeiger auf eine auf NULL beendete Zeichenfolge, die die Ports identifiziert, die zum Übertragen von Daten an den Drucker verwendet werden. Wenn ein Drucker mit mehr als einem Anschluss verbunden ist, werden die Namen der Ports durch Kommas getrennt (z.B. "LPT1:,LPT2:,LPT3:"). | 0x02  |
| BENUTZERNAME \_ DES \_ FELDS "AUFTRAGSBENACHRICHTIGUNG" \_ \_           | **pBuf ist** ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen des Benutzers angibt, der den Druckauftrag gesendet hat.                                                                                                                                           | 0x03  |
| NAME DES \_ \_ AUFTRAGSBENACHRICHTIGUNGSFELDS \_ \_ BENACHRICHTIGEN         | **pBuf** ist ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen des Benutzers angibt, der benachrichtigt werden soll, wenn der Auftrag gedruckt wurde oder wenn beim Drucken des Auftrags ein Fehler auftritt.                                                              | 0x04  |
| DATENTYP DES \_ FELDS \_ \_ "AUFTRAGSBENACHRICHTIGUNG"             | **pBuf ist** ein Zeiger auf eine mit NULL beendete Zeichenfolge, die den Datentyp angibt, der zum Aufzeichnen des Druckauftrags verwendet wird.                                                                                                                                         | 0x05  |
| DRUCKPROZESSOR \_ FÜR \_ \_ AUFTRAGSBENACHRICHTIGUNGSFELD \_     | **pBuf ist** ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen des Druckprozessors angibt, der zum Drucken des Auftrags verwendet werden soll.                                                                                                                           | 0x06  |
| FELDPARAMETER \_ FÜR \_ AUFTRAGSBENACHRICHTIGUNG \_           | **pBuf ist** ein Zeiger auf eine auf NULL beendete Zeichenfolge, die Druckprozessorparameter angibt.                                                                                                                                                            | 0x07  |
| NAME DES \_ \_ AUFTRAGSBENACHRICHTIGUNGSFELDTREIBERS \_ \_         | **pBuf ist** ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen des Druckertreibers angibt, der zum Verarbeiten des Druckauftrags verwendet werden soll.                                                                                                           | 0x08  |
| \_ \_ AUFTRAGSBENACHRICHTIGUNGSFELD \_ DEVMODE              | **pBuf ist** ein Zeiger auf eine [**DEVMODE-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-devmodea) die Gerätein initialisierungs- und Umgebungsdaten für den Druckertreiber enthält.                                                                                                        | 0x09  |
| STATUS DES \_ \_ AUFTRAGSBENACHRICHTIGUNGSFELDS \_               | **adwData** \[ 0 \] gibt den Auftragsstatus an. Eine Liste der möglichen Werte finden Sie in der [**JOB \_ INFO \_ 2-Struktur.**](job-info-2.md)                                                                                                                        | 0x0A  |
| STATUSZEICHENFOLGE \_ DES \_ FELDS \_ "AUFTRAGSBENACHRICHTIGUNG" \_       | **pBuf ist** ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Status des Druckauftrags angibt.                                                                                                                                                           | 0x0B  |
| SICHERHEITSDESKRIPTOR \_ \_ FÜR \_ \_ AUFTRAGSBENACHRICHTIGUNGSFELD | Wird nicht unterstützt.                                                                                                                                                                                                                                          | 0x0C  |
| FELDDOKUMENT \_ \_ \_ "AUFTRAGSBENACHRICHTIGUNG"             | **pBuf ist** ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen des Druckauftrags angibt (z. B. "MS-WORD: Review.doc").                                                                                                                        | 0x0D  |
| FELDPRIORITÄT \_ FÜR \_ AUFTRAGSBENACHRICHTIGUNG \_             | **adwData** \[ 0 \] gibt die Auftragspriorität an.                                                                                                                                                                                                           | 0x0E  |
| POSITION DES \_ \_ AUFTRAGSBENACHRICHTIGUNGSFELDS \_             | **adwData** \[ 0 \] gibt die Position des Auftrags in der Druckwarteschlange an.                                                                                                                                                                                      | 0x0F  |
| FELD \_ \_ "AUFTRAGSBENACHRICHTIGUNG \_ GESENDET"            | **pBuf ist** ein Zeiger auf eine [**SYSTEMTIME-Struktur,**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) die den Zeitpunkt angibt, zu dem der Auftrag übermittelt wurde.                                                                                                                          | 0x10  |
| STARTZEIT \_ DES \_ FELDS \_ "AUFTRAGSBENACHRICHTIGUNG" \_          | **adwData** \[ 0 \] gibt den frühesten Zeitpunkt an, zu dem der Auftrag gedruckt werden kann. (Dieser Wert wird in Minuten angegeben, die seit 12:00 Uhr verstrichen sind.)                                                                                                                | 0x11  |
| FELD \_ \_ "AUFTRAGSBENACHRICHTIGUNG \_ BIS ZUR \_ ZEIT"          | **adwData** \[ 0 \] gibt den zeitpunkt an, zu dem der Auftrag zuletzt gedruckt werden kann. (Dieser Wert wird in Minuten angegeben, die seit 12:00 Uhr verstrichen sind.)                                                                                                                  | 0x12  |
| FELDZEIT DER \_ AUFTRAGSBENACHRICHTIGUNG \_ \_                 | **adwData** \[ 0 \] gibt die Gesamtzeit in Sekunden an, die seit dem Druckvorgang des Auftrags verstrichen ist.                                                                                                                                                  | 0x13  |
| \_ \_ AUFTRAGSBENACHRICHTIGUNGSFELD \_ SEITEN GESAMT \_         | **adwData** \[ 0 \] gibt die Größe des Auftrags in Seiten an.                                                                                                                                                                                             | 0x14  |
| \_ \_ \_ GEDRUCKTE FELDSEITEN FÜR AUFTRAGSBENACHRICHTIGUNGEN \_       | **adwData** \[ 0 \] gibt die Anzahl der Seiten an, die gedruckt wurden.                                                                                                                                                                                      | 0x15  |
| FELD \_ \_ "AUFTRAGSBENACHRICHTIGUNG" \_ \_ GESAMTBYTES         | **adwData** \[ 0 \] gibt die Größe des Auftrags in Bytes an.                                                                                                                                                                                             | 0x16  |
| \_ \_ AUFTRAGSBENACHRICHTIGUNGSFELD \_ \_ BYTES GEDRUCKT       | **adwData** \[ 0 \] gibt die Anzahl der Bytes an, die für diesen Auftrag ausgegeben wurden. Für dieses Feld wird das Änderungsbenachrichtigungsobjekt signalisiert, wenn Bytes an den Drucker gesendet werden.                                                                      | 0x17  |



 

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

[**Devmode**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> <dt>

[**AUFTRAGSINFORMATIONEN \_ \_ 2**](job-info-2.md)
</dt> <dt>

[**DRUCKERINFORMATIONEN \_ \_ 2**](printer-info-2.md)
</dt> <dt>

[**\_ \_ DRUCKERBENACHRICHTIGUNGSINFORMATIONEN**](printer-notify-info.md)
</dt> <dt>

[**\_SICHERHEITSBESCHREIBUNG**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[**Systemtime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)
</dt> </dl>

