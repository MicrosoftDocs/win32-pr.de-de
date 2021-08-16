---
description: Erhält den Besitz der logischen Datendatei, die im Objektpfad angegeben ist. Diese Methode ist eine erweiterte Version der TakeOwnerShip-Methode und wird von CIM \_ LogicalFile geerbt.
ms.assetid: 3bc5a060-d805-46f6-802d-9ed16b52da59
ms.tgt_platform: multiple
title: TakeOwnerShipEx-Methode der CIM_DataFile Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: baf0ffe9d9eb961d07731ee9967b32e940dbdb3231935588387972433c61aa74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117834586"
---
# <a name="takeownershipex-method-of-the-cim_datafile-class"></a>TakeOwnerShipEx-Methode der CIM \_ DataFile-Klasse

Die **TakeOwnerShipEx-Methode** erhält den Besitz der logischen Datendatei, die im Objektpfad angegeben ist. Diese Methode ist eine erweiterte Version der [**TakeOwnerShip-Methode**](takeownership-method-in-class-cim-datafile.md) und wird von [**CIM \_ LogicalFile geerbt.**](cim-logicalfile.md) Wenn es sich bei der logischen Datei um ein Verzeichnis handelt, wird diese Methode rekursiv und übernimmt den Besitz aller Dateien und Unterverzeichnisse, die das Verzeichnis enthält.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 TakeOwnerShipEx(
  [out] string  StopFileName,
  [in]  string  StartFileName,
  [in]  boolean Recursive
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*StopFileName* \[ out\]
</dt> <dd>

Name der Datei (oder des Verzeichnisses), in der bzw. dem die Methode fehlgeschlagen ist. Dieser Parameter ist NULL, wenn die Methode erfolgreich ist.

</dd> <dt>

*StartFileName* \[ In\]
</dt> <dd>

Untergeordnete Datei (oder Verzeichnis), die als Ausgangspunkt für diese Methode verwendet werden soll. In der Regel ist der *StartFileName-Parameter* der *StopFileName-Parameter,* der die Datei (oder das Verzeichnis) angibt, in der beim vorherigen Methodenaufruf ein Fehler aufgetreten ist. Wenn dieser Parameter NULL ist, wird der Vorgang für die Datei (oder das Verzeichnis) ausgeführt, die im [**ExecMethod-Aufruf angegeben**](/windows/desktop/WmiSdk/swbemservices-execmethod) ist.

Wenn *StartFileName* verwendet wird, *muss Recursive* auch auf TRUE festgelegt werden.

</dd> <dt>

*Rekursiv* \[ In\]
</dt> <dd>

True **gibt** an, dass die -Methode auch rekursiv auf Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**CIM \_ DataFile-Instanz angegeben**](cim-datafile.md) wird. Bei Dateiinstanzen wird dieser Parameter ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Wert 0 (null) und eine beliebige andere Zahl zurück, um einen Fehler anzugeben. Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstistenzen**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**0**
</dt> <dd>

Erfolg.

</dd> <dt>

**2**
</dt> <dd>

Zugriff verweigert:

</dd> <dt>

**8**
</dt> <dd>

Nicht angegebener Fehler.

</dd> <dt>

**9**
</dt> <dd>

Ungültiges Objekt.

</dd> <dt>

**10**
</dt> <dd>

Das Objekt ist bereits vorhanden.

</dd> <dt>

**11**
</dt> <dd>

Dateisystem, nicht NTFS.

</dd> <dt>

**12**
</dt> <dd>

Plattform nicht Windows.

</dd> <dt>

**13**
</dt> <dd>

Laufwerk nicht identisch.

</dd> <dt>

**14**
</dt> <dd>

„Verzeichnis ist nicht leer.“

</dd> <dt>

**15**
</dt> <dd>

Freigabeverletzung.

</dd> <dt>

**16**
</dt> <dd>

Ungültige Startdatei.

</dd> <dt>

**17**
</dt> <dd>

Die Berechtigung wurde nicht gehalten.

</dd> <dt>

**21**
</dt> <dd>

Ungültiger Parameter.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **TakeOwnerShipEx-Methode** in [**CIM \_ DataFile**](cim-datafile.md) wird von WMI implementiert.

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von DMTF veröffentlicht wurden. Microsoft hat möglicherweise Änderungen vorgenommen, um kleinere Fehler zu beheben, die Dokumentationsstandards des Microsoft SDK zu erfüllen oder weitere Informationen zur Verfügung zu stellen.

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

[CIM \_ DataFile](takeownershipex-method-in-class-cim-datafile.md)
</dt> <dt>

[**CIM \_ DataFile**](cim-datafile.md)
</dt> <dt>

[WMI-Aufgaben: Dateien und Ordner](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[**Konstanten für Datei- und Verzeichniszugriffsrechte**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

