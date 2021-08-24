---
title: EnableCentralCAP-Methode der Win32_TSGatewayServerSettings Klasse
description: Steuert die CentralCAPEnabled-Eigenschaft, die die Remotedesktopdienste Verbindungsautorisierungsrichtlinien steuert (RD \ 160; CAPs) für den Remotedesktop Gatewayserver (RD-Gateway).
ms.assetid: 43e476df-714d-43bd-b40f-33511b7757a4
ms.tgt_platform: multiple
keywords:
- EnableCentralCAP-Remotedesktopdienste
- EnableCentralCAP-Methode Remotedesktopdienste , Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings klasse Remotedesktopdienste , EnableCentralCAP-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableCentralCAP
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f53bc180d2f4636ed2fd8d7b32d819a9d953416e4022b5cf4c18a900b15776fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119574760"
---
# <a name="enablecentralcap-method-of-the-win32_tsgatewayserversettings-class"></a>EnableCentralCAP-Methode der Win32 \_ TSGatewayServerSettings-Klasse

Steuert die **CentralCAPEnabled-Eigenschaft,** die die Remotedesktopdienste-Verbindungsautorisierungsrichtlinien (CAPs) für den Remotedesktop-Gatewayserver (RD-Gateway) steuert.

## <a name="syntax"></a>Syntax


```mof
uint32 EnableCentralCAP(
  [in] boolean CentralCAPEnabled
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*CentralCAPEnabled* \[ In\]
</dt> <dd>

Wenn dies auf **True festgelegt ist,** werden RD-CAPs von zentralen RD-CAP-Servern verwendet. Wenn false festgelegt **ist,** werden nur Richtlinien vom lokalen Server verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter Remotedesktopdienste [WMI-Anbieterfehlercodes](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufrufen zu können.

Managed Object Format (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

