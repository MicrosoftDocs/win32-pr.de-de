---
description: Die ResetCounter-Methode setzt die Fehler-und Warnungs Zähler zurück.
ms.assetid: 5bc6c939-cd97-40ca-a16c-5227e7f27c76
ms.tgt_platform: multiple
title: ResetCounter-Methode der CIM_DeviceErrorCounts-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceErrorCounts.ResetCounter
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 386547362f5a7aa52bddfbf9df3af01949aecbdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860707"
---
# <a name="resetcounter-method-of-the-cim_deviceerrorcounts-class"></a>ResetCounter-Methode der CIM \_ deviceerrorcounts-Klasse

Die **ResetCounter** -Methode setzt die Fehler-und Warnungs Zähler zurück. Eine-Methode wird verwendet, damit die Instrumentation des logischen Geräts, das die Fehler und Warnungen in der Tabelle auffüllt, auch die interne Verarbeitung und Leistungsindikatoren zurücksetzen kann. In einer Unterklasse kann der Satz möglicher Rückgabecodes mit einem **ValueMap** -Qualifizierer für die-Methode angegeben werden. Die Zeichen folgen, in die der **ValueMap** -Inhalt übersetzt wird, können auch in der Unterklasse als **Werte** Array Qualifizierer angegeben werden.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 ResetCounter(
  [in] uint16 SelectedCounter
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Selectedcounter* \[ in\]
</dt> <dd>

Der zurück zusetzenden Fehlerwert.

<dt>

<span id="All"></span><span id="all"></span><span id="ALL"></span>

**Alle** (0)


</dt> <dd></dd> <dt>

<span id="Indeterminate_Error_Counter"></span><span id="indeterminate_error_counter"></span><span id="INDETERMINATE_ERROR_COUNTER"></span>

**Unbestimmter Fehler Zählers** (1)


</dt> <dd></dd> <dt>

<span id="Critical_Error_Counter"></span><span id="critical_error_counter"></span><span id="CRITICAL_ERROR_COUNTER"></span>

**Kritischer Fehler Zählers** (2)


</dt> <dd></dd> <dt>

<span id="Major_Error_Counter"></span><span id="major_error_counter"></span><span id="MAJOR_ERROR_COUNTER"></span>

**Hauptfehler-Counter** (3)


</dt> <dd></dd> <dt>

<span id="Minor_Error_Counter"></span><span id="minor_error_counter"></span><span id="MINOR_ERROR_COUNTER"></span>

**Kleiner Fehler-Counter** (4)


</dt> <dd></dd> <dt>

<span id="Warning_Counter"></span><span id="warning_counter"></span><span id="WARNING_COUNTER"></span>

**Warnungs Counter** (5)


</dt> <dd></dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 (null) zurück, 1 (eins), wenn nicht unterstützt, und einen anderen Wert, wenn ein Fehler aufgetreten ist.

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

[CIM \_ deviceerrorcounts](resetcounter-method-in-class-cim-deviceerrorcounts.md)
</dt> <dt>

[**CIM \_ deviceerrorcounts**](cim-deviceerrorcounts.md)
</dt> </dl>

 

