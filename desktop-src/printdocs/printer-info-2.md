---
description: Die PRINTER \_ INFO \_ 2-Struktur gibt detaillierte Druckerinformationen an.
ms.assetid: 944cbfcd-9edf-4b60-a45c-9bb1839f8141
title: PRINTER_INFO_2 -Struktur (Winspool.h)
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
ms.openlocfilehash: 1f7a2b871cc0181fbceab56e4ac14170bf46fa1b31081f4b4365ad7296ec2e85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600610"
---
# <a name="printer_info_2-structure"></a>PRINTER \_ INFO \_ 2-Struktur

Die **PRINTER \_ INFO \_ 2-Struktur** gibt detaillierte Druckerinformationen an.

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

**pServerName**
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Server identifiziert, der den Drucker steuert. Wenn diese Zeichenfolge **NULL ist,** wird der Drucker lokal gesteuert.

</dd> <dt>

**pPrinterName**
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen des Druckers angibt.

</dd> <dt>

**pShareName**
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Freigabepunkt für den Drucker identifiziert. (Diese Zeichenfolge wird nur verwendet, wenn der DRUCKER \_ Die \_ ATTRIBUTE SHARED-Konstante wurde für das **Attributes-Member** festgelegt.)

</dd> <dt>

**pPortName**
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die die Ports identifiziert, die zum Übertragen von Daten an den Drucker verwendet werden. Wenn ein Drucker mit mehr als einem Anschluss verbunden ist, müssen die Namen der einzelnen Ports durch Kommas getrennt werden (z.B. "LPT1:,LPT2:,LPT3:").

</dd> <dt>

**pDriverName**
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen des Druckertreibers angibt.

</dd> <dt>

**pComment**
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die eine kurze Beschreibung des Druckers enthält.

</dd> <dt>

**pLocation**
</dt> <dd>

Ein Zeiger auf eine auf NULL terminierte Zeichenfolge, die den physischen Speicherort des Druckers angibt (z. B. "Bldg. 38, Raum 1164").

</dd> <dt>

**pDevMode**
</dt> <dd>

Ein Zeiger auf eine [**DEVMODE-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-devmodea) die Standarddruckerdaten definiert, z. B. die Papierausrichtung und die Auflösung.

</dd> <dt>

**pSepFile**
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen der Datei angibt, die zum Erstellen der Trennseite verwendet wird. Diese Seite wird verwendet, um druckaufträge zu trennen, die an den Drucker gesendet werden.

</dd> <dt>

**pPrintProcessor**
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen des vom Drucker verwendeten Druckprozessors angibt. Sie können die [**EnumPrintProcessors-Funktion**](enumprintprocessors.md) verwenden, um eine Liste der auf einem Server installierten Druckprozessoren zu erhalten.

</dd> <dt>

**pDatatype**
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Datentyp angibt, der zum Aufzeichnen des Druckauftrags verwendet wird. Sie können die [**Funktion EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) verwenden, um eine Liste der Datentypen zu erhalten, die von einem bestimmten Druckprozessor unterstützt werden.

</dd> <dt>

**pParameters**
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die die Standardparameter des Druckprozessors angibt.

</dd> <dt>

**pSecurityDescriptor**
</dt> <dd>

Ein Zeiger auf eine [**SECURITY \_ DESCRIPTOR-Struktur**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) für den Drucker. Dieser Member kann NULL **sein.**

</dd> <dt>

**Attribute**
</dt> <dd>

Die Druckerattribute. Dieser Member kann eine beliebige sinnvolle Kombination der folgenden Werte sein.

| Wert                                   | Bedeutung                                                                                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PRINTER \_ ATTRIBUTE \_ DIRECT              | Der Auftrag wird direkt an den Drucker gesendet (er wird nicht in einen Pool pooliert).                                                                                                                                |
| \_ \_ DRUCKERATTRIBUT \_ ZUERST \_ ABGESCHLOSSEN | Wenn set und printer für das Drucken während des Spoolings festgelegt sind, werden alle Aufträge, die das Spooling abgeschlossen haben, so geplant, dass sie vor Aufträgen gedruckt werden, die das Spoolen nicht abgeschlossen haben.                          |
| PRINTER \_ ATTRIBUTE ENABLE DEVQ (DRUCKERATTRIBUT \_ AKTIVIEREN VON \_ DEVQ)        | Wenn festgelegt, **wird DevQueryPrint** aufgerufen. **DevQueryPrint kann** fehlschlagen, wenn die Dokument- und Druckersetups nicht übereinstimmen. Wenn Sie dieses Flag festlegen, werden nicht übereinstimmende Dokumente in der Warteschlange gespeichert. |
| \_DRUCKERATTRIBUT \_ AUSGEBLENDET              | Reserviert.                                                                                                                                                                               |
| \_ \_ DRUCKERATTRIBUT KEEPPRINTEDJOBS     | Wenn festgelegt, werden Aufträge beibehalten, nachdem sie gedruckt wurden. Wenn der Satz nicht geändert wird, werden Aufträge gelöscht.                                                                                                               |
| \_DRUCKERATTRIBUT \_ LOKAL               | Der Drucker ist ein lokaler Drucker.                                                                                                                                                             |
| \_ \_ DRUCKERATTRIBUTNETZWERK             | Drucker ist eine Netzwerkdruckerverbindung.                                                                                                                                                |
| \_DRUCKERATTRIBUT \_ VERÖFFENTLICHT           | Gibt an, ob der Drucker im Verzeichnisdienst veröffentlicht wird.                                                                                                                    |
| \_ \_ DRUCKERATTRIBUT IN WARTESCHLANGE              | Wenn festgelegt, wird der Drucker gepoolt und mit dem Drucken gestartet, nachdem die letzte Seite in die Warteschlange gesetzt wurde. Wenn nicht festgelegt und PRINTER ATTRIBUTE DIRECT nicht festgelegt ist, wird der Drucker beim Spoolen gepoolt \_ \_ und gedruckt.      |
| NUR \_ \_ RAW-DRUCKERATTRIBUT \_           | Gibt an, dass nur Unformatierte Druckaufträge vom Datentyp spoolt werden können.                                                                                                                            |
| \_DRUCKERATTRIBUT \_ FREIGEGEBEN              | Der Drucker wird freigegeben.                                                                                                                                                                      |



 

In Windows XP und neueren Versionen von Windows kann auch der folgende Wert verwendet werden.

| Wert                   | Bedeutung                                                                                                                                                                                           |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_DRUCKERATTRIBUT \_ FAX | Wenn festgelegt, ist der Drucker ein Faxdrucker. Dies kann nur von [**AddPrinter**](addprinter.md)festgelegt werden, kann aber von [**EnumPrinters**](enumprinters.md) und [**GetPrinter abgerufen werden.**](getprinter.md) |



 

In Windows Vista und neueren Versionen von Windows können auch die folgenden Werte verwendet werden.

| Wert                               | Bedeutung                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------|
| ANGEZEIGTER \_ NAME \_ DES \_ DRUCKERATTRIBUTS  | Ein Computer hat mit diesem Drucker verbunden und ihm einen Benutzerfreundlichen Namen gegeben.           |
| \_DRUCKERATTRIBUTCOMPUTER \_         | Drucker ist eine Computerverbindung.                                             |
| \_ \_ DRUCKERATTRIBUT PUSHED \_ USER    | Der Drucker wurde mithilfe der Benutzerrichtlinie Pushdruckerverbindungen installiert.     |
| \_ \_ DRUCKERATTRIBUT – PUSHCOMPUTER \_ | Der Drucker wurde mithilfe der Computerrichtlinie Pushdruckerverbindungen installiert. |



 

In Windows Server 2003 kann auch der folgende Wert verwendet werden.

| Wert                  | Bedeutung                                                                 |
|------------------------|-------------------------------------------------------------------------|
| \_DRUCKERATTRIBUT \_ TS | Gibt an, dass der Drucker derzeit über einen Terminalserver verbunden ist. |



 

</dd> <dt>

**Priority**
</dt> <dd>

Ein Prioritätswert, der vom Spooler zum Routen von Druckaufträgen verwendet wird.

</dd> <dt>

**DefaultPriority**
</dt> <dd>

Der Standardprioritätswert, der jedem Druckauftrag zugewiesen ist.

</dd> <dt>

**StartTime**
</dt> <dd>

Der früheste Zeitpunkt, zu dem der Drucker einen Auftrag druckt. Dieser Wert wird als seit 12:00 Uhr GMT (Greenwich Mean Time) verstrichene Minuten ausgedrückt.

</dd> <dt>

**UntilTime**
</dt> <dd>

Der letzte Zeitpunkt, zu dem der Drucker einen Auftrag druckt. Dieser Wert wird als seit 12:00 Uhr GMT (Greenwich Mean Time) verstrichene Minuten ausgedrückt.

</dd> <dt>

**Status**
</dt> <dd>

Der Druckerstatus. Dieser Member kann eine beliebige sinnvolle Kombination der folgenden Werte sein.



| Wert                               | Bedeutung                                                          |
|-------------------------------------|------------------------------------------------------------------|
| DRUCKERSTATUS \_ \_ AUSGELASTET               | Der Drucker ist ausgelastet.                                             |
| \_ \_ DRUCKERSTATUSTÜR \_ GEÖFFNET         | Die Druckertür ist geöffnet.                                        |
| \_ \_ DRUCKERSTATUSFEHLER              | Der Drucker weist einen Fehlerzustand auf.                                |
| DRUCKERSTATUS \_ \_ WIRD INITIALISIERT       | Der Drucker wird zurzeit initialisiert.                                     |
| DRUCKERSTATUS \_ \_ E/A \_ AKTIV         | Der Drucker befindet sich in einem aktiven Eingabe-/Ausgabezustand.                   |
| DRUCKERSTATUS \_ \_ – MANUELLER \_ FEED       | Der Drucker befindet sich in einem manuellen Vorschubzustand.                           |
| DRUCKERSTATUS \_ \_ KEIN \_ TONER          | Im Drucker ist kein Toner vorhanden.                                     |
| DRUCKERSTATUS \_ \_ NICHT \_ VERFÜGBAR     | Der Drucker ist nicht zum Drucken verfügbar.                       |
| DRUCKERSTATUS \_ \_ OFFLINE            | Der Drucker ist offline.                                          |
| DRUCKERSTATUS \_ \_ NICHT GENÜGEND \_ \_ ARBEITSSPEICHER    | Für den Drucker ist nicht genügend Arbeitsspeicher verfügbar.                               |
| \_ \_ DRUCKERSTATUSAUSGABEBEHÄLTER \_ \_ VOLL  | Das Ausgabefach des Druckers ist voll.                                |
| \_ \_ DRUCKERSTATUSSEITE \_ PUNT         | Der Drucker kann die aktuelle Seite nicht drucken.                       |
| \_DRUCKERSTATUS \_ \_ PAPIERSTAU         | Papier ist im Drucker verkleinert                                   |
| DRUCKERSTATUS \_ \_ AUF \_ PAPIER         | Der Drucker ist ohne Papier.                                     |
| \_DRUCKERSTATUS \_ \_ PAPIERPROBLEM     | Der Drucker hat ein Papierproblem.                                 |
| DRUCKERSTATUS \_ \_ ANGEHALTEN             | Der Drucker ist angehalten.                                           |
| DRUCKERSTATUS \_ \_ AUSSTEHEND \_ BEIM LÖSCHEN  | Der Drucker wird gelöscht.                                    |
| DRUCKERSTATUS \_ \_ – \_ STROMSPAREN        | Der Drucker befindet sich im Energiesparmodus.                               |
| \_ \_ DRUCKERSTATUSDRUCK           | Der Drucker druckt.                                         |
| \_ \_ DRUCKERSTATUSVERARBEITUNG         | Der Drucker verarbeitet einen Druckauftrag.                           |
| \_ \_ DRUCKERSTATUSSERVER \_ UNBEKANNT    | Der Druckerstatus ist unbekannt.                                   |
| DRUCKERSTATUS \_ \_ TONER \_ LOW         | Der Drucker verfügt über wenig Toner.                                     |
| \_DRUCKERSTATUS \_ \_ BENUTZEREINGRIFF | Der Drucker hat einen Fehler, der erfordert, dass der Benutzer etwas tun muss. |
| DRUCKERSTATUS \_ \_ WARTET            | Der Drucker wartet.                                          |
| \_ \_ \_ DRUCKERSTATUSAUFWÄRMUNG        | Der Drucker befindet sich in der Aufwärmphase.                                       |



 

</dd> <dt>

**cJobs**
</dt> <dd>

Die Anzahl der Druckaufträge, die für den Drucker in die Warteschlange gestellt wurden.

</dd> <dt>

**AveragePPM**
</dt> <dd>

Die durchschnittliche Anzahl von Seiten pro Minute, die auf dem Drucker gedruckt wurden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ PRINTER \_ INFO \_ 2W** (Unicode) und **\_ PRINTER INFO \_ \_ 2A** (ANSI)<br/>                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Devmode**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**DRUCKERINFORMATIONEN \_ \_ 1**](printer-info-1.md)
</dt> <dt>

[**DRUCKERINFORMATIONEN \_ \_ 3**](printer-info-3.md)
</dt> <dt>

[**DRUCKERINFORMATIONEN \_ \_ 4**](printer-info-4.md)
</dt> <dt>

[**\_SICHERHEITSDESKRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

