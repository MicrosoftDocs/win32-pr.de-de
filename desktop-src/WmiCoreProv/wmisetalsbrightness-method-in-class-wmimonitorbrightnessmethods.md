---
description: Wird zum Festlegen des Helligkeitswerts des Umgebungslichtsensors verwendet.
ms.assetid: 8b3ec692-4043-42b3-8dd6-7a147620e382
title: WmiSetALSBrightness-Methode der WmiMonitorBrightnessMethods-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiSetALSBrightness
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 93ea1208f81a38b846a1e6a4bf49a8def8a5a8874423a2779b169764016bd193
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118110754"
---
# <a name="wmisetalsbrightness-method-of-the-wmimonitorbrightnessmethods-class"></a>WmiSetALSBrightness-Methode der WmiMonitorBrightnessMethods-Klasse

Mit **der WmiSetALSBrightness-Methode** wird der Helligkeitswert des Umgebungslichtsensors festgelegt. Wenn eine aktive Helligkeitsüberschreibung mithilfe der [**WmiSetBrightness-Methode**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) eingerichtet wurde, hat diese Überschreibung Vorrang vor der ALS-Helligkeit, die mit dieser Methode festgelegt wurde. Damit eine aktivierte ALS-Helligkeitsüberschreibung wirksam wird, muss die Helligkeitsrichtlinie mithilfe der [**WmiRevertToPolicyBrightness-Methode zurückverwendet**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) werden.

## <a name="syntax"></a>Syntax


```mof
uint32 WmiSetALSBrightness(
   uint8 Brightness
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Helligkeit* 
</dt> <dd>

Die ALS-Helligkeit als Prozentsatz.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt null (0) zurück, um den Erfolg anzugeben. Jede andere Zahl gibt einen Fehler an. Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehlerkonstistenzen**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).

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

 

