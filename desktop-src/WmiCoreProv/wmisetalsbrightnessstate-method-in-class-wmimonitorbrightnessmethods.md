---
description: Wird verwendet, um den Helligkeitszustand des Umgebungslichtsensors zu steuern.
ms.assetid: ff400d4e-be8c-450b-ad53-d43b0ab84ab3
title: WmiSetALSBrightnessState-Methode der WmiMonitorBrightnessMethods-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiSetALSBrightnessState
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 1c8a99ea92391626975d635802f82dd81b663247f4bb3522db19d14237d920f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051118"
---
# <a name="wmisetalsbrightnessstate-method-of-the-wmimonitorbrightnessmethods-class"></a>WmiSetALSBrightnessState-Methode der WmiMonitorBrightnessMethods-Klasse

Die **WmiSetALSBrightnessState-Methode** wird verwendet, um den Helligkeitszustand des Umgebungslichtsensors zu steuern. Wenn mithilfe der [**WmiSetBrightness-Methode**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) eine Außerkraftsetzung der aktiven Helligkeit eingerichtet wurde, hat diese Außerkraftsetzung Vorrang vor der mit dieser Methode festgelegten ALS-Helligkeit. Damit eine aktivierte ALS-Helligkeitsüberschreibung wirksam wird, muss die Helligkeitsrichtlinie mithilfe der [**WmiRevertToPolicyBrightness-Methode**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) zurückgesetzt werden.

## <a name="syntax"></a>Syntax


```mof
uint32 WmiSetALSBrightnessState(
   boolean State
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*State* 
</dt> <dd>

ALS-Helligkeitszustand. False deaktiviert die Als-Helligkeitsüberschreibung, und true aktiviert sie.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, um den Erfolg anzugeben. Jede andere Zahl gibt einen Fehler an. Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehlerkonstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum.**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Namespace<br/>                | Root \\ wmi<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WmiMonitorBrightnessMethods**](wmimonitorbrightnessmethods.md)
</dt> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

