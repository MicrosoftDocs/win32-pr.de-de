---
description: Wählen Sie eine statische oder dynamische Kontextmenümethode aus, wenn Sie ein benutzerdefiniertes Dateiformat in der Windows Shell implementieren.
title: Auswählen einer statischen oder dynamischen Kontextmenümethode
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 44227BCF-D35E-4a9e-B4E6-D50E6AFBAEDF
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 22f6a0edd0820127e65915fbc3c67645cf759354
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475546"
---
# <a name="choosing-a-static-or-dynamic-shortcut-menu-method"></a>Auswählen einer statischen oder dynamischen Kontextmenümethode

Dieses Thema ist wie folgt organisiert:

-   [Auswählen einer Verbmethode](#choose-a-verb-method)
    -   [Statische Verbmethoden](#static-verb-methods)
    -   [Bevorzugte dynamische Verbmethoden](#preferred-dynamic-verb-methods)
    -   [Von dynamischen Verbmethoden abgeraten](#discouraged-dynamic-verb-methods)
-   [Erweitern eines Kontextmenüs](#extend-a-shortcut-menu)
-   [Unterstützung für Verbmethoden nach Betriebssystem](#support-for-verb-methods-by-operating-system)
-   [Zugehörige Themen](#related-topics)

## <a name="choose-a-verb-method"></a>Auswählen einer Verbmethode

Es wird dringend empfohlen, ein Kontextmenü mit einer der statischen Verbmethoden zu implementieren.

### <a name="static-verb-methods"></a>Statische Verbmethoden

Statische Verben sind die einfachsten Verben, die implementiert werden müssen, bieten aber dennoch umfangreiche Funktionen. Wählen Sie immer die einfachste Kontextmenümethode aus, die Ihren Anforderungen entspricht.




| Statisches Verb | BESCHREIBUNG | 
|-------------|-------------|
| <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> mit Befehlszeilenparametern | Dies ist das einfachste und vertrauteste Mittel zum Implementieren eines statischen Verbs. Ein Prozess wird durch einen Aufruf der <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess-Funktion</strong></a> mit den ausgewählten Dateien und optionalen Parametern aufgerufen, die als Befehlszeile übergeben werden. Dadurch wird die Datei oder der Ordner geöffnet.<br /> Für diese Methode gelten die folgenden Einschränkungen:<ul><li>Die Befehlszeilenlänge ist auf 2.000 Zeichen beschränkt, wodurch die Anzahl der Elemente begrenzt wird, die das Verb verarbeiten kann.</li><li>Kann nur mit Dateisystemelementen verwendet werden.</li><li>Aktiviert nicht die erneute Verwendung eines bereits ausgeführten Prozesses.</li><li>Erfordert, dass eine ausführbare Datei installiert wird, um das Verb zu verarbeiten.</li></ul><br /> | 
| <strong>DropTarget</strong> / <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"> <strong>IDropTarget</strong></a> | Eine COM-basierte Verbaktivierung bedeutet, dass die In-Proc- oder Out-of-Proc-Aktivierung unterstützt. <strong>DropTarget</strong> / <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a> unterstützt auch die erneute Verwendung eines bereits ausgeführten Handlers, wenn die <strong>IDropTarget-Schnittstelle</strong> von einem lokalen Server implementiert wird. Außerdem werden die Elemente perfekt über das gemarshallte Datenobjekt ausgedrückt, und es wird ein Verweis auf die aufrufende Websitekette angezeigt, sodass Sie über <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>queryService</strong></a>mit dem Aufrufer interagieren können. | 
| Windows 7 und höher: <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"> <strong>IExecuteCommand</strong></a> | Die direkteste Implementierungsmethode. Da es sich um eine COM-basierte Aufrufmethode (z.B. DropTarget) handelt, unterstützt diese Schnittstelle die In-Proc- und Out-of-Proc-Aktivierung. Das Verb implementiert <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a> und <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithselection"><strong>IObjectWithSelection</strong></a>und optional <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializecommand"><strong>IInitializeCommand.</strong></a> Die Elemente werden direkt als Shell-Elementarray übergeben, und weitere Parameter des Aufrufrs sind für die Verbimplementierungen verfügbar, einschließlich des Aufrufpunkts, des Tastaturzustands usw. | 
| Windows 7 und höher:<strong>ExplorerCommand</strong> /  <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a> | Ermöglicht Datenquellen, die ihre Befehlsmodulbefehle über <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>IExplorerCommandProvider</strong></a> bereitstellen, diese Befehle als Verben in einem Kontextmenü zu verwenden. Da diese Schnittstelle nur die Prozessaktivierung unterstützt, wird die Verwendung durch Shell-Datenquellen empfohlen, die die Implementierung zwischen Befehlen und Kontextmenüs freigeben müssen. | 




 

> [!Note]  
> [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) ist ein Hybrid zwischen einem statischen und einem dynamischen Verb. **IExplorerCommand** wurde in Windows Vista deklariert, aber die Möglichkeit, ein Verb in einem Kontextmenü zu implementieren, ist neu in Windows 7.

 

Weitere Informationen zu [**IDropTarget-**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) und Shell-Abfragen für Dateizuordnungsattribute finden Sie unter [Wahrgenommene Typen und Anwendungsregistrierung.](fa-perceivedtypes.md)

### <a name="preferred-dynamic-verb-methods"></a>Bevorzugte dynamische Verbmethoden

Die folgenden dynamischen Verbmethoden werden bevorzugt:



| Verbtyp                                                                                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Statisches Verb (in der vorherigen Tabelle aufgeführt) + Erweiterte Abfragesyntax (AQS)                  | Diese Auswahl ruft dynamische Verbsichtbarkeit ab.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Windows 7 und höher: [ **IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)                         | Diese Auswahl ermöglicht eine allgemeine Implementierung von Verben und Explorer-Befehlen, die im Befehlsmodul in Windows Explorer angezeigt werden.                                                                                                                                                                                                                                                                                                                                                                                               |
| Windows 7 und höher: [**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) + statisches Verb | Diese Auswahl erhält auch dynamische Verbsichtbarkeit. Es handelt sich um ein Hybridmodell, bei dem ein einfacher In-Process-Handler verwendet wird, um zu berechnen, ob ein bestimmtes statisches Verb disponiert werden soll. Dies kann auf alle Implementierungsmethoden für statische Verben angewendet werden, um dynamisches Verhalten zu erzielen und die Gefährdung der Prozesslogik zu minimieren. [**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) bietet den Vorteil der Ausführung in einem Hintergrundthread und vermeidet dadurch das Hängen der Benutzeroberfläche. Sie ist erheblich einfacher als [**IContextMenu.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) |



 

### <a name="discouraged-dynamic-verb-methods"></a>Von dynamischen Verbmethoden abgeraten

[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) ist die leistungsfähigste, aber auch die komplizierteste Methode, die implementiert werden muss. Sie basiert auf prozessin-process-COM-Objekten, die im Thread des Aufrufers ausgeführt werden. Dies Windows Explorer, kann aber eine beliebige Anwendung sein, die die Elemente hostet. **IContextMenu** unterstützt Verbsichtbarkeit, Sortierung und benutzerdefiniertes Zeichnen. Einige dieser Features wurden den statischen Verbfeatures hinzugefügt, z. B. einem Symbol, das einem Befehl zugeordnet werden soll, und [**IExplorerCommand,**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) um die Sichtbarkeit zu behandeln.

Wenn Sie das Kontextmenü für einen Dateityp erweitern müssen, indem Sie ein dynamisches Verb für den Dateityp registrieren, befolgen Sie die Anweisungen unter [Anpassen eines Kontextmenüs mit dynamischen Verben.](shortcut-menu-using-dynamic-verbs.md)

## <a name="extend-a-shortcut-menu"></a>Erweitern eines Kontextmenüs

Nachdem Sie eine Verbmethode ausgewählt haben, können Sie ein Kontextmenü für einen Dateityp erweitern, indem Sie ein statisches Verb für den Dateityp registrieren. Weitere Informationen finden Sie unter [Erstellen von Kontextmenühandlern.](context-menu-handlers.md)

## <a name="support-for-verb-methods-by-operating-system"></a>Unterstützung für Verbmethoden nach Betriebssystem

Die Unterstützung für Verbaufrufmethoden nach Betriebssystem ist in der folgenden Tabelle aufgeführt.



| Verb-Methode          | Windows XP | Windows Vista | Windows 7 und darüber hinaus |
|----------------------|------------|---------------|----------------------|
| CreateProcess        | X          | X             | X                    |
| DDE                  | X          | X             | X                    |
| DropTarget           | X          | X             | X                    |
| Executecommand       |            | X             | X                    |
| ExplorerCommand      |            |               | X                    |
| ExplorerCommandState |            |               | X                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bewährte Methoden für Kontextmenühandler und Verben für mehrfache Auswahl](verbs-best-practices.md)
</dt> <dt>

[Erstellen von Kontextmenühandlern](context-menu-handlers.md)
</dt> <dt>

[Anpassen eines Kontextmenüs mit dynamischen Verben](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[Kontextmenüs und Kontextmenühandler](context-menu.md)
</dt> <dt>

[Kontextmenüreferenz](context-menu-reference.md)
</dt> <dt>

[Verben und Dateizuordnungen](fa-verbs.md)
</dt> </dl>

 

 
