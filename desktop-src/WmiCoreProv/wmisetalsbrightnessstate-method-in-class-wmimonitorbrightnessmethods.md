---
description: Wird verwendet, um den Umgebungslichtsensor-Helligkeits Zustand zu steuern.
ms.assetid: ff400d4e-be8c-450b-ad53-d43b0ab84ab3
title: Wmiantalsbrightnessstate-Methode der wmimonitorbrightnessmethods-Klasse
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
ms.openlocfilehash: 593b007f75c7eb134de4bb4c9f83c7246e9a51b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352385"
---
# <a name="wmisetalsbrightnessstate-method-of-the-wmimonitorbrightnessmethods-class"></a>Wmiantalsbrightnessstate-Methode der wmimonitorbrightnessmethods-Klasse

Die **wmiantalsbrightnessstate** -Methode wird verwendet, um den Umgebungszustand des hellen hell Sensors zu steuern. Wenn eine Überschreibung der aktiven Helligkeit mithilfe der [**wmisethelligkeit**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) -Methode festgelegt wurde, hat diese außer Kraft Setzung Vorrang vor der als-Helligkeit, die mithilfe dieser Methode festgelegt wird. Damit eine aktivierte außer Kraft setzung der Helligkeit wirksam wird, muss die Helligkeit-Richtlinie mithilfe der [**wmireverttopolicybrightness**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) -Methode wieder hergestellt werden.

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

ALS-Helligkeits Zustand. False deaktiviert die außer Kraft Setzung von als Helligkeit, und true aktiviert Sie.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt NULL (0) zurück, um den Erfolg anzugeben. Jede andere Zahl gibt einen Fehler an. Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Namespace<br/>                | WMI-Stammdatei \\<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WMI Core. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Wmimonitorbrightnessmethods**](wmimonitorbrightnessmethods.md)
</dt> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

