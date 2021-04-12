---
description: Die \_ Datenstruktur für den Drucker Benachrichtigungs \_ \_ Daten identifiziert ein Auftrags-oder Drucker Informationsfeld und stellt die aktuellen Daten für dieses Feld bereit.
ms.assetid: 7a7b9e01-32e0-47f8-a5b1-5f7e6a663714
title: PRINTER_NOTIFY_INFO_DATA Struktur (winspool. h)
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
ms.openlocfilehash: 4c76ffe70a8388e920b5f8576830e31ed23edc81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216444"
---
# <a name="printer_notify_info_data-structure"></a>\_Datenstruktur zum Benachrichtigen von Drucker \_ Informationen \_

Die Datenstruktur für den **Drucker \_ Benachrichtigungs \_ \_ Daten** identifiziert ein Auftrags-oder Drucker Informationsfeld und stellt die aktuellen Daten für dieses Feld bereit.

Die [**findnextprinterchangenotifi-**](findnextprinterchangenotification.md) Funktion gibt [**eine \_ druckerbenachrichtigungs \_**](printer-notify-info.md) -Struktur zurück, die ein Array von **\_ druckerbenachrichtigungs- \_ \_ Daten** Strukturen enthält.

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

**Type**
</dt> <dd>

Gibt den Typ der bereitgestellten Informationen an. Dieser Member kann einen der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                                                      | Bedeutung                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="JOB_NOTIFY_TYPE"></span><span id="job_notify_type"></span><dl> <dt>**Auftrag \_ Benachrichtigen von \_ Typ**</dt> <dt>0x01</dt> </dl>             | Gibt an, dass der **Feldmember** eine \_ Feldkonstante für den Auftrags Benachrichtigungs Wert angibt \_ \_ \* .<br/>     |
| <span id="PRINTER_NOTIFY_TYPE"></span><span id="printer_notify_type"></span><dl> <dt>**Drucker \_ Benachrichtigen von \_ Typ**</dt> <dt>0x00</dt> </dl> | Gibt an, dass der **Feldmember** eine \_ Feldkonstante für den Drucker Benachrichtigungs Wert angibt \_ \_ \* .<br/> |



 

</dd> <dt>

**Feld**
</dt> <dd>

Gibt das Feld an, das sich geändert hat. Eine Liste möglicher Werte finden Sie im Abschnitt "Hinweise".

</dd> <dt>

**Reserved**
</dt> <dd>

Reserviert.

</dd> <dt>

**Id**
</dt> <dd>

Gibt den Auftrags Bezeichner an, wenn der **Typmember** den \_ Benachrichtigungs-Typ des Auftrags angibt \_ Wenn der **Typmember** einen \_ druckerbenachrichtigungstyp angibt \_ , ist dieser Member nicht definiert.

</dd> <dt>

**Notifydata**
</dt> <dd>

Eine Union von Daten Informationen, die auf dem **Typ** und den **Feldmembern** basiert. Eine Beschreibung des Datentyps, der den einzelnen Feldern zugeordnet ist, finden Sie im Abschnitt "Hinweise".

<dl> <dt>

**adwdata \[ 2\]**
</dt> <dd>

Ein Array mit zwei **DWORD** -Werten. Für Informationsfelder, die nur ein einzelnes **DWORD** verwenden, befinden sich die Daten in **adwdata** \[ 0 \] .

</dd> <dt>

**Daten**
</dt> <dd> <dl> <dt>

**cbbuf**
</dt> <dd>

Gibt die Größe des Puffers, auf den **PBUF** zeigt, in Bytes an.

</dd> <dt>

**PBUF**
</dt> <dd>

Zeiger auf einen Puffer, der die aktuellen Daten des Felds enthält.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn der **Typmember** \_ \_ einen druckerbenachrichtigungstyp angibt, kann der **Feldmember** einen der folgenden Werte aufweisen.



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
<td><strong>PBUF</strong> ist ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Druckers enthält.</td>
<td>0x01</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_SHARE_NAME</td>
<td><strong>PBUF</strong> ist ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Freigabe Punkt für den Drucker angibt.</td>
<td>0x02</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_PORT_NAME</td>
<td><strong>PBUF</strong> ist ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Ports enthält, an den die Druckaufträge ausgegeben werden. Wenn &quot; Drucker Pooling &quot; ausgewählt ist, ist dies eine durch Trennzeichen getrennte Liste von Ports.</td>
<td>0x03</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_DRIVER_NAME</td>
<td><strong>PBUF</strong> ist ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Druckertreibers enthält.</td>
<td>0x04</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_COMMENT</td>
<td><strong>PBUF</strong> ist ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die neue Kommentar Zeichenfolge enthält, die in der Regel eine kurze Beschreibung des Druckers ist.</td>
<td>0x05</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_LOCATION</td>
<td><strong>PBUF</strong> ist ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den neuen physischen Speicherort des Druckers enthält (z. b &quot; . Bldg). 38, Raum 1164 &quot; ).</td>
<td>0x06</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_DEVMODE</td>
<td><strong>PBUF</strong> ist ein Zeiger auf eine <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea"><strong>DEVMODE</strong></a> -Struktur, die die Standarddrucker Daten definiert, z. b. die Papier Ausrichtung und die Lösung.</td>
<td>0x07</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_SEPFILE</td>
<td><strong>PBUF</strong> ist ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen der Datei angibt, die zum Erstellen der Trenn Zeichenseite verwendet wurde. Diese Seite wird verwendet, um Druckaufträge, die an den Drucker gesendet werden, zu trennen.</td>
<td>0x08</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_PRINT_PROCESSOR</td>
<td><strong>PBUF</strong> ist ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des vom Drucker verwendeten Druck Prozessors angibt.</td>
<td>0x09</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_PARAMETERS</td>
<td><strong>PBUF</strong> ist ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die Standardparameter für den Druck Prozessor angibt.</td>
<td>0x0A</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_DATATYPE</td>
<td><strong>PBUF</strong> ist ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Datentyp angibt, der zum Aufzeichnen des Druckauftrags verwendet wird.</td>
<td>0x0B</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_SECURITY_DESCRIPTOR</td>
<td><strong>PBUF</strong> ist ein Zeiger auf eine <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> Struktur für den Drucker. Der Zeiger ist möglicherweise <strong>null</strong> , wenn keine Sicherheits Beschreibung vorhanden ist.</td>
<td>0x0c</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_ATTRIBUTES</td>
<td><strong>adwdata</strong> [0] gibt die Drucker Attribute an. dabei kann es sich um einen der folgenden Werte handeln:<dl> PRINTER_ATTRIBUTE_QUEUED<br />
PRINTER_ATTRIBUTE_DIRECT<br />
PRINTER_ATTRIBUTE_DEFAULT<br />
PRINTER_ATTRIBUTE_SHARED<br />
</dl></td>
<td>0x0D</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_PRIORITY</td>
<td><strong>adwdata</strong> [0] gibt einen Prioritätswert an, den der Spooler zum Weiterleiten von Druckaufträgen verwendet.</td>
<td>0x0E</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_DEFAULT_PRIORITY</td>
<td><strong>adwdata</strong> [0] gibt den Standard Prioritätswert an, der jedem Druckauftrag zugewiesen ist.</td>
<td>0x0f</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_START_TIME</td>
<td><strong>adwdata</strong> [0] gibt den frühesten Zeitpunkt an, an dem der Drucker einen Auftrag druckt. (Dieser Wert wird in Minuten angegeben, die seit 12:00 Uhr vergangen sind.)</td>
<td>0x10</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_UNTIL_TIME</td>
<td><strong>adwdata</strong> [0] gibt den letzten Zeitpunkt an, zu dem der Drucker einen Auftrag druckt. (Dieser Wert wird in Minuten angegeben, die seit 12:00 Uhr vergangen sind.)</td>
<td>0x11</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_STATUS</td>
<td><strong>adwdata</strong> [0] gibt den Druckerstatus an. Eine Liste möglicher Werte finden Sie in der <a href="printer-info-2.md"><strong>PRINTER_INFO_2</strong></a> -Struktur.</td>
<td>0x12</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_STATUS_STRING</td>
<td>Wird nicht unterstützt.</td>
<td>0x13</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_CJOBS</td>
<td><strong>adwdata</strong> [0] gibt die Anzahl der Druckaufträge an, die für den Drucker in die Warteschlange eingereiht wurden.</td>
<td>0x14</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_AVERAGE_PPM</td>
<td><strong>adwdata</strong> [0] gibt die durchschnittliche Anzahl der Seiten pro Minute an, die auf dem Drucker gedruckt wurden.</td>
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
<td>Dieser Wert wird festgelegt, wenn die Objekt-GUID geändert wird.</td>
<td>0x1A</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_FRIENDLY_NAME</td>
<td>Dieser Wert wird festgelegt, wenn die Druckerverbindung umbenannt wird.</td>
<td>0x1B</td>
</tr>
</tbody>
</table>



 

Wenn das **Typelement** den \_ Benachrichtigungs Datentyp "Auftrag" angibt \_ , kann der **Feldmember** einen der folgenden Werte aufweisen.



| Feld                                    | Datentyp                                                                                                                                                                                                                                            | Wert |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| \_ \_ Feld \_ Drucker \_ Name für Auftrags Benachrichtigung        | **PBUF** ist ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Druckers enthält, für den der Auftrag gespoolkt ist.                                                                                                                                      | 0x00  |
| \_ \_ \_ Computer Name des Auftrags Benachrichtigungs Felds \_        | **PBUF** ist ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Computers angibt, der den Druckauftrag erstellt hat.                                                                                                                                    | 0x01  |
| \_ \_ Feldname für Auftrags Benachrichtigung \_ \_           | **PBUF** ist ein Zeiger auf eine auf NULL endende Zeichenfolge, die die Ports identifiziert, die zum Übertragen von Daten an den Drucker verwendet werden. Wenn ein Drucker mit mehr als einem Port verbunden ist, werden die Namen der Ports durch Kommas getrennt (z. b. "LPT1:, LPT2:, LPT3:"). | 0x02  |
| \_ \_ Feld \_ Benutzer \_ Name für Auftrags Benachrichtigung           | **PBUF** ist ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Benutzers angibt, der den Druckauftrag gesendet hat.                                                                                                                                           | 0x03  |
| \_ \_ \_ Benachrichtigungs Name für Benachrichtigungs Feld Benachrichtigen \_         | **PBUF** ist ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Benutzers angibt, der benachrichtigt werden soll, wenn der Auftrag gedruckt wurde oder wenn beim Drucken des Auftrags ein Fehler auftritt.                                                              | 0x04  |
| \_DataType des Auftrags Benachrichtigungs \_ Felds \_             | **PBUF** ist ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Typ der Daten angibt, die zum Aufzeichnen des Druckauftrags verwendet werden.                                                                                                                                         | 0x05  |
| \_ \_ \_ Druck Prozessor des Auftrags Benachrichtigungs Felds \_     | **PBUF** ist ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Druck Prozessors angibt, der zum Drucken des Auftrags verwendet werden soll.                                                                                                                           | 0x06  |
| \_ \_ Feld \_ Parameter für Auftrags Benachrichtigung           | **PBUF** ist ein Zeiger auf eine NULL-terminierte Zeichenfolge, die Druck Prozessor Parameter angibt.                                                                                                                                                            | 0x07  |
| \_ \_ Feld \_ Treiber \_ Name für Auftrags Benachrichtigung         | **PBUF** ist ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Druckertreibers angibt, der zum Verarbeiten des Druckauftrags verwendet werden soll.                                                                                                           | 0x08  |
| Feld "Auftrags \_ Benachrichtigung" \_ \_ DEVMODE              | **PBUF** ist ein Zeiger auf eine [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur, die die Geräte Initialisierungs-und Umgebungs Daten für den Druckertreiber enthält.                                                                                                        | 0x09  |
| Status des Auftrags \_ Benachrichtigungs \_ Felds \_               | **adwdata** \[ 0 \] gibt den Auftragsstatus an. Eine Liste möglicher Werte finden Sie in der Struktur der [**Auftrags \_ Informationen \_ 2**](job-info-2.md) .                                                                                                                        | 0x0A  |
| \_ \_ Feld Status- \_ \_ Zeichenfolge für Auftrags Benachrichtigung       | **PBUF** ist ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Status des Druckauftrags angibt.                                                                                                                                                           | 0x0B  |
| \_ \_ \_ Sicherheits \_ Beschreibung für das Feld "Auftrags Benachrichtigung" | Wird nicht unterstützt.                                                                                                                                                                                                                                          | 0x0c  |
| \_ \_ Feld \_ Dokument für Auftrags Benachrichtigung             | **PBUF** ist ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Druckauftrags (z. b. "MS-Word: Review.doc") angibt.                                                                                                                        | 0x0D  |
| Priorität der Auftrags \_ Benachrichtigungs \_ Felder \_             | **adwdata** \[ 0 \] gibt die Auftrags Priorität an.                                                                                                                                                                                                           | 0x0E  |
| \_ \_ Feld \_ Position für Auftrags Benachrichtigung             | **adwdata** \[ 0 \] gibt die Position des Auftrags in der Druck Warteschlange an.                                                                                                                                                                                      | 0x0f  |
| Feld "Auftrags \_ Benachrichtigung über \_ \_ mittelt"            | **PBUF** ist ein Zeiger auf eine [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur, die die Uhrzeit angibt, zu der der Auftrag übermittelt wurde.                                                                                                                          | 0x10  |
| \_Startzeit des Auftrags Benachrichtigungs \_ Felds \_ \_          | **adwdata** \[ der Wert 0 \] gibt den frühesten Zeitpunkt an, zu dem der Auftrag gedruckt werden kann. (Dieser Wert wird in Minuten angegeben, die seit 12:00 Uhr vergangen sind.)                                                                                                                | 0x11  |
| Feld "Auftrags \_ Benachrichtigung" \_ \_ bis zur \_ Zeit          | **adwdata** \[ der Wert 0 \] gibt den letzten Zeitpunkt an, zu dem der Auftrag gedruckt werden kann. (Dieser Wert wird in Minuten angegeben, die seit 12:00 Uhr vergangen sind.)                                                                                                                  | 0x12  |
| \_ \_ Feld \_ Zeit für Auftrags Benachrichtigung                 | **adwdata** \[ der Wert 0 \] gibt die Gesamtzeit in Sekunden an, die seit dem Drucken des Auftrags verstrichen ist.                                                                                                                                                  | 0x13  |
| \_Gesamtanzahl \_ der \_ \_ Seiten für Auftrags Benachrichtigung         | **adwdata** \[ 0 \] gibt die Größe des Auftrags in Seiten an.                                                                                                                                                                                             | 0x14  |
| \_Feld Seiten für Auftrags Benachrichtigung \_ \_ \_ gedruckt       | **adwdata** \[ 0 \] gibt die Anzahl der Seiten an, die gedruckt wurden.                                                                                                                                                                                      | 0x15  |
| Auftrags \_ Benachrichtigungs \_ Feld \_ Gesamt ( \_ Bytes)         | **adwdata** \[ der Wert 0 \] gibt die Größe (in Bytes) des Auftrags an.                                                                                                                                                                                             | 0x16  |
| Felder für Auftrags \_ Benachrichtigung \_ \_ \_ gedruckt       | **adwdata** \[ der Wert 0 \] gibt die Anzahl der Bytes an, die in diesem Auftrag gedruckt wurden. Für dieses Feld wird das Änderungs Benachrichtigungs Objekt signalisiert, wenn Bytes an den Drucker gesendet werden.                                                                      | 0x17  |



 

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

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**Findnextprinterchangenotifizierung**](findnextprinterchangenotification.md)
</dt> <dt>

[**Auftrags \_ Informationen \_ 2**](job-info-2.md)
</dt> <dt>

[**Drucker \_ Informationen \_ 2**](printer-info-2.md)
</dt> <dt>

[**Drucker \_ Benachrichtigungs \_ Informationen**](printer-notify-info.md)
</dt> <dt>

[**Sicherheits \_ Beschreibung**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[**System Time**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)
</dt> </dl>

