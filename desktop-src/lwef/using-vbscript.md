---
title: Verwenden von VBScript
description: Verwenden von VBScript
ms.assetid: a078eb60-aa12-42ea-850c-7b845fc8037c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afa94bd5b3576e80cf8a0c17857bbb0902bd254e95113d87ae9d1d1fca1e38b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975500"
---
# <a name="using-vbscript"></a>Verwenden von VBScript

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

VBScript ist eine Programmiersprache, die in Microsoft Internet Explorer. Wenden Sie sich bei anderen Browsern an Ihren Anbieter, um Support zu erhalten. VBScript 2.0 (oder höher) wird für die Verwendung mit dem -Agent empfohlen. Obwohl frühere Versionen von VBScript möglicherweise mit dem -Agent funktionieren, fehlen ihnen bestimmte Funktionen, die Sie möglicherweise verwenden möchten. Sie können VBScript 2.0 herunterladen und weitere Informationen zu VBScript auf der Microsoft Downloads-Website und auf der Microsoft VBScript-Website abrufen.

Verwenden Sie zum Programmieren von Microsoft Agent aus VBScript den HTML-Code. <SCRIPT> tags. To access the programming interface, use the name of control you assign in the <OBJECT> tag, followed by the subobject (if any), the name of the method or property, and any parameters or values supported by the method or property:

``` syntax
agent[.object].Method parameter, [parameter]
agent[.object].Property = value
```

Fügen Sie für Ereignisse den Namen des Steuerelements gefolgt vom Namen des Ereignisses und allen Parametern ein:

``` syntax
Sub agent_event (ByVal parameter[,ByVal parameter])
statements
End Sub
```

Sie können auch einen Ereignishandler mithilfe von angeben. <SCRIPT> tag's **For...Event** syntax:

``` syntax
<SCRIPT LANGUAGE=VBScript For=agent Event=event[(parameter[,parameter])]>
statements
</SCRIPT>
```

Obwohl Microsoft Internet Explorer diese zweite Syntax unterstützt, ist dies nicht in allen Browsern der Fall. Verwenden Sie zur Kompatibilität nur die frühere Syntax für Ereignisse.

Mit VBScript (2.0 oder höher) können Sie überprüfen, ob Microsoft Agent installiert ist, indem Sie versuchen, das Objekt zu erstellen und zu überprüfen, ob es vorhanden ist. Im folgenden Beispiel wird veranschaulicht, wie Sie das -Steuerelement auf das -Agent-Steuerelement überprüfen, ohne einen automatischen Download des Steuerelements auszulösen (wie dies der Fall wäre, wenn Sie ein Tag für das Steuerelement auf der <OBJECT> Seite enthalten würden):

``` syntax
<!-- WARNING - This code requires VBScript 2.0.
It will always fail to detect the Agent control
in VbScript 1.x, because CreateObject doesn't work.
-->

<SCRIPT LANGUAGE=VBSCRIPT>
If HaveAgent() Then
      'Microsoft Agent control was found.
document.write "<H2 align=center>Found</H2>"
Else
      'Microsoft Agent control was not found.
document.write "<H2 align=center>Not Found</H2>"
End If

Function HaveAgent()
' This procedure attempts to create an Agent Control object.
' If it succeeds, it returns True.
'    This means the control is available on the client.
' If it fails, it returns False.
'    This means the control hasn't been installed on the client.

   Dim agent
   HaveAgent = False
   On Error Resume Next
   Set agent = CreateObject("Agent.Control.1")
   HaveAgent = IsObject(agent)

End Function

</SCRIPT>
```

 

 




