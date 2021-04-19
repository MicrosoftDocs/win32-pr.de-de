---
title: Das Anforderungs Objekt.
description: Das Anforderungs Objekt.
ms.assetid: d8b37164-6855-48c0-bcf8-a86c0f8b3a59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a50d554a5799af9a434b456113d7c826d2a0aa2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106337219"
---
# <a name="the-request-object"></a>Das Anforderungs Objekt.

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Der Server verarbeitet einige Methoden asynchron. Dadurch kann der Anwendungscode fortgesetzt werden, während die Methode abgeschlossen wird. Wenn eine Client Anwendung eine dieser Methoden aufruft, erstellt und gibt das-Steuerelement ein [**Request**](/windows/desktop/lwef/the-request-object) -Objekt für die Anforderung zurück. Sie können das **Request** -Objekt verwenden, um den Status der Methode zu verfolgen, indem Sie der-Methode eine Objekt Variable zuweisen. Deklarieren Sie in Visual Basic zuerst eine Objekt Variable:


```
   Dim MyRequest as Object
```



In VBScript schließen Sie den Variablentyp nicht in die Deklaration ein:


```
   Dim MyRequest
```



Und verwenden die Set-Anweisung von Visual Basic, um die Variable dem Methoden aufzurufen:


```
   Set MyRequest = <i>agent</i>.Characters("<i>CharacterID</i>").<i>method</i> (<i>parameter</i>[s])
```



Dadurch wird ein Verweis auf das [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt hinzugefügt. Das **Anforderungs** Objekt wird zerstört, wenn keine weiteren Verweise darauf vorhanden sind. Wo Sie das **Anforderungs** Objekt deklarieren und wie Sie es verwenden, legt seine Lebensdauer fest. Wenn das Objekt in einer Unterroutine oder Funktion als lokal deklariert ist, wird es zerstört, wenn es den Gültigkeitsbereich verlässt. Das heißt, wenn die Unterroutine oder Funktion beendet wird. Wenn das Objekt global deklariert ist, wird es erst zerstört, wenn das Programm beendet wird oder ein neuer Wert (oder ein als "leer" festgelegter Wert) dem Objekt zugewiesen wird.

Das [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt bietet verschiedene Eigenschaften, die Sie Abfragen können. Die [**Status**](status-property.md) -Eigenschaft gibt beispielsweise den aktuellen Status der Anforderung zurück. Sie können diese Eigenschaft verwenden, um den Status Ihrer Anforderung zu überprüfen:


```
   Dim MyRequest
   
   Set MyRequest = Agent1.Characters.Load ("Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf")

   If (MyRequest.Status = 2) then
      'do something

   Else If (MyRequest.Status = 0) then
      'do something right away

   End If
```



Die [**Status**](status-property.md) -Eigenschaft gibt den Status eines [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekts als Long Integer-Wert zurück.



| Status | Definition                                        |
|--------|---------------------------------------------------|
| 0      | Die Anforderung wurde erfolgreich abgeschlossen.                   |
| 1      | Fehler bei der Anforderung.                                   |
| 2      | Ausstehende Anforderung (in der Warteschlange, aber nicht abgeschlossen). |
| 3      | Die Anforderung wurde unterbrochen.                              |
| 4      | Die Anforderung wird ausgeführt.                              |



 

Das [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt enthält außerdem einen Long Integer-Wert in der [**Number**](https://www.bing.com/search?q=**Number**) -Eigenschaft, der den Fehler oder die Ursache des [**Status**](status-property.md) Codes zurückgibt. Wenn kein Wert ist, ist dieser Wert 0 (null). Die [**Description**](description-property.md) -Eigenschaft enthält einen Zeichen folgen Wert, der der Fehlernummer entspricht. Wenn die Zeichenfolge nicht vorhanden ist, enthält die **Beschreibung** "Anwendungs-oder Objekt definierter Fehler".

Informationen zu den Werten und der von der [**Number**](https://www.bing.com/search?q=**Number**) -Eigenschaft zurückgegebenen Bedeutung finden Sie unter [Error Codes](microsoft-agent-error-codes.md).

Der Server platziert Animations Anforderungen in der Warteschlange des angegebenen Zeichens. Dadurch kann der Server die Animation in einem separaten Thread wiedergeben, und der Code der Anwendung kann fortgesetzt werden, während Animationen wiedergegeben werden. Wenn Sie einen [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt Verweis erstellen, benachrichtigt der Server Sie automatisch, wenn eine Animations Anforderung durch das [**requeststart**](https://www.bing.com/search?q=**RequestStart**) -Ereignis und das [**requestcomplete**](https://www.bing.com/search?q=**RequestComplete**) -Ereignis gestartet oder abgeschlossen wurde. Da Methoden, die **Anforderungs** Objekte zurückgeben, asynchron sind und während des Gültigkeits Bereichs der aufrufenden Funktion möglicherweise nicht vervollständigt werden, deklarieren Sie den Verweis auf das **Anforderungs** Objekt Global.

Die folgenden Methoden können verwendet werden, um ein [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt zurückzugeben: [**gestureat**](gestureat-method.md), [**Get**](get-method.md), [**Hide**](hide-method.md), [**Interrupt**](interrupt-method.md), [**Load**](load-method.md), [**muveto**](moveto-method.md), [**Play**](play-method.md), [**Show**](show-method.md), [**Speak**](speak-method.md)und [**Wait**](https://www.bing.com/search?q=**Wait**).

 

 