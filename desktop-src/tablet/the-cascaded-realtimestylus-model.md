---
description: Übersicht über das kaskadierenden-Modell für die RealTimeStylus-Klasse.
ms.assetid: f4c377a7-979d-4a06-a8de-31b8e67d74f8
title: Das Cascaded RealTimeStylus-Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2f61ea3cd44753d1d91fb2662226a716ee5590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104561841"
---
# <a name="the-cascaded-realtimestylus-model"></a>Das Cascaded RealTimeStylus-Modell

Das kaskadierenden [**RealTimeStylus**](realtimestylus-class.md) -Modell ermöglicht es Ihnen, zwei **RealTimeStylus** -Objekte zu verwenden, die jeweils in einem anderen Thread ausgeführt werden. Mit diesem Modell fügen Sie ein sekundäres **RealTimeStylus** -Objekt an ein primäres **RealTimeStylus** -Objekt an. Das sekundäre **RealTimeStylus** -Objekt wird als einziges asynchrones Plug-in in die asynchrone Plug-in-Auflistung des primären **RealTimeStylus** -Objekts angefügt.

Das kaskadierenden [**RealTimeStylus**](realtimestylus-class.md) -Modell kann in den folgenden Szenarien nützlich sein.

-   Sie können bestimmte Aufgaben hinzufügen, die rechnerisch anspruchsvoll sind, aber trotzdem in Echtzeit auf den Datenstrom des Tablettstifts zugreifen müssen, z. b. die Erkennung von Zeitgeber-Gesten, um die synchrone Plug-in-Auflistung des sekundären [**RealTimeStylus**](realtimestylus-class.md) -Objekts zu erhalten.
-   Sie können die computingressource ihrer synchronen Plug-Ins auf zwei Threads verteilen und so Verzögerungen bei der frei Hand Erfassung auf einigen Tablet PCs verringern.

Das folgende Diagramm veranschaulicht den Fluss von Tablet Pen-Daten durch zwei kaskadierenden- [**RealTimeStylus**](realtimestylus-class.md) -Objekte und deren Plug-in-Auflistungen.

![Abbildung mit einem kaskadierenden RealTimeStylus-Datenfluss](images/72ca1999-e078-49f8-a336-3b4d0157a472.gif)

In diesem Diagramm stellt der Kreis "A" Tablet Pen-Daten dar, die bereits von den primären und sekundären [**RealTimeStylus**](realtimestylus-class.md) -Objekten verarbeitet und in der Ausgabe Warteschlange des sekundären **RealTimeStylus** -Objekts abgelegt wurden. Der Kreis mit dem Wert "B" stellt Tablet-Stift Daten dar, die bereits vom primären **RealTimeStylus** -Objekt verarbeitet und der Ausgabe Warteschlange des primären **RealTimeStylus** -Objekts hinzugefügt wurden und noch nicht an das sekundäre **RealTimeStylus** -Objekt gesendet wurden. Der Kreis mit dem Wert "C" stellt die Tablet Pen-Daten dar, die das primäre **RealTimeStylus** -Objekt gerade verarbeitet. Sie wird an die synchrone Plug-in-Auflistung gesendet und in der Ausgabe Warteschlange abgelegt. Der leere Kreis stellt die Position in der Ausgabe Warteschlange dar, an der zukünftige Tablet Pen-Daten hinzugefügt werden.

## <a name="constraints"></a>Einschränkungen

Wenn Sie den standardmäßigen [**RealTimeStylus**](realtimestylus-class.md) -Konstruktor verwenden, erstellen Sie ein **RealTimeStylus** -Objekt, das nur Eingaben von einem anderen **RealTimeStylus** -Objekt akzeptieren kann.

In der folgenden Liste werden die Einschränkungen beschrieben, die mit der Verwendung des kaskadierenden [**RealTimeStylus**](realtimestylus-class.md) -Modells verknüpft sind.

-   Es können nur zwei [**RealTimeStylus**](realtimestylus-class.md) -Objekte verwendet werden, ein primäres **RealTimeStylus** -Objekt und ein sekundäres **RealTimeStylus** -Objekt.
-   Das primäre [**RealTimeStylus**](realtimestylus-class.md) -Objekt muss mit einem Konstruktor erstellt werden, der den Parameter " **AttachedControl** " oder " *handle* " verwendet. Das sekundäre **RealTimeStylus** -Objekt muss mit dem No-Argument-Konstruktor erstellt werden.
-   Das sekundäre [**RealTimeStylus**](realtimestylus-class.md) -Objekt muss das einzige asynchrone Plug-in in der asynchronen Plug-in-Auflistung des primären **RealTimeStylus** -Objekts sein.
-   Ein sekundäres [**RealTimeStylus**](realtimestylus-class.md) -Objekt kann jeweils nur an ein primäres **RealTimeStylus** -Objekt angefügt werden. Wenn Sie einem zweiten primären **RealTimeStylus** -Objekt hinzugefügt wird, löst die [Add](/previous-versions/ms824814(v=msdn.10)) -Methode eine Ausnahme aus, und das sekundäre **RealTimeStylus** -Objekt ist nicht an das zweite primäre **RealTimeStylus** -Objekt angefügt.
-   Das Verhalten einiger der Elemente des sekundären [**RealTimeStylus**](realtimestylus-class.md) -Objekts wird geändert. In der folgenden Tabelle wird das geänderte Verhalten dieser Member beschrieben.

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Member</th>
    <th>Verhalten</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><a href="/previous-versions/ms825905(v=msdn.10)">GetDesiredPacketDescription</a></td>
    <td>Diese Methode gibt die Informationen aus dem primären <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> -Objekt zurück.<br/> Wenn der sekundäre <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> nicht an ein primäres <strong>RealTimeStylus</strong> -Objekt angefügt ist, gibt diese Methode den Standardwert zurück.<br/></td>
    </tr>
    <tr class="even">
    <td><a href="/previous-versions/ms826041(v=msdn.10)">SetDesiredPacketDescription</a></td>
    <td>Diese Methode löst eine <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> -Ausnahme aus.<br/></td>
    </tr>
    <tr class="odd">
    <td><a href="/previous-versions/ms825913(v=msdn.10)">GetStyluses</a></td>
    <td>Diese Methode gibt die Informationen aus dem primären <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> -Objekt zurück.<br/> Wenn der sekundäre <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> nicht an ein primäres <strong>RealTimeStylus</strong> -Objekt angefügt ist, gibt diese Methode ein leeres Array zurück.<br/></td>
    </tr>
    <tr class="even">
    <td><a href="/previous-versions/ms824832(v=msdn.10)">Aktiviert</a></td>
    <td>Wenn Sie diese Eigenschaft erhalten, werden die Informationen aus dem primären <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> -Objekt zurückgegeben.<br/> Wenn der sekundäre <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> nicht an ein primäres <strong>RealTimeStylus</strong> -Objekt angefügt ist, wird beim erhalten dieser Eigenschaft der Standardwert zurückgegeben.<br/>
    <blockquote>
    [!Note]<br />
Durch Festlegen dieser Eigenschaft wird eine <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> -Ausnahme ausgelöst.
    </blockquote>
    <br/></td>
    </tr>
    <tr class="odd">
    <td><a href="/previous-versions/ms824834(v=msdn.10)">Windowinputrechteck</a></td>
    <td>Wenn Sie diese Eigenschaft erhalten, werden die Informationen aus dem primären <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> -Objekt zurückgegeben.<br/> Wenn der sekundäre <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> nicht an ein primäres <strong>RealTimeStylus</strong> -Objekt angefügt ist, wird beim erhalten dieser Eigenschaft der Standardwert zurückgegeben.<br/>
    <blockquote>
    [!Note]<br />
Durch Festlegen dieser Eigenschaft wird eine <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> -Ausnahme ausgelöst.
    </blockquote>
    <br/></td>
    </tr>
    </tbody>
    </table>

    

     

-   Es wird erwartet, dass das übergeordnete [**RealTimeStylus**](realtimestylus-class.md) -Objekt nicht mehr funktioniert, wenn der untergeordnete **RealTimeStylus** verworfen wird.

 

 
