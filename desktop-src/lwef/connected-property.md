---
title: Connected-Eigenschaft
description: Connected-Eigenschaft
ms.assetid: 61b7f550-d8d6-4719-a0d4-0bf3a8cf096c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d19326f7770bbd4a42f6ff66a4517cd6151f3c54
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884928"
---
# <a name="connected-property"></a>Connected-Eigenschaft

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt zurück oder legt fest, ob das aktuelle Steuerelement mit dem Microsoft Agent-Server verbunden ist.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent.**Connected* *  \[  =  *Boolescher Wert*\]



| Teil      | Beschreibung                                                                                                     |
|-----------|-----------------------------------------------------------------------------------------------------------------|
| *boolean* | Ein boolescher Ausdruck, der an gibt, ob das Steuerelement verbunden ist. **True** Das Steuerelement ist verbunden.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

In vielen Situationen wird durch die Angabe des Steuerelements automatisch eine Verbindung mit dem Microsoft Agent-Server hergestellt. Wenn Sie z. B. die CLSID des Microsoft Agent-Steuerelements im OBJECT-Tag auf einer Webseite angeben, wird automatisch eine Serververbindung geöffnet, und das Beenden der Seite schließt &lt; &gt; die Verbindung. Ebenso wird Visual Basic- oder anderen Sprachen, mit denen Sie ein Steuerelement auf einem Formular ablegen können, beim Ausführen des Programms automatisch eine Verbindung geöffnet, und durch Beenden des Programms wird die Verbindung geschlossen. Wenn der Server derzeit nicht ausgeführt wird, wird er automatisch gestartet.

Wenn Sie jedoch zur Laufzeit ein -Agent-Steuerelement erstellen möchten, müssen Sie möglicherweise auch explizit eine neue Verbindung mit dem Server mithilfe der **Connected-Eigenschaft** öffnen. In diesem Beispiel Visual Basic Sie zur Laufzeit ein ActiveX-Objekt erstellen, indem Sie die Set-Anweisung mit dem **New-Schlüsselwort** (oder der CreateObject-Funktion) verwenden. Obwohl dadurch das -Objekt erstellt wird, wird möglicherweise keine Verbindung mit dem Server hergestellt. Sie können die **Connected-Eigenschaft** vor jedem Code verwenden, der die Microsoft Agent-Programmierschnittstelle aufruft, wie im folgenden Beispiel gezeigt:


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



Das Erstellen eines Steuerelements mit dieser Technik macht die Ereignisse des -Agent-Steuerelements nicht verfügbar. In Visual Basic 5.0 (und höher) können Sie auf die Ereignisse des Steuerelements zugreifen, indem Sie das -Steuerelement in die Verweise Ihres Projekts einreihen und das **WithEvents-Schlüsselwort** in Ihrer Variablendeklaration verwenden:


```
   Dim WithEvents MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent
```



Die **Verwendung von WithEvents** zum Erstellen einer Instanz des -Agent-Steuerelements zur Laufzeit öffnet automatisch die Verbindung mit dem Microsoft Agent-Server. Daher müssen Sie keine **Connected-Anweisung** enthalten.

Sie können die Verbindung mit dem Server schließen, indem Sie alle Verweise freigeben, die Sie für Agent-Objekte erstellt haben, z. B. IAgentCtlCharacterEx und IAgentCtlCommandEx. Sie müssen auch ihren Verweis auf das -Agent-Steuerelement selbst veröffentlichen. In Visual Basic können Sie einen Verweis auf ein Objekt veröffentlichen, indem Sie seine Variable auf **Nothing festlegen.** Wenn Sie Zeichen geladen haben, entladen Sie sie, bevor Sie das Zeichenobjekt freigeben.


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
> Sie können die Verbindung mit dem Server nicht schließen, indem Sie Verweise freigeben, in denen die Komponente hinzugefügt wurde. Beispielsweise können Sie die Verbindung mit dem Server nicht auf Webseiten schließen, auf denen Sie das OBJECT-Tag verwenden, um das Steuerelement zu deklarieren, oder in einer Visual Basic-Anwendung, auf der Sie das Steuerelement in einem Formular &lt; &gt; ablegen. Während die Freigabe aller Agent-Verweise den Arbeitssatz des -Agents reduziert, bleibt die Verbindung bestehen, bis Sie zur nächsten Seite navigieren oder die Anwendung beenden.

 

 

 





