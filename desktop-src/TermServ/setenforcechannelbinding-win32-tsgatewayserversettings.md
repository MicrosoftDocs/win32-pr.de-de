---
title: SetEnforceChannelBinding-Methode der Win32_TSGatewayServerSettings-Klasse
description: Legt die EnforceChannelBinding-Eigenschaft fest.
ms.assetid: 8bd64fe7-bad5-44e6-a309-10802d9a8bd4
ms.tgt_platform: multiple
keywords:
- SetEnforceChannelBinding-Methode Remotedesktopdienste
- SetEnforceChannelBinding-Methode Remotedesktopdienste , Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste , SetEnforceChannelBinding-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetEnforceChannelBinding
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1a2e076fb4ba439faa7cc22f30da1f815b0571ede0477b875e25176a7f0297e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988030"
---
# <a name="setenforcechannelbinding-method-of-the-win32_tsgatewayserversettings-class"></a>SetEnforceChannelBinding-Methode der Win32 \_ TSGatewayServerSettings-Klasse

Legt die **EnforceChannelBinding-Eigenschaft** fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetEnforceChannelBinding(
  [in] boolean EnforceChannelBinding
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*EnforceChannelBinding* \[ In\]
</dt> <dd>

Gibt den neuen **EnforceChannelBinding-Eigenschaftswert an.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                           |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





