---
description: Jedes Protokoll im Eventlog-Schlüssel enthält Unterschlüssel, die als Ereignisquellen bezeichnet werden. Die Ereignisquelle ist der Name der Software, die das Ereignis protokolliert.
ms.assetid: bc7fdc74-be41-4d17-997c-27171ef73f0f
title: Ereignisquellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75c82c3328709a16ee7788025624a904ae7e25a21ddc83cecc9c41b27c283ab7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914790"
---
# <a name="event-sources"></a>Ereignisquellen

Jedes Protokoll im [Eventlog-Schlüssel](eventlog-key.md) enthält Unterschlüssel, die als Ereignisquellen bezeichnet *werden.* Die Ereignisquelle ist der Name der Software, die das Ereignis protokolliert. Dies ist häufig der Name der Anwendung oder der Name einer Unterkomponente der Anwendung, wenn die Anwendung groß ist. Sie können der Registrierung maximal 16.384 Ereignisquellen hinzufügen. Das **Sicherheitsprotokoll** ist nur für die Systemverwendung vorgesehen. Gerätetreiber sollten ihre Namen dem **Systemprotokoll** hinzufügen. Anwendungen und Dienste sollten ihre Namen dem **Anwendungsprotokoll** hinzufügen oder ein benutzerdefiniertes Protokoll erstellen.

Die Struktur der Ereignisquellen sieht wie folgt aus:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            EventLog
               Application
                  AppName
               Security
               System
                  DriverName
               CustomLog
                  AppName
```

Sie können keinen Quellnamen verwenden, der bereits als Protokollname verwendet wurde. Darüber hinaus können Quellnamen nicht hierarchisch sein. das heißt, sie dürfen keinen umgekehrten Schrägstrich ("") enthalten. \\

Jede Ereignisquelle enthält Informationen (z. B. eine [Nachrichtendatei),](message-files.md)die für die Software spezifisch sind, die die Ereignisse protokolliert, wie in der folgenden Tabelle dargestellt.



<table>
<thead>
<tr class="header">
<th>Registrierungswert</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>CategoryCount</strong></td>
<td>Anzahl der unterstützten Ereigniskategorien. Dieser Wert ist vom Typ <strong>REG_DWORD</strong>.</td>
</tr>
<tr class="even">
<td><strong>CategoryMessageFile</strong></td>
<td>Pfad zur Kategoriemeldungsdatei. Eine Kategoriemeldungsdatei enthält sprachabhängige Zeichenfolgen, die die Kategorien beschreiben. Dieser Wert kann vom Typ <strong>REG_SZ</strong> oder <strong>REG_EXPAND_SZ</strong>sein.</td>
</tr>
<tr class="odd">
<td><strong>EventMessageFile</strong></td>
<td>Pfad zu einer oder mehreren Ereignismeldungsdateien; Verwenden Sie ein Semikolon, um mehrere Dateien zu begrenzen. Eine Ereignismeldungsdatei enthält sprachabhängige Zeichenfolgen, die die Ereignisse beschreiben. Dieser Wert kann vom Typ <strong>REG_SZ</strong> oder <strong>REG_EXPAND_SZ</strong>sein.</td>
</tr>
<tr class="even">
<td><strong>ParameterMessageFile</strong></td>
<td>Pfad zur Parametermeldungsdatei. Eine Parametermeldungsdatei enthält sprachunabhängige Zeichenfolgen, die in die Zeichenfolgen der Ereignisbeschreibung eingefügt werden sollen. Dieser Wert kann vom Typ <strong>REG_SZ</strong> oder <strong>REG_EXPAND_SZ</strong>sein.</td>
</tr>
<tr class="odd">
<td><strong>TypesSupported</strong></td>
<td>Bitmaske mit unterstützten Typen. Dieser Wert ist vom Typ <strong>REG_DWORD</strong>. Dies kann mindestens einer der folgenden Werte sein: <dl> <strong>EVENTLOG_AUDIT_FAILURE</strong> (0x0010)<br />
<strong>EVENTLOG_AUDIT_SUCCESS</strong> (0x0008)<br />
<strong>EVENTLOG_ERROR_TYPE</strong> (0x0001)<br />
<strong>EVENTLOG_INFORMATION_TYPE</strong> (0x0004)<br />
<strong>EVENTLOG_WARNING_TYPE</strong> (0x0002)<br />
</dl></td>
</tr>
</tbody>
</table>



 

Wenn eine Anwendung die [**RegisterEventSource-**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) oder [**OpenEventLog-Funktion**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) verwendet, um ein Handle für ein Ereignisprotokoll abzurufen, sucht der Ereignisprotokollierungsdienst nach der angegebenen Ereignisquelle in der Registrierung. Beispielsweise kann das **Anwendungsprotokoll** Ereignisquellen für Microsoft SQL Server und Microsoft Excel enthalten. Wenn eine Anwendung [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) oder **OpenEventLog** mit dem Quellnamen Application, SQL oder Excel verwendet, gibt der Ereignisprotokollierungsdienst ein Handle für das **Anwendungsprotokoll** zurück.

Eine Anwendung kann das **Anwendungsprotokoll** verwenden, ohne der Registrierung eine neue Ereignisquelle hinzuzufügen. Wenn die Anwendung [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) aufruft und einen Quellnamen übergibt, der in der Registrierung nicht gefunden werden kann, verwendet der Ereignisprotokollierungsdienst standardmäßig das **Anwendungsprotokoll.** Da es jedoch keine Meldungsdateien gibt, kann der Ereignisanzeige keine Ereignisbezeichner oder Ereigniskategorien einer Beschreibungszeichenfolge zuordnen und zeigt einen Fehler an. Aus diesem Grund sollten Sie der Registrierung für Ihre Anwendung eine eindeutige Ereignisquelle hinzufügen und eine Meldungsdatei angeben.

 

 



