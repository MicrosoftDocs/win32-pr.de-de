---
title: SetMaxMonitors-Methode der Win32_TSClientSetting-Klasse
description: Legt die MaxMonitors-Eigenschaft fest.
ms.assetid: 1c8266e1-ff2b-4fbc-af70-6f7b4499d88c
ms.tgt_platform: multiple
keywords:
- SetMaxMonitors-Methode Remotedesktopdienste
- SetMaxMonitors-Methode Remotedesktopdienste , Win32_TSClientSetting-Klasse
- Win32_TSClientSetting-Klasse Remotedesktopdienste , SetMaxMonitors-Methode
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
ms.openlocfilehash: e91cc6a53bbec769236e5c1b462e7bdfe5859cc140a11366299a3eaab46e1777
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987910"
---
# <a name="setmaxmonitors-method-of-the-win32_tsclientsetting-class"></a>SetMaxMonitors-Methode der Win32 \_ TSClientSetting-Klasse

Legt die **MaxMonitors-Eigenschaft** fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetMaxMonitors(
  [in] uint32 MaxMonitors
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*MaxMonitors* \[ In\]
</dt> <dd>

Gibt die neue maximale Anzahl von Monitoren an, die vom Server unterstützt werden. Der Mindestwert ist 1 und der Höchstwert 10.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls einen WMI-Fehlercode. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md) Die -Methode gibt einen Fehler zurück, wenn die Verbindungseinstellungen des Benutzers vom Server überschrieben werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSClientSetting**](win32-tsclientsetting.md)
</dt> </dl>

 

 





