---
title: Verwenden von VBScript
description: Verwenden von VBScript
ms.assetid: a078eb60-aa12-42ea-850c-7b845fc8037c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691ed6bf520c83e4b679bb174274abb984eaa2f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206887"
---
# <a name="using-vbscript"></a>Verwenden von VBScript

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

VBScript ist eine Programmiersprache, die in Microsoft Internet Explorer enthalten ist. Wenden Sie sich für andere Browser an Ihren Anbieter. VBScript 2,0 (oder höher) wird für die Verwendung mit dem-Agent empfohlen. Obwohl frühere Versionen von VBScript möglicherweise mit dem-Agent funktionieren, fehlen Ihnen bestimmte Funktionen, die Sie möglicherweise verwenden möchten. Sie können VBScript 2,0 herunterladen und weitere Informationen zu VBScript auf der Microsoft-Download Website und der Microsoft VBScript-Website erhalten.

Verwenden Sie zum Programmieren des Microsoft-Agents aus VBScript den HTML-Code <SCRIPT> tags. To access the programming interface, use the name of control you assign in the <OBJECT> tag, followed by the subobject (if any), the name of the method or property, and any parameters or values supported by the method or property:

``` syntax
agent[.object].Method parameter, [parameter]
agent[.object].Property = value
```

Fügen Sie für Ereignisse den Namen des Steuer Elements, gefolgt vom Namen des Ereignisses und Parametern, ein:

``` syntax
Sub agent_event (ByVal parameter[,ByVal parameter])
statements
End Sub
```

Sie können auch einen Ereignishandler angeben, indem Sie das <SCRIPT> tag's **For...Event** syntax:

``` syntax
<SCRIPT LANGUAGE=VBScript For=agent Event=event[(parameter[,parameter])]>
statements
</SCRIPT>
```

Obwohl Microsoft Internet Explorer diese letztere Syntax unterstützt, werden nicht alle Browser unterstützt. Verwenden Sie aus Kompatibilitätsgründen nur die erste Syntax für-Ereignisse.

Mit VBScript (2,0 oder höher) können Sie überprüfen, ob der Microsoft-Agent installiert ist, indem Sie versuchen, das Objekt zu erstellen und zu überprüfen, ob es vorhanden ist. Im folgenden Beispiel wird veranschaulicht, wie Sie das-Agent-Steuerelement überprüfen können, ohne ein automatisches Herunterladen des Steuer Elements auszulösen (wie dies bei der Aufnahme eines- <OBJECT> Tags für das Steuerelement auf der Seite der Fall wäre):

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

 

 




