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
# <a name="using-vbscript"></a><span data-ttu-id="59cb2-103">Verwenden von VBScript</span><span class="sxs-lookup"><span data-stu-id="59cb2-103">Using VBScript</span></span>

<span data-ttu-id="59cb2-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="59cb2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="59cb2-105">VBScript ist eine Programmiersprache, die in Microsoft Internet Explorer enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="59cb2-105">VBScript is a programming language included with Microsoft Internet Explorer.</span></span> <span data-ttu-id="59cb2-106">Wenden Sie sich für andere Browser an Ihren Anbieter.</span><span class="sxs-lookup"><span data-stu-id="59cb2-106">For other browsers, contact your vendor about support.</span></span> <span data-ttu-id="59cb2-107">VBScript 2,0 (oder höher) wird für die Verwendung mit dem-Agent empfohlen.</span><span class="sxs-lookup"><span data-stu-id="59cb2-107">VBScript 2.0 (or later) is recommended for use with Agent.</span></span> <span data-ttu-id="59cb2-108">Obwohl frühere Versionen von VBScript möglicherweise mit dem-Agent funktionieren, fehlen Ihnen bestimmte Funktionen, die Sie möglicherweise verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="59cb2-108">Although earlier versions of VBScript may work with Agent, they lack certain functions that you may want to use.</span></span> <span data-ttu-id="59cb2-109">Sie können VBScript 2,0 herunterladen und weitere Informationen zu VBScript auf der Microsoft-Download Website und der Microsoft VBScript-Website erhalten.</span><span class="sxs-lookup"><span data-stu-id="59cb2-109">You can download VBScript 2.0 and obtain further information on VBScript at the Microsoft Downloads site and the Microsoft VBScript site.</span></span>

<span data-ttu-id="59cb2-110">Verwenden Sie zum Programmieren des Microsoft-Agents aus VBScript den HTML-Code</span><span class="sxs-lookup"><span data-stu-id="59cb2-110">To program Microsoft Agent from VBScript, use the HTML</span></span> <SCRIPT> <span data-ttu-id="59cb2-111">tags. To access the programming interface, use the name of control you assign in the <OBJECT> tag, followed by the subobject (if any), the name of the method or property, and any parameters or values supported by the method or property:</span><span class="sxs-lookup"><span data-stu-id="59cb2-111">tags. To access the programming interface, use the name of control you assign in the <OBJECT> tag, followed by the subobject (if any), the name of the method or property, and any parameters or values supported by the method or property:</span></span>

``` syntax
agent[.object].Method parameter, [parameter]
agent[.object].Property = value
```

<span data-ttu-id="59cb2-112">Fügen Sie für Ereignisse den Namen des Steuer Elements, gefolgt vom Namen des Ereignisses und Parametern, ein:</span><span class="sxs-lookup"><span data-stu-id="59cb2-112">For events, include the name of the control followed by the name of the event and any parameters:</span></span>

``` syntax
Sub agent_event (ByVal parameter[,ByVal parameter])
statements
End Sub
```

<span data-ttu-id="59cb2-113">Sie können auch einen Ereignishandler angeben, indem Sie das</span><span class="sxs-lookup"><span data-stu-id="59cb2-113">You can also specify an event handler using the</span></span> <SCRIPT> <span data-ttu-id="59cb2-114">tag's **For...Event** syntax:</span><span class="sxs-lookup"><span data-stu-id="59cb2-114">tag's **For...Event** syntax:</span></span>

``` syntax
<SCRIPT LANGUAGE=VBScript For=agent Event=event[(parameter[,parameter])]>
statements
</SCRIPT>
```

<span data-ttu-id="59cb2-115">Obwohl Microsoft Internet Explorer diese letztere Syntax unterstützt, werden nicht alle Browser unterstützt.</span><span class="sxs-lookup"><span data-stu-id="59cb2-115">Although Microsoft Internet Explorer supports this latter syntax, not all browsers do.</span></span> <span data-ttu-id="59cb2-116">Verwenden Sie aus Kompatibilitätsgründen nur die erste Syntax für-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="59cb2-116">For compatibility, use only the former syntax for events.</span></span>

<span data-ttu-id="59cb2-117">Mit VBScript (2,0 oder höher) können Sie überprüfen, ob der Microsoft-Agent installiert ist, indem Sie versuchen, das Objekt zu erstellen und zu überprüfen, ob es vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="59cb2-117">With VBScript (2.0 or later), you can verify whether Microsoft Agent is installed by trying to create the object and checking to see if it exists.</span></span> <span data-ttu-id="59cb2-118">Im folgenden Beispiel wird veranschaulicht, wie Sie das-Agent-Steuerelement überprüfen können, ohne ein automatisches Herunterladen des Steuer Elements auszulösen (wie dies bei der Aufnahme eines- <OBJECT> Tags für das Steuerelement auf der Seite der Fall wäre):</span><span class="sxs-lookup"><span data-stu-id="59cb2-118">The following sample demonstrates how to check for the Agent control without triggering an auto-download of the control (as would happen if you included an <OBJECT> tag for the control on the page):</span></span>

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

 

 




