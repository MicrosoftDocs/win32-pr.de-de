---
description: Benennt die logische Datei (oder das Verzeichnis) um, die im Objektpfad angegeben ist. Das Umbenennen wird nicht unterstützt, wenn sich das Ziel auf einem anderen Laufwerk befindet oder das Überschreiben einer vorhandenen logischen Datei erforderlich ist.
ms.assetid: 728737a7-7cb8-4237-be03-16c4dac530b2
ms.tgt_platform: multiple
title: Umbenennen der CIM_Directory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b9236b3384b8d945cea41c1a1fbe7b8db22f7ed70d692144e1691c6bfcf97270
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077480"
---
# <a name="rename-method-of-the-cim_directory-class"></a>Rename-Methode der CIM \_ Directory-Klasse

Die **Rename-Methode** benennt die logische Datei (oder das Verzeichnis) um, die im Objektpfad angegeben ist. Das Umbenennen wird nicht unterstützt, wenn sich das Ziel auf einem anderen Laufwerk befindet oder das Überschreiben einer vorhandenen logischen Datei erforderlich ist.

Diese Methode wird von [**CIM \_ LogicalFile geerbt.**](cim-logicalfile.md)

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 Rename(
  [in] string FileName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FileName* \[ In\]
</dt> <dd>

Vollqualifizierter neuer Name der Datei (oder des Verzeichnisses).

Beispiel: "c: \\ temp \\newname.txt"

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Wert 0 (null) und eine beliebige andere Zahl zurück, um einen Fehler anzugeben.

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

Diese Methode wird derzeit nicht von WMI implementiert. Um diese Methode zu verwenden, müssen Sie sie in Ihrem eigenen Anbieter implementieren.

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von DMTF veröffentlicht wurden. Microsoft hat möglicherweise Änderungen vorgenommen, um kleinere Fehler zu beheben, die Dokumentationsstandards des Microsoft SDK zu erfüllen oder weitere Informationen zur Verfügung zu stellen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[\_CIM-Verzeichnis](rename-method-in-class-cim-directory.md)
</dt> <dt>

[**\_CIM-Verzeichnis**](cim-directory.md)
</dt> </dl>

 

