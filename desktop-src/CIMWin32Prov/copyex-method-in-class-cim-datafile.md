---
description: Die CopyEx-Methode kopiert die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist, an den Speicherort, der durch den FileName-Parameter angegeben wird.
ms.assetid: e52c1a0f-e34c-4a61-9e54-ed172976cb61
ms.tgt_platform: multiple
title: CopyEx-Methode der CIM_DataFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 60d2d0e6802aac62384a9d686831867d556cdb2c4a63630199c9989a5263188a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119547480"
---
# <a name="copyex-method-of-the-cim_datafile-class"></a>CopyEx-Methode der CIM \_ DataFile-Klasse

Die **CopyEx-Methode** kopiert die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist, an den Speicherort, der durch den *FileName-Parameter* angegeben wird. Eine Kopie wird nicht unterstützt, wenn eine vorhandene logische Datei überschrieben werden muss. Diese Methode ist eine erweiterte Version der [**Copy-Methode**](copy-method-in-class-cim-datafile.md) und wird von [CIM \_ LogicalFile](cim-logicalfile.md)geerbt.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 CopyEx(
  [in]  string     FileName,
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
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

*StartFileName* \[ In\]
</dt> <dd>

Zeichenfolge, die die untergeordnete Datei (oder das Verzeichnis) darstellt, die als Ausgangspunkt für diese Methode verwendet werden soll. In der Regel ist der *StartFileName-Parameter* der *StopFileName-Parameter,* der die Datei (oder das Verzeichnis) angibt, bei der beim vorherigen Methodenaufruf ein Fehler aufgetreten ist. Wenn dieser Parameter **NULL** ist, wird der Vorgang für die Datei (oder das Verzeichnis) ausgeführt, die im [**ExecMethod-Aufruf**](/windows/desktop/WmiSdk/swbemservices-execmethod) angegeben ist.

Wenn *StartFileName* verwendet wird, muss *Recursive* auch auf TRUE festgelegt werden.

</dd> <dt>

*Rekursiv* \[ In\]
</dt> <dd>

True gibt an, dass die Methode auch rekursiv auf Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**CIM \_ DataFile-Instanz**](cim-datafile.md) angegeben wird. Bei Dateiinstanzen wird dieser Parameter ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Wert 0 (null) und eine beliebige andere Zahl zurück, um einen Fehler anzugeben. Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes.](/windows/desktop/Debug/system-error-codes)

<dl> <dt>


</dt> <dd>

0

Erfolg.

</dd> <dt>


</dt> <dd>

2

Zugriff verweigert:

</dd> <dt>


</dt> <dd>

8

Nicht angegebener Fehler.

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

Dateisystem nicht NTFS.

</dd> <dt>


</dt> <dd>

12

Plattform nicht Windows.

</dd> <dt>


</dt> <dd>

13

Laufwerk nicht identisch.

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

Die Berechtigung wurde nicht gehalten.

</dd> <dt>


</dt> <dd>

21

Ungültiger Parameter.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **CopyEx-Methode** in [**CIM \_ DataFile**](cim-datafile.md) wird von WMI implementiert.

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

[**CIM \_ DataFile**](cim-datafile.md)
</dt> <dt>

[WMI-Aufgaben: Dateien und Ordner](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[**Datei- und Verzeichniszugriffsrechtekonstanten**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

