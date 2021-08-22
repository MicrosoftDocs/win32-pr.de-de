---
title: Konfigurieren der Methode der Win32_TSGatewayServerSettings-Klasse
description: Konfiguriert die IIS- und RPC-Einstellungen, die für den dienst Remotedesktop Gateway (RD-Gateway) erforderlich sind.
ms.assetid: 12d7264e-46aa-457f-b89d-547231573db8
ms.tgt_platform: multiple
keywords:
- Konfigurieren von methoden Remotedesktopdienste
- Konfigurieren der Methode Remotedesktopdienste , Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings Klasse Remotedesktopdienste , Configure-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.Configure
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e246b81569f63c3a6eac9cafe043c837deca593072b622efa3f854a4a74862
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119515690"
---
# <a name="configure-method-of-the-win32_tsgatewayserversettings-class"></a>Configure-Methode der Win32 \_ TSGatewayServerSettings-Klasse

Konfiguriert die IIS- und RPC-Einstellungen, die für den dienst Remotedesktop Gateway (RD-Gateway) erforderlich sind.

## <a name="syntax"></a>Syntax


```mof
uint32 Configure();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufzurufen.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                        |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

