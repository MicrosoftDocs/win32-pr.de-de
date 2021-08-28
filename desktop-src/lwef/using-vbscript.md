---
title: Verwenden von VBScript
description: Verwenden von VBScript
ms.assetid: a078eb60-aa12-42ea-850c-7b845fc8037c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0bc64419af4d8dc47de5a2393fcf5cb259374ed
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881016"
---
# <a name="using-vbscript"></a>Verwenden von VBScript

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

VBScript ist eine Programmiersprache, die in Microsoft Internet Explorer. Wenden Sie sich bei anderen Browsern an Ihren Anbieter, um Support zu erhalten. VBScript 2.0 (oder höher) wird für die Verwendung mit dem -Agent empfohlen. Obwohl frühere Versionen von VBScript möglicherweise mit dem -Agent funktionieren, fehlen ihnen bestimmte Funktionen, die Sie möglicherweise verwenden möchten. Sie können VBScript 2.0 herunterladen und weitere Informationen zu VBScript auf der Microsoft Downloads-Website und auf der Microsoft VBScript-Website abrufen.

Verwenden Sie zum Programmieren von Microsoft Agent aus VBScript die HTML &lt; &gt; SCRIPT-Tags. Verwenden Sie für den Zugriff auf die Programmierschnittstelle den Namen des Steuerelements, das Sie im OBJECT-Tag zuweisen, gefolgt vom Unterobjekt (falls verfügbar), dem Namen der Methode oder Eigenschaft sowie allen Parametern oder Werten, die von der Methode oder Eigenschaft unterstützt &lt; &gt; werden:

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

Sie können auch einen Ereignishandler angeben, indem Sie die &lt; &gt; For... des **SCRIPT-Tags verwenden.** Ereignissyntax:

``` syntax
<SCRIPT LANGUAGE=VBScript For=agent Event=event[(parameter[,parameter])]>
statements
</SCRIPT>
```

Obwohl Microsoft Internet Explorer diese zweite Syntax unterstützt, ist dies nicht bei allen Browsern der Fall. Verwenden Sie zur Kompatibilität nur die frühere Syntax für Ereignisse.

Mit VBScript (2.0 oder höher) können Sie überprüfen, ob Microsoft Agent installiert ist, indem Sie versuchen, das Objekt zu erstellen und zu überprüfen, ob es vorhanden ist. Im folgenden Beispiel wird veranschaulicht, wie Sie das -Steuerelement auf das -Agent-Steuerelement überprüfen, ohne einen automatischen Download des Steuerelements auszulösen (wie dies der Fall wäre, wenn Sie ein OBJECT-Tag für das Steuerelement auf der &lt; &gt; Seite enthalten würden):

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

 

 




