---
description: Die SetPowerState-Methode der CIM SCSIController-Klasse legt den gewünschten Energiezustand für ein logisches Gerät fest und legt fest, wann ein Gerät \_ in diesen Zustand gesetzt werden soll.
ms.assetid: 7e484ec8-85b9-4c9e-b91f-04945592ec1c
ms.tgt_platform: multiple
title: SetPowerState-Methode der CIM_SCSIController Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SCSIController.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 250c7ce327986f98f06b807af23f3577abccff34554879fef6ea8ee001f21108
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119700360"
---
# <a name="setpowerstate-method-of-the-cim_scsicontroller-class"></a>SetPowerState-Methode der CIM \_ SCSIController-Klasse

Die **SetPowerState-Methode** der CIM SCSIController-Klasse legt den gewünschten Energiezustand für ein logisches Gerät fest und legt fest, wann ein Gerät \_ in diesen Zustand gesetzt werden soll. In einer Unterklasse sollte der Satz möglicher Rückgabecodes  mithilfe eines ValueMap-Qualifizierers für die -Methode angegeben werden. Die Zeichenfolgen, in die **der ValueMap-Inhalt** übersetzt wird, sollten auch in der Unterklasse als Values-Arrayqualifizierer angegeben werden.  Diese Methode wird von [**CIM \_ LogicalDevice geerbt.**](cim-logicaldevice.md)

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

## <a name="syntax"></a>Syntax


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PowerState* \[ In\]
</dt> <dd>

Ein **ValueMap-Wert,** der den gewünschten Energiezustand für dieses logische Gerät angibt.

<dt>

1
</dt> <dd>

Volle Leistung.

</dd> <dt>

2
</dt> <dd>

Energiesparmodus mit geringer Leistung.

</dd> <dt>

3
</dt> <dd>

Standbymodus "Energie sparen".

</dd> <dt>

4
</dt> <dd>

Energie sparen Sie andere.

</dd> <dt>

5
</dt> <dd>

Energiezyklus.

</dd> <dt>

6
</dt> <dd>

Ausschalten.

</dd> </dl> </dd> <dt>

*Zeit* \[ In\]
</dt> <dd>

Gibt an, wann der Energiezustand festgelegt werden soll, entweder als regulärer Datums-/Uhrzeitwert oder als Intervallwert (wobei das Intervall beginnt, wenn der Methodenaufruf empfangen wird). Wenn der *PowerState-Parameter* gleich 5 ("Power Cycle") ist, gibt der *Time-Parameter* an, wann das Gerät wieder ein-/aus netzen soll. Das Ausschalten ist sofort.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 (null) zurück, 1 (eins), wenn die angegebene *PowerState-* und *Time-Anforderung* nicht unterstützt wird, und einen anderen Wert, wenn ein anderer Fehler aufgetreten ist.

## <a name="remarks"></a>Hinweise

Diese Methode wird derzeit nicht von WMI implementiert. Um diese Methode zu verwenden, müssen Sie sie in Ihrem eigenen Anbieter implementieren.

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von DMTF veröffentlicht wurden. Microsoft hat möglicherweise Änderungen vorgenommen, um kleinere Fehler zu beheben, die Dokumentationsstandards des Microsoft SDK zu erfüllen oder weitere Informationen zur Verfügung zu stellen.

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

[CIM \_ SCSIController](setpowerstate-method-in-class-cim-scsicontroller.md)
</dt> <dt>

[**CIM \_ SCSIController**](cim-scsicontroller.md)
</dt> </dl>

 

 




