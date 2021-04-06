---
title: Setsharedsecret-Methode der Win32_TSGatewayRADIUSServer-Klasse
description: Legt die sharedsecret-Eigenschaft für diesen Remote Authentication Dial-in User Service Server (RADIUS) fest.
ms.assetid: b4f7afb7-862f-4c30-b60a-aa6a8dbbe3e9
ms.tgt_platform: multiple
keywords:
- Setsharedsecret-Methode Remotedesktopdienste
- Setsharedsecret-Methode Remotedesktopdienste, Win32_TSGatewayRADIUSServer-Klasse
- Win32_TSGatewayRADIUSServer-Klasse Remotedesktopdienste, setsharedsecret-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.SetSharedSecret
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f17e22061467194bdb09fc3f2c6105706f58e587
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742368"
---
# <a name="setsharedsecret-method-of-the-win32_tsgatewayradiusserver-class"></a>Setsharedsecret-Methode der Win32- \_ Klasse "segatewayradiusserver"

Legt die **sharedsecret** -Eigenschaft für diesen Remote Authentication Dial-in User Service Server (RADIUS) fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetSharedSecret(
  [in] string SharedSecret
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Sharedsecret* \[ in\]
</dt> <dd>

Neuer gemeinsamer geheimer Schlüssel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Bemerkungen

Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>"T-Gateway. mof"</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32-"t- \_ gatewayradiusserver"**](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

