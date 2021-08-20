---
description: Die SetEncy-Methode legt die gewünschte Notfallstufe für einen Alarm fest.
ms.assetid: ac2e7fda-1317-440a-adbd-1ef0844d124c
ms.tgt_platform: multiple
title: SetEncy-Methode der CIM_AlarmDevice-Klasse
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
ms.openlocfilehash: 9557ad9e65b33e1ed8889ef1fd013b2d9f5426f8e819fe56608cb6846ea8669f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118172634"
---
# <a name="seturgency-method-of-the-cim_alarmdevice-class"></a>SetEncy-Methode der CIM \_ AlarmDevice-Klasse

Die **SetEncy-Methode** legt die gewünschte Notfallstufe für einen Alarm fest.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 SetUrgency(
  [in] uint16 RequestedUrgency
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Requested Vererzung* \[ In\]
</dt> <dd>

Relative Häufigkeit, mit der der Alarm blinkt, vibriert oder akustische Töne ausgibt. Die folgenden Werte stammen aus der **Eigenschaft "Urgenty"** in [**CIM \_ AlarmDevice**](cim-alarmdevice.md).

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

Unrecoverable.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Wert 0 (null) zurück, 1 (eins), wenn die angeforderte Notfallstufe nicht unterstützt wird, und eine beliebige andere Zahl, um einen Fehler anzugeben.

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

[CIM \_ AlarmDevice](seturgency-method-in-class-cim-alarmdevice.md)
</dt> <dt>

[**CIM \_ AlarmDevice**](cim-alarmdevice.md)
</dt> </dl>

 

