---
description: Die NMEVENTDATA-Struktur enthält Informationen zu einer Ereignisbedingung, die an Netzwerkmonitor übergeben wird, um eine Zeile in den Expert Viewer einzufügungen.
ms.assetid: 35cda410-d45a-4a51-91b7-8bd4a0c9957f
title: NMEVENTDATA-Struktur (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMEVENTDATA
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: af2a4775be7d9e123974fbab865a8171d9bc9dec7dacae7692054bc6db0d3085
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037040"
---
# <a name="nmeventdata-structure"></a>NMEVENTDATA-Struktur

Die **NMEVENTDATA-Struktur** enthält Informationen zu einer Ereignisbedingung, die an Netzwerkmonitor übergeben wird, um eine Zeile in den Expert Viewer einzufügungen.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  BYTE         Version;
  DWORD        EventIdent;
  DWORD        Flags;
  DWORD        Severity;
  BYTE         NumColumns;
  LPSTR        szSourceName;
  LPSTR        szEventName;
  LPSTR        szDescription;
  LPSTR        szMachine;
  JTYPE        Justification;
  LPSTR        szUrl;
  SYSTEMTIME   SysTime;
  NMCOLUMNINFO Column[];
} NMEVENTDATA, *PNMEVENTDATA;
```



## <a name="members"></a>Member

<dl> <dt>

**Version**
</dt> <dd>

Versionsnummer der **NMEVENTDATA-Struktur.** Die Versionsnummer muss 0 (null) sein. Zukünftige Versionen von Netzwerkmonitor unterstützen möglicherweise eine höhere Versionsnummer.

</dd> <dt>

**EventIdent**
</dt> <dd>

Bezeichner des Ereignisses **EventIdent** ist für jeden Experten eindeutig und verweist auf eine [Ereignisreferenzseite.](event-reference-page.md)

</dd> <dt>

**Flags**
</dt> <dd>

Eine Gruppe von Flags, die beschreiben, wer die Ereignisdaten sendet und wie das Ereignis angezeigt wird.



| Wert                                                                                                                                                                                                                                              | Bedeutung                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EVENT_FLAG_EXPERT"></span><span id="event_flag_expert"></span><dl> <dt>**EVENT \_ FLAG \_ EXPERT**</dt> </dl>                                                                         | Die Veranstaltung stammt von einem Experten. <br/>                                                                                                                                  |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_SEVERITY"></span><span id="nmeventflag_do_not_display_severity"></span><dl> <dt>**NMEVENTFLAG \_ ZEIGT KEINEN SCHWEREGRAD \_ \_ \_ AN**</dt> </dl>                 | Zeigen Sie den Schweregrad für das Ereignis nicht an. <br/>                                                                                                                |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_SOURCE"></span><span id="nmeventflag_do_not_display_source"></span><dl> <dt>**NMEVENTFLAG \_ ZEIGT QUELLE NICHT \_ \_ \_ AN**</dt> </dl>                       | Zeigen Sie den Quellnamen für das Ereignis nicht an. <br/>                                                                                                                   |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_EVENT_NAME"></span><span id="nmeventflag_do_not_display_event_name"></span><dl> <dt>**NMEVENTFLAG \_ ZEIGT \_ KEINEN \_ \_ EREIGNISNAMEN \_ AN**</dt> </dl>          | Zeigen Sie den Ereignisnamen für das Ereignis nicht an. <br/>                                                                                                                    |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_DESCRIPTION"></span><span id="nmeventflag_do_not_display_description"></span><dl> <dt>**NMEVENTFLAG \_ ZEIGT KEINE BESCHREIBUNG \_ \_ \_ AN**</dt> </dl>        | Zeigen Sie die Beschreibung für das Ereignis nicht an. <br/>                                                                                                                   |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_MACHINE"></span><span id="nmeventflag_do_not_display_machine"></span><dl> <dt>**NMEVENTFLAG \_ ZEIGT COMPUTER NICHT \_ \_ \_ AN**</dt> </dl>                    | Zeigen Sie den Computernamen für das Ereignis nicht an. <br/>                                                                                                                  |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_TIME"></span><span id="nmeventflag_do_not_display_time"></span><dl> <dt>**NMEVENTFLAG \_ ZEIGT KEINE ZEIT \_ \_ \_ AN**</dt> </dl>                             | Zeit für das Ereignis nicht anzeigen <br/>                                                                                                                           |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_FIXED_COLUMNS"></span><span id="nmeventflag_do_not_display_fixed_columns"></span><dl> <dt>**NMEVENTFLAG \_ ZEIGT KEINE FESTEN SPALTEN \_ \_ \_ \_ AN**</dt> </dl> | Die Spalten Schweregrad, Quelle, Ereignisname, Beschreibung, Computer oder Uhrzeit werden nicht angezeigt. Dies ist kein einzelnes Flag, aber es ist eine Vereinigung der vorherigen sechs Flags. <br/> |



 

</dd> <dt>

**Severity**
</dt> <dd>

Schweregrad des Ereignisses. Der Schweregrad kann einen der folgenden Werte haben:

NMEVENT \_ SEVERITY \_ INFORMATIONAL NMEVENT \_ SEVERITY \_ WARNING NMEVENT \_ SEVERITY \_ STRONG \_ WARNING NMEVENT \_ SEVERITY \_ ERROR NMEVENT \_ SEVERITY \_ SEVERE \_ ERROR NMEVENT \_ SEVERITY \_ CRITICAL \_ ERROR

</dd> <dt>

**NumColumns**
</dt> <dd>

Anzahl der spalten, die in der aktuellen Struktur angegeben sind.

</dd> <dt>

**szSourceName**
</dt> <dd>

Name des angezeigten Experten.

</dd> <dt>

**szEventName**
</dt> <dd>

Name des angezeigten Ereignisses.

</dd> <dt>

**szDescription**
</dt> <dd>

Beschreibung des angezeigten Ereignisses.

</dd> <dt>

**szMachine**
</dt> <dd>

Veraltet, sollte NULL **sein.**

</dd> <dt>

**Begründung**
</dt> <dd>

Informationen, die im zweiten Fenster der -Ereignisanzeige. Der **Justification-Member** kann **NULL sein.** Wenn es NULL **ist,** ist das zweite Fenster nicht sichtbar.

</dd> <dt>

**szUrl**
</dt> <dd>

Reserviert; dieser Member muss NULL **sein.**

</dd> <dt>

**Systime**
</dt> <dd>

Zeitpunkt, zu dem die Ereignisbedingung auftritt. Die Zeit wird relativ zum Anfang der Erfassung gemessen.

</dd> <dt>

**Spalte**
</dt> <dd>

Tabelle mit Spaltenstrukturen, die im oberen Bereich der Tabelle Ereignisanzeige.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




