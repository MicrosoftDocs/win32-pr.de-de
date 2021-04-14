---
description: Die Methode "Take Ownership" der WMI-Klasse ruft den Besitz der logischen Datei ab, die im Objekt Pfad angegeben ist.
ms.assetid: 1112823b-0bb6-4dc0-a5c4-8d3839a47a3a
ms.tgt_platform: multiple
title: TakeOwnership-Methode der Win32_Directory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c06441b7728ed8b9178e889cbd60c047f0f3a497
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523011"
---
# <a name="takeownership-method-of-the-win32_directory-class"></a>TakeOwnership-Methode der Win32- \_ Verzeichnis Klasse

Die Methode " **Take Ownership** " der [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) Ruft den Besitz der logischen Datei ab, die im Objekt Pfad angegeben ist. Wenn die logische Datei tatsächlich ein Verzeichnis ist, wird der **Take Ownership** rekursiv durchlaufen und übernimmt den Besitz aller Dateien und Unterverzeichnisse, die das Verzeichnis enthält.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden Werte zurück.

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

## <a name="examples"></a>Beispiele

Der folgende Visual Basic Skriptcode Ruft die [**TakeOwnership**](takeownership-method-in-class-cim-directory.md) -Methode auf, um den Besitz des Ordners "C: Temp" zu übernehmen \\ .


```VB
strComputer = "." 

Set objWMIService = _
    GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 

' Obtain the definition of the class.
Set objShare = objWMIService.Get("Win32_Directory")

' Execute the method and obtain the return status.
' The OutParameters object in objOutParams
' is created by the provider.
Set objOutParams = objWMIService.ExecMethod( _
    "Win32_Directory.Name='C:\\temp'", "TakeOwnerShip")

wscript.echo objOutParams.ReturnValue
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

 

