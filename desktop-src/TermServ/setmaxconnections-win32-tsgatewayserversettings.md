---
title: SetMaxConnections-Methode der Win32_TSGatewayServerSettings Klasse
description: Legt die Eigenschaften MaxConnections und UnlimitedConnections fest, die die maximale Anzahl zulässiger Verbindungen mit dem Remotedesktop Gateway (RD-Gateway)-Server steuern.
ms.assetid: cfdbacb7-4969-4ec5-8301-e8020f3af0cd
ms.tgt_platform: multiple
keywords:
- SetMaxConnections-Remotedesktopdienste
- SetMaxConnections-Methode Remotedesktopdienste , Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings klasse Remotedesktopdienste , SetMaxConnections-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetMaxConnections
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e241b137f2a3a061be06538b934c163ea6445ff177fecf9aaf4dc7db5367990
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009045"
---
# <a name="setmaxconnections-method-of-the-win32_tsgatewayserversettings-class"></a>SetMaxConnections-Methode der Win32 \_ TSGatewayServerSettings-Klasse

Legt die **Eigenschaften MaxConnections** und **UnlimitedConnections** fest, die die maximale Anzahl zulässiger Verbindungen mit dem Remotedesktop-Gatewayserver (RD-Gateway) steuern.

## <a name="syntax"></a>Syntax


```mof
uint32 SetMaxConnections(
  [in] uint32  Connections,
  [in] boolean IsUnlimited
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Verbindungen* \[ In\]
</dt> <dd>

Anzahl der Verbindungen, die dieser Server akzeptieren soll. Legen Sie für eine unbegrenzte Anzahl von Verbindungen den *IsUnlimited-Parameter* auf **True fest.**

</dd> <dt>

*IsUnlimited* \[ In\]
</dt> <dd>

True **gibt an,** dass Verbindungen mit dem Dienst nicht auf eine bestimmte Anzahl beschränkt sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter Remotedesktopdienste [WMI-Anbieterfehlercodes](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufrufen zu können.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

 

