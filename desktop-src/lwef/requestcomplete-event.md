---
title: RequestComplete-Ereignis
description: RequestComplete-Ereignis
ms.assetid: 543b79d1-f09d-4061-a1a8-8c8ab496bceb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf5202cc6aee6e8727651279fd216d5f0e5676025584c9cb66c4c6ad958da54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118746557"
---
# <a name="requestcomplete-event"></a>RequestComplete-Ereignis

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Tritt ein, wenn der Server eine Anforderung in der Warteschlange abschließt.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

 *Sub-Agent** \_ RequestComplete* *  **(ByVal-Anforderung))** *



| Teil      | Beschreibung                                            |
|-----------|--------------------------------------------------------|
| *Anforderung* | Gibt das [**Request-Objekt zurück.**](/windows/desktop/lwef/the-request-object) |



 

</dd> </dl>

### <a name="remarks"></a>Hinweise

Dieses Ereignis gibt ein [**Request-Objekt**](/windows/desktop/lwef/the-request-object) zurück. Da Anforderungen asynchron verarbeitet werden, können Sie dieses Ereignis verwenden, um zu bestimmen, wann der Server die Verarbeitung einer Anforderung abgeschlossen hat (z. B. eine [**Get-,**](get-method.md) [**Play-**](play-method.md)oder [**Speak-Methode),**](speak-method.md) um dieses Ereignis mit anderen aktionen zu synchronisieren, die von Ihrer Anwendung generiert werden. Der Server sendet das Ereignis nur an den Client, der den Verweis auf das **Request-Objekt** erstellt hat, und nur, wenn Sie eine globale Variable für den Anforderungsverweis definiert haben:


```
   Dim MyRequest 
   Dim Genie 

   Sub window_Onload
   
   Agent1.Characters.Load "Genie","https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent.Characters("Genie")

   ' This syntax will generate RequestStart and RequestComplete events.
   Set MyRequest = Genie.Get("state", "Showing")
   ' This syntax will not generate RequestStart and RequestComplete events.
   Genie.Get "state", "Hiding"
   
   End Sub

   Sub Agent1_RequestComplete(ByVal Request)

   If Request = MyRequest Then
      Status = "Showing animation is now loaded"

   End Sub
```



Da [**Animationsanforderungsobjekte**](/windows/desktop/lwef/the-request-object) erst zugewiesen werden, wenn der Server die Anforderung verarbeitet, stellen Sie sicher, dass das **Request-Objekt** vorhanden ist, bevor Sie versuchen, es auszuwerten. Wenn Sie beispielsweise in Visual Basic eine Bedingung verwenden, um zu testen, ob eine bestimmte Anforderung abgeschlossen wurde, können Sie das **Schlüsselwort Nothing** verwenden:


```
   Sub Agent1_RequestComplete (ByVal Request)

   If Not (MyRequest Is Nothing) Then
      If Request = MyRequest Then
      '-- Do whatever
      End If
   End If

   End Sub
```



> [!Note]  
> In VBScript 1.0 wird dieses Ereignis ausgelöst, auch wenn Sie keine Verweise auf ein [**Request-Objekt**](/windows/desktop/lwef/the-request-object) definieren. Dies wurde in VBScript 2.0 behoben, das von heruntergeladen werden <https://microsoft.com/msdownload/vbscript/scripting.asp> kann.

 

### <a name="see-also"></a>Weitere Informationen

[**RequestStart-Ereignis**](requeststart-event.md)


 

 