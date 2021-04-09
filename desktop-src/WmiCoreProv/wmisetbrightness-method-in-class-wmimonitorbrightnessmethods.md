---
description: Legt die Anzeige Helligkeit eines Computermonitors fest.
ms.assetid: 900cf5fd-6888-4f0b-8e0b-01eeaaeeeb8f
title: Wmisethelligkeit-Methode der wmimonitorbrightnessmethods-Klasse
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
ms.openlocfilehash: 599610b0d81de283d97ca347486c4adcbe0103dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042477"
---
# <a name="wmisetbrightness-method-of-the-wmimonitorbrightnessmethods-class"></a>Wmisethelligkeit-Methode der wmimonitorbrightnessmethods-Klasse

Die **wmisethelligkeit** -Methode legt die Anzeige Helligkeit eines Computermonitors fest.

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

Gibt NULL (0) zurück, um den Erfolg anzugeben. Jede andere Zahl gibt einen Fehler an. Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).

## <a name="examples"></a>Beispiele

Eine ausführliche Erläuterung zum Abrufen und Festlegen der Helligkeit des Monitors finden Sie im Blogbeitrag [Verwenden von PowerShell zum melden und Festlegen von Monitor Helligkeit](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx) .

Im folgenden PowerShell-Beispiel wird die Helligkeit des Monitors auf 50% festgelegt.


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
| Namespace<br/>                | WMI-Stammdatei \\<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WMI Core. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Wmimonitorbrightnessmethods**](wmimonitorbrightnessmethods.md)
</dt> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

