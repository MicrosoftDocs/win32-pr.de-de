---
title: Load-Methode
description: Load-Methode
ms.assetid: 72a37471-f69b-49a5-a6eb-d65bff970c0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e201053bf3eb9fbd7a3c5c7eb94f9b032cde13087f76e1fcfa176d068655137a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118748652"
---
# <a name="load-method"></a>Load-Methode

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Lädt ein Zeichen in die [**Characters-Auflistung.**](/windows/desktop/lwef/the-characters-object)

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Characters.Load "**_CharacterID_*_",_ *  *Provider*



| Teil          | BESCHREIBUNG                                                                                                                                                                                                                              |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Erforderlich. Ein Zeichenfolgenwert, mit dem Sie auf die zu ladenden Zeichendaten verweisen.                                                                                                                                                  |
| *Anbieter*    | Erforderlich. Ein variant-Datentyp, der einen der folgenden Sein muss: **Filespec** Der lokale Dateispeicherort der Definitionsdatei des angegebenen Zeichens. <br/> **URL** Die HTTP-Adresse für die Definitionsdatei des Zeichens.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Sie können Zeichen aus dem -Agent-Unterverzeichnis laden, indem Sie einen relativen Pfad angeben (einen Pfad, der keinen Doppelpunkt oder führenden Schrägstrich enthält). Dadurch wird dem Pfad das Zeichenverzeichnis des -Agents vorangestellt (das sich im lokalisierten Windows \\ msagent-Verzeichnis befindet). Wenn Sie beispielsweise Folgendes angeben, wird Genie.acs aus dem Chars-Verzeichnis des Agents geladen:


```
   Agent.Character.Load "genie", "genie.acs"
```



Sie können auch ihr eigenes Verzeichnis im Chars-Verzeichnis des Agents angeben.


```
   Agent.Character.Load "genie", "MyCharacters\genie.acs"
```



Sie können das Zeichen laden, das derzeit als Standardzeichen des aktuellen Benutzers festgelegt ist, indem Sie keinen Pfad als zweiten Parameter der **Load-Methode** einschließen.


```
   Agent.Character.Load "character"
```



Sie können das gleiche Zeichen (ein Zeichen mit derselben GUID) nicht mehr als einmal aus einer einzelnen Instanz des Steuerelements laden. Ebenso können Sie das Standardzeichen und andere Zeichen nicht gleichzeitig aus einer einzelnen Instanz des Steuerelements laden, da das Standardzeichen mit dem anderen Zeichen identisch sein kann. Wenn Sie dies versuchen, löst der Server einen Fehler aus. Sie können jedoch eine weitere Instanz des -Agent-Steuerelements erstellen und das gleiche Zeichen laden.

Der Microsoft-Agent-Datenanbieter unterstützt das Laden von Zeichendaten, die entweder als einzelne strukturierte Datei gespeichert sind (. ACS) mit Zeichendaten und Animationsdaten zusammen oder als separate Zeichendaten (. ACF) und Animation (. ACA)-Dateien. Verwenden Sie die einzelne strukturierte . ACS-Datei zum Laden eines Zeichens, das auf einem lokalen Datenträger oder Netzwerk gespeichert ist und auf das mithilfe eines herkömmlichen Dateiprotokolls (z. B. UNC-Pfadnamen) zugegriffen wird. Verwenden Sie die separate . ACF und . ACA-Dateien, wenn Sie die Animationsdateien einzeln von einem Remotestandort laden möchten, an dem über das HTTP-Protokoll auf sie zugegriffen wird.

Für. ACS-Dateien, die die **Load-Methode** verwenden, bieten Zugriff auf die Animationen eines Zeichens. Für. ACF-Dateien verwenden Sie [](get-method.md) auch die Get-Methode, um Animationsdaten zu laden. Das Herunterladen von wird von der **Load-Methode** nicht unterstützt. ACS-Dateien von einer HTTP-Website.

Beim Laden eines Zeichens wird das Zeichen nicht automatisch angezeigt. Verwenden [](show-method.md) Sie zuerst die Show-Methode, um das Zeichen sichtbar zu machen.

Wenn Sie die **Load-Methode** verwenden, um eine auf dem lokalen Computer gespeicherte Zeichendatei zu laden, schlägt der Aufruf fehl. Da die Datei beispielsweise nicht gefunden wird, löst der -Agent einen Fehler aus. Sie können die Unterstützung in Ihrer Programmiersprache verwenden, um eine Fehlerbehandlungsroutine zum Abfangen und Verarbeiten des Fehlers bereitzustellen.


```
   Sub Form_Load
      On Error GoTo ErrorHandler
      Agent1.Characters.Load "mychar", "genie.acs"
      ' Successful load
      . . .
      Exit Sub
      ErrorHandler:
      ' Unsuccessful load
      . . .
      Resume Next
   End Sub
```



Sie können den Fehler auch behandeln, indem Sie [**RaiseRequestErrors**](https://www.bing.com/search?q=**RaiseRequestErrors**) auf **False** festlegen, ein -Objekt deklarieren und ihm die **Load-Anforderung** zuweisen. Folgen Sie dann dem **Load-Aufruf** mit einer -Anweisung, die den Status des [**Request-Objekts**](/windows/desktop/lwef/the-request-object) überprüft.


```
Dim LoadRequest as Object

   Sub Form_Load
      Agent1.RaiseRequestErrors = False
      Set LoadRequest = Agent1.Characters.Load _
         ("mychar", "c:\some directory\some character.acs")
      If LoadRequest.Status Not 0 Then
         ' Unsuccessful load
         . . .
         Exit Sub
      Else 
         ' Successful load
         . . .
   End Sub
```



Wenn Sie ein Zeichen laden, das nicht lokal ist, Beispielsweise können Sie mithilfe des HTTP-Protokolls auch nach einem **Ladefehler** suchen, indem Sie der **Load-Methode** ein [**Request-Objekt**](/windows/desktop/lwef/the-request-object) zuweisen. Da diese Methode zum Laden eines Zeichens jedoch asynchron behandelt wird, überprüfen Sie seinen Status im [**RequestComplete-Ereignis.**](requestcomplete-event.md) Diese Technik funktioniert nicht beim Laden eines Zeichens mithilfe des UNC-Protokolls, da die **Load-Methode** synchron verarbeitet wird.

 

