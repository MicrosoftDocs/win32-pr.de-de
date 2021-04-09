---
description: Mit der SetUrgency-Methode wird die gewünschte Dringlichkeits Stufe für einen Alarm festgelegt.
ms.assetid: ac2e7fda-1317-440a-adbd-1ef0844d124c
ms.tgt_platform: multiple
title: Die-Methode der CIM_AlarmDevice-Klasse.
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AlarmDevice.SetUrgency
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 35918677e210ac2fe7ac4798a04db9dc628f5fa1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958384"
---
# <a name="seturgency-method-of-the-cim_alarmdevice-class"></a>Die Methode "tarturgency" der CIM \_ alarmdevice-Klasse

Mit der **SetUrgency** -Methode wird die gewünschte Dringlichkeits Stufe für einen Alarm festgelegt.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 SetUrgency(
  [in] uint16 RequestedUrgency
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*RequestedUrgency* \[ in\]
</dt> <dd>

Relative Häufigkeit, mit der der Alarm blinkt, vibriert oder akustische Töne ausgibt. Die folgenden Werte stammen aus der Eigenschaft **Dringlichkeit** in [**CIM \_ alarmdevice**](cim-alarmdevice.md).

<dt>

0
</dt> <dd>

Unbekannt

</dd> <dt>

1
</dt> <dd>

Sonstiges

</dd> <dt>

2
</dt> <dd>

Wird nicht unterstützt.

</dd> <dt>

3
</dt> <dd>

Zur Information.

</dd> <dt>

4
</dt> <dd>

Nicht kritisch.

</dd> <dt>

5
</dt> <dd>

Kritisch.

</dd> <dt>

6
</dt> <dd>

Nicht BEHEB barer.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Wert 0 (null) zurück, 1 (eins), wenn die angeforderte Dringlichkeits Ebene nicht unterstützt wird, und jede andere Zahl gibt einen Fehler an.

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

[CIM- \_ alarmdevice](seturgency-method-in-class-cim-alarmdevice.md)
</dt> <dt>

[**CIM- \_ alarmdevice**](cim-alarmdevice.md)
</dt> </dl>

 

