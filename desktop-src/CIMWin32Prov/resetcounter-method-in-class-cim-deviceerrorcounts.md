---
description: Die ResetCounter-Methode setzt die Fehler- und Warnindikatoren zurück.
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
ms.openlocfilehash: b36a525be507945113120fc2bdb0084b0a6b1a076101b5e4ab69445146479d1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588260"
---
# <a name="resetcounter-method-of-the-cim_deviceerrorcounts-class"></a>ResetCounter-Methode der CIM \_ DeviceErrorCounts-Klasse

Die **ResetCounter-Methode** setzt die Fehler- und Warnindikatoren zurück. Eine -Methode wird verwendet, damit die Instrumentierung des logischen Geräts, die die Fehler und Warnungen zurückgibt, auch die interne Verarbeitung und die Leistungsindikatoren zurücksetzen kann. In einer Unterklasse kann der Satz möglicher Rückgabecodes mithilfe eines **ValueMap-Qualifizierers** für die -Methode angegeben werden. Die Zeichenfolgen, in die der **ValueMap-Inhalt** übersetzt wird, können auch in der Unterklasse als Values-Arrayqualifizierer angegeben werden. 

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 ResetCounter(
  [in] uint16 SelectedCounter
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SelectedCounter* \[ In\]
</dt> <dd>

Der zurückzusetzende Fehlerindikator.

<dt>

<span id="All"></span><span id="all"></span><span id="ALL"></span>

**Alle** (0)


</dt> <dd></dd> <dt>

<span id="Indeterminate_Error_Counter"></span><span id="indeterminate_error_counter"></span><span id="INDETERMINATE_ERROR_COUNTER"></span>

**Unbestimmter Fehlerindikator** (1)


</dt> <dd></dd> <dt>

<span id="Critical_Error_Counter"></span><span id="critical_error_counter"></span><span id="CRITICAL_ERROR_COUNTER"></span>

**Zähler für kritische Fehler** (2)


</dt> <dd></dd> <dt>

<span id="Major_Error_Counter"></span><span id="major_error_counter"></span><span id="MAJOR_ERROR_COUNTER"></span>

**Hauptfehlerindikator** (3)


</dt> <dd></dd> <dt>

<span id="Minor_Error_Counter"></span><span id="minor_error_counter"></span><span id="MINOR_ERROR_COUNTER"></span>

**Kleiner Fehlerindikator** (4)


</dt> <dd></dd> <dt>

<span id="Warning_Counter"></span><span id="warning_counter"></span><span id="WARNING_COUNTER"></span>

**Warnindikator** (5)


</dt> <dd></dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, 1 (eins), falls nicht unterstützt, und einen anderen Wert, wenn ein Fehler aufgetreten ist.

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

[CIM \_ DeviceErrorCounts](resetcounter-method-in-class-cim-deviceerrorcounts.md)
</dt> <dt>

[**CIM \_ DeviceErrorCounts**](cim-deviceerrorcounts.md)
</dt> </dl>

 

