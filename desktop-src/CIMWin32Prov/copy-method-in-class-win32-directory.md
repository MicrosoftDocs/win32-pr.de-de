---
description: Kopiert die im Objekt Pfad angegebene Datei bzw. das Verzeichnis für den logischen Verzeichniseintrag an den Speicherort, der durch den Eingabeparameter angegeben wird.
ms.assetid: 038e23d7-71db-4db6-8fb1-e84e972510c9
ms.tgt_platform: multiple
title: Copy-Methode der Win32_Directory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 25568167d9532303a7cbee794757bc674a378b39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126924"
---
# <a name="copy-method-of-the-win32_directory-class"></a>Copy-Methode der Win32- \_ Verzeichnis Klasse

Die **Copy** - [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode kopiert die im Objekt Pfad angegebene Datei bzw. das Verzeichnis für den logischen Verzeichniseintrag in den Speicherort, der durch den Eingabeparameter angegeben wird. Eine Kopie wird nicht unterstützt, wenn eine vorhandene logische Datei überschrieben werden muss.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 Copy(
   string FileName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FileName* 
</dt> <dd>

Der voll qualifizierte Name der Kopie der Datei (oder des Verzeichnisses). Beispiel: c: \\ Temp \\ NewDirectory

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert 0 (null) zurück, wenn die Datei erfolgreich kopiert wurde, und jede andere Zahl gibt einen Fehler an.

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

Ordner müssen häufig von einem Speicherort in einen anderen kopiert werden. Beispielsweise können Sie einen Ordner von einem Server auf einen anderen kopieren, um eine Sicherungskopie dieses Ordners zu erstellen. Möglicherweise verfügen Sie auch über einen Vorlagen Ordner, der auf Benutzer Arbeitsstationen kopiert werden muss, oder einen Skript Ordner, der auf alle DNS-Server kopiert werden soll.

Mit der Win32- \_ Verzeichnis Kopiermethode können Sie einen Ordner von einem Speicherort auf einen anderen kopieren (z. b. Kopieren eines Ordners von Laufwerk C auf Laufwerk D) oder auf einem Remote Computer. Um einen Ordner zu kopieren, geben Sie eine Instanz des Ordners zurück, die kopiert werden soll, und dann die Kopiermethode, wobei Sie als Parameter den Zielort für die neue Kopie des Ordners übergeben. Diese Codezeile kopiert z. b. einen Ordner in den Ordner Scripts auf Laufwerk F:

`objFolder.Copy("F:\Scripts")`

Ein vorhandener Ordner wird von WMI beim Ausführen der Kopiermethode nicht überschrieben. Dies bedeutet, dass der Kopiervorgang fehlschlägt, wenn der Zielordner vorhanden ist. Angenommen, Sie verfügen über einen Ordner mit dem Namen "Scripts", und Sie versuchen, diesen Ordner auf eine Remote Freigabe namens " \\ \\ ATL-fs-01 Archive" zu kopieren \\ . Wenn ein Ordner mit dem Namen Skripts auf dieser Freigabe bereits vorhanden ist, schlägt der Kopiervorgang fehl.

## <a name="examples"></a>Beispiele

Mit dem folgenden Codebeispiel, das aus dem [Kopieren eines Ordners mithilfe von WMI](https://Gallery.TechNet.Microsoft.Com/71b8f517-0240-42a2-be5c-e5a3921604d2)stammt, wird die Copy-Methode verwendet, um den Ordner C: \\ Scripts in D: Archive zu kopieren \\ .


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colFolders = objWMIService.ExecQuery( _ 
    "Select * from Win32_Directory where Name = 'c:\\Scripts'") 
 
For Each objFolder in colFolders 
    errResults  = objFolder.Copy("D:\Archive") 
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

 

