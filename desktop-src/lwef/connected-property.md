---
title: Verbundene Eigenschaft
description: Verbundene Eigenschaft
ms.assetid: 61b7f550-d8d6-4719-a0d4-0bf3a8cf096c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bba78358c7c42f0754da017aa0c188d41acd189
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310584"
---
# <a name="connected-property"></a>Verbundene Eigenschaft

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt zurück oder legt fest, ob das aktuelle Steuerelement mit dem Microsoft-Agent-Server verbunden ist.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent. * * * verbunden* *  \[  =  *boolescher* Wert\]



| Teil      | BESCHREIBUNG                                                                                                     |
|-----------|-----------------------------------------------------------------------------------------------------------------|
| *boolean* | Ein boolescher Ausdruck, der angibt, ob das Steuerelement verbunden ist. **True** Das Steuerelement ist verbunden.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

In vielen Fällen wird durch das Angeben des Steuer Elements automatisch eine Verbindung mit dem Microsoft-Agent-Server hergestellt. Wenn Sie z. b. die CLSID des Microsoft-Agent-Steuer Elements im- <OBJECT> Tag einer Webseite angeben, wird automatisch eine Server Verbindung geöffnet, und das Beenden der Seite schließt die Verbindung. Ebenso wird bei Visual Basic oder anderen Sprachen, mit denen Sie ein Steuerelement auf einem Formular ablegen können, durch das Ausführen des Programms automatisch eine Verbindung geöffnet, und die Verbindung wird beendet. Wenn der Server zurzeit nicht ausgeführt wird, wird er automatisch gestartet.

Wenn Sie jedoch ein agentsteuerelement zur Laufzeit erstellen möchten, müssen Sie möglicherweise auch explizit eine neue Verbindung mit dem Server mithilfe der **verbundenen** Eigenschaft öffnen. Beispielsweise können Sie in Visual Basic zur Laufzeit ein ActiveX-Objekt mit der Set-Anweisung mit dem **New** -Schlüsselwort (oder der Funktion "comateobject") erstellen. Obwohl das-Objekt erstellt wird, wird die Verbindung mit dem Server möglicherweise nicht erstellt. Sie können die **verbundene** Eigenschaft vor jedem beliebigen Code verwenden, der die Programmierschnittstelle des Microsoft-Agents aufruft, wie im folgenden Beispiel gezeigt:


```
   ' Declare a global variable for the control
   Dim MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent

   ' Open a connection to the server
   MyAgent.Connected = True

   ' Load a character
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Display the character
   MyAgent.Characters("Genie").Show
```



Wenn Sie ein Steuerelement mit dieser Technik erstellen, werden die Ereignisse des Agent-Steuer Elements nicht verfügbar gemacht. In Visual Basic 5,0 (und höher) können Sie auf die Ereignisse des-Steuer Elements zugreifen, indem Sie das-Steuerelement in die Verweise Ihres Projekts einschließen und das **widervents** -Schlüsselwort in der Variablen Deklaration verwenden:


```
   Dim WithEvents MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent
```



Durch die Verwendung von **wiwitvents** zum Erstellen einer Instanz des Agent-Steuer Elements zur Laufzeit wird die Verbindung mit dem Microsoft-Agent-Server automatisch geöffnet. Daher müssen Sie keine **verbundene** Anweisung einschließen.

Sie können die Verbindung mit dem Server schließen, indem Sie alle von Ihnen erstellten Verweise auf-Agent-Objekte, z. b. iagentctlcharakteriex und iagentctlcommandex, freigeben. Sie müssen auch den Verweis auf das agentsteuerelement selbst freigeben. In Visual Basic können Sie einen Verweis auf ein Objekt freigeben, indem Sie die Variable auf " **Nothing**" festlegen. Wenn Sie Zeichen geladen haben, entladen Sie diese, bevor Sie das Zeichen Objekt freigeben.


```
   Dim WithEvents MyAgent as Agent
   Dim Genie as IAgentCtlCharacterEx
   
   Sub Form_Load

   ' Create an instance of the control using New
   Set MyAgent = New Agent

   ' Open a connection to the server
   MyAgent.Connected = True

   ' Load the character into the Characters collection
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Create a reference to the character
   Set Genie = MyAgent.Characters("Genie")

   End Sub

   Sub CloseConnection

   ' Unload the character
   MyAgent.Characters.Unload "Genie"

   ' Release the reference to the character object
   Set Genie = Nothing

   ' Release the reference to the Agent control
   Set MyAgent = Nothing
   End Sub
```



> [!Note]  
> Sie können die Verbindung mit dem Server nicht schließen, indem Sie Verweise freigeben, bei denen die Komponente hinzugefügt wurde. Beispielsweise können Sie die Verbindung mit dem Server auf Webseiten nicht schließen, auf dem Sie das- <OBJECT> Tag verwenden, um das Steuerelement zu deklarieren, oder in einer Visual Basic Anwendung, in der Sie das Steuerelement in einem Formular ablegen. Wenn alle agentverweise freigegeben werden, wird die Arbeitsgruppe des Agents reduziert. die Verbindung bleibt so lange erhalten, bis Sie zur nächsten Seite navigieren oder die Anwendung beenden.

 

 

 





