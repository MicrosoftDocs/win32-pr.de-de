---
description: 'Dieses Thema ist wie folgt organisiert:'
title: Auswählen einer statischen oder dynamischen Kontextmenü Methode
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 44227BCF-D35E-4a9e-B4E6-D50E6AFBAEDF
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 70c6cb74e2c9a432bfdae2f26da1fdbebfc5f00b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042569"
---
# <a name="choosing-a-static-or-dynamic-shortcut-menu-method"></a>Auswählen einer statischen oder dynamischen Kontextmenü Methode

Dieses Thema ist wie folgt organisiert:

-   [Verb Methode auswählen](#choose-a-verb-method)
    -   [Statische Verb-Methoden](#static-verb-methods)
    -   [Bevorzugte dynamische Verb-Methoden](#preferred-dynamic-verb-methods)
    -   [Nicht abgewehrt dynamische Verb Methoden](#discouraged-dynamic-verb-methods)
-   [Erweitern eines Kontextmenüs](#extend-a-shortcut-menu)
-   [Unterstützung für Verb-Methoden nach Betriebs System](#support-for-verb-methods-by-operating-system)
-   [Zugehörige Themen](#related-topics)

## <a name="choose-a-verb-method"></a>Verb Methode auswählen

Es wird dringend empfohlen, dass Sie ein Kontextmenü mit einer der statischen Verb-Methoden implementieren.

### <a name="static-verb-methods"></a>Statische Verb-Methoden

Statische Verben sind die einfachsten zu implementierenden Verben, aber Sie bieten weiterhin umfassende Funktionen. Wählen Sie immer die einfachste Kontextmenü Methode aus, die Ihren Anforderungen entspricht.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Statisches Verb</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>" <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>Kreateprocess</strong></a> " mit Befehlszeilen Parametern</td>
<td>Dies ist die einfachste und vertraute Methode zum Implementieren eines statischen Verbs. Ein Prozess wird durch einen Aufruf der Funktion " <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>deateprocess</strong></a> " mit den ausgewählten Dateien und allen optionalen Parametern aufgerufen, die als Befehlszeile übergeben werden. Dadurch wird die Datei oder der Ordner geöffnet.<br/> Für diese Methode gelten die folgenden Einschränkungen:
<ul>
<li>Die Länge der Befehlszeile ist auf 2000 Zeichen beschränkt, was die Anzahl der Elemente einschränkt, die das Verb verarbeiten kann.</li>
<li>Kann nur mit Dateisystem Elementen verwendet werden.</li>
<li>Die Wiederverwendung eines bereits laufenden Prozesses wird von nicht unterstützt.</li>
<li>Erfordert, dass eine ausführbare Datei installiert wird, um das Verb zu verarbeiten.</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><strong>DropTarget</strong> / <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"> <strong>IDropTarget</strong></a></td>
<td>Eine COM-basierte Verb Aktivierung bedeutet, dass die in-proc-oder out-of-proc-Aktivierung unterstützt. <strong>DropTarget</strong> / <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a> unterstützt auch die Wiederverwendung eines bereits laufenden Handlers, wenn die <strong>IDropTarget</strong> -Schnittstelle von einem lokalen Server implementiert wird. Außerdem werden die Elemente über das gemarshallte Datenobjekt hervorragend ausgedrückt, und es wird ein Verweis auf die aufrufende Site Kette bereitgestellt, sodass Sie mit dem aufrufende Instanz über den <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService</strong></a>interagieren können.</td>
</tr>
<tr class="odd">
<td>Windows 7 und höher: <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"> <strong>iexecutecommand</strong></a></td>
<td>Die direkteste Implementierungsmethode. Da es sich hierbei um eine COM-basierte Aufruf Methode (z. b. DropTarget) handelt, unterstützt diese Schnittstelle in-proc und außerhalb der proc-Aktivierung. Das Verb implementiert <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>iexecutecommand</strong></a> und <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithselection"><strong>iobjectwithselection</strong></a>und optional <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializecommand"><strong>iinitializecommand</strong></a>. Die Elemente werden direkt als shellelementarray weitergegeben, und weitere Parameter aus dem aufrufende Instanz sind für die Verb-Implementierung verfügbar, einschließlich des Aufruf Punkts, des Tastatur Zustands usw.</td>
</tr>
<tr class="even">
<td>Windows 7 und höher:<strong>explorercommand</strong> /  <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a></td>
<td>Ermöglicht Datenquellen, die ihre Befehls Modul Befehle über <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>IExplorerCommandProvider</strong></a> bereitstellen, diese Befehle als Verben in einem Kontextmenü zu verwenden. Da diese Schnittstelle nur die Prozess interne Aktivierung unterstützt, empfiehlt es sich, von shelldatenquellen zu verwenden, die die Implementierung zwischen Befehlen und Kontextmenüs freigeben müssen.</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) ist ein Hybrid zwischen einem statischen und dynamischen Verb. **IExplorerCommand** wurde in Windows Vista deklariert, aber seine Fähigkeit zum Implementieren eines Verbs in einem Kontextmenü ist neu in Windows 7.

 

Weitere Informationen zu [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) -und Shell-Abfragen für Datei Zuordnungs Attribute finden Sie unter [wahrgenommene Typen und Anwendungs Registrierung](fa-perceivedtypes.md).

### <a name="preferred-dynamic-verb-methods"></a>Bevorzugte dynamische Verb-Methoden

Die folgenden dynamischen Verb Methoden werden bevorzugt:



| Vertyp                                                                                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Statisches Verb (in der vorherigen Tabelle aufgelistet) + Erweiterte Abfrage Syntax (AQS)                  | Mit dieser Auswahl wird die Sichtbarkeit des dynamischen Verbs abgerufen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Windows 7 und höher: [ **IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)                         | Diese Auswahl aktiviert eine gängige Implementierung von Verben-und Explorer-Befehlen, die im Befehls Modul in Windows-Explorer angezeigt werden.                                                                                                                                                                                                                                                                                                                                                                                               |
| Windows 7 und höher: [**iexplorercommandstate**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) + statisches Verb | Diese Auswahl erhält auch dynamische Verb Sichtbarkeit. Dabei handelt es sich um ein Hybridmodell, bei dem ein einfacher in-Process-Handler verwendet wird, um zu berechnen, ob ein bestimmtes statisches Verb verteilt werden soll. Dies kann auf alle statischen Verb Implementierungs Methoden angewendet werden, um dynamisches Verhalten zu erreichen und das verfügbar machen der in-Process-Logik zu minimieren. [**Iexplorercommandstate**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) hat den Vorteil, dass Sie in einem Hintergrund Thread ausgeführt wird. Dadurch wird die Benutzeroberfläche nicht mehr reagiert. Es ist wesentlich einfacher als [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu). |



 

### <a name="discouraged-dynamic-verb-methods"></a>Nicht abgewehrt dynamische Verb Methoden

[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) ist die leistungsfähigste, aber auch die komplizierteste Methode, die implementiert werden kann. Es basiert auf in-Process-COM-Objekten, die auf dem Thread des Aufrufers ausgeführt werden, der normalerweise Windows Explorer ist, aber eine beliebige Anwendung sein kann, die die Elemente gehostet. **IContextMenu** unterstützt die Sichtbarkeit, Reihenfolge und benutzerdefinierte Zeichnung. Einige dieser Features wurden den statischen Verb Features hinzugefügt, z. b. einem Symbol, das einem Befehl zugeordnet werden soll, und [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) , um die Sichtbarkeit zu behandeln.

Wenn Sie das Kontextmenü für einen Dateityp erweitern müssen, indem Sie für den Dateityp ein dynamisches Verb registrieren, befolgen Sie die Anweisungen unter [Anpassen eines Kontextmenüs mithilfe dynamischer Verben](shortcut-menu-using-dynamic-verbs.md).

## <a name="extend-a-shortcut-menu"></a>Erweitern eines Kontextmenüs

Nachdem Sie eine Verb Methode ausgewählt haben, können Sie ein Kontextmenü für einen Dateityp erweitern, indem Sie für den Dateityp ein statisches Verb registrieren. Weitere Informationen finden Sie unter [Erstellen von Kontextmenü Handlern](context-menu-handlers.md).

## <a name="support-for-verb-methods-by-operating-system"></a>Unterstützung für Verb-Methoden nach Betriebs System

In der folgenden Tabelle sind die Unterstützung für Verb Aufruf Methoden nach Betriebssystem aufgeführt.



|                      |            |               |                      |
|----------------------|------------|---------------|----------------------|
|                      | Windows XP | Windows Vista | Windows 7 und darüber hinaus |
| CreateProcess        | X          | X             | X                    |
| DDE                  | X          | X             | X                    |
| DropTarget           | X          | X             | X                    |
| ExecuteCommand       |            | X             | X                    |
| Explorercommand      |            |               | X                    |
| Explorercommandstate |            |               | X                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bewährte Methoden für Kontextmenü Handler und Mehrfachauswahl Verben](verbs-best-practices.md)
</dt> <dt>

[Erstellen von Kontextmenü Handlern](context-menu-handlers.md)
</dt> <dt>

[Anpassen eines Kontextmenüs mithilfe dynamischer Verben](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[Kontextmenüs und Kontextmenü Handler](context-menu.md)
</dt> <dt>

[Verweis auf das Kontextmenü](context-menu-reference.md)
</dt> <dt>

[Verben und Dateizuordnungen](fa-verbs.md)
</dt> </dl>

 

 
