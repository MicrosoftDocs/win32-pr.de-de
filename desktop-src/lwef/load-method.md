---
title: Load-Methode
description: Load-Methode
ms.assetid: 72a37471-f69b-49a5-a6eb-d65bff970c0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0927fc8e49e55c2bdfcd7b1109bb8604540c199c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106337425"
---
# <a name="load-method"></a>Load-Methode

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Lädt ein Zeichen in die [**Zeichen**](/windows/desktop/lwef/the-characters-object) Auflistung.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent ***. Zeichen. Load "*** Merkmal-ID * *",* *  *Anbieter*



| Teil          | BESCHREIBUNG                                                                                                                                                                                                                              |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Merkmal-ID* | Erforderlich. Ein Zeichen folgen Wert, mit dem auf die zu ladenden Zeichendaten verwiesen wird.                                                                                                                                                  |
| *Anbieter*    | Erforderlich. Ein Variant-Datentyp, bei dem es sich um einen der folgenden Typen handeln muss: **filespec** der lokale Datei Speicherort der Definitionsdatei des angegebenen Zeichens. <br/> **URL** Die http-Adresse für die Definitionsdatei des Zeichens.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Sie können Zeichen aus dem Unterverzeichnis des Agents laden, indem Sie einen relativen Pfad angeben (einer, der keinen Doppelpunkt oder vorangestellenden Schrägstrich enthält). Dadurch wird der Pfad mit dem Zeichen Verzeichnis des Agents (befindet sich im lokalisierten Windows \\ MSAgent-Verzeichnis) als Präfix versehen. Wenn Sie z. b. Folgendes angeben, wird Genie. ACS aus dem chars-Verzeichnis des Agents geladen:


```
   Agent.Character.Load "genie", "genie.acs"
```



Sie können auch Ihr eigenes Verzeichnis im chars-Verzeichnis des Agents angeben.


```
   Agent.Character.Load "genie", "MyCharacters\genie.acs"
```



Sie können das Zeichen, das momentan als Standard Zeichen des aktuellen Benutzers festgelegt ist, laden, indem Sie keinen Pfad als zweiten Parameter der **Load** -Methode einschließen.


```
   Agent.Character.Load "character"
```



Es ist nicht möglich, dasselbe Zeichen (ein Zeichen mit derselben GUID) mehrmals aus einer einzelnen Instanz des Steuer Elements zu laden. Ebenso können Sie das Standard Zeichen und andere Zeichen nicht gleichzeitig von einer einzelnen Instanz des Steuer Elements laden, da das Standard Zeichen mit dem anderen Zeichen identisch sein könnte. Wenn Sie versuchen, dies zu tun, löst der Server einen Fehler aus. Sie können jedoch eine weitere Instanz des agentsteuerelements erstellen und dasselbe Zeichen laden.

Der Microsoft-Agent Datenanbieter unterstützt das Laden von Zeichendaten, die entweder als einzelne strukturierte Datei () gespeichert werden. ACS) mit Zeichendaten und Animationsdaten oder als separate Zeichendaten (. ACF) und Animation (. ACA-Dateien. Verwenden Sie die strukturierte Struktur. Die ACS-Datei zum Laden eines Zeichens, das auf einem lokalen Datenträger oder Netzwerk gespeichert wird und auf das mithilfe eines herkömmlichen Datei Protokolls (z. b. UNC-Pfadnamen) zugegriffen wird. Verwenden Sie die separate. ACF und. ACA-Dateien, wenn Sie die Animationsdateien einzeln von einer Remote Site laden möchten, auf die über das HTTP-Protokoll zugegriffen wird.

Damit. ACS-Dateien, die die **Load** -Methode verwenden, bieten Zugriff auf die Animationen eines Zeichens. Damit. ACF-Dateien verwenden Sie auch die [**Get**](get-method.md) -Methode, um Animationsdaten zu laden. Die **Load** -Methode unterstützt nicht das herunterladen. ACS-Dateien von einer HTTP-Site.

Beim Laden eines Zeichens wird das Zeichen nicht automatisch angezeigt. Verwenden Sie zuerst die [**Show**](show-method.md) -Methode, um das Zeichen sichtbar zu machen.

Wenn Sie die **Load** -Methode verwenden, um eine auf dem lokalen Computer gespeicherte Zeichen Datei zu laden, schlägt der-Befehl fehl. Da die Datei z. b. nicht gefunden wird, löst der-Agent einen Fehler aus. Mithilfe der-Unterstützung in der Programmiersprache können Sie eine Fehler Behandlungs Routine bereitstellen, um den Fehler zu erfassen und zu verarbeiten.


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



Sie können den Fehler auch behandeln, indem Sie [**raiserequesterrors**](https://www.bing.com/search?q=**RaiseRequestErrors**) auf **false** festlegen, ein-Objekt deklarieren und ihm die **Lade** Anforderung zuweisen. Befolgen Sie dann den **Lade** Vorgang mit einer-Anweisung, die den Status des [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekts überprüft.


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



Wenn Sie ein nicht lokales Zeichen laden. Beispielsweise können Sie mithilfe des HTTP-Protokolls auch überprüfen, ob ein **Lade** Fehler vorliegt, indem Sie der **Load** -Methode ein [**Request**](/windows/desktop/lwef/the-request-object) -Objekt zuweisen. Da diese Methode zum Laden eines Zeichens jedoch asynchron verarbeitet wird, überprüfen Sie seinen Status im [**requestcomplete**](requestcomplete-event.md) -Ereignis. Dieses Verfahren funktioniert nicht, wenn ein Zeichen mithilfe des UNC-Protokolls geladen wird, da die **Load** -Methode synchron verarbeitet wird.

 

