---
description: Ereignisbezeichner identifizieren ein bestimmtes Ereignis eindeutig.
ms.assetid: 83a84db4-572b-48bd-bc0f-071b2089a5ca
title: Ereignisbezeichner (Ereignisprotokollierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 933ef3fafe77a2d0fbc2e62b5b11dd499eb850dc5cb6b2ecdc6c952fe1a3f205
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951439"
---
# <a name="event-identifiers-event-logging"></a>Ereignisbezeichner (Ereignisprotokollierung)

Ereignisbezeichner identifizieren ein bestimmtes Ereignis eindeutig. Jede [Ereignisquelle](event-sources.md) kann eigene nummerierte Ereignisse und die Beschreibungszeichenfolgen definieren, denen sie in der Nachrichtendatei zugeordnet sind. Ereignisanzeigen können diese Zeichenfolgen dem Benutzer anzeigen. Sie sollten dem Benutzer helfen, zu verstehen, was schief gelaufen ist, und vorschlagen, welche Maßnahmen ergriffen werden sollen. Leiten Sie die Beschreibung an die Benutzer, die ihre eigenen Probleme lösen, nicht an Administratoren oder Supporttechniker. Weitere Informationen finden Sie unter [Richtlinien für Fehlermeldungen.](/windows/desktop/Debug/error-message-guidelines)

## <a name="format"></a>Format

Das folgende Diagramm veranschaulicht das Format eines Ereignisbezeichners.

``` syntax
  3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
  1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
 +---+-+-+-----------------------+-------------------------------+
 |Sev|C|R|     Facility          |               Code            |
 +---+-+-+-----------------------+-------------------------------+
```

<dl> <dt>

<span id="Sev"></span><span id="sev"></span><span id="SEV"></span>Sev
</dt> <dd>

Schweregrad Der Schweregrad ist wie folgt definiert:

<dl> <dd>00 – Erfolgreich</dd> <dd>01 – Information</dd> <dd>10 – Warnung</dd> <dd>11 – Fehler</dd> </dl> </dd> <dt>

<span id="C"></span><span id="c"></span>C
</dt> <dd>

Kundenbit. Dieses Bit wird wie folgt definiert:

<dl> <dd>0 – Systemcode</dd> <dd>1– Kundencode</dd> </dl> </dd> <dt>

<span id="R"></span><span id="r"></span>R
</dt> <dd>

Reservierte Bitzahl.

</dd> <dt>

<span id="Facility"></span><span id="facility"></span><span id="FACILITY"></span>Anlage
</dt> <dd>

Einrichtungscode. Dieser Wert kann FACILITY \_ NULL sein.

</dd> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Code
</dt> <dd>

Statuscode für die Einrichtung.

</dd> </dl>

## <a name="message-definitions"></a>Nachrichtendefinitionen

Nachrichten werden in der Ereignismeldungsdatei definiert. Die Beschreibungszeichenfolgen in der Ereignismeldungsdatei werden nach Ereignisbezeichner indiziert, sodass Ereignisanzeige ereignisspezifischen Text für jedes Ereignis basierend auf dem Ereignisbezeichner anzeigen kann. Alle Beschreibungen sind lokalisiert und sprachabhängig. Weitere Informationen zum Erstellen einer Nachrichtendatei finden Sie unter [Nachrichtentextdateien.](message-text-files.md)

Die Beschreibungszeichenfolgen können Platzhalter für Einfügezeichenfolgen im Format %*n* enthalten, wobei %1 die erste Einfügezeichenfolge angibt usw. Im Folgenden ist beispielsweise ein Beispieleintrag in der MC-Datei enthalten:

``` syntax
MessageId=0x4
Severity=Error
Facility=System
SymbolicName=MSG_CMD_DELETE
Language=English
File %1 contains %2, which is in error.
.
```

In diesem Fall enthält der von [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) zurückgegebene Puffer Einfügezeichenfolgen. Der **NumStrings-Member** der [**EVENTLOGRECORD-Struktur**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) gibt die Anzahl der Einfügezeichenfolgen an. Der **StringOffset-Member** der **EVENTLOGRECORD-Struktur** gibt die Position der ersten Einfügezeichenfolge im Puffer an. Sie können ein Array von \_ DWORD-PTRs übergeben, die beim Aufrufen der [**FormatMessage-Funktion**](/windows/desktop/api/winbase/nf-winbase-formatmessage) auf die Adresse jeder Zeichenfolge im Puffer zeigen, und die Zeichenfolgen werden in die Nachricht eingefügt.

Die Beschreibungszeichenfolge kann auch Platzhalter für Parameterzeichenfolgen aus der Parametermeldungsdatei enthalten. Die Platzhalter haben das Format %%*n*, wobei %%1 durch die Parameterzeichenfolge mit dem Bezeichner 1 ersetzt wird usw. Es liegt jedoch an Ihnen, die Parameterzeichenfolgen in die Meldungszeichenfolge einzufügen, die [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) zurückgibt. In der Regel rufen Sie **FormatMessage** auf, um die Nachrichtenzeichenfolge für das Ereignis abzurufen. Anschließend analysieren Sie die Meldungszeichenfolge für %%*n* Parameter. Wenn die Nachricht einen oder mehrere Parameter enthält, laden Sie den **ParameterMessageFile-Registrierungswert** für die Quelle. Abrufen Sie für jeden Parameter in der Nachrichtenzeichenfolge den Bezeichner, und übergeben Sie ihn an **FormatMessage,** um die Parameterzeichenfolge abzurufen. Ersetzen Sie den Parameter in der Meldungszeichenfolge durch die Parameterzeichenfolge, die **FormatMessage** zurückgegeben hat.

## <a name="insertion-strings"></a>Einfügezeichenfolgen

Einfügezeichenfolgen sind optionale sprachunabhängige Zeichenfolgen, die zum Ausfüllen von Werten für Platzhalter in Beschreibungszeichenfolgen verwendet werden. Da die Zeichenfolgen nicht lokalisiert sind, ist es wichtig, dass diese Platzhalter nur verwendet werden, um sprachunabhängige Zeichenfolgen wie numerische Werte, Dateinamen, Benutzernamen usw. darzustellen. Die Zeichenfolgenlänge darf 32 Kilobyte bis 1 Zeichen nicht überschreiten.

Vermeiden Sie die Verwendung mehrerer Zeichenfolgen, um eine größere Beschreibung zu erstellen. Eine Einfügezeichenfolge sollte als Daten und nicht als Text behandelt werden. Im folgenden Beispiel sollten pszString1 und pszString2 beispielsweise nicht als Einfügezeichenfolgen für pszDescription verwendet werden.

``` syntax
LPSTR pszString1 = "successfully"; 
LPSTR pszString2 = "not"; 
LPSTR pszDescription = "The user was %1 added to the database.";
```

Im folgenden Beispiel ist es sinnvoll, entweder pszString1 oder pszString2 für die Einfügezeichenfolge in pszDescription zu verwenden.

``` syntax
LPSTR pszString1 = "c:\\testapp1.c"; 
LPSTR pszString2 = "c:\\testapp2.c"; 
LPSTR pszDescription = "Access denied. Attempted to open the file %1."
```

 

 
