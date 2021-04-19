---
description: WMI bietet eine Reihe von Techniken zum Abrufen und Bearbeiten von WMI-Klassen-und-Instanzinformationen mithilfe von Microsoft PowerShell, Visual&\# 160; Basic Scripting Edition (VBScript) und C++.
ms.assetid: 682cbe12-1487-4681-8d2f-4caf21cb068a
ms.tgt_platform: multiple
title: Manipulieren von Klassen-und Instanzinformationen
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 86e3e84deae73e206f41e9ea25e02b5d11373f3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359502"
---
# <a name="manipulating-class-and-instance-information"></a>Manipulieren von Klassen-und Instanzinformationen

WMI bietet eine Reihe von Techniken zum Abrufen und Bearbeiten von WMI-Klassen-und-Instanzinformationen mithilfe von Microsoft PowerShell, Visual Basic Scripting Edition (VBScript) und C++.

In der folgenden Tabelle sind die Themen zum Abrufen und Bearbeiten von WMI-Klassen-und-Instanzinformationen aufgeführt.



| Thema                                                                                  | BESCHREIBUNG                                                                                                                                                                       |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Abrufen von WMI-Klassen-oder-Instanzdaten](retrieving-class-or-instance-data.md)         | Abrufen und Festlegen von Daten aus und in das WMI-Informationsrepository.                                                                                                                 |
| [Ändern einer Instanzeigenschaft](modifying-an-instance-property.md)                   | Ändern Sie die Informationen in der-Instanz, nachdem Sie abgerufen wurde.                                                                                                                     |
| [Ändern der Vererbung einer Instanz](changing-the-inheritance-of-an-instance.md) | Ändern Sie die übergeordnete Klasse einer Instanz.                                                                                                                                           |
| [Ändern einer Methode](modifying-a-method.md)                                           | Ändern Sie die Parameter einer Instanz.                                                                                                                                             |
| [Auflisten von WMI](enumerating-wmi.md)                                                 | Enumerieren von WMI-Objekten.                                                                                                                                                            |
| [WMI-Abfrage](querying-wmi.md)                                                       | WMI-Objekte Abfragen.                                                                                                                                                                |
| [Aufrufen einer Methode](calling-a-method.md)                                               | Verwenden Sie zugeordnete Methoden, die von Microsoft oder anderen Entwicklern von Drittanbietern erstellt wurden, um WMI-Objekte weiter zu bearbeiten, oder ändern Sie das Objekt direkt, das das WMI-Objekt darstellt. |
| [Zugreifen auf eine Sammlung](accessing-a-collection.md)                                   | Auflisten von Auflistungen im Skript.                                                                                                                                                  |



 

## <a name="manipulating-data-using-vbscript"></a>Bearbeiten von Daten mithilfe von VBScript

Sie können direkt Zugriff verwenden, um auf die WMI-Eigenschaften einer WMI-Klasse oder-Instanz direkt in einem " [**Swap**](swbemobject.md)"-Objekt zuzugreifen, anstatt über [die Eigenschafts](accessing-a-collection.md) Auflistung dieses Objekts. Sie können auch Methoden für dieses Objekt im systemeigenen Stil der Programmiersprache ausführen, anstatt den [**SWbemServices.Execmethod**](swbemservices-execmethod.md) -aufzurufen. Beispielsweise enthielt die [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) -Methode im [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process) in Windows 2000 drei Parameter, verfügt jedoch über vier Parameter in Windows Server 2003.

Mithilfe von Direct Access können Sie WMI-Eigenschaften und-Methoden so behandeln, als wären Sie Automatisierungs Eigenschaften und-Methoden von " [**errbemubject**](swbemobject.md)".

Im folgenden Beispiel wird gezeigt, wie Sie auf eine Eigenschaft zugreifen können.


```VB
VolumeName = MyDisk.Properties_("VolumeName")
```



Im folgenden Beispiel wird gezeigt, wie Sie auf eine Eigenschaft zugreifen können, wenn Sie über direkten Zugriff verfügen.


```VB
VolumeName = MyDisk.VolumeName
```



Das Verketten von Objekten ist ebenfalls akzeptabel.

Das folgende Beispiel zeigt, wie Sie auf eine Eigenschaft eines Objekts zugreifen, das in ein anderes-Objekt eingebettet ist.


```VB
value = MyComputer.MyDisk.VolumeName
```



Im folgenden Beispiel wird gezeigt, wie Sie auf eine Eigenschaft mit einer Array Index-Notation zugreifen können.


```VB
valueOfElement = MyDisk.MyArrayProperty(3)
```



Im folgenden VBScript-Codebeispiel wird veranschaulicht, wie Sie eine Instanz der Eingabeparameter für die Create-Methode in der [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process) Klasse als ein [**Swap-Objekt**](swbemobject.md) [**Erstellen**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) , die Eingabe Eigenschaften auffüllen und dann die **Create** -Methode mithilfe [**SWbemServices.Execmethod**](swbemservices-execmethod.md)ausführen.

Die " [**errbemubject. \_ Methods**](swbemobject-methods-.md) "-Eigenschaft gibt eine " [**errbemmethodset**](swbemmethodset.md) "-Auflistung der [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process) Methoden zurück. Die Member des-Methoden Satzes sind ' [**taubemmethod**](swbemmethod.md) '-Objekte, und ' [**taubemmethod. InParameters**](swbemmethod-inparameters.md) ' gibt die Eingabeparameter für die [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) -Methode zurück. Der erforderliche *CommandLine* -Eingabeparameter ist auf "calc.exe" festgelegt. Die Methode wird dann von [**SWbemServices.Execmethod**](swbemservices-execmethod.md)ausgeführt, wodurch ein calc.exe Prozess gestartet wird.


```VB
set Services = GetObject("winmgmts:root\cimv2")
Set obj = Services.Get("Win32_Process")
Set objIns = obj.Methods_("Create").InParameters.SpawnInstance_
objIns.CommandLine = "calc.exe"
Set objOut = Services.ExecMethod("Win32_Process", "Create", objIns)
MsgBox "Return value = " & objOut.returnvalue & VBCRLF & "Process ID = " & objOut.processid
```



Im folgenden Codebeispiel wird gezeigt, wie der vorherige Vorgang mithilfe von Direct Access durchgeführt wird.


```VB
set Services = GetObject("winmgmts:root\cimv2")
Set Obj = Services.Get("Win32_Process")
returnvalue = Obj.create("calc.exe",,,processid)
MsgBox "Return value = " & returnvalue & VBCRLF & "Process ID = " & processid
```



Weitere Informationen finden Sie unter [Aufrufen einer Anbieter Methode](calling-a-provider-method.md) und [Skripterstellung mit "errbemubject](scripting-with-swbemobject.md)".

 

 
