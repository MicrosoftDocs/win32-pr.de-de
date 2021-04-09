---
description: Die nmeventdata-Struktur enthält Informationen zu einer Ereignis Bedingung, die an Netzwerkmonitor übermittelt wird, um eine Zeile in den expertenviewer einzufügen.
ms.assetid: 35cda410-d45a-4a51-91b7-8bd4a0c9957f
title: Nmeventdata-Struktur (Netmon. h)
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
ms.openlocfilehash: 6258b1b1bfde5b159165de2efb9a010053c0421a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863031"
---
# <a name="nmeventdata-structure"></a>Nmeventdata-Struktur

Die **nmeventdata** -Struktur enthält Informationen zu einer Ereignis Bedingung, die an Netzwerkmonitor übermittelt wird, um eine Zeile in den expertenviewer einzufügen.

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

Die Versionsnummer der **nmeventdata** -Struktur. Die Versionsnummer muss NULL sein. In zukünftigen Versionen von Netzwerkmonitor wird möglicherweise eine höhere Versionsnummer unterstützt.

</dd> <dt>

**Eventident**
</dt> <dd>

Bezeichner des Ereignisses **Eventident** ist für jeden Experten eindeutig und verweist auf eine [Ereignis Referenzseite](event-reference-page.md).

</dd> <dt>

**Flags**
</dt> <dd>

Ein Satz von Flags, der beschreibt, wer die Ereignisdaten sendet und wie das Ereignis angezeigt wird.



| Wert                                                                                                                                                                                                                                              | Bedeutung                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EVENT_FLAG_EXPERT"></span><span id="event_flag_expert"></span><dl> <dt>**\_ereignisflag- \_ Experte**</dt> </dl>                                                                         | Das Ereignis stammt von einem Experten. <br/>                                                                                                                                  |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_SEVERITY"></span><span id="nmeventflag_do_not_display_severity"></span><dl> <dt>**nmeventflag \_ \_ zeigt keinen \_ \_ Schweregrad an**</dt> </dl>                 | Der Schweregrad für das Ereignis wird nicht angezeigt. <br/>                                                                                                                |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_SOURCE"></span><span id="nmeventflag_do_not_display_source"></span><dl> <dt>**nmeventflag \_ \_ keine \_ Quelle anzeigen \_**</dt> </dl>                       | Der Quell Name für das Ereignis wird nicht angezeigt. <br/>                                                                                                                   |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_EVENT_NAME"></span><span id="nmeventflag_do_not_display_event_name"></span><dl> <dt>**nmeventflag \_ \_ zeigt den \_ \_ Ereignis \_ Namen nicht an**</dt> </dl>          | Der Ereignis Name für das Ereignis wird nicht angezeigt. <br/>                                                                                                                    |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_DESCRIPTION"></span><span id="nmeventflag_do_not_display_description"></span><dl> <dt>**nmeventflag \_ \_ keine \_ Beschreibung anzeigen \_**</dt> </dl>        | Die Beschreibung für das Ereignis nicht anzeigen. <br/>                                                                                                                   |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_MACHINE"></span><span id="nmeventflag_do_not_display_machine"></span><dl> <dt>**nmeventflag \_ keinen \_ \_ Computer anzeigen \_**</dt> </dl>                    | Der Computername für das Ereignis wird nicht angezeigt. <br/>                                                                                                                  |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_TIME"></span><span id="nmeventflag_do_not_display_time"></span><dl> <dt>**nmeventflag \_ \_ zeigt keine \_ \_ Zeit an**</dt> </dl>                             | Zeit für das Ereignis nicht anzeigen <br/>                                                                                                                           |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_FIXED_COLUMNS"></span><span id="nmeventflag_do_not_display_fixed_columns"></span><dl> <dt>**"nmeventflag" \_ \_ \_ zeigt keine \_ festgelegten \_ Spalten an.**</dt> </dl> | Die Spalten Schweregrad, Quelle, Ereignis Name, Beschreibung, Computer oder Zeit werden nicht angezeigt. Dabei handelt es sich nicht um ein einzelnes Flag, aber es handelt sich um eine Union der vorherigen sechs Flags. <br/> |



 

</dd> <dt>

**Severity**
</dt> <dd>

Schweregrad des Ereignisses. Der Schweregrad kann einen der folgenden Werte aufweisen:

nmevent \_ Schweregrad \_ Information nmevent \_ Schweregrad \_ Warnung nmevent \_ Schweregrad \_ Strong \_ Warnung nmevent \_ schwere \_ Fehler nmevent Schweregrad \_ \_ schwerwiegender Fehler \_ nmevent \_ Schweregrad \_ kritisch \_

</dd> <dt>

**NumColumns**
</dt> <dd>

Anzahl der in der aktuellen-Struktur bezeichneten Spalten.

</dd> <dt>

**szsourcename**
</dt> <dd>

Der Name des angezeigten Experten.

</dd> <dt>

**szeventname**
</dt> <dd>

Der Name des angezeigten Ereignisses.

</dd> <dt>

**szDescription**
</dt> <dd>

Die Beschreibung des angezeigten Ereignisses.

</dd> <dt>

**szmachine**
</dt> <dd>

Veraltet, sollte **null** sein.

</dd> <dt>

**Begründung**
</dt> <dd>

Informationen, die im zweiten Fenster der Ereignisanzeige angezeigt werden. Der  ausrichtungmember kann **null** sein. Wenn der Wert **null** ist, ist das zweite Fenster nicht sichtbar.

</dd> <dt>

**szURL**
</dt> <dd>

Bleiben Dieser Member muss **null** sein.

</dd> <dt>

**SysTime**
</dt> <dd>

Der Zeitpunkt, zu dem die Ereignis Bedingung auftritt. Die Zeit wird relativ zum Anfang der Erfassung gemessen.

</dd> <dt>

**Spalte**
</dt> <dd>

Tabelle mit Spalten Strukturen, die im oberen Bereich der Ereignisanzeige angezeigt wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




