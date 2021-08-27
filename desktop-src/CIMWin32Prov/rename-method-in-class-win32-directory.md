---
description: Benennt die im Objektpfad angegebene Verzeichniseintragsdatei um.
ms.assetid: 8bfe1b69-5f93-4408-a742-f03a9cb16bfe
ms.tgt_platform: multiple
title: Umbenennen der Win32_Directory-Klasse
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
ms.openlocfilehash: 86b6bd35b14ee2a342dee27615c1ff21d9274a5f3020c4f804df5065f430813f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077440"
---
# <a name="rename-method-of-the-win32_directory-class"></a>Rename-Methode der Win32 \_ Directory-Klasse

Die **Methode** [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) umbenennen benennt die im Objektpfad angegebene Verzeichniseintragsdatei um. Eine Umbenennung wird nicht unterstützt, wenn sich das Ziel auf einem anderen Laufwerk befindet oder wenn das Überschreiben einer vorhandenen logischen Datei erforderlich ist.

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

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

Vollqualifizierter neuer Name der Datei (oder des Verzeichnisses). Beispiel: c: \\ temp \\newfile.txt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert 0 (null) zurück, wenn die Datei erfolgreich umbenannt wurde, und eine beliebige andere Zahl, um einen Fehler anzugeben.

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

Es ist ein nicht angegebener Fehler aufgetreten.

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

Es ist ein Freigabeverstoß vor worden.

</dd> <dt>

**16**
</dt> <dd>

Die angegebene Startdatei war ungültig.

</dd> <dt>

**17**
</dt> <dd>

Für den Vorgang ist keine Berechtigung erforderlich.

</dd> <dt>

**21**
</dt> <dd>

Ein angegebener Parameter ist ungültig.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Um einen Ordner umzubenennen, binden Sie zunächst an den in Frage gestellten Ordner, und rufen Sie dann die Rename-Methode auf. Übergeben Sie als einziger Parameter für die -Methode den neuen Namen für den Ordner als vollständigen Pfadnamen. Wenn der Ordner in der Sicherung von C: Skriptprotokollen beispielsweise in C: Skriptarchiv umbenannt werden soll, müssen Sie C: Scripts Archive als vollständigen \\ \\ \\ \\ \\ \\ \\ Ordnernamen übergeben. Die Übergabe des Ordnernamens Archive führt zu einem Fehler mit ungültigen Pfaden.

Die Win32 \_ Directory-Klasse stellt keine einstufige Methode zum Verschieben von Ordnern zur Verfügung. Stattdessen umfasst das Verschieben eines Ordners in der Regel zwei Schritte:

<dl> 1. Kopieren des Ordners an den neuen Speicherort  
2. Löschen des ursprünglichen Ordners  
</dl>

Die einzige Ausnahme dieses zweistufigen Prozesses besteht darin, einen Ordner an einen neuen Speicherort auf demselben Laufwerk zu verschieben. Angenommen, Sie möchten C: Temp in \\ C: \\ Scripts Temporary Files \\ Archive \\ verschieben. Solange sich der aktuelle und der neue Speicherort auf demselben Laufwerk befinden, können Sie den Ordner verschieben, indem Sie einfach die Rename-Methode aufrufen und den neuen Speicherort als Methodenparameter übergeben. Mit diesem Ansatz können Sie den Ordner in einem einzigen Schritt verschieben. Das Skript schlägt jedoch fehl, wenn sich das aktuelle Laufwerk und das neue Laufwerk unterscheiden. Fehler beim Umbenennen von C: Temp in D: Temp mit dem Fehler \\ \\ "Laufwerk nicht identisch".

## <a name="examples"></a>Beispiele

Der folgende Code aus dem Beispiel Verschieben eines Ordners [mithilfe](https://Gallery.TechNet.Microsoft.Com/f4f9643c-d7ed-4f54-b155-c6515396431f) von WMI VBScript im TechNet-Katalog verwendet die Rename-Methode, um den Ordner C: \\ Scripts nach C: \\ Admins Documents Archive VBScript zu \\ \\ \\ verschieben.


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
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32-Verzeichnis \_**](win32-directory.md)
</dt> </dl>

 

