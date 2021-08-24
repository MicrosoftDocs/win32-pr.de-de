---
title: Connected-Eigenschaft
description: Connected-Eigenschaft
ms.assetid: 61b7f550-d8d6-4719-a0d4-0bf3a8cf096c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6af3a44e97236060733adc55ec6e44eddd0b1d8879250b2a28b54c0bca384cac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726091"
---
# <a name="connected-property"></a>Connected-Eigenschaft

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt zurück oder legt fest, ob das aktuelle Steuerelement mit dem Microsoft-Agent-Server verbunden ist.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent.einander verbunden* *  \[  =  *boolescher Wert*\]



| Teil      | Beschreibung                                                                                                     |
|-----------|-----------------------------------------------------------------------------------------------------------------|
| *boolean* | Ein boolescher Ausdruck, der angibt, ob das Steuerelement verbunden ist. **True** Das Steuerelement ist verbunden.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

In vielen Situationen wird durch die Angabe des Steuerelements automatisch eine Verbindung mit dem Microsoft-Agent-Server hergestellt. Wenn Sie beispielsweise die CLSID des Microsoft-Agent-Steuerelements im -Tag auf einer Webseite angeben, <OBJECT> wird automatisch eine Serververbindung geöffnet, und beim Beenden der Seite wird die Verbindung geschlossen. Ebenso wird bei Visual Basic oder anderen Sprachen, die es Ihnen ermöglichen, ein Steuerelement auf einem Formular zu löschen, die Ausführung des Programms automatisch eine Verbindung geöffnet, und wenn das Programm beendet wird, wird die Verbindung geschlossen. Wenn der Server derzeit nicht ausgeführt wird, wird er automatisch gestartet.

Wenn Sie jedoch zur Laufzeit ein Agent-Steuerelement erstellen möchten, müssen Sie möglicherweise auch mithilfe der **Connected-Eigenschaft** explizit eine neue Verbindung mit dem Server öffnen. In Visual Basic können Sie beispielsweise zur Laufzeit ein ActiveX-Objekt erstellen, indem Sie die Set-Anweisung mit dem **New-Schlüsselwort** (oder der CreateObject-Funktion) verwenden. Dadurch wird zwar das -Objekt erstellt, aber möglicherweise wird die Verbindung mit dem Server nicht hergestellt. Sie können die **Connected-Eigenschaft** vor jedem Code verwenden, der die Programmierschnittstelle des Microsoft-Agents aufruft, wie im folgenden Beispiel gezeigt:


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



Beim Erstellen eines Steuerelements mit dieser Technik werden die Ereignisse des -Agent-Steuerelements nicht verfügbar gemacht. In Visual Basic 5.0 (und höher) können Sie auf die Ereignisse des Steuerelements zugreifen, indem Sie das Steuerelement in die Verweise Ihres Projekts einschließen und das **WithEvents-Schlüsselwort** in Ihrer Variablendeklaration verwenden:


```
   Dim WithEvents MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent
```



Wenn **Sie WithEvents** verwenden, um zur Laufzeit eine Instanz des Agent-Steuerelements zu erstellen, wird automatisch die Verbindung mit dem Microsoft-Agent-Server geöffnet. Daher müssen Sie keine **Connected-Anweisung** einschließen.

Sie können die Verbindung mit dem Server schließen, indem Sie alle erstellten Verweise auf Agent-Objekte freigeben, z. B. IAgentCtlCharacterEx und IAgentCtlCommandEx. Sie müssen auch ihren Verweis auf das -Agent-Steuerelement selbst freigeben. In Visual Basic können Sie einen Verweis auf ein Objekt freigeben, indem Sie dessen Variable auf **Nothing** festlegen. Wenn Sie Zeichen geladen haben, entladen Sie sie, bevor Sie das Zeichenobjekt freigeben.


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
> Sie können die Verbindung mit dem Server nicht schließen, indem Sie Verweise freigeben, an denen die Komponente hinzugefügt wurde. Beispielsweise können Sie die Verbindung mit dem Server nicht auf Webseiten schließen, auf denen Sie das <OBJECT> -Tag zum Deklarieren des Steuerelements verwenden, oder in einer Visual Basic Anwendung, in der Sie das Steuerelement in einem Formular ablegen. Während das Freigeben aller Agent-Verweise den Arbeitssatz des Agents reduziert, bleibt die Verbindung bestehen, bis Sie zur nächsten Seite navigieren oder die Anwendung beenden.

 

 

 





