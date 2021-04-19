---
description: Jedes Protokoll im EventLog-Schlüssel enthält Unterschlüssel, die als Ereignis Quellen bezeichnet werden. Die Ereignis Quelle ist der Name der Software, von der das Ereignis protokolliert wird.
ms.assetid: bc7fdc74-be41-4d17-997c-27171ef73f0f
title: Ereignisquellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2b408b76cdbc6e93e44099fea2842f9655a963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345895"
---
# <a name="event-sources"></a>Ereignisquellen

Jedes Protokoll im [EventLog-Schlüssel](eventlog-key.md) enthält Unterschlüssel, die als *Ereignis Quellen* bezeichnet werden. Die Ereignis Quelle ist der Name der Software, von der das Ereignis protokolliert wird. Dies ist häufig der Name der Anwendung oder der Name einer Unterkomponente der Anwendung, wenn die Anwendung groß ist. Sie können der Registrierung maximal 16.384 Ereignis Quellen hinzufügen. Das **Sicherheits** Protokoll ist nur für die Verwendung durch das System vorgesehen. Gerätetreiber sollten ihre Namen dem **System** Protokoll hinzufügen. Anwendungen und Dienste sollten ihre Namen dem **Anwendungs** Protokoll hinzufügen oder ein benutzerdefiniertes Protokoll erstellen.

Die Struktur der Ereignis Quellen lautet wie folgt:

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

Sie können keinen Quellnamen verwenden, der bereits als Protokoll Name verwendet wurde. Außerdem können Quellnamen nicht hierarchisch sein. Das heißt, Sie dürfen keinen umgekehrten Schrägstrich (" \\ ") enthalten.

Jede Ereignis Quelle enthält Informationen (z. b. eine [Nachrichtendatei](message-files.md)), die für die Software spezifisch sind, die die Ereignisse protokolliert, wie in der folgenden Tabelle dargestellt.



<table>
<thead>
<tr class="header">
<th>Registrierungs Wert</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>CategoryCount</strong></td>
<td>Anzahl der unterstützten Ereignis Kategorien. Dieser Wert ist vom Typ <strong>REG_DWORD</strong>.</td>
</tr>
<tr class="even">
<td><strong>Categorymessagefile</strong></td>
<td>Der Pfad zur kategorienachrichtendatei. Eine kategorienachrichtendatei enthält sprachabhängige Zeichen folgen, die die Kategorien beschreiben. Dieser Wert kann vom Typ <strong>REG_SZ</strong> oder <strong>REG_EXPAND_SZ</strong>sein.</td>
</tr>
<tr class="odd">
<td><strong>EventMessageFile</strong></td>
<td>Der Pfad zu einer oder mehreren Ereignis Meldungs Dateien. Verwenden Sie ein Semikolon, um mehrere Dateien zu begrenzen. Eine Ereignis Nachrichtendatei enthält sprachabhängige Zeichen folgen, die die Ereignisse beschreiben. Dieser Wert kann vom Typ <strong>REG_SZ</strong> oder <strong>REG_EXPAND_SZ</strong>sein.</td>
</tr>
<tr class="even">
<td><strong>ParameterMessageFile</strong></td>
<td>Der Pfad zur Parameter Nachrichtendatei. Eine Parameter Nachrichtendatei enthält sprachunabhängige Zeichen folgen, die in die Ereignis Beschreibungs Zeichenfolgen eingefügt werden sollen. Dieser Wert kann vom Typ <strong>REG_SZ</strong> oder <strong>REG_EXPAND_SZ</strong>sein.</td>
</tr>
<tr class="odd">
<td><strong>Typessupported</strong></td>
<td>Bitmaske unterstützter Typen. Dieser Wert ist vom Typ <strong>REG_DWORD</strong>. Folgende Werte sind möglich: <dl> <strong>EVENTLOG_AUDIT_FAILURE</strong> (0x0010)<br />
<strong>EVENTLOG_AUDIT_SUCCESS</strong> (0x0008)<br />
<strong>EVENTLOG_ERROR_TYPE</strong> (0x0001)<br />
<strong>EVENTLOG_INFORMATION_TYPE</strong> (0x0004)<br />
<strong>EVENTLOG_WARNING_TYPE</strong> (0x0002)<br />
</dl></td>
</tr>
</tbody>
</table>



 

Wenn eine Anwendung die [**registereventsource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) -Funktion oder die [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) -Funktion verwendet, um ein Handle für ein Ereignisprotokoll zu erhalten, sucht der Ereignis Protokollierungs Dienst nach der angegebenen Ereignis Quelle in der Registrierung. Beispielsweise kann das **Anwendungs** Protokoll Ereignis Quellen für Microsoft SQL Server und Microsoft Excel enthalten. Wenn eine Anwendung " [**registereventsource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) " oder " **OpenEventLog** " mit dem Quellnamen "Application", "SQL" oder "Excel" verwendet, gibt der Ereignis Protokollierungs Dienst ein Handle an das **Anwendungs** Protokoll zurück.

Eine Anwendung kann das **Anwendungs** Protokoll verwenden, ohne der Registrierung eine neue Ereignis Quelle hinzuzufügen. Wenn die Anwendung [**registereventsource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) aufruft und einen Quellnamen übergibt, der in der Registrierung nicht gefunden werden kann, verwendet der Ereignis Protokollierungs Dienst standardmäßig das **Anwendungs** Protokoll. Da jedoch keine Nachrichten Dateien vorhanden sind, kann der Ereignisanzeige keine Ereignis Bezeichner oder Ereignis Kategorien einer Beschreibungs Zeichenfolge zuordnen und zeigt einen Fehler an. Aus diesem Grund sollten Sie der Registrierung eine eindeutige Ereignis Quelle für Ihre Anwendung hinzufügen und eine Nachrichtendatei angeben.

 

 



