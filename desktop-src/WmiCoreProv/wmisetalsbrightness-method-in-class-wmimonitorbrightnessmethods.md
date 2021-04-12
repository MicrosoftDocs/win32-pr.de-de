---
description: Wird verwendet, um den Umgebungs Wert des Umgebungslicht Sensors festzulegen.
ms.assetid: 8b3ec692-4043-42b3-8dd6-7a147620e382
title: Wmisegtalsbrightness-Methode der wmimonitorbrightnessmethods-Klasse
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
ms.openlocfilehash: 0768917f9197b6ee3de52877e031acbbdc8f9aed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218659"
---
# <a name="wmisetalsbrightness-method-of-the-wmimonitorbrightnessmethods-class"></a>Wmisegtalsbrightness-Methode der wmimonitorbrightnessmethods-Klasse

Die **wmisetalsbrightness** -Methode wird verwendet, um den Helligkeit-Wert des Umgebungslicht Sensors festzulegen. Wenn eine Überschreibung der aktiven Helligkeit mithilfe der [**wmisethelligkeit**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) -Methode festgelegt wurde, hat diese außer Kraft Setzung Vorrang vor der als-Helligkeit, die mithilfe dieser Methode festgelegt wird. Damit eine aktivierte außer Kraft setzung der Helligkeit wirksam wird, muss die Helligkeit-Richtlinie mithilfe der [**wmireverttopolicybrightness**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) -Methode wieder hergestellt werden.

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

Die als-Helligkeit als Prozentsatz.

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

 

