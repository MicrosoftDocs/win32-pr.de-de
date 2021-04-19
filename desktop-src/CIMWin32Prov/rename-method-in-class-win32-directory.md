---
description: Benennt die im Objekt Pfad angegebene Verzeichniseintrags Datei um.
ms.assetid: 8bfe1b69-5f93-4408-a742-f03a9cb16bfe
ms.tgt_platform: multiple
title: Rename-Methode der Win32_Directory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 874151e1ff8c9feca375df3eb441665863d1070d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346621"
---
# <a name="rename-method-of-the-win32_directory-class"></a>Rename-Methode der Win32- \_ Verzeichnis Klasse

Die Methode zum **Umbenennen** der [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) benennt die Verzeichniseintrags Datei um, die im Objekt Pfad angegeben ist. Ein umbenennen wird nicht unterstützt, wenn sich das Ziel auf einem anderen Laufwerk befindet oder wenn eine vorhandene logische Datei überschrieben werden muss.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 Rename(
   string FileName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FileName* 
</dt> <dd>

Voll qualifizierter neuer Name der Datei (oder des Verzeichnisses). Beispiel: c: \\ Temp \\newfile.txt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert 0 (null) zurück, wenn die Datei erfolgreich umbenannt wurde, und jede andere Zahl gibt einen Fehler an.

<dl> <dt>

**0**
</dt> <dd>

Die Anforderung wurde erfolgreich gesendet.

</dd> <dt>

**2**
</dt> <dd>

Der Zugriff wurde verweigert.

</dd> <dt>

**8**
</dt> <dd>

Ein nicht angegebener Fehler ist aufgetreten.

</dd> <dt>

**9**
</dt> <dd>

Der angegebene Name war ungültig.

</dd> <dt>

**10**
</dt> <dd>

Das angegebene Objekt ist bereits vorhanden.

</dd> <dt>

**11**
</dt> <dd>

Das Dateisystem ist nicht NTFS.

</dd> <dt>

**12**
</dt> <dd>

Die Plattform ist nicht Windows.

</dd> <dt>

**13**
</dt> <dd>

Das Laufwerk ist nicht identisch.

</dd> <dt>

**14**
</dt> <dd>

Das Verzeichnis ist nicht leer.

</dd> <dt>

**15**
</dt> <dd>

Es ist eine Freigabe Verletzung aufgetreten.

</dd> <dt>

**16**
</dt> <dd>

Die angegebene Startdatei war ungültig.

</dd> <dt>

**17**
</dt> <dd>

Eine für den Vorgang erforderliche Berechtigung wird nicht aufrechterhalten.

</dd> <dt>

**21**
</dt> <dd>

Ein angegebener Parameter ist ungültig.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Zum Umbenennen eines Ordners müssen Sie zuerst eine Bindung an den fraglichen Ordner herstellen und dann die Rename-Methode aufzurufen. Übergeben Sie als einzigen Parameter für die-Methode den neuen Namen für den Ordner als einen kompletten Pfadnamen. Wenn beispielsweise der Ordner in der Datei "c: Scripts" die \\ \\ Sicherung " \\ c: Scripts Archive" umbenennen soll \\ \\ , müssen Sie c: \\ Scripts \\ Archive als den gesamten Ordnernamen übergeben. Wenn nur der Ordnername-Archive übergeben wird, führt dies zu einem ungültigen Pfad Fehler.

Die Win32- \_ Verzeichnis Klasse bietet keine einstufige Methode zum Verschieben von Ordnern. Stattdessen umfasst das Verschieben eines Ordners im Allgemeinen zwei Schritte:

<dl> 1. Der Ordner wird an den neuen Speicherort kopiert.  
2. Löschen des ursprünglichen Ordners  
</dl>

Die einzige Ausnahme zu diesem zweistufigen Prozess besteht darin, einen Ordner an einen neuen Speicherort auf demselben Laufwerk zu verschieben. Nehmen Sie beispielsweise an, dass Sie "c: \\ Temp" in "c: \\ Scripts \\ temporäre Dateien \\ Archive" verschieben möchten. Solange sich der aktuelle Speicherort und der neue Speicherort auf demselben Laufwerk befinden, können Sie den Ordner verschieben, indem Sie einfach die Rename-Methode aufrufen und den neuen Speicherort als Methoden Parameter übergeben. Diese Vorgehensweise ermöglicht es Ihnen, den Ordner in einem einzigen Schritt zu verschieben. Das Skript schlägt jedoch fehl, wenn sich das aktuelle Laufwerk und das neue Laufwerk unterscheiden. Der Versuch, C: \\ Temp in D: Temp umzubenennen, \\ schlägt mit dem Fehler "Laufwerk nicht identisch" fehl.

## <a name="examples"></a>Beispiele

Der folgende Code aus dem Beispiel zum [Verschieben eines Ordners mit WMI](https://Gallery.TechNet.Microsoft.Com/f4f9643c-d7ed-4f54-b155-c6515396431f) VBScript in der TechNet Gallery verwendet die Rename-Methode, um den Ordner c: \\ Scripts in c: \\ Admins \\ Documents \\ Archive \\ VBScript zu verschieben.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colFolders = objWMIService.ExecQuery _ 
    ("Select * from Win32_Directory where name = 'c:\\Scripts'") 
 
For Each objFolder in colFolders 
    errResults = objFolder.Rename("C:\Admins\Documents\Archive\VBScript") 
Next
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32- \_ Verzeichnis**](win32-directory.md)
</dt> </dl>

 

