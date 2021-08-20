---
title: Das Anforderungsobjekt
description: Das Anforderungsobjekt
ms.assetid: d8b37164-6855-48c0-bcf8-a86c0f8b3a59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d2bc9ecf65403ca6dbb471c81a65b105bcc5b69701760a73f8fbc8a5684a9b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117882393"
---
# <a name="the-request-object"></a>Das Anforderungsobjekt

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

Der Server verarbeitet einige Methoden asynchron. Dadurch kann Ihr Anwendungscode fortgesetzt werden, während die -Methode abgeschlossen wird. Wenn eine Clientanwendung eine dieser Methoden aufruft, erstellt das Steuerelement ein [**Request-Objekt**](/windows/desktop/lwef/the-request-object) für die Anforderung und gibt es zurück. Mit dem **Request-Objekt** können Sie den Status der Methode nachverfolgen, indem Sie der -Methode eine Objektvariable zuweisen. Deklarieren Visual Basic zunächst eine Objektvariable:


```
   Dim MyRequest as Object
```



In VBScript fügen Sie den Variablentyp nicht in Ihre Deklaration ein:


```
   Dim MyRequest
```



Verwenden Sie Visual Basic Set-Anweisung von , um die Variable dem Methodenaufruf zu zuweisen:


```
   Set MyRequest = <i>agent</i>.Characters("<i>CharacterID</i>").<i>method</i> (<i>parameter</i>[s])
```



Dadurch wird ein Verweis auf das [**Request-Objekt**](/windows/desktop/lwef/the-request-object) addiert. Das **Request-Objekt** wird zerstört, wenn keine Verweise mehr darauf verfügbar sind. Wo Sie das **Request-Objekt deklarieren** und wie Sie es verwenden, bestimmt seine Lebensdauer. Wenn das Objekt für eine Unterroutine oder Funktion als lokal deklariert wird, wird es zerstört, wenn es den Gültigkeitsbereich übergeht. Das heißt, wenn die Unterroutine oder Funktion beendet wird. Wenn das Objekt global deklariert wird, wird es erst zerstört, wenn das Programm beendet wird oder dem -Objekt ein neuer Wert (oder ein wert, der auf "empty" festgelegt ist) zugewiesen wird.

Das [**Request-Objekt**](/windows/desktop/lwef/the-request-object) stellt mehrere Eigenschaften zur Verfügung, die Sie abfragen können. Beispielsweise gibt die [**Status -Eigenschaft**](status-property.md) den aktuellen Status der Anforderung zurück. Sie können diese Eigenschaft verwenden, um den Status Ihrer Anforderung zu überprüfen:


```
   Dim MyRequest
   
   Set MyRequest = Agent1.Characters.Load ("Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf")

   If (MyRequest.Status = 2) then
      'do something

   Else If (MyRequest.Status = 0) then
      'do something right away

   End If
```



Die [**Status-Eigenschaft**](status-property.md) gibt den Status eines [**Request-Objekts**](/windows/desktop/lwef/the-request-object) als Long-Ganzzahlwert zurück.



| Status | Definition                                        |
|--------|---------------------------------------------------|
| 0      | Die Anforderung wurde erfolgreich abgeschlossen.                   |
| 1      | Fehler bei der Anforderung.                                   |
| 2      | Ausstehende Anforderung (in der Warteschlange, aber nicht abgeschlossen). |
| 3      | Anforderung unterbrochen.                              |
| 4      | Die Anforderung wird in Bearbeitung.                              |



 

Das [**Request-Objekt**](/windows/desktop/lwef/the-request-object) enthält auch einen ganzzahligen Long-Wert in der [**Number-Eigenschaft,**](https://www.bing.com/search?q=**Number**) der den Fehler oder die Ursache des [**Statuscodes zurückgibt.**](status-property.md) Wenn keines der Fall ist, ist dieser Wert 0 (null). Die [**Description-Eigenschaft**](description-property.md) enthält einen Zeichenfolgenwert, der der Fehlernummer entspricht. Wenn die Zeichenfolge nicht vorhanden ist, enthält **Die Beschreibung** "Anwendungsdefinierter oder objektdefinierter Fehler".

Die von der Number-Eigenschaft [**zurückgegebenen**](https://www.bing.com/search?q=**Number**) Werte und Bedeutungen finden Sie unter [Fehlercodes](microsoft-agent-error-codes.md).

Der Server platziert Animationsanforderungen in der Warteschlange des angegebenen Zeichens. Dadurch kann der Server die Animation in einem separaten Thread wieder geben, und der Code Ihrer Anwendung kann fortgesetzt werden, während Animationen wieder verwendet werden. Wenn Sie [](/windows/desktop/lwef/the-request-object) einen Request-Objektverweis erstellen, benachrichtigt Sie der Server automatisch, wenn eine Animationsanforderung über die [**Ereignisse RequestStart**](https://www.bing.com/search?q=**RequestStart**) und [**RequestComplete**](https://www.bing.com/search?q=**RequestComplete**) gestartet oder abgeschlossen wurde. Da Methoden, die **Anforderungsobjekte** zurückgeben, asynchron sind und während des Bereichs der aufrufenden Funktion möglicherweise nicht abgeschlossen werden, deklarieren Sie Ihren Verweis auf das **Request-Objekt** global.

Die folgenden Methoden können zum Zurückgeben eines [**Request-Objekts**](/windows/desktop/lwef/the-request-object) verwendet werden: [**GestureAt**](gestureat-method.md), [**Get**](get-method.md), [**Hide**](hide-method.md), [**Interrupt**](interrupt-method.md), [**Load**](load-method.md), [**MoveTo**](moveto-method.md), [**Play**](play-method.md), [**Show**](show-method.md), [**Speak**](speak-method.md)und [**Wait**](https://www.bing.com/search?q=**Wait**).

 

 