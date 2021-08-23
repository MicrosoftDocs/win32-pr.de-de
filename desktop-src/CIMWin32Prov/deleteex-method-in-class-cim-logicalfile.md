---
description: Die DeleteEx-Methode löscht die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist. Diese Methode ist eine erweiterte Version der Delete-Methode.
ms.assetid: 53785f2e-8796-446c-8228-9abc2d9a0d68
ms.tgt_platform: multiple
title: DeleteEx-Methode der CIM_LogicalFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 715e7bbe0b6346ff6e00cc9812e9a154debe10ac8315ab74f67471ff4c1658e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119080094"
---
# <a name="deleteex-method-of-the-cim_logicalfile-class"></a>DeleteEx-Methode der \_ CIM LogicalFile-Klasse

Die **DeleteEx-Methode** löscht die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist. Diese Methode ist eine erweiterte Version der [**Delete-Methode.**](delete-method-in-class-cim-logicalfile.md)

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 DeleteEx(
  [out]          string StopFileName,
  [in, optional] string StartFileName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*StopFileName* \[ out\]
</dt> <dd>

Zeichenfolge, die den Namen der Datei (oder des Verzeichnisses) darstellt, in der die Methode fehlgeschlagen ist. Dieser Parameter ist NULL, wenn die Methode erfolgreich ist.

</dd> <dt>

*StartFileName* \[ in, optional\]
</dt> <dd>

Zeichenfolge, die die untergeordnete Datei (oder das Verzeichnis) benennt, die als Ausgangspunkt für die Methode verwendet werden soll. In der Regel ist dieser Parameter der *StopFileName-Parameter,* der die Datei oder das Verzeichnis angibt, bei der beim vorherigen Methodenaufruf ein Fehler aufgetreten ist. Wenn dieser Parameter NULL ist, wird der Vorgang für die Datei oder das Verzeichnis ausgeführt, die bzw. das im [**ExecMethod-Aufruf**](/windows/desktop/WmiSdk/swbemservices-execmethod) angegeben ist.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[CIM \_ LogicalFile](deleteex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[**CIM \_ LogicalFile**](cim-logicalfile.md)
</dt> </dl>

 

