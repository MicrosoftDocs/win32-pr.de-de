---
description: Entpackt die logische Datendatei (oder das Verzeichnis), die im Objektpfad angegeben ist. Diese Methode wird von CIM \_ LogicalFile geerbt.
ms.assetid: 0966ba13-8bbc-4283-919a-7675444409be
ms.tgt_platform: multiple
title: Uncompress-Methode der CIM_DataFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.Uncompress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c5d2f1a475800506dadc8929079ecb2549d59bfd838f340c56e5f763aa9af24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002890"
---
# <a name="uncompress-method-of-the-cim_datafile-class"></a>Uncompress-Methode der CIM \_ DataFile-Klasse

Die **Uncompress-Methode** entpackt die logische Datendatei (oder das Verzeichnis), die im Objektpfad angegeben ist. Diese Methode wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 Uncompress();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Wert 0 (null) und eine beliebige andere Zahl zurück, um einen Fehler anzugeben. Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes.](/windows/desktop/Debug/system-error-codes)

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

Dateisystem nicht NTFS.

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

Die **Uncompress-Methode** in [**CIM \_ DataFile**](cim-datafile.md) wird von WMI implementiert.

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von dmtf veröffentlicht wurden. Möglicherweise hat Microsoft Änderungen vorgenommen, um kleinere Fehler zu korrigieren, den Dokumentationsstandards des Microsoft SDK zu entsprechen oder weitere Informationen bereitzustellen.

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

[**CIM \_ DataFile**](uncompress-method-in-class-cim-datafile.md)
</dt> <dt>

[**CIM \_ DataFile**](cim-datafile.md)
</dt> <dt>

[WMI-Aufgaben: Dateien und Ordner](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[**Datei- und Verzeichniszugriffsrechtekonstanten**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

