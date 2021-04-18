---
title: Setmaxmonitors-Methode der Win32_TSClientSetting-Klasse
description: Legt die maxmonitors-Eigenschaft fest.
ms.assetid: 1c8266e1-ff2b-4fbc-af70-6f7b4499d88c
ms.tgt_platform: multiple
keywords:
- Setmaxmonitors-Methode Remotedesktopdienste
- Setmaxmonitors-Methode Remotedesktopdienste, Win32_TSClientSetting-Klasse
- Win32_TSClientSetting-Klasse Remotedesktopdienste, setmaxmonitors-Methode
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetMaxMonitors
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76cdbe29079f5006cbf596751bef73cda1e94e52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338349"
---
# <a name="setmaxmonitors-method-of-the-win32_tsclientsetting-class"></a>Setmaxmonitors-Methode der Win32- \_ Klasse tsclientsetting

Legt die **maxmonitors** -Eigenschaft fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetMaxMonitors(
  [in] uint32 MaxMonitors
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Maxmonitors* \[ in\]
</dt> <dd>

Gibt die neue maximale Anzahl von Monitoren an, die vom Server unterstützt werden. Der Minimalwert ist 1, und der Maximalwert ist 10.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) . Die-Methode gibt einen Fehler zurück, wenn die Verbindungseinstellungen des Benutzers vom Server überschrieben werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tscsgwmi. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ tsclientsetting**](win32-tsclientsetting.md)
</dt> </dl>

 

 





