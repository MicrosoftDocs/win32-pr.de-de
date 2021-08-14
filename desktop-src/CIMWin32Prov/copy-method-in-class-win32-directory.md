---
description: Kopiert die im Objektpfad angegebene logische Verzeichniseintragsdatei oder das verzeichnis an den speicherort, der durch den Eingabeparameter angegeben wird.
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
ms.openlocfilehash: 85a16d3e63ef46ad2c536103a4e462a3e830e17f56f83cdcf39bbad5a33ebb23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118419755"
---
# <a name="copy-method-of-the-win32_directory-class"></a>Copy-Methode der Win32 \_ Directory-Klasse

Die [Methode WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) **kopieren** kopiert die im Objektpfad angegebene logische Verzeichniseintragsdatei oder das verzeichnis an den speicherort, der durch den Eingabeparameter angegeben wird. Eine Kopie wird nicht unterstützt, wenn das Überschreiben einer vorhandenen logischen Datei erforderlich ist.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

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

Vollqualifizierte Name der Kopie der Datei (oder des Verzeichnisses). Beispiel: c: \\ temp \\ newdirectory

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert 0 (null) zurück, wenn die Datei erfolgreich kopiert wurde, und eine beliebige andere Zahl, um einen Fehler anzugeben.

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

Es ist ein Freigabeverstoß aufgetreten.

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

Ordner müssen häufig von einem Speicherort an einen anderen kopiert werden. Beispielsweise können Sie einen Ordner von einem Server auf einen anderen kopieren, um eine Sicherungskopie dieses Ordners zu erstellen. Oder Sie verfügen über einen Vorlagenordner, der auf Benutzerarbeitsstationen kopiert werden muss, oder einen Skriptordner, der auf alle DNS-Server kopiert werden soll.

Mit der Win32 \_ Directory Copy-Methode können Sie einen Ordner von einem Speicherort an einen anderen kopieren, entweder auf demselben Computer (z. B. beim Kopieren eines Ordners von Laufwerk C auf Laufwerk D) oder auf einem Remotecomputer. Um einen Ordner zu kopieren, geben Sie eine Instanz des zu kopierenden Ordners zurück und rufen dann die Copy-Methode auf, wobei Sie als Parameter den Zielspeicherort für die neue Kopie des Ordners übergeben. Mit dieser Codezeile wird beispielsweise ein Ordner in den Ordner Scripts auf Laufwerk F kopiert:

`objFolder.Copy("F:\Scripts")`

WMI überschreibt beim Ausführen der Copy-Methode keinen vorhandenen Ordner. Dies bedeutet, dass der Kopiervorgang fehlschlägt, wenn der Zielordner vorhanden ist. Angenommen, Sie verfügen über einen Ordner mit dem Namen Scripts und versuchen, diesen Ordner in eine Remotefreigabe mit dem Namen \\ \\ atl-fs-01 archive zu \\ kopieren. Wenn auf dieser Freigabe bereits ein Ordner mit dem Namen Scripts vorhanden ist, schlägt der Kopiervorgang fehl.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel aus dem Copy [a Folder Using WMI (Kopieren eines Ordners mithilfe von WMI)](https://Gallery.TechNet.Microsoft.Com/71b8f517-0240-42a2-be5c-e5a3921604d2)wird die Copy-Methode verwendet, um den Ordner C: \\ Scripts to D: Archive (C: Skripts in D: Archiv) zu \\ kopieren.


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
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Win32-Verzeichnis**](win32-directory.md)
</dt> </dl>

 

