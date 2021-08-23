---
description: Legt die Anzeigestärke eines Computermonitors fest.
ms.assetid: 900cf5fd-6888-4f0b-8e0b-01eeaaeeeb8f
title: WmiSetBrightness-Methode der WmiMonitorBrightnessMethods-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiSetBrightness
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 0a9425668ad00422033a77233ade2822966db0f19d6e6628ada24866be9953f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794440"
---
# <a name="wmisetbrightness-method-of-the-wmimonitorbrightnessmethods-class"></a>WmiSetBrightness-Methode der WmiMonitorBrightnessMethods-Klasse

Die **WmiSetBrightness-Methode** legt die Anzeigestärke eines Computermonitors fest.

## <a name="syntax"></a>Syntax


```mof
uint32 WmiSetBrightness(
   uint32 Timeout,
   uint8  Brightness
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Timeout* 
</dt> <dd>

Timeout in Sekunden.

</dd> <dt>

*Helligkeit* 
</dt> <dd>

Helligkeit in Prozent.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, um den Erfolg anzugeben. Jede andere Zahl gibt einen Fehler an. Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehlerkonstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum.**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)

## <a name="examples"></a>Beispiele

Eine erweiterte Erläuterung zum Abrufen und Festlegen der Helligkeit des Monitors finden Sie im Blogthema Scripting Guy es [Use PowerShell to Report and Set Monitor Brightness (Verwenden von PowerShell zum Melden und Festlegen](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx) der Helligkeit des Monitors).

Im folgenden PowerShell-Beispiel wird die Helligkeit des Monitors auf 50 % festgelegt.


```PowerShell
$brightness = 50
$delay = 5
$myMonitor = Get-WmiObject -Namespace root\wmi -Class WmiMonitorBrightnessMethods
$myMonitor.wmisetbrightness($delay, $brightness)
```



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

 

