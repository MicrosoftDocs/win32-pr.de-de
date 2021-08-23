---
description: Komprimiert die logische Verknüpfungsdatei (oder das Verzeichnis), die im Objektpfad angegeben ist (diese Methode ist eine erweiterte Version der Compress-Methode).
ms.assetid: 1f7b6182-6ab7-4801-83a8-b57b1c78001f
ms.tgt_platform: multiple
title: CompressEx-Methode der Win32_ShortcutFile Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 71302c86cdf1928bdc451a3062c20885bb808dbc60c8c7ede70314b5aa01ba2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119505090"
---
# <a name="compressex-method-of-the-win32_shortcutfile-class"></a>CompressEx-Methode der Win32 \_ ShortcutFile-Klasse

Die **CompressEx** [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) komprimiert die logische Verknüpfungsdatei (oder das Verzeichnis), die im Objektpfad angegeben ist (diese Methode ist eine erweiterte Version der [**Compress-Methode).**](compress-method-in-class-win32-directory.md)

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 CompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*StopFileName* \[ out\]
</dt> <dd>

Name der Datei oder des Verzeichnisses, in der bzw. dem die [**CompressEx-Methode**](compressex-method-in-class-win32-directory.md) fehlgeschlagen ist. Dieser Parameter ist **NULL,** wenn die Methode erfolgreich ist.

</dd> <dt>

*StartFileName* \[ in, optional\]
</dt> <dd>

Benennt die untergeordnete Datei oder das untergeordnete Verzeichnis, die bzw. das als Ausgangspunkt für [**CompressEx verwendet werden soll.**](compressex-method-in-class-win32-directory.md) Der *StartFileName-Parameter* ist in der Regel der *StopFileName-Parameter,* der die Datei oder das Verzeichnis angibt, in der bzw. dem beim vorherigen Methodenaufruf ein Fehler aufgetreten ist. Wenn dieser Parameter **NULL ist,** wird der Vorgang für die Datei oder das Verzeichnis ausgeführt, die bzw. das **im ExecMethod-Aufruf angegeben** ist.

</dd> <dt>

*Rekursiv* \[ in, optional\]
</dt> <dd>

True **gibt an,** dass die Besitzänderung rekursiv auf Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**CIM \_ LogicalFile-Instanz angegeben**](cim-logicalfile.md) wird.

> [!Note]  
> Bei Dateiinstanzen wird *der Rekursive -Parameter* ignoriert.

 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert 0 (null) zurück, wenn die Datei erfolgreich komprimiert wurde, und eine beliebige andere Zahl, um einen Fehler anzugeben.

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

[**Win32 \_ ShortcutFile**](win32-shortcutfile.md)
</dt> </dl>

 

