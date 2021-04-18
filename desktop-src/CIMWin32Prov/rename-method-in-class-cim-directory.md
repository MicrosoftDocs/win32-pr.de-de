---
description: Benennt die logische Datei (oder das Verzeichnis) um, die im Objekt Pfad angegeben ist. Das Umbenennen wird nicht unterstützt, wenn sich das Ziel auf einem anderen Laufwerk befindet oder wenn eine vorhandene logische Datei überschrieben werden muss.
ms.assetid: 728737a7-7cb8-4237-be03-16c4dac530b2
ms.tgt_platform: multiple
title: Rename-Methode der CIM_Directory-Klasse
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
ms.openlocfilehash: 83429f3a5248b1d3be24832b26bf99213d442ce5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483731"
---
# <a name="rename-method-of-the-cim_directory-class"></a>Rename-Methode der CIM- \_ Verzeichnis Klasse

Die **Rename** -Methode benennt die logische Datei (oder das Verzeichnis) um, die im Objekt Pfad angegeben ist. Das Umbenennen wird nicht unterstützt, wenn sich das Ziel auf einem anderen Laufwerk befindet oder wenn eine vorhandene logische Datei überschrieben werden muss.

Diese Methode wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 Rename(
  [in] string FileName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dateiname* \[ in\]
</dt> <dd>

Voll qualifizierter neuer Name der Datei (oder des Verzeichnisses).

Beispiel: "c: \\ Temp \\newname.txt"

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.

<dl> <dt>

**0**
</dt> <dd>

Erfolg.

</dd> <dt>

**2**
</dt> <dd>

Zugriff verweigert.

</dd> <dt>

**8**
</dt> <dd>

Nicht spezifizierter Fehler.

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

Das Dateisystem ist nicht NTFS.

</dd> <dt>

**12**
</dt> <dd>

Plattform nicht Windows.

</dd> <dt>

**13**
</dt> <dd>

Das Laufwerk ist nicht identisch.

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

Die Berechtigung wurde nicht aufrechterhalten.

</dd> <dt>

**21**
</dt> <dd>

Ungültiger Parameter.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Methode wird zurzeit nicht von WMI implementiert. Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.

Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet. Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.

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

[CIM- \_ Verzeichnis](rename-method-in-class-cim-directory.md)
</dt> <dt>

[**CIM- \_ Verzeichnis**](cim-directory.md)
</dt> </dl>

 

