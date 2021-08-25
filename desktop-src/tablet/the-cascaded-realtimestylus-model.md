---
description: Übersicht über das kaskadierte Modell für die RealTimeStylus-Klasse.
ms.assetid: f4c377a7-979d-4a06-a8de-31b8e67d74f8
title: Das kaskadierte RealTimeStylus-Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf848f1382a8c6a54f58fb6db864ece165c7cff2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467997"
---
# <a name="the-cascaded-realtimestylus-model"></a>Das kaskadierte RealTimeStylus-Modell

Mit dem [**kaskadierten RealTimeStylus-Modell**](realtimestylus-class.md) können Sie zwei **RealTimeStylus-Objekte** verwenden, die jeweils in einem anderen Thread ausgeführt werden. Mit diesem Modell fügen Sie ein sekundäres **RealTimeStylus-Objekt** an ein **primäres RealTimeStylus-Objekt** an. Das **sekundäre RealTimeStylus-Objekt** wird als einziges asynchrones Plug-In in der asynchronen Plug-In-Auflistung des primären **RealTimeStylus-Objekts** angefügt.

Das kaskadierte [**RealTimeStylus-Modell**](realtimestylus-class.md) kann in den folgenden Szenarien nützlich sein.

-   Sie können bestimmte Aufgaben hinzufügen, die rechenintensiv sein können, aber dennoch Echtzeitzugriff auf den Datenstrom des Tablettstifts erfordern, z. B. die Erkennung von Multistrokegesten, auf die synchrone Plug-In-Sammlung des sekundären [**RealTimeStylus-Objekts.**](realtimestylus-class.md)
-   Sie können die Rechenlast Ihrer synchronen Plug-Ins auf zwei Threads verteilen, um Verzögerungen bei der Ink-Sammlung auf einigen Tablet-PCs zu reduzieren.

Das folgende Diagramm veranschaulicht den Fluss von Tablettstiftdaten durch zwei kaskadierte [**RealTimeStylus-Objekte**](realtimestylus-class.md) und deren Plug-In-Sammlungen.

![Abbildung des kaskadierten Echtzeit-Datenflusses](images/72ca1999-e078-49f8-a336-3b4d0157a472.gif)

In diesem Diagramm stellt der Kreis mit dem Buchstaben "A" Tablettstiftdaten dar, die bereits von den primären und sekundären [**RealTimeStylus-Objekten**](realtimestylus-class.md) verarbeitet und in der Ausgabewarteschlange des sekundären **RealTimeStylus-Objekts** platziert wurden. Der Kreis mit dem Buchstaben "B" stellt Tablettstiftdaten dar, die bereits vom primären **RealTimeStylus-Objekt** verarbeitet und der Ausgabewarteschlange des primären **RealTimeStylus-Objekts** hinzugefügt wurden und noch nicht an das sekundäre **RealTimeStylus-Objekt** gesendet wurden. Der Kreis mit dem Buchstaben "C" stellt die Tablettstiftdaten dar, die das primäre **RealTimeStylus-Objekt** derzeit verarbeitet. Sie wird an die synchrone Plug-In-Sammlung gesendet und in der Ausgabewarteschlange platziert. Der leere Kreis stellt die Position in der Ausgabewarteschlange dar, an der zukünftige Tablettstiftdaten hinzugefügt werden.

## <a name="constraints"></a>Einschränkungen

Wenn Sie den [**Standardkonstruktor RealTimeStylus**](realtimestylus-class.md) verwenden, erstellen Sie ein **RealTimeStylus-Objekt,** das nur Eingaben von einem anderen **RealTimeStylus-Objekt akzeptieren** kann.

In der folgenden Liste werden die Einschränkungen beschrieben, die der Verwendung des kaskadierten [**RealTimeStylus-Modells zugeordnet**](realtimestylus-class.md) sind.

-   Es können [**nur zwei RealTimeStylus-Objekte**](realtimestylus-class.md) verwendet werden: ein primäres **RealTimeStylus-Objekt** und ein sekundäres **RealTimeStylus-Objekt.**
-   Das primäre [**RealTimeStylus-Objekt**](realtimestylus-class.md) muss mit einem Konstruktor erstellt werden, der **den attachedControl-** oder handle-Parameter verwendet.  Das **sekundäre RealTimeStylus-Objekt** muss mit dem Konstruktor ohne Argument erstellt werden.
-   Das [**sekundäre RealTimeStylus-Objekt**](realtimestylus-class.md) muss das einzige asynchrone Plug-In in der asynchronen Plug-In-Auflistung des primären **RealTimeStylus-Objekts** sein.
-   Ein [**sekundäres RealTimeStylus-Objekt**](realtimestylus-class.md) kann nur an ein primäres **RealTimeStylus-Objekt** gleichzeitig angefügt werden. Wenn es einem zweiten primären **RealTimeStylus-Objekt** hinzugefügt wird, löst die [Add-Methode](/previous-versions/ms824814(v=msdn.10)) eine Ausnahme aus, und das sekundäre **RealTimeStylus-Objekt** ist nicht an das zweite primäre **RealTimeStylus-Objekt** angefügt.
-   Das Verhalten einiger Member des sekundären [**RealTimeStylus-Objekts**](realtimestylus-class.md) wird geändert. In der folgenden Tabelle wird das geänderte Verhalten dieser Member beschrieben.

    

    
| Member | Verhalten | 
|--------|----------|
| <a href="/previous-versions/ms825905(v=msdn.10)">GetDesiredPacketDescription</a> | Diese Methode gibt die Informationen aus dem primären <a href="realtimestylus-class.md"><strong>RealTimeStylus-Objekt</strong></a> zurück.<br /> Wenn der <a href="realtimestylus-class.md"><strong>sekundäre RealTimeStylus</strong></a> nicht an ein primäres <strong>RealTimeStylus-Objekt</strong> angefügt ist, gibt diese Methode den Standardwert zurück.<br /> | 
| <a href="/previous-versions/ms826041(v=msdn.10)">SetDesiredPacketDescription</a> | Diese Methode löst eine <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException-Ausnahme</a> aus.<br /> | 
| <a href="/previous-versions/ms825913(v=msdn.10)">GetStyluses</a> | Diese Methode gibt die Informationen aus dem primären <a href="realtimestylus-class.md"><strong>RealTimeStylus-Objekt</strong></a> zurück.<br /> Wenn der <a href="realtimestylus-class.md"><strong>sekundäre RealTimeStylus</strong></a> nicht an ein primäres <strong>RealTimeStylus-Objekt</strong> angefügt ist, gibt diese Methode ein leeres Array zurück.<br /> | 
| <a href="/previous-versions/ms824832(v=msdn.10)">Aktiviert</a> | Beim Abrufen dieser Eigenschaft werden die Informationen aus dem primären <a href="realtimestylus-class.md"><strong>RealTimeStylus-Objekt</strong></a> zurückgegeben.<br /> Wenn der <a href="realtimestylus-class.md"><strong>sekundäre RealTimeStylus</strong></a> nicht an ein primäres <strong>RealTimeStylus-Objekt</strong> angefügt ist, gibt das Abrufen dieser Eigenschaft den Standardwert zurück.<br /><blockquote>    [!Note]<br />    Das Festlegen dieser Eigenschaft löst eine <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException-Ausnahme</a> aus.    </blockquote><br /> | 
| <a href="/previous-versions/ms824834(v=msdn.10)">WindowInputRectangle</a> | Beim Abrufen dieser Eigenschaft werden die Informationen aus dem primären <a href="realtimestylus-class.md"><strong>RealTimeStylus-Objekt</strong></a> zurückgegeben.<br /> Wenn der <a href="realtimestylus-class.md"><strong>sekundäre RealTimeStylus</strong></a> nicht an ein primäres <strong>RealTimeStylus-Objekt</strong> angefügt ist, gibt das Abrufen dieser Eigenschaft den Standardwert zurück.<br /><blockquote>    [!Note]<br />    Das Festlegen dieser Eigenschaft löst eine <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException-Ausnahme</a> aus.    </blockquote><br /> | 


    

     

-   Es wird erwartet, dass das übergeordnete [**RealTimeStylus-Objekt**](realtimestylus-class.md) nicht mehr funktioniert, wenn der untergeordnete **RealTimeStylus** verworfen wird.

 

 
