---
description: Gibt eine UInt32-Bitmap mit den Zugriffsrechten für die Freigabe zurück, die der Benutzer oder die Gruppe hat, in deren Auftrag die Instanz zurückgegeben wird.
ms.assetid: 234f44a4-ffff-431d-a973-98f2bd313c7d
ms.tgt_platform: multiple
title: Getaccessmask-Methode der Win32_Share-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.GetAccessMask
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 745ce6d607adf84827c14a588640572b5d92be00
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958312"
---
# <a name="getaccessmask-method-of-the-win32_share-class"></a>Getaccessmask-Methode der Win32- \_ Freigabe Klasse

Die **getaccessmask** -Methode gibt eine UInt32-Bitmap mit den Zugriffsrechten für die Freigabe zurück, die der Benutzer oder die Gruppe hat, in deren Auftrag die Instanz zurückgegeben wird.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 GetAccessMask();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Zugriffsrechte für die Freigabe, die der Benutzer oder die Gruppe innehat.

<dl> <dt>

**Datei \_ Listen \_ Verzeichnis**
</dt> <dd>

1 (0x1)

Gewährt das Recht, Daten aus der Datei zu lesen. Bei einem Verzeichnis gewährt dieser Wert das Recht, den Inhalt des Verzeichnisses aufzulisten.

</dd> <dt>

**Datei \_ Hinzufügen \_**
</dt> <dd>

2 (0x2)

Gewährt das Recht, Daten in die Datei zu schreiben. Bei einem Verzeichnis gewährt dieser Wert das Recht, eine Datei im Verzeichnis zu erstellen.

</dd> <dt>

**\_Unterverzeichnis "Datei hinzufügen" \_**
</dt> <dd>

4 (0x4)

Gewährt das Recht zum Anfügen von Daten an die Datei. Bei einem Verzeichnis gewährt dieser Wert das Recht, ein Unterverzeichnis zu erstellen.

</dd> <dt>

**Datei \_ Lese- \_ EA**
</dt> <dd>

8 (0x8)

Gewährt das Recht zum Lesen erweiterter Attribute.

</dd> <dt>

**Datei \_ Schreib- \_ EA**
</dt> <dd>

16 (0x10)

Gewährt das Recht, erweiterte Attribute zu schreiben.

</dd> <dt>

**Datei \_ Durchlauf**
</dt> <dd>

32 (0x20)

Gewährt das Recht, eine Datei auszuführen. Für ein Verzeichnis kann das Verzeichnis durchsucht werden.

</dd> <dt>

**Datei \_ Delete \_ Child**
</dt> <dd>

64 (0x40)

Gewährt das Recht, ein Verzeichnis und alle darin enthaltenen Dateien (seine untergeordneten Elemente) zu löschen, selbst wenn die Dateien schreibgeschützt sind.

</dd> <dt>

**Datei \_ Lese \_ Attribute**
</dt> <dd>

128 (0x80)

Gewährt das Recht zum Lesen von Dateiattributen.

</dd> <dt>

**Datei \_ Schreib \_ Attribute**
</dt> <dd>

256 (0x100)

Erteilt das Recht, Dateiattribute zu ändern.

</dd> <dt>

**DELETE**
</dt> <dd>

65536 (0x10000)

Gewährt Lösch Zugriff.

</dd> <dt>

**Lese \_ Steuerelement**
</dt> <dd>

131072 (0x20000)

Gewährt Lesezugriff auf die Sicherheits Beschreibung und den Besitzer.

</dd> <dt>

**\_DAC schreiben**
</dt> <dd>

262144 (0x40000)

Gewährt Schreibzugriff auf die freigegebene Zugriffs Steuerungs Liste (DACL).

</dd> <dt>

**\_Besitzer schreiben**
</dt> <dd>

524288 (0x80000)

Weist den Schreib Besitzer zu.

</dd> <dt>

**SYNCHRONIZE**
</dt> <dd>

1048576 (0x100000)

Synchronisiert den Zugriff und ermöglicht es einem Prozess zu warten, bis ein Objekt in den signalisierten Zustand wechselt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **getaccessmask** -Methode ist eine Objektmethode und wird bei einem Vorkommen dieser Klasse verwendet.

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel wird ein Freigabe Ordner erstellt und dann der Wert der Zugriffs Maske in der Sicherheits Beschreibung abgerufen, mit der der Freigabe Ordner gesichert wird.


```VB
Const FILE_SHARE = 0
Const MAXIMUM_CONNECTIONS = 4000 
strComputer = "."

Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objNewShare = objWMIService.Get("Win32_Share")
Return = objNewShare.Create ("C:\Temp", "TestShare", FILE_SHARE, MAXIMUM_CONNECTIONS, "test share")

If Return <> 0 Then
          WScript.Echo Return
          WScript.Quit
End If

Set objShare = objWMIService.Get("Win32_Share.Name='TestShare'")
Return = objShare.GetAccessMask
WScript.Echo Return
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

[**Win32- \_ Freigabe**](win32-share.md)
</dt> </dl>

 

