---
description: Die Drucker \_ Info \_ 2-Struktur gibt ausführliche Drucker Informationen an.
ms.assetid: 944cbfcd-9edf-4b60-a45c-9bb1839f8141
title: PRINTER_INFO_2 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_2
- _PRINTER_INFO_2A
- _PRINTER_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b299cb1bbdd3ac2475b7a9f2b600bcd9652246d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529756"
---
# <a name="printer_info_2-structure"></a>Drucker \_ Info \_ 2-Struktur

Die **Drucker \_ Info \_ 2** -Struktur gibt ausführliche Drucker Informationen an.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PRINTER_INFO_2 {
  LPTSTR               pServerName;
  LPTSTR               pPrinterName;
  LPTSTR               pShareName;
  LPTSTR               pPortName;
  LPTSTR               pDriverName;
  LPTSTR               pComment;
  LPTSTR               pLocation;
  LPDEVMODE            pDevMode;
  LPTSTR               pSepFile;
  LPTSTR               pPrintProcessor;
  LPTSTR               pDatatype;
  LPTSTR               pParameters;
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
  DWORD                Attributes;
  DWORD                Priority;
  DWORD                DefaultPriority;
  DWORD                StartTime;
  DWORD                UntilTime;
  DWORD                Status;
  DWORD                cJobs;
  DWORD                AveragePPM;
} PRINTER_INFO_2, *PPRINTER_INFO_2;
```



## <a name="members"></a>Member

<dl> <dt>

**pservername**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Server identifiziert, der den Drucker steuert. Wenn diese Zeichenfolge **null** ist, wird der Drucker lokal gesteuert.

</dd> <dt>

**pprintername**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Druckers angibt.

</dd> <dt>

**psharename**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Freigabe Punkt für den Drucker angibt. (Diese Zeichenfolge wird nur verwendet, wenn der Drucker \_ \_Die freigegebene Attribut Konstante wurde für den **Attributmember** festgelegt.)

</dd> <dt>

**pportname**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die die Ports identifiziert, die zum Übertragen von Daten an den Drucker verwendet werden. Wenn ein Drucker mit mehr als einem Port verbunden ist, müssen die Namen der einzelnen Ports durch Kommas getrennt werden (z. b. "LPT1:, LPT2:, LPT3:").

</dd> <dt>

**pdrivername**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Druckertreibers angibt.

</dd> <dt>

**pcomment**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die eine kurze Beschreibung des Druckers bereitstellt.

</dd> <dt>

**pLocation**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den physischen Speicherort des Druckers angibt (z. b. "Bldg". 38, Raum 1164 ").

</dd> <dt>

**pdevmode**
</dt> <dd>

Ein Zeiger auf eine [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur, die Standarddrucker Daten definiert, wie z. b. die Papier Ausrichtung und die Auflösung.

</dd> <dt>

**psepfile**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen der Datei angibt, die zum Erstellen der Trenn Zeichenseite verwendet wurde. Diese Seite wird verwendet, um Druckaufträge, die an den Drucker gesendet werden, zu trennen.

</dd> <dt>

**pprintprocessor**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des vom Drucker verwendeten Druck Prozessors angibt. Mit der [**enumprintprocessor**](enumprintprocessors.md) -Funktion können Sie eine Liste der auf einem Server installierten Druck Prozessoren abrufen.

</dd> <dt>

**pdatatype**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Datentyp angibt, der zum Aufzeichnen des Druckauftrags verwendet wird. Sie können die [**enumprintprocessordatatypes**](enumprintprocessordatatypes.md) -Funktion verwenden, um eine Liste von Datentypen abzurufen, die von einem bestimmten Druck Prozessor unterstützt werden.

</dd> <dt>

**pParameters**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die Standardparameter für den Druck Prozessor angibt.

</dd> <dt>

**psecuritydescriptor**
</dt> <dd>

Ein Zeiger auf eine [**Sicherheits \_ deskriptorstruktur**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) für den Drucker. Dieser Member kann **null** sein.

</dd> <dt>

**Attribute**
</dt> <dd>

Die Drucker Attribute. Dieser Member kann eine beliebige Kombination der folgenden Werte sein.

| Wert                                   | Bedeutung                                                                                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Drucker \_ Attribut \_ Direct              | Der Auftrag wird direkt an den Drucker gesendet (er ist nicht Spoolvorgang).                                                                                                                                |
| das Drucker \_ Attribut ist \_ \_ \_ zuerst fertig. | Wenn Set und Printer für Druck-während-Spoolvorgänge festgelegt sind, werden alle Aufträge, für die das Spoolvorgang abgeschlossen wurde, vor Aufträgen gedruckt, für die das Spoolvorgang noch nicht abgeschlossen wurde.                          |
| Drucker \_ Attribut \_ Aktivieren von \_ devq        | Wenn festgelegt, wird **devqueryprint** aufgerufen. **Devqueryprint** schlägt möglicherweise fehl, wenn die Dokument-und Drucker Einrichtung nicht identisch ist. Das Festlegen dieses Flags bewirkt, dass nicht übereinstimmende Dokumente in der Warteschlange gespeichert werden. |
| Drucker \_ Attribut \_ ausgeblendet              | Reserviert.                                                                                                                                                                               |
| Drucker \_ Attribut \_ KeepPrintedJobs     | Wenn festgelegt, werden die Aufträge nach dem Drucken beibehalten. Wenn der Wert nicht festgelegt ist, werden Aufträge gelöscht.                                                                                                               |
| Drucker \_ Attribut \_ lokal               | Der Drucker ist ein lokaler Drucker.                                                                                                                                                             |
| Drucker \_ Attribut \_ Netzwerk             | Der Drucker ist eine Netzwerkdrucker Verbindung.                                                                                                                                                |
| Drucker \_ Attribut \_ veröffentlicht           | Gibt an, ob der Drucker im Verzeichnisdienst veröffentlicht wird.                                                                                                                    |
| Drucker \_ Attribut in \_ Warteschlange eingereiht              | Wenn diese Einstellung festgelegt ist, wird der Drucker vor dem Spoolvorgang gedruckt und der Druckvorgang gestartet. Wenn nicht festgelegt und Drucker \_ Attribut \_ Direct nicht festgelegt ist, wird der Drucker beim Spoolvorgang Spool und druckt.      |
| Drucker \_ Attribut \_ \_ nur RAW           | Gibt an, dass nur unformatierte Datentypen Druckaufträge gespoolte werden können.                                                                                                                            |
| Drucker \_ Attribut frei \_ gegeben              | Der Drucker ist freigegeben.                                                                                                                                                                      |



 

In Windows XP und höheren Versionen von Windows kann auch der folgende Wert verwendet werden.

| Wert                   | Bedeutung                                                                                                                                                                                           |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Drucker \_ Attribut \_ Fax | Wenn festgelegt, ist der Drucker ein Faxdrucker. Dies kann nur von [**addprinter**](addprinter.md)festgelegt werden, kann jedoch von [**enumprinter**](enumprinters.md) und [**GetPrinter**](getprinter.md)abgerufen werden. |



 

In Windows Vista und höheren Versionen von Windows können auch die folgenden Werte verwendet werden.

| Wert                               | Bedeutung                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------|
| Anzeige \_ Name des Drucker Attributs \_ \_  | Ein Computer hat eine Verbindung mit diesem Drucker hergestellt und einen anzeigen Amen erhalten.           |
| Drucker \_ Attribut \_ Computer         | Der Drucker ist eine Computer spezifische Verbindung.                                             |
| Drucker \_ Attribut mit \_ pushübertragung für \_ Benutzer    | Der Drucker wurde mithilfe der Benutzer Richtlinie "Push Printer Connections" installiert.     |
| Drucker \_ Attribut \_ mit \_ gedrückter Maschine | Der Drucker wurde mithilfe der Computer Richtlinie "Push Printer Connections" installiert. |



 

In Windows Server 2003 kann auch der folgende Wert verwendet werden.

| Wert                  | Bedeutung                                                                 |
|------------------------|-------------------------------------------------------------------------|
| Drucker \_ Attribut \_ TS | Gibt an, dass der Drucker zurzeit über einen Terminal Server verbunden ist. |



 

</dd> <dt>

**Priority**
</dt> <dd>

Ein Prioritätswert, den der Spooler zum Weiterleiten von Druckaufträgen verwendet.

</dd> <dt>

**DefaultPriority**
</dt> <dd>

Der Standard Prioritätswert, der jedem Druckauftrag zugewiesen ist.

</dd> <dt>

**StartTime**
</dt> <dd>

Die früheste Uhrzeit, zu der der Drucker einen Auftrag druckt. Dieser Wert wird in Minuten angegeben, die seit 12:00 Uhr GMT (Greenwich Mean Time) verstrichen sind.

</dd> <dt>

**UntilTime**
</dt> <dd>

Der letzte Zeitpunkt, zu dem der Drucker einen Auftrag druckt. Dieser Wert wird in Minuten angegeben, die seit 12:00 Uhr GMT (Greenwich Mean Time) verstrichen sind.

</dd> <dt>

**Status**
</dt> <dd>

Der Druckerstatus. Dieser Member kann eine beliebige Kombination der folgenden Werte sein.



| Wert                               | Bedeutung                                                          |
|-------------------------------------|------------------------------------------------------------------|
| Drucker \_ Status \_ ausgelastet               | Der Drucker ist ausgelastet.                                             |
| \_ \_ druckerstatustür \_ geöffnet         | Die Drucker Tür ist offen.                                        |
| Drucker \_ Status \_ Fehler              | Der Drucker weist einen Fehlerzustand auf.                                |
| Drucker \_ Status wird \_ initialisiert.       | Der Drucker wird zurzeit initialisiert.                                     |
| Drucker Status-e/a \_ \_ \_ aktiv         | Der Drucker befindet sich in einem aktiven Eingabe-/ausgabezustand.                   |
| \_manueller Drucker Status- \_ \_ Feed       | Der Drucker befindet sich in einem manuellen Feed-Zustand.                           |
| Drucker \_ Status \_ nicht \_ Toner          | Im Drucker ist kein Toner vorhanden.                                     |
| Drucker \_ Status \_ nicht \_ verfügbar     | Der Drucker ist nicht zum Drucken verfügbar.                       |
| Drucker \_ Status \_ Offline            | Der Drucker ist offline.                                          |
| Drucker \_ Status \_ nicht genügend Arbeits \_ \_ Speicher    | Der Drucker verfügt nicht über genügend Arbeitsspeicher.                               |
| Drucker \_ Status- \_ Ausgabe \_ bin \_ voll  | Das Ausgabefach des Druckers ist voll.                                |
| Drucker \_ Status \_ Seite \_ Punt         | Der Drucker kann die aktuelle Seite nicht drucken.                       |
| Drucker \_ Status \_ Papier \_ Stau         | Das Papier ist im Drucker gejammt.                                   |
| Drucker \_ Status \_ Papier \_ out         | Der Drucker ist nicht mehr im Papier.                                     |
| Problem mit dem Drucker \_ Status \_ Papier \_     | Der Drucker hat ein Papier Problem.                                 |
| Drucker \_ Status \_ angehalten             | Der Drucker ist angehalten.                                           |
| Drucker \_ Status \_ Ausstehend \_ gelöscht  | Der Drucker wird gelöscht.                                    |
| Drucker \_ Status- \_ Energie \_ Spar Speicher        | Der Drucker befindet sich im Energiesparmodus.                               |
| Drucker \_ Status \_ Drucken           | Der Drucker wird gedruckt.                                         |
| Drucker \_ Status \_ Verarbeitung         | Der Drucker verarbeitet einen Druckauftrag.                           |
| Drucker \_ Status \_ Server \_ unbekannt    | Der Druckerstatus ist unbekannt.                                   |
| Drucker \_ Status- \_ Toner \_ niedrig         | Der Drucker ist niedrig auf dem Toner.                                     |
| Drucker \_ Status \_ Benutzer \_ Eingriff | Der Drucker weist einen Fehler auf, der erfordert, dass der Benutzer eine Aktion durchführen kann. |
| Drucker \_ Status \_ wartet            | Der Drucker wartet.                                          |
| Drucker \_ Status \_ \_ Aufwärmphase        | Der Drucker befindet sich in der Aufwärmphase.                                       |



 

</dd> <dt>

**cjobs**
</dt> <dd>

Die Anzahl der Druckaufträge, die für den Drucker in die Warteschlange eingereiht wurden.

</dd> <dt>

**AveragePPM**
</dt> <dd>

Die durchschnittliche Anzahl der Seiten pro Minute, die auf dem Drucker gedruckt wurden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ Drucker \_ Info \_ 2W** (Unicode) und **\_ Drucker \_ Info \_ 2a** (ANSI)<br/>                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**Enumdrucker**](enumprinters.md)
</dt> <dt>

[**Drucker \_ Informationen \_ 1**](printer-info-1.md)
</dt> <dt>

[**Drucker \_ Informationen \_ 3**](printer-info-3.md)
</dt> <dt>

[**Drucker \_ Info \_ 4**](printer-info-4.md)
</dt> <dt>

[**Sicherheits \_ Beschreibung**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

