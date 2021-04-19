---
description: Überlegungen zum Erstellen oder Öffnen einer Datei mithilfe der Funktion "Funktion".
ms.assetid: 094cac29-c66d-409e-8928-878dc693d393
title: Erstellen und Öffnen von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1430675862b10f9e9221d968242481525dc7632f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362889"
---
# <a name="creating-and-opening-files"></a>Erstellen und Öffnen von Dateien

Die [**Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) "Funktion" kann eine neue Datei erstellen oder eine vorhandene Datei öffnen. Sie müssen den Dateinamen, die Erstellungs Anweisungen und andere Attribute angeben. Wenn eine Anwendung eine neue Datei erstellt, wird Sie vom Betriebssystem dem angegebenen Verzeichnis hinzugefügt.

Das Betriebssystem weist eine eindeutige ID, die als *handle* bezeichnet wird, jeder Datei zu, die mit " [**foratefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)" geöffnet oder erstellt wird. Eine Anwendung kann dieses Handle mit Funktionen verwenden, die die Datei lesen, schreiben und beschreiben. Er ist gültig, bis alle Verweise auf diesen Handle geschlossen sind. Beim Starten einer Anwendung erbt Sie alle geöffneten Handles vom Prozess, der Sie gestartet hat, wenn die Handles als vererbbar erstellt wurden.

Eine Anwendung sollte den Wert des Handles überprüfen, das von " [**kreatefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) " zurückgegeben wurde, bevor versucht wird, den Handle für den Zugriff auf die Datei zu Wenn ein Fehler auftritt, ist der Handle-Wert ein **ungültiger \_ handle- \_ Wert** , und die Anwendung kann die [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion für erweiterte Fehlerinformationen verwenden.

Wenn eine Anwendung " [**fiatefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)" verwendet, muss Sie den *dwDesiredAccess* -Parameter verwenden, um anzugeben, ob Sie aus der Datei lesen, in die Datei schreiben soll, sowohl Lese-als auch Schreibvorgänge oder keines von beiden. Dies wird als Anfordern eines *Zugriffsmodus* bezeichnet. Die Anwendung muss auch den *dwkreationdisposition* -Parameter verwenden, um anzugeben, welche Aktion ausgeführt werden soll, wenn die Datei bereits vorhanden ist, die als *Erstellungs Disposition* bezeichnet wird. Eine Anwendung kann z. b. "angleichen **Datei** " aufrufen, wobei " *dwkreationdisposition* " auf " **\_ immer erstellen** " festgelegt ist, um immer eine neue Datei zu erstellen, auch wenn bereits eine Datei mit demselben Namen vorhanden ist (wodurch die vorhandene Datei überschrieben wird). Ob dies erfolgreich ist oder nicht, hängt von Faktoren wie den Attributen der vorherigen Datei und den Sicherheitseinstellungen ab (Weitere Informationen finden Sie in den folgenden Abschnitten).

Außerdem wird in einer Anwendung mithilfe von " [**kreatefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) " angegeben, ob Sie die Datei für das Lesen, schreiben, beides oder keines von beiden freigeben möchte. Dies wird als *Freigabe Modus* bezeichnet. Eine geöffnete Datei, die nicht freigegeben ist (*dwsharemode* ist auf NULL festgelegt), kann nicht erneut geöffnet werden, entweder von der Anwendung, die Sie geöffnet hat, oder von einer anderen Anwendung, bis das Handle geschlossen wurde. Dies wird auch als exklusiver Zugriff bezeichnet.

Wenn ein Prozess mithilfe von " [**foratefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) " versucht, eine Datei zu öffnen, die bereits in einem Freigabe Modus geöffnet wurde (*dwsharemode* ist auf einen gültigen Wert ungleich NULL festgelegt), vergleicht das System die angeforderten Zugriffs-und Freigabe Modi mit den beim Öffnen der Datei angegebenen Einstellungen. Wenn Sie einen Zugriffs-oder Freigabe Modus angeben, der in Konflikt mit den im vorherigen-Befehl angegebenen Modi steht, schlägt " **foratefile** " fehl.

In der folgenden Tabelle werden die gültigen Kombinationen von zwei Aufrufen von " [**foratefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) " mithilfe verschiedener Zugriffs Modi und Freigabe Modi (*dwDesiredAccess*, *dwsharemode* ) veranschaulicht. Es spielt keine Rolle, in welcher Reihenfolge die aufgerufenen **Aufrufe durch** geführt werden. Alle nachfolgenden Datei-e/a-Vorgänge für die einzelnen Datei Handles werden jedoch weiterhin durch die aktuellen Zugriffs-und Freigabe Modi eingeschränkt, die dem jeweiligen Datei Handle zugeordnet sind.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Erster Befehl an " <a href="/windows/desktop/api/FileAPI/nf-fileapi-createfilea"> <strong>anatefile</strong> "</a></th>
<th>Gültige zweite Aufrufe von " <a href="/windows/desktop/api/FileAPI/nf-fileapi-createfilea"> <strong>kreatefile</strong> "</a></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>GENERIC_READ</strong> <strong>FILE_SHARE_READ</strong><br/></td>
<td><ul>
<li><strong>GENERIC_READ</strong> <strong>FILE_SHARE_READ</strong></li>
<li><strong>GENERIC_READ</strong> <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="even">
<td><strong>GENERIC_READ</strong> <strong>FILE_SHARE_WRITE</strong><br/></td>
<td><ul>
<li><strong>GENERIC_WRITE</strong> <strong>FILE_SHARE_READ</strong></li>
<li><strong>GENERIC_WRITE</strong> <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>GENERIC_READ</strong> <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong><br/></td>
<td><ul>
<li><strong>GENERIC_READ</strong> <strong>FILE_SHARE_READ</strong></li>
<li><strong>GENERIC_READ</strong> <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_WRITE</strong> <strong>FILE_SHARE_READ</strong></li>
<li><strong>GENERIC_WRITE</strong> <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong> <strong>FILE_SHARE_READ</strong></li>
<li><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong> <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="even">
<td><strong>GENERIC_WRITE</strong> <strong>FILE_SHARE_READ</strong><br/></td>
<td><ul>
<li><strong>GENERIC_READ</strong> <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_READ</strong> <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>GENERIC_WRITE</strong> <strong>FILE_SHARE_WRITE</strong><br/></td>
<td><ul>
<li><strong>GENERIC_WRITE</strong> <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_WRITE</strong> <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="even">
<td><strong>GENERIC_WRITE</strong> <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong><br/></td>
<td><ul>
<li><strong>GENERIC_READ</strong> <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_READ</strong> <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_WRITE</strong> <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_WRITE</strong> <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong> <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong> <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong> <strong>FILE_SHARE_READ</strong><br/></td>
<td><ul>
<li><strong>GENERIC_READ</strong> <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="even">
<td><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong> <strong>FILE_SHARE_WRITE</strong><br/></td>
<td><ul>
<li><strong>GENERIC_WRITE</strong> <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong> <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong><br/></td>
<td><ul>
<li><strong>GENERIC_READ</strong> <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_WRITE</strong> <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong> <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
</tbody>
</table>



 

Zusätzlich zu den Standarddatei Attributen können Sie auch Sicherheits Attribute angeben, indem Sie einen Zeiger auf eine Struktur von [**Sicherheits \_ Attributen**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) als vierten Parameter von " [**kreatefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)" einschließen. Allerdings muss das zugrunde liegende Dateisystem die Sicherheit unterstützen, damit dies Auswirkungen haben kann (z. b., das NTFS-Dateisystem unterstützt dies jedoch nicht die verschiedenen FAT-Dateisysteme). Weitere Informationen zu Sicherheits Attributen finden Sie unter [Access Control](/windows/desktop/SecAuthZ/access-control).

Eine Anwendung, die eine neue Datei erstellt, kann ein optionales Handle für eine Vorlagen Datei bereitstellen, aus [**der die Datei**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) Attribute und erweiterten Attribute für die Erstellung der neuen Datei von "" erstellt werden.

## <a name="createfile-scenarios"></a>Szenarios mit der Datei ""

Es gibt mehrere grundlegende Szenarios, [**um den Zugriff**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) auf eine Datei mithilfe der Funktion "Funktion" zu initiieren. Diese werden zusammengefasst als:

-   Es wird eine neue Datei erstellt, wenn nicht bereits eine Datei mit diesem Namen vorhanden ist.
-   Erstellen einer neuen Datei, auch wenn bereits eine Datei mit demselben Namen vorhanden ist, die Ihre Daten löscht und die leere Datei startet.
-   Öffnen einer vorhandenen Datei nur, wenn Sie vorhanden und nur intakt ist.
-   Eine vorhandene Datei wird nur geöffnet, wenn Sie vorhanden ist, und Sie wird so abgeschnitten, dass Sie leer ist.
-   Das Öffnen einer Datei ist immer: Wenn Sie vorhanden ist, wird eine neue Datei erstellt, wenn Sie nicht vorhanden ist.

Diese Szenarien werden durch die ordnungsgemäße Verwendung des Parameters *dwroationdisposition* gesteuert. Im folgenden finden Sie eine Aufschlüsselung der Art und Weise, wie diese Szenarien Werten für diesen Parameter zugeordnet werden und was geschieht, wenn Sie verwendet werden.

Beim Erstellen oder Öffnen einer neuen Datei, wenn noch keine Datei mit diesem Namen vorhanden ist (*dwdeationdisposition* muss entweder auf **Create \_ New**, **Create \_ Always** oder **Open \_ Always** festgelegt sein), führt [**die Funktion "Funktion" die folgenden**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) Aktionen aus:

-   Kombiniert die Dateiattribute und Flags, die von *dwflagsandattribute* angegeben werden, mit dem **Datei \_ Attribut \_ Archiv**.
-   Legt die Dateilänge auf 0 (null) fest.
-   Kopiert die erweiterten Attribute, die von der Vorlagen Datei bereitgestellt werden, in die neue Datei, wenn der *htemplatefile* -Parameter angegeben wird (Dies überschreibt alle zuvor angegebenen **file \_ \_ \* Attribute* _-Flags).
-   Legt das erbende Flag fest, das vom Element "*binherithandle**" angegeben wird, und die Sicherheits Beschreibung, die durch den **lpsecuritydescriptor** -Member des *lpsecurityattribute* -Parameters (Struktur der [**Sicherheits \_ Attribute**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) ) angegeben wird, sofern angegeben.

Wenn eine neue Datei erstellt wird, auch wenn bereits eine Datei mit demselben Namen vorhanden ist (*dwdeationdisposition* ist auf **Create \_ Always** festgelegt), führt [**die Funktion "Funktion" die folgenden**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) Aktionen aus:

-   Überprüft die aktuellen Dateiattribute und Sicherheitseinstellungen für den Schreibzugriff, wenn dies verweigert wird.
-   Kombiniert die Dateiattribute und Flags, die von *dwflagsandattribute* angegeben werden, mit dem **Datei \_ Attribut \_ Archiv** und den vorhandenen Dateiattributen.
-   Legt die Dateilänge auf NULL fest (d. h., alle in der Datei vorhandenen Daten sind nicht mehr verfügbar, und die Datei ist leer).
-   Kopiert die erweiterten Attribute, die von der Vorlagen Datei bereitgestellt werden, in die neue Datei, wenn der *htemplatefile* -Parameter angegeben wird (Dies überschreibt alle zuvor angegebenen **file \_ \_ \* Attribute* _-Flags).
-   Legt das erbende Flag fest, das vom Element "_ *binherithandle**" des *lpsecurityattribute* -Parameters (Struktur der [**Sicherheits \_ Attribute**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) ) angegeben wird, wenn angegeben, ignoriert jedoch den **lpsecuritydescriptor** -Member der Struktur der **Sicherheits \_ Attribute** .
-   Wenn andernfalls erfolgreich (d. h. [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) gibt ein gültiges Handle zurück), führt der Aufruf von [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) dazu, dass der Code **Fehler \_ bereits \_ vorhanden** ist, obwohl es für diesen speziellen Anwendungsfall nicht tatsächlich zu einem Fehler kommt (wenn Sie eine neue (leere) Datei anstelle der vorhandenen Datei erstellen wollten).

Wenn Sie eine vorhandene Datei öffnen (*dwkreationdisposition* ist auf **" \_ vorhandenes öffnen**", " **\_ immer öffnen**" oder "TRUNCATE" festgelegt), führt [**die Funktion "Funktion" die folgenden**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) Aktionen aus: **\_**

-   Überprüft die aktuellen Dateiattribute und Sicherheitseinstellungen für den angeforderten Zugriff, wenn dies verweigert wird.
-   Kombiniert die von _dwFlagsAndAttributes * angegebenen Dateiflags (**\_ Dateiflag \_ \** _) mit vorhandenen Dateiattributen und ignoriert alle Dateiattribute \_ \_ \* (* * File* Attribute _), die von _dwFlagsAndAttributes * angegeben werden.
-   Legt die Dateilänge nur dann auf NULL fest, wenn *dwkreationdisposition* auf das **Abschneiden \_ vorhandener** festgelegt ist. andernfalls wird die aktuelle Dateilänge beibehalten und die Datei unverändert geöffnet.
-   Ignoriert den *htemplatefile* -Parameter.
-   Legt das erbende Flag fest, das vom **binherithandle** -Member des *lpsecurityattribute* -Parameters (Struktur der [**Sicherheits \_ Attribute**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) ) angegeben wird, wenn angegeben, ignoriert jedoch den **lpsecuritydescriptor** -Member der Struktur der **Sicherheits \_ Attribute** .

## <a name="file-attributes-and-directories"></a>Dateiattribute und-Verzeichnisse

Dateiattribute sind Teil der Metadaten, die einer Datei oder einem Verzeichnis zugeordnet sind, von denen jede den eigenen Zweck und seine eigenen Regeln für die Festlegung und Änderung hat. Einige dieser Attribute gelten nur für Dateien und einige nur für Verzeichnisse. Das Attribut " **file \_ Attribute \_ Directory** " gilt z. b. nur für Verzeichnisse: Es wird vom Dateisystem verwendet, um zu bestimmen, ob ein Objekt auf dem Datenträger ein Verzeichnis ist, aber nicht für ein vorhandenes Dateisystem Objekt geändert werden kann.

Einige Dateiattribute können für ein Verzeichnis festgelegt werden, haben jedoch nur für Dateien, die in diesem Verzeichnis erstellt werden, eine Bedeutung, die als Standard Attribute fungieren. Beispielsweise kann **das \_ \_ komprimierte Datei Attribut** für ein Verzeichnis Objekt festgelegt werden, aber da das Verzeichnis Objekt selbst keine tatsächlichen Daten enthält, ist es nicht wirklich komprimiert. Verzeichnisse, die mit diesem Attribut gekennzeichnet sind, weisen jedoch das Dateisystem an, alle neuen Dateien zu komprimieren, die dem Verzeichnis hinzugefügt wurden. Alle Dateiattribute, die für ein Verzeichnis festgelegt werden können und auch für neue Dateien festgelegt werden, die diesem Verzeichnis hinzugefügt werden, werden als *geerbte Attribute* bezeichnet.

Die Funktion " [**deatefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) " stellt einen Parameter zum Festlegen bestimmter Dateiattribute bereit, wenn eine Datei erstellt wird. Im Allgemeinen sind diese Attribute am häufigsten für eine Anwendung, die zum Zeitpunkt der Dateierstellung verwendet werden kann, aber nicht alle möglichen Dateiattribute sind für " **anatefile**" verfügbar. Einige Dateiattribute erfordern die Verwendung anderer Funktionen wie " [**setfileattribute**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)", " [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)" oder " [**DecryptFile**](/windows/desktop/api/WinBase/nf-winbase-decryptfilea) ", nachdem die Datei bereits vorhanden ist. Im Fall eines **Datei \_ Attribut \_ Verzeichnisses** ist die Funktion " [**deatedirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) " zum Zeitpunkt der Erstellung erforderlich **, da "** Create" keine Verzeichnisse erstellen kann. Die anderen Dateiattribute, die eine besondere Behandlung erfordern, sind der **Datei \_ Attribut Analyse \_ \_ Punkt** und die Dateiattribute- **\_ \_ \_ Datei** mit geringer Dichte, die **DeviceIoControl** erfordern. Weitere Informationen finden Sie unter [**setfileattribute**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa).

Wie bereits erwähnt, tritt die Datei Attribut Vererbung auf, wenn eine Datei mit Dateiattributen erstellt wird, die aus den Verzeichnis Attributen gelesen werden, in denen sich die Datei befindet. In der folgenden Tabelle sind die geerbten Attribute und deren Beziehung zu den Funktionen von " [**foratefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) " zusammengefasst.



| Verzeichnis Attribut Status                                      | Ersetzungs [**Überschreibungs Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) für die Erstellungs Funktion für neue Dateien      |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| **Datei \_ \_Komprimierte Attribut** Satz.<br/>                | Kein Steuerelement. Löschen Sie mithilfe von " [**entviceiocontrol**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) ".<br/>    |
| **Datei \_ \_Komprimiertes Attribut** nicht festgelegt.<br/>            | Kein Steuerelement. Legen [**Sie mithilfe**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) von "Debug" den Wert fest.<br/>      |
| **Datei \_ \_Verschlüsselter Attribut** Satz.<br/>                 | Kein Steuerelement. Verwenden Sie [**DecryptFile**](/windows/desktop/api/WinBase/nf-winbase-decryptfilea).<br/>                      |
| **Datei \_ Das \_ verschlüsselte Attribut** ist nicht festgelegt.<br/>             | Kann mithilfe von " [**kreatefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)" festgelegt werden.<br/>                       |
| **Datei \_ Das Attribut ist \_ keine \_ Inhalts \_ indizierte** Gruppe.<br/>     | Kein Steuerelement. Verwenden Sie [**setfileattribute**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) , um zu löschen.<br/> |
| **Datei \_ Das nicht für \_ \_ Inhalt \_ indizierte Attribut** ist nicht festgelegt.<br/> | Kein Steuerelement. Verwenden Sie [**setfileattribute**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) , um festzulegen.<br/>   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zugriffssteuerung](/windows/desktop/SecAuthZ/access-control)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**Datei Attribut Konstanten**](file-attribute-constants.md)
</dt> <dt>

[Dateikomprimierung und-Dekomprimierung](file-compression-and-decompression.md)
</dt> <dt>

[Dateiverschlüsselung](file-encryption.md)
</dt> <dt>

[Dateiverwaltungsfunktionen](file-management-functions.md)
</dt> <dt>

[Handles und Objekte](/windows/desktop/SysInfo/handles-and-objects)
</dt> <dt>

[Behandlung von Vererbung](/windows/desktop/SysInfo/handle-inheritance)
</dt> <dt>

[Öffnen einer Datei zum Lesen oder Schreiben](opening-a-file-for-reading-or-writing.md)
</dt> <dt>

[**Setfileattribute**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)
</dt> </dl>

 

