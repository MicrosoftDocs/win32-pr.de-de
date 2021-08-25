---
description: 'GetAccessMask-Methode der Win32_Share-Klasse: Gibt eine uint32-Bitmap mit den Zugriffsrechten für die Freigabe zurück, die vom Benutzer oder der Gruppe gehalten wird, in dessen Auftrag die Instanz zurückgegeben wird.'
ms.assetid: 234f44a4-ffff-431d-a973-98f2bd313c7d
ms.tgt_platform: multiple
title: GetAccessMask-Methode der Win32_Share-Klasse
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
ms.openlocfilehash: ebc2b2620b0bdc019e117f9a4b2c376be6320be968fdae42509dc3f62c3cc9a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077660"
---
# <a name="getaccessmask-method-of-the-win32_share-class"></a>GetAccessMask-Methode der Win32 \_ Share-Klasse

Die **GetAccessMask-Methode** gibt eine uint32-Bitmap mit den Zugriffsrechten auf die Freigabe zurück, die vom Benutzer oder der Gruppe, in dessen Auftrag die Instanz zurückgegeben wird, gehalten wird.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 GetAccessMask();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Zugriffsrechte für die Freigabe, die vom Benutzer oder der Gruppe gehalten wird.

<dl> <dt>

**\_ \_ DATEILISTENVERZEICHNIS**
</dt> <dd>

1 (0x1)

Gewährt das Recht, Daten aus der Datei zu lesen. Für ein Verzeichnis gewährt dieser Wert das Recht, den Inhalt des Verzeichnisses aufzulisten.

</dd> <dt>

**FILE \_ ADD \_ FILE**
</dt> <dd>

2 (0x2)

Gewährt das Recht, Daten in die Datei zu schreiben. Bei einem Verzeichnis gewährt dieser Wert das Recht, eine Datei im Verzeichnis zu erstellen.

</dd> <dt>

**FILE \_ ADD \_ SUBDIRECTORY**
</dt> <dd>

4 (0x4)

Gewährt das Recht, Daten an die Datei anzufügen. Für ein Verzeichnis gewährt dieser Wert das Recht, ein Unterverzeichnis zu erstellen.

</dd> <dt>

**FILE \_ READ \_ EA**
</dt> <dd>

8 (0x8)

Gewährt das Recht, erweiterte Attribute zu lesen.

</dd> <dt>

**FILE \_ WRITE \_ EA**
</dt> <dd>

16 (0x10)

Gewährt das Recht, erweiterte Attribute zu schreiben.

</dd> <dt>

**FILE \_ TRAVERSE**
</dt> <dd>

32 (0x20)

Gewährt das Recht zum Ausführen einer Datei. Für ein Verzeichnis kann das Verzeichnis durchlaufen werden.

</dd> <dt>

**UNTERGEORDNETE \_ \_ DATEILÖSCHUNG**
</dt> <dd>

64 (0x40)

Gewährt das Recht, ein Verzeichnis und alle darin enthaltenen Dateien (seine untergeordneten Dateien) zu löschen, auch wenn die Dateien schreibgeschützt sind.

</dd> <dt>

**\_ \_ DATEILESEATTRIBUTE**
</dt> <dd>

128 (0x80)

Gewährt das Recht zum Lesen von Dateiattributen.

</dd> <dt>

**\_ \_ DATEISCHREIBATTRIBUTE**
</dt> <dd>

256 (0x100)

Gewährt das Recht, Dateiattribute zu ändern.

</dd> <dt>

**DELETE**
</dt> <dd>

65536 (0x10000)

Gewährt Löschzugriff.

</dd> <dt>

**\_READ-STEUERELEMENT**
</dt> <dd>

131072 (0x20000)

Gewährt Lesezugriff auf den Sicherheitsdeskriptor und den Besitzer.

</dd> <dt>

**\_SCHREIB-DAC**
</dt> <dd>

262144 (0x40000)

Gewährt Schreibzugriff auf die DACL (Discretionary Access Control List).

</dd> <dt>

**WRITE \_ OWNER**
</dt> <dd>

524288 (0x80000)

Weist den Schreibbesitzer zu.

</dd> <dt>

**Synchronisieren**
</dt> <dd>

1048576 (0x100000)

Synchronisiert den Zugriff und ermöglicht einem Prozess, auf den Eintritt eines Objekts in den signalisierten Zustand zu warten.

</dd> </dl>

## <a name="remarks"></a>Hinweise

**Die GetAccessMask-Methode** ist eine Objektmethode und wird bei einem Vorkommen dieser Klasse verwendet.

## <a name="examples"></a>Beispiele

Das folgende VBScript-Codebeispiel erstellt einen Freigabeordner und ruft dann den Wert der Zugriffsmaske in der Sicherheitsbeschreibung ab, die den Freigabeordner sichert.


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
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_Win32-Freigabe**](win32-share.md)
</dt> </dl>

 

