---
description: Die DeleteEx-Methode löscht die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist. Bei dieser Methode handelt es sich um eine erweiterte Version der Delete-Methode, die von der CIM \_ LogicalFile geerbt wird.
ms.assetid: 565d604f-01e0-4cd4-b182-9750c58bae5f
ms.tgt_platform: multiple
title: DeleteEx-Methode der CIM_DataFile-Klasse
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
ms.openlocfilehash: 9af120c76e4ab8c53c945bd13aa62a2295385ac2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126530"
---
# <a name="deleteex-method-of-the-cim_datafile-class"></a>DeleteEx-Methode der CIM \_ DataFile-Klasse

Die **DeleteEx** -Methode löscht die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist. Bei dieser Methode handelt es sich um eine erweiterte Version der [**Delete**](delete-method-in-class-cim-datafile.md) -Methode, die von der [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt wird.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 DeleteEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Stop filename* \[ vorgenommen\]
</dt> <dd>

Eine Zeichenfolge, die den Namen der Datei (oder des Verzeichnisses) darstellt, in der die Methode fehlgeschlagen ist. Dieser Parameter ist NULL, wenn die Methode erfolgreich ist.

</dd> <dt>

*Startdateiname* \[ in\]
</dt> <dd>

Eine Zeichenfolge, die die untergeordnete Datei (oder das Verzeichnis) darstellt, die als Ausgangspunkt für diese Methode verwendet werden soll. In der Regel ist der Parameter " *StartFileName* " der Parameter " *StopFileName* ", der die Datei oder das Verzeichnis angibt, in dem ein Fehler im vorherigen Methoden aufrufstyp aufgetreten Wenn dieser Parameter NULL ist, wird der Vorgang für die Datei (oder das Verzeichnis) ausgeführt, die im [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) -Befehl angegeben ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an. Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).

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

Die **DeleteEx** -Methode in [**CIM \_ DataFile**](cim-datafile.md) wird von WMI implementiert.

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

[CIM- \_ Datendatei](deleteex-method-in-class-cim-datafile.md)
</dt> <dt>

[**CIM- \_ Datendatei**](cim-datafile.md)
</dt> <dt>

[WMI-Tasks: Dateien und Ordner](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[**Datei-und Verzeichniszugriffs Rechte-Konstanten**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

