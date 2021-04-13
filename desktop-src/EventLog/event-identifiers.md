---
description: Ereignis Bezeichner identifizieren ein bestimmtes Ereignis eindeutig.
ms.assetid: 83a84db4-572b-48bd-bc0f-071b2089a5ca
title: Ereignis Bezeichner (Ereignisprotokollierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402337cb2c7e862785a88ec604c6382152736fd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527272"
---
# <a name="event-identifiers-event-logging"></a>Ereignis Bezeichner (Ereignisprotokollierung)

Ereignis Bezeichner identifizieren ein bestimmtes Ereignis eindeutig. Jede [Ereignis Quelle](event-sources.md) kann Ihre eigenen nummerierten Ereignisse und die Beschreibungs Zeichenfolgen definieren, denen Sie in ihrer Nachrichtendatei zugeordnet sind. Ereignis Betrachter können diese Zeichen folgen für den Benutzer darstellen. Sie sollten dem Benutzer helfen, zu verstehen, was schief gelaufen ist, und die zu übergreifenden Maßnahmen vorzuschlagen. Leiten Sie die Beschreibung an Benutzer weiter, die ihre eigenen Probleme lösen, nicht bei Administratoren oder Support Technikern. Weitere Informationen finden Sie unter [Richtlinien für Fehlermeldungen](/windows/desktop/Debug/error-message-guidelines).

## <a name="format"></a>Format

Das folgende Diagramm veranschaulicht das Format eines Ereignis Bezeichners.

``` syntax
  3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
  1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
 +---+-+-+-----------------------+-------------------------------+
 |Sev|C|R|     Facility          |               Code            |
 +---+-+-+-----------------------+-------------------------------+
```

<dl> <dt>

<span id="Sev"></span><span id="sev"></span><span id="SEV"></span>Schweregrad
</dt> <dd>

Schweregrad Der Schweregrad wird wie folgt definiert:

<dl> <dd>00-Erfolg</dd> <dd>01-Information</dd> <dd>10-Warnung</dd> <dd>11-Fehler</dd> </dl> </dd> <dt>

<span id="C"></span><span id="c"></span>Scher
</dt> <dd>

Customer-Bit. Dieses Bit wird wie folgt definiert:

<dl> <dd>0-System Code</dd> <dd>1: Kundencode</dd> </dl> </dd> <dt>

<span id="R"></span><span id="r"></span>R
</dt> <dd>

Reservierte Bitzahl.

</dd> <dt>

<span id="Facility"></span><span id="facility"></span><span id="FACILITY"></span>Maschine
</dt> <dd>

Betriebs Code. Dieser Wert kann eine Anlage \_ NULL sein.

</dd> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Ordnung
</dt> <dd>

Status Code für die Einrichtung.

</dd> </dl>

## <a name="message-definitions"></a>Nachrichten Definitionen

Nachrichten werden in der Ereignis Nachrichtendatei definiert. Die Beschreibungs Zeichenfolgen in der Ereignis Meldungs Datei werden anhand der Ereignis Kennung indiziert, sodass Ereignisanzeige ereignisspezifischen Text für ein beliebiges Ereignis basierend auf dem Ereignis Bezeichner anzeigen kann. Alle Beschreibungen sind lokalisiert und von der Sprache abhängig. Weitere Informationen zum Aufbau einer Nachrichtendatei finden Sie unter [Message Text Files](message-text-files.md).

Die Beschreibungs Zeichenfolgen enthalten möglicherweise Einfügungs Zeichenfolgen im Format "%*n*", wobei "%1" die erste Einfügezeichenfolge angibt usw. Das folgende Beispiel zeigt einen Beispiel Eintrag in der MC-Datei:

``` syntax
MessageId=0x4
Severity=Error
Facility=System
SymbolicName=MSG_CMD_DELETE
Language=English
File %1 contains %2, which is in error.
.
```

In diesem Fall enthält der von [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) zurückgegebene Puffer Einfügezeichenfolgen. Der **numstrings** -Member der [**EventLogRecord**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) -Struktur gibt die Anzahl der Einfügezeichenfolgen an. Der **stringoffset** -Member der **EventLogRecord** -Struktur gibt den Speicherort der ersten Einfügezeichenfolge im Puffer an. Sie können ein Array von DWORD \_ -PTRS übergeben, das auf die Adresse jeder Zeichenfolge im Puffer zeigt, wenn Sie die [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) -Funktion aufrufen, und Sie fügt die Zeichen folgen in die Nachricht ein.

Die Beschreibungs Zeichenfolge kann auch Platzhalter für Parameter Zeichenfolgen aus der Parameter Nachrichtendatei enthalten. Die Platzhalter weisen das Format%%*n* auf, wobei% %1 durch die Parameter Zeichenfolge mit dem Bezeichner 1 ersetzt wird usw. Allerdings müssen Sie die Parameter Zeichenfolgen in die von [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) zurückgegebene Meldungs Zeichenfolge einfügen. In der Regel rufen Sie **FormatMessage** auf, um die Meldungs Zeichenfolge für das Ereignis zu erhalten. Anschließend analysieren Sie die Meldungs Zeichenfolge für%%*n* Parameter. Wenn die Nachricht einen oder mehrere Parameter enthält, laden Sie den **ParameterMessageFile** -Registrierungs Wert für die Quelle. Rufen Sie für jeden Parameter in der Meldungs Zeichenfolge den Bezeichner ab, und übergeben Sie ihn an **FormatMessage** , um den Parameter String zu erhalten. Ersetzen Sie den-Parameter in der Nachrichten Zeichenfolge durch die von **FormatMessage** zurückgegebene Parameter Zeichenfolge.

## <a name="insertion-strings"></a>Einfügen von Zeichen folgen

Einfügezeichenfolgen sind optionale sprachunabhängige Zeichen folgen, mit denen Werte für Platzhalter in Beschreibungs Zeichenfolgen ausgefüllt werden Da die Zeichen folgen nicht lokalisiert werden, ist es wichtig, dass diese Platzhalter nur zur Darstellung von sprachunabhängigen Zeichen folgen verwendet werden, wie z. b. numerische Werte, Dateinamen, Benutzernamen usw. Die Zeichen folgen Länge darf nicht länger als 32 Kilobyte-1 Zeichen sein.

Vermeiden Sie die Verwendung mehrerer Zeichen folgen, um eine größere Beschreibung zu erstellen. Eine Einfügezeichenfolge sollte als Daten und nicht als Text behandelt werden. Im folgenden Beispiel sollten z. b. pszString1 und pszString2 nicht als Einfügezeichenfolgen für pszdescription verwendet werden.

``` syntax
LPSTR pszString1 = "successfully"; 
LPSTR pszString2 = "not"; 
LPSTR pszDescription = "The user was %1 added to the database.";
```

Im folgenden Beispiel ist es sinnvoll, für die Einfügezeichenfolge in pszdescription entweder pszString1 oder pszString2 zu verwenden.

``` syntax
LPSTR pszString1 = "c:\\testapp1.c"; 
LPSTR pszString2 = "c:\\testapp2.c"; 
LPSTR pszDescription = "Access denied. Attempted to open the file %1."
```

 

 
