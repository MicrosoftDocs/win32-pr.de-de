---
description: Dekomprimiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist. Diese Methode ist eine erweiterte Version der uncompress-Methode.
ms.assetid: 383475ba-77d4-4bfb-a241-9c37aa594a1e
ms.tgt_platform: multiple
title: UncompressEx-Methode der CIM_LogicalFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c514939425625c15f3b683e4dc10bd5e05cb511
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748936"
---
# <a name="uncompressex-method-of-the-cim_logicalfile-class"></a>UncompressEx-Methode der CIM \_ LogicalFile-Klasse

Die **UncompressEx** -Methode entkomprimiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist. Diese Methode ist eine erweiterte Version der [**uncompress**](uncompress-method-in-class-cim-logicalfile.md) -Methode.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 UncompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Stop filename* \[ vorgenommen\]
</dt> <dd>

Der Name der Datei (oder des Verzeichnisses), in der die Methode fehlgeschlagen ist. Dieser Parameter ist **null** , wenn die Methode erfolgreich ist.

</dd> <dt>

*Startdateiname* \[ in, optional\]
</dt> <dd>

Der Name der untergeordneten Datei (oder des Verzeichnisses), die als Ausgangspunkt für die Methode verwendet werden soll. In der Regel handelt es sich bei diesem Parameter um den *StopFileName* -Parameter, der die Datei oder das Verzeichnis angibt, in dem ein Fehler aus dem vorherigen Methoden aufzurufen Wenn dieser Parameter **null** ist, wird der Vorgang für die im [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) -Befehl angegebene Datei oder das Verzeichnis ausgeführt.

</dd> <dt>

*Rekursiv* \[ in, optional\]
</dt> <dd>

**True** gibt an, dass die Methode auch rekursiv auf Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**CIM \_ LogicalFile**](cim-logicalfile.md) -Instanz angegeben wird. Bei Datei Instanzen wird dieser Parameter ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.

<dl> <dt>

**Erfolgreich**
</dt> <dd>

0

Erfolg.

</dd> <dt>

**Zugriff verweigert**
</dt> <dd>

2

Zugriff verweigert.

</dd> <dt>

**Nicht spezifizierter Fehler**
</dt> <dd>

8

Nicht spezifizierter Fehler.

</dd> <dt>

**Ungültiges Objekt**
</dt> <dd>

9

Ungültiges Objekt.

</dd> <dt>

**Objekt ist bereits vorhanden.**
</dt> <dd>

10

Das Objekt ist bereits vorhanden.

</dd> <dt>

**Dateisystem nicht NTFS**
</dt> <dd>

11

Das Dateisystem ist nicht NTFS.

</dd> <dt>

**Plattform nicht NT/Windows 2000**
</dt> <dd>

12

Plattform nicht Windows.

</dd> <dt>

**Laufwerk nicht identisch**
</dt> <dd>

13

Das Laufwerk ist nicht identisch.

</dd> <dt>

**Verzeichnis nicht leer**
</dt> <dd>

14

„Verzeichnis ist nicht leer.“

</dd> <dt>

**Freigabe Verletzung**
</dt> <dd>

15

Freigabeverletzung.

</dd> <dt>

**Ungültige Startdatei**
</dt> <dd>

16

Ungültige Startdatei.

</dd> <dt>

**Berechtigung nicht aufrechterhalten**
</dt> <dd>

17

Die Berechtigung wurde nicht aufrechterhalten.

</dd> <dt>

**Ungültiger Parameter**
</dt> <dd>

21

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

[CIM \_ LogicalFile](uncompressex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[**CIM \_ LogicalFile**](cim-logicalfile.md)
</dt> </dl>

 

