---
description: Die DeleteEx-Methode löscht die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist. Diese Methode ist eine erweiterte Version der Delete-Methode und wird von CIM \_ LogicalFile geerbt.
ms.assetid: 565d604f-01e0-4cd4-b182-9750c58bae5f
ms.tgt_platform: multiple
title: DeleteEx-Methode der CIM_DataFile Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1e52a1d974afdc123e79f85252a68c52aa99e7e78a2b997b6eca1f1bced60997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020508"
---
# <a name="deleteex-method-of-the-cim_datafile-class"></a>DeleteEx-Methode der CIM \_ DataFile-Klasse

Die **DeleteEx-Methode** löscht die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist. Diese Methode ist eine erweiterte Version der [**Delete-Methode**](delete-method-in-class-cim-datafile.md) und wird von [**CIM \_ LogicalFile geerbt.**](cim-logicalfile.md)

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 DeleteEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*StopFileName* \[ out\]
</dt> <dd>

Eine Zeichenfolge, die den Namen der Datei (oder des Verzeichnisses) darstellt, in der bzw. dem die Methode fehlgeschlagen ist. Dieser Parameter ist NULL, wenn die Methode erfolgreich ist.

</dd> <dt>

*StartFileName* \[ In\]
</dt> <dd>

Eine Zeichenfolge, die die untergeordnete Datei (oder das Verzeichnis) darstellt, die als Ausgangspunkt für diese Methode verwendet werden soll. In der Regel ist der *StartFileName-Parameter* der *StopFileName-Parameter,* der die Datei oder das Verzeichnis angibt, in der bzw. dem beim vorherigen Methodenaufruf ein Fehler aufgetreten ist. Wenn dieser Parameter NULL ist, wird der Vorgang für die Datei (oder das Verzeichnis) ausgeführt, die im [**ExecMethod-Aufruf angegeben**](/windows/desktop/WmiSdk/swbemservices-execmethod) ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Wert 0 (null) und eine beliebige andere Zahl zurück, um einen Fehler anzugeben. Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstistenzen**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes](/windows/desktop/Debug/system-error-codes).

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

Dateisystem, nicht NTFS.

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

Die **DeleteEx-Methode** in [**CIM \_ DataFile**](cim-datafile.md) wird von WMI implementiert.

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von DMTF veröffentlicht wurden. Microsoft hat möglicherweise Änderungen vorgenommen, um kleinere Fehler zu beheben, die Dokumentationsstandards des Microsoft SDK zu erfüllen oder weitere Informationen zur Verfügung zu stellen.

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

[CIM \_ DataFile](deleteex-method-in-class-cim-datafile.md)
</dt> <dt>

[**CIM \_ DataFile**](cim-datafile.md)
</dt> <dt>

[WMI-Aufgaben: Dateien und Ordner](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[**Konstanten für Datei- und Verzeichniszugriffsrechte**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

