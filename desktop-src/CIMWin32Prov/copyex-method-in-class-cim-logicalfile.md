---
description: Kopiert die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist, an den Speicherort, der durch den FileName-Parameter angegeben wird.
ms.assetid: 534d8b73-fc22-4a42-b8e6-24a54353bb14
ms.tgt_platform: multiple
title: CopyEx-Methode der CIM_LogicalFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e63c4b588c4ff4c22bf0d1e8998163884634e4545537de3c275503652dbb81c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003870"
---
# <a name="copyex-method-of-the-cim_logicalfile-class"></a>CopyEx-Methode der CIM \_ LogicalFile-Klasse

Die **CopyEx-Methode** kopiert die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist, an den Speicherort, der durch den *FileName-Parameter* angegeben wird. Eine Kopie wird nicht unterstützt, wenn das Überschreiben einer vorhandenen logischen Datei erforderlich ist. Diese Methode ist eine erweiterte Version der [**Copy-Methode.**](copy-method-in-class-cim-logicalfile.md)

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 CopyEx(
  [in]           string  FileName,
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FileName* \[ In\]
</dt> <dd>

Vollqualifizierte Name der Zieldatei (oder des Verzeichnisses).

Beispiel: "c: \\ temp \\ newdirectory"

</dd> <dt>

*StopFileName* \[ out\]
</dt> <dd>

Zeichenfolge, die den Namen der Datei (oder des Verzeichnisses) darstellt, in der die Methode fehlgeschlagen ist. Dieser Parameter ist **NULL,** wenn die Methode erfolgreich ist.

</dd> <dt>

*StartFileName* \[ in, optional\]
</dt> <dd>

Zeichenfolge, die die untergeordnete Datei (oder das Verzeichnis) benennt, die als Ausgangspunkt für diese Methode verwendet werden soll. In der Regel ist der *StartFileName-Parameter* der *StopFileName-Parameter,* der die Datei (oder das Verzeichnis) angibt, bei der beim vorherigen Methodenaufruf ein Fehler aufgetreten ist. Wenn dieser Parameter **NULL** ist, wird der Vorgang für die Datei oder das Verzeichnis ausgeführt, die bzw. das im [**ExecMethod-Aufruf**](/windows/desktop/WmiSdk/swbemservices-execmethod) angegeben ist.

</dd> <dt>

*Rekursiv* \[ in, optional\]
</dt> <dd>

True gibt an, dass die Methode auch rekursiv auf Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**\_ CIM LogicalFile-Instanz**](cim-logicalfile.md) angegeben wird. Bei Dateiinstanzen wird dieser Parameter ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Wert 0 (null) und eine beliebige andere Zahl zurück, um einen Fehler anzugeben.

<dl> <dt>

**Erfolgreich**
</dt> <dd>

0

Erfolg.

</dd> <dt>

**Zugriff verweigert**
</dt> <dd>

2

Zugriff verweigert:

</dd> <dt>

**Nicht angegebener Fehler**
</dt> <dd>

8

Nicht angegebener Fehler.

</dd> <dt>

**Ungültiges Objekt**
</dt> <dd>

9

Ungültiges Objekt.

</dd> <dt>

**Objekt ist bereits vorhanden**
</dt> <dd>

10

Das Objekt ist bereits vorhanden.

</dd> <dt>

**Dateisystem nicht NTFS**
</dt> <dd>

11

Dateisystem nicht NTFS.

</dd> <dt>

**Plattform nicht NT/Windows 2000**
</dt> <dd>

12

Plattform nicht Windows.

</dd> <dt>

**Laufwerk nicht identisch**
</dt> <dd>

13

Laufwerk nicht identisch.

</dd> <dt>

**Verzeichnis nicht leer**
</dt> <dd>

14

„Verzeichnis ist nicht leer.“

</dd> <dt>

**Verletzung der Freigabe**
</dt> <dd>

15

Freigabeverletzung.

</dd> <dt>

**Ungültige Startdatei**
</dt> <dd>

16

Ungültige Startdatei.

</dd> <dt>

**Berechtigung nicht gehalten**
</dt> <dd>

17

Die Berechtigung wurde nicht gehalten.

</dd> <dt>

**Ungültiger Parameter**
</dt> <dd>

21

Ungültiger Parameter.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Methode wird derzeit nicht von WMI implementiert. Um diese Methode zu verwenden, müssen Sie sie in Ihrem eigenen Anbieter implementieren.

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

[CIM \_ LogicalFile](copyex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[**CIM \_ LogicalFile**](cim-logicalfile.md)
</dt> </dl>

 

