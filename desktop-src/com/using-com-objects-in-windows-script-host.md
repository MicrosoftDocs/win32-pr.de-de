---
title: Verwenden von COM-Objekten in Windows Script Host
description: Microsoft Windows Script Host ist ein Skript-Hilfsprogramm, das Sie verwenden können, um Skripts innerhalb des Basis Betriebssystems auszuführen.
ms.assetid: b13c1bdf-91ce-42a2-b66a-20d68952bb34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7cb28fc0e388ba69f28c56e780d058d27f9e165
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761586"
---
# <a name="using-com-objects-in-windows-script-host"></a>Verwenden von COM-Objekten in Windows Script Host

Microsoft Windows Script Host ist ein Skript-Hilfsprogramm, das Sie verwenden können, um Skripts innerhalb des Basis Betriebssystems auszuführen. Sie können Windows Script Host verwenden, um häufige Aufgaben zu automatisieren und leistungsstarke Makros und Anmelde Skripts zu erstellen. Windows Script Host enthält VBScript-und JScript-ActiveX-Skript-Engines. Andere Softwareunternehmen stellen ActiveX-Skript-Engines für Sprachen wie z. b. Perl Script, Pscript, Python und andere bereit.

Wenn Sie ein COM-Objekt in einem Skript verwenden möchten, das von Windows Script Host ausgeführt wird, müssen Sie zunächst eine Instanz des-Objekts erstellen. Nachdem ein COM-Objekt erstellt wurde, können Sie es in Skripts verwenden.

Windows Script Host besteht aus zwei Anwendungen. Mit einem Befehl werden Skripts aus dem Windows-Desktop ( `WScript.exe` ) ausgeführt. der andere Befehl führt Skripts von der Eingabeaufforderung ( `CScript.exe` ) aus.

Zum Ausführen eines Skripts auf dem Desktop doppelklicken Sie einfach auf eine Skriptdatei. Skriptdateien sind Textdateien. Gemäß der Konvention weisen VBScript-Dateien die Erweiterung `.vbs` und die JScript-Dateien auf `.js` .

Wenn Sie ein Skript an der Eingabeaufforderung ausführen möchten, führen Sie die `Cscript.exe` Anwendung mit einer Befehlszeile wie dem folgenden aus:

```console
cscript "c:\\sample scripts\\chart.vbs"
```

dabei `c:\\sample scripts\\chart.vbs` ist der Pfad zu der Datei, die das Skript enthält.

Sie können eine Liste der von Cscript.exe unterstützten Parameter ausdrucken, indem Sie die folgende Befehlszeile eingeben:

```console
call cscript //?
```

Wenn Sie ein COM-Objekt in einem Skript verwenden möchten, das von Windows Script Host ausgeführt wird, müssen Sie zunächst eine Instanz des-Objekts erstellen. In VBScript können Sie dies erreichen, indem Sie die- `CreateObject()` Methode aufrufen. In JScript kann entweder das- `ActiveXObject` Objekt oder die- `WScript.CreateObject()` Methode verwendet werden. Das folgende Beispiel veranschaulicht den Aufruf von `CreateObject()` mithilfe von VBScript:


```VB
Dim objXL
Set objXL = CreateObject("Excel.Application")
 
```



Das folgende Beispiel veranschaulicht das Erstellen eines `ActiveXObject` Objekts mithilfe von JScript:


```JScript
var objXL = new ActiveXObject("Excel.Application");
 
```
Alternativ dazu können Sie die `WScript.CreateObject()` Methode in JScript verwenden:

```JScript
var objXL = WScript.CreateObject("Excel.Application");
```


Nachdem Sie eine Instanz des COM-Objekts erstellt haben, können Sie Skripts schreiben, die das-Objekt verwenden, z. b.:


```VB
objXL.Visible = true;
 
```



Neben der Methode "kreateobject" und dem ActiveXObject-Objekt stellen sowohl VBScript als auch JScript die Methode "GetObject" bereit, die eine Objektinstanz zurückgibt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Skripterstellung mit COM-Objekten](scripting-with-com-objects.md)
</dt> </dl>

 

 




