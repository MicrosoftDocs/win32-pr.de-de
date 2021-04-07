---
title: Requeststart-Ereignis
description: Requeststart-Ereignis
ms.assetid: ecfb9691-cbc4-48f5-8e26-a99389e85eed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2be5954636084d3cbc299c718f2b4e6d9330ef90
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103727025"
---
# <a name="requeststart-event"></a>Requeststart-Ereignis

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Tritt auf, wenn der Server eine Anforderung in der Warteschlange startet.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

**Sub** - *Agent * * * \_ requeststart* *  **(ByVal** - *Anforderung * * *)**



| Teil      | BESCHREIBUNG                                            |
|-----------|--------------------------------------------------------|
| *Anforderung* | Gibt das [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt zurück. |



 

</dd> </dl>

### <a name="remarks"></a>Bemerkungen

Das-Ereignis gibt ein [**Request**](/windows/desktop/lwef/the-request-object) -Objekt zurück. Da Anforderungen asynchron verarbeitet werden, können Sie dieses Ereignis verwenden, um zu bestimmen, wann der Server mit der Verarbeitung einer Anforderung beginnt (z. b. eine [**Get**](get-method.md)-, [**Play**](play-method.md)-oder [**Sprech**](speak-method.md) Methode) und damit diese mit anderen von Ihrer Anwendung generierten Aktionen synchronisieren. Das Ereignis wird nur an den Client gesendet, der den Verweis auf das **Anforderungs** Objekt erstellt hat, und nur, wenn Sie eine globale Variable für den Anforderungs Verweis definiert haben:


```
   Dim MyRequest 
   Dim Genie 

   Sub window_Onload
   
   Agent1.Characters.Load "Genie", _
      "https://agent.microsoft.com/characters/v2/genie/genie.acf"   

   Set Genie = Agent1.Characters("Genie")

   ' This syntax will generate RequestStart and RequestComplete events.
   Set MyRequest = Genie.Get("state", "Showing")

   ' This syntax will not generate RequestStart and RequestComplete events.
   Genie.Get ("state", "Hiding")

   End Sub

   Sub Agent1_RequestStart(ByVal Request)

   If Request = MyRequest Then
      Status = "Loading the Showing animation"

   End Sub
```



Der [**Status**](status-property.md) gibt 4 (Anforderungs Vorgang) für das zurückgegebene [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt zurück.

Da Animations [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekte erst zugewiesen werden, wenn der Server die Anforderung verarbeitet hat, stellen Sie sicher, dass das **Anforderungs** Objekt vorhanden ist, bevor Sie es auswerten. Wenn Sie z. b. in Visual Basic eine bedingte Anforderung verwenden, um zu testen, ob eine bestimmte Anforderung abgeschlossen wurde, können Sie das **Nothing** -Schlüsselwort verwenden:


```
   Sub Agent1_RequestStart (ByVal Request)

   If Not (MyRequest Is Nothing) Then
      If Request = MyRequest Then
      '-- Do whatever
      End If
   End If

   End Sub
```



> [!Note]  
> In VBScript 1,0 wird dieses Ereignis auch dann ausgelöst, wenn Sie keine Verweise auf ein [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt definieren. Dies wurde in VBScript 2,0 behoben, das von heruntergeladen werden kann <https://microsoft.com/msdownload/vbscript/scripting.asp> .

 

### <a name="see-also"></a>Weitere Informationen

[**Requestcomplete-Ereignis**](requestcomplete-event.md)


 

 