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
# <a name="using-com-objects-in-windows-script-host"></a><span data-ttu-id="d19b1-103">Verwenden von COM-Objekten in Windows Script Host</span><span class="sxs-lookup"><span data-stu-id="d19b1-103">Using COM Objects in Windows Script Host</span></span>

<span data-ttu-id="d19b1-104">Microsoft Windows Script Host ist ein Skript-Hilfsprogramm, das Sie verwenden können, um Skripts innerhalb des Basis Betriebssystems auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d19b1-104">Microsoft Windows Script Host is a scripting utility you can use to run scripts within the base operating system.</span></span> <span data-ttu-id="d19b1-105">Sie können Windows Script Host verwenden, um häufige Aufgaben zu automatisieren und leistungsstarke Makros und Anmelde Skripts zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d19b1-105">You can use Windows Script Host to automate common tasks and to create powerful macros and logon scripts.</span></span> <span data-ttu-id="d19b1-106">Windows Script Host enthält VBScript-und JScript-ActiveX-Skript-Engines.</span><span class="sxs-lookup"><span data-stu-id="d19b1-106">Windows Script Host comes with VBScript and JScript ActiveX scripting engines.</span></span> <span data-ttu-id="d19b1-107">Andere Softwareunternehmen stellen ActiveX-Skript-Engines für Sprachen wie z. b. Perl Script, Pscript, Python und andere bereit.</span><span class="sxs-lookup"><span data-stu-id="d19b1-107">Other software companies provide ActiveX scripting engines for languages such as PerlScript, PScript, Python, and others.</span></span>

<span data-ttu-id="d19b1-108">Wenn Sie ein COM-Objekt in einem Skript verwenden möchten, das von Windows Script Host ausgeführt wird, müssen Sie zunächst eine Instanz des-Objekts erstellen.</span><span class="sxs-lookup"><span data-stu-id="d19b1-108">To use a COM object in a script run by Windows Script Host, you must first create an instance of the object.</span></span> <span data-ttu-id="d19b1-109">Nachdem ein COM-Objekt erstellt wurde, können Sie es in Skripts verwenden.</span><span class="sxs-lookup"><span data-stu-id="d19b1-109">After a COM object has been created, you can then use it in scripts.</span></span>

<span data-ttu-id="d19b1-110">Windows Script Host besteht aus zwei Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="d19b1-110">Windows Script Host consists of two applications.</span></span> <span data-ttu-id="d19b1-111">Mit einem Befehl werden Skripts aus dem Windows-Desktop ( `WScript.exe` ) ausgeführt. der andere Befehl führt Skripts von der Eingabeaufforderung ( `CScript.exe` ) aus.</span><span class="sxs-lookup"><span data-stu-id="d19b1-111">One runs scripts from the Windows desktop (`WScript.exe`); the other runs scripts from the command prompt (`CScript.exe`).</span></span>

<span data-ttu-id="d19b1-112">Zum Ausführen eines Skripts auf dem Desktop doppelklicken Sie einfach auf eine Skriptdatei.</span><span class="sxs-lookup"><span data-stu-id="d19b1-112">To run a script from the desktop, simply double-click a script file.</span></span> <span data-ttu-id="d19b1-113">Skriptdateien sind Textdateien.</span><span class="sxs-lookup"><span data-stu-id="d19b1-113">Script files are text files.</span></span> <span data-ttu-id="d19b1-114">Gemäß der Konvention weisen VBScript-Dateien die Erweiterung `.vbs` und die JScript-Dateien auf `.js` .</span><span class="sxs-lookup"><span data-stu-id="d19b1-114">By convention, VBScript files have the extension `.vbs` and JScript files `.js`.</span></span>

<span data-ttu-id="d19b1-115">Wenn Sie ein Skript an der Eingabeaufforderung ausführen möchten, führen Sie die `Cscript.exe` Anwendung mit einer Befehlszeile wie dem folgenden aus:</span><span class="sxs-lookup"><span data-stu-id="d19b1-115">To run a script from the command prompt, run the `Cscript.exe` application with a command line such as the following:</span></span>

```console
cscript "c:\\sample scripts\\chart.vbs"
```

<span data-ttu-id="d19b1-116">dabei `c:\\sample scripts\\chart.vbs` ist der Pfad zu der Datei, die das Skript enthält.</span><span class="sxs-lookup"><span data-stu-id="d19b1-116">where `c:\\sample scripts\\chart.vbs` is the path to the file containing the script.</span></span>

<span data-ttu-id="d19b1-117">Sie können eine Liste der von Cscript.exe unterstützten Parameter ausdrucken, indem Sie die folgende Befehlszeile eingeben:</span><span class="sxs-lookup"><span data-stu-id="d19b1-117">You can print out a list of the parameters supported by Cscript.exe by entering the following command line:</span></span>

```console
call cscript //?
```

<span data-ttu-id="d19b1-118">Wenn Sie ein COM-Objekt in einem Skript verwenden möchten, das von Windows Script Host ausgeführt wird, müssen Sie zunächst eine Instanz des-Objekts erstellen.</span><span class="sxs-lookup"><span data-stu-id="d19b1-118">To use a COM object in a script run by Windows Script Host, you must first create an instance of the object.</span></span> <span data-ttu-id="d19b1-119">In VBScript können Sie dies erreichen, indem Sie die- `CreateObject()` Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d19b1-119">In VBScript you can do this by calling the `CreateObject()` method.</span></span> <span data-ttu-id="d19b1-120">In JScript kann entweder das- `ActiveXObject` Objekt oder die- `WScript.CreateObject()` Methode verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d19b1-120">In JScript one can use either the `ActiveXObject` object or the `WScript.CreateObject()` method.</span></span> <span data-ttu-id="d19b1-121">Das folgende Beispiel veranschaulicht den Aufruf von `CreateObject()` mithilfe von VBScript:</span><span class="sxs-lookup"><span data-stu-id="d19b1-121">The following example illustrates calling `CreateObject()` using VBScript:</span></span>


```VB
Dim objXL
Set objXL = CreateObject("Excel.Application")
 
```



<span data-ttu-id="d19b1-122">Das folgende Beispiel veranschaulicht das Erstellen eines `ActiveXObject` Objekts mithilfe von JScript:</span><span class="sxs-lookup"><span data-stu-id="d19b1-122">The following example illustrates creating an `ActiveXObject` object using JScript:</span></span>


```JScript
var objXL = new ActiveXObject("Excel.Application");
 
```
<span data-ttu-id="d19b1-123">Alternativ dazu können Sie die `WScript.CreateObject()` Methode in JScript verwenden:</span><span class="sxs-lookup"><span data-stu-id="d19b1-123">Alternatively using `WScript.CreateObject()` method inside JScript:</span></span>

```JScript
var objXL = WScript.CreateObject("Excel.Application");
```


<span data-ttu-id="d19b1-124">Nachdem Sie eine Instanz des COM-Objekts erstellt haben, können Sie Skripts schreiben, die das-Objekt verwenden, z. b.:</span><span class="sxs-lookup"><span data-stu-id="d19b1-124">After you have created an instance of the COM object, you can write script that uses the object, for example:</span></span>


```VB
objXL.Visible = true;
 
```



<span data-ttu-id="d19b1-125">Neben der Methode "kreateobject" und dem ActiveXObject-Objekt stellen sowohl VBScript als auch JScript die Methode "GetObject" bereit, die eine Objektinstanz zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d19b1-125">In addition to the CreateObject method and ActiveXObject object, both VBScript and JScript provide the method GetObject, which returns an object instance.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d19b1-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d19b1-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d19b1-127">Skripterstellung mit COM-Objekten</span><span class="sxs-lookup"><span data-stu-id="d19b1-127">Scripting with COM Objects</span></span>](scripting-with-com-objects.md)
</dt> </dl>

 

 




