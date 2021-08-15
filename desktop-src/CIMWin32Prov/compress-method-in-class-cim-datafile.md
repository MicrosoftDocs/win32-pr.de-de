---
description: 'Compress-Methode der CIM_DataFile Klasse: Verwendet die NTFS-Komprimierung, um die logische Datei (oder das Verzeichnis) zu komprimieren, die im Objektpfad angegeben ist. Diese Methode wird von CIM \_ LogicalFile geerbt.'
ms.assetid: fce57569-8290-420e-a938-10ab08ac67c3
ms.tgt_platform: multiple
title: Compress-Methode der CIM_DataFile Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 61da18a85935c2c7e7b9ff246347c7a52059f78900b5a7b7b51c76f09780b955
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118420320"
---
# <a name="compress-method-of-the-cim_datafile-class"></a>Compress-Methode der CIM \_ DataFile-Klasse

Die **Compress-Methode** verwendet die NTFS-Komprimierung, um die logische Datei (oder das Verzeichnis) zu komprimieren, die im Objektpfad angegeben ist. Diese Methode wird von [**CIM \_ LogicalFile geerbt.**](cim-logicalfile.md)

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 Compress();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

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

Die **Compress-Methode** in [**CIM \_ DataFile**](cim-datafile.md) wird von WMI implementiert.

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

[**CIM \_ DataFile**](compress-method-in-class-cim-datafile.md)
</dt> <dt>

[**CIM \_ DataFile**](cim-datafile.md)
</dt> <dt>

[WMI-Aufgaben: Dateien und Ordner](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[**Konstanten für Datei- und Verzeichniszugriffsrechte**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

