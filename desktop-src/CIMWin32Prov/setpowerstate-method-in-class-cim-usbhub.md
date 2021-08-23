---
description: Die SetPowerState-Methode der CIM \_ USBHub-Klasse legt den gewünschten Energiezustand für ein logisches Gerät fest und legt fest, wann ein Gerät in diesen Zustand versetzt werden soll.
ms.assetid: 000ea180-16c0-4c0b-89e5-620ee8112c8a
ms.tgt_platform: multiple
title: SetPowerState-Methode der CIM_USBHub-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBHub.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bc16b806782055328fe576851e0b227d2178289c1d3cece35f7ce6f1f2e66d00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119578230"
---
# <a name="setpowerstate-method-of-the-cim_usbhub-class"></a>SetPowerState-Methode der \_ CIM-USBHub-Klasse

Die **SetPowerState-Methode** der CIM \_ USBHub-Klasse legt den gewünschten Energiezustand für ein logisches Gerät fest und legt fest, wann ein Gerät in diesen Zustand versetzt werden soll. In einer Unterklasse sollte der Satz möglicher Rückgabecodes mithilfe eines [**ValueMap-Qualifizierers**](/windows/desktop/WmiSdk/standard-qualifiers) für die -Methode angegeben werden. Die Zeichenfolgen, in die der **ValueMap-Inhalt** übersetzt wird, sollten auch in der Unterklasse als Values-Arrayqualifizierer angegeben werden.  Diese Methode wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

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

Ein [**ValueMap-Wert,**](/windows/desktop/WmiSdk/standard-qualifiers) der den gewünschten Energiezustand für dieses logische Gerät angibt.

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

Energiesparmodus.

</dd> <dt>

4
</dt> <dd>

Andere Energie speichern.

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

Gibt an, wann der Energiezustand festgelegt werden soll, entweder als regulärer Datums-/Uhrzeitwert oder als Intervallwert (wobei das Intervall beginnt, wenn der Methodenaufruf empfangen wird). Wenn der *PowerState-Parameter* gleich 5 ist ("Power Cycle"), gibt der *Time-Parameter* an, wann das Gerät wieder eingeschaltet werden soll. Das Ausschalten erfolgt sofort.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 (null) zurück, 1 (eins), wenn die angegebene *PowerState-* und *Time-Anforderung* nicht unterstützt wird, und einen anderen Wert, wenn ein anderer Fehler aufgetreten ist.

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

[CIM \_ USBHub](setpowerstate-method-in-class-cim-usbhub.md)
</dt> <dt>

[**CIM \_ USBHub**](cim-usbhub.md)
</dt> </dl>

 

