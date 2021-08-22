---
description: Ruft den Besitz der logischen Codecdatei ab, die im Objektpfad angegeben ist. Diese Methode ist eine erweiterte Version der TakeOwnerShip-Methode.
ms.assetid: 8f3b495a-f654-4818-b0ea-dc88819d72af
ms.tgt_platform: multiple
title: TakeOwnerShipEx-Methode der Win32_CodecFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 04af6ed0953f25c5b02e988569eecad806ae62cb4757463831132e3c22dd40b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119546640"
---
# <a name="takeownershipex-method-of-the-win32_codecfile-class"></a>TakeOwnerShipEx-Methode der Win32 \_ CodecFile-Klasse

Die [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnerShipEx** ruft den Besitz der logischen Codecdatei ab, die im Objektpfad angegeben ist. Diese Methode ist eine erweiterte Version der [**TakeOwnerShip-Methode.**](takeownership-method-in-class-win32-directory.md) Wenn die logische Datei tatsächlich ein Verzeichnis ist, verhält sich diese Methode rekursiv und übernimmt den Besitz aller Dateien und Unterverzeichnisse, die das Verzeichnis enthält.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 TakeOwnerShipEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*StopFileName* \[ out\]
</dt> <dd>

Name der Datei oder des Verzeichnisses, in der die **TakeOwnerShipEx-Methode** fehlgeschlagen ist. Dieser Parameter ist **NULL,** wenn die Methode erfolgreich ist.

</dd> <dt>

*StartFileName* \[ in, optional\]
</dt> <dd>

Benennt die untergeordnete Datei oder das Verzeichnis, die bzw. das als Ausgangspunkt für **TakeOwnerShipEx** verwendet werden soll. Der *StartFileName-Parameter* ist in der Regel der *StopFileName-Parameter,* der die Datei oder das Verzeichnis angibt, bei der beim vorherigen Methodenaufruf ein Fehler aufgetreten ist. Wenn dieser Parameter **NULL** ist, wird der Vorgang für die Datei oder das Verzeichnis ausgeführt, die bzw. das im **ExecMethod-Aufruf** angegeben ist.

</dd> <dt>

*Rekursiv* \[ in, optional\]
</dt> <dd>

True gibt an, dass die Besitzänderung rekursiv auf Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**CIM \_ LogicalFile-Instanz**](cim-logicalfile.md) angegeben wird. Hinweis: Bei Dateiinstanzen wird der *Rekursive* Eingabeparameter ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen ganzzahligen Wert von 0 (null) und eine beliebige andere Zahl zurück, um einen Fehler anzugeben.

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

[**Win32 \_ CodecFile**](win32-codecfile.md)
</dt> </dl>

 

