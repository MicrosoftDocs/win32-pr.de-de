---
description: Die im Objekt Pfad angegebene Datei (oder das Verzeichnis) des logischen Geräts wird von unkomprimiert. Diese Methode ist eine erweiterte Version der uncompress-Methode. Diese Methode wird von CIM \_ LogicalFile geerbt.
ms.assetid: dfa53b75-56ef-4119-83b9-08b4371762c6
ms.tgt_platform: multiple
title: UncompressEx-Methode der CIM_DeviceFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a760c31a2067c294ffb43064402ac179c5fba7c9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524128"
---
# <a name="uncompressex-method-of-the-cim_devicefile-class"></a>UncompressEx-Methode der CIM \_ Devicefile-Klasse

Durch die **UncompressEx** -Methode wird die im Objekt Pfad angegebene Datei (oder das Verzeichnis) für das logische Gerät unkomprimiert. Diese Methode ist eine erweiterte Version der [**uncompress**](uncompress-method-in-class-cim-devicefile.md) -Methode. Diese Methode wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 UncompressEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Stop filename* \[ vorgenommen\]
</dt> <dd>

Eine Zeichenfolge, die den Namen der Datei (oder des Verzeichnisses) darstellt, in der die Methode fehlgeschlagen ist. Dieser Parameter ist **null** , wenn die Methode erfolgreich ist.

</dd> <dt>

*Startdateiname* \[ in\]
</dt> <dd>

Eine Zeichenfolge, die die untergeordnete Datei (oder das Verzeichnis) darstellt, die als Ausgangspunkt für die Methode verwendet werden soll. In der Regel ist der Parameter " *StartFileName* " der Parameter " *StopFileName* ", der die Datei oder das Verzeichnis angibt, in dem ein Fehler im vorherigen Methoden aufrufstyp aufgetreten Wenn dieser Parameter **null** ist, wird der Vorgang für die im [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) -Befehl angegebene Datei oder das Verzeichnis ausgeführt.

</dd> <dt>

*Rekursiv* \[ in\]
</dt> <dd>

**True** gibt an, dass diese Methode auch rekursiv auf Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**CIM \_ Devicefile**](cim-devicefile.md) -Instanz angegeben wird. Bei Datei Instanzen wird dieser Parameter ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Wert 0 zurück, und jede andere Zahl gibt einen Fehler an.

<dl> <dt>


</dt> <dd>

0

Erfolg.

</dd> <dt>


</dt> <dd>

2

Zugriff verweigert.

</dd> <dt>


</dt> <dd>

8

Nicht spezifizierter Fehler.

</dd> <dt>


</dt> <dd>

9

Ungültiges Objekt.

</dd> <dt>


</dt> <dd>

10

Das Objekt ist bereits vorhanden.

</dd> <dt>


</dt> <dd>

11

Das Dateisystem ist nicht NTFS.

</dd> <dt>


</dt> <dd>

12

Plattform nicht Windows.

</dd> <dt>


</dt> <dd>

13

Das Laufwerk ist nicht identisch.

</dd> <dt>


</dt> <dd>

14

„Verzeichnis ist nicht leer.“

</dd> <dt>


</dt> <dd>

15

Freigabeverletzung.

</dd> <dt>


</dt> <dd>

16

Ungültige Startdatei.

</dd> <dt>


</dt> <dd>

17

Die Berechtigung wurde nicht aufrechterhalten.

</dd> <dt>


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

[CIM- \_ Devicefile](uncompressex-method-in-class-cim-devicefile.md)
</dt> <dt>

[**CIM- \_ Devicefile**](cim-devicefile.md)
</dt> </dl>

 

