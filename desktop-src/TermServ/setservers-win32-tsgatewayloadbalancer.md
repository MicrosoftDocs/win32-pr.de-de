---
title: SetServers-Methode der Win32_TSGatewayLoadBalancer Klasse
description: Legt die Server-Eigenschaft mit der Liste der Lastenausgleichsserver Remotedesktop Gateways (RD-Gateway) fest.
ms.assetid: c82de8e2-301b-465d-b375-038b8a480cde
ms.tgt_platform: multiple
keywords:
- SetServers-Remotedesktopdienste
- SetServers-Methode Remotedesktopdienste , Win32_TSGatewayLoadBalancer-Klasse
- Win32_TSGatewayLoadBalancer der Remotedesktopdienste , SetServers-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer.SetServers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da2c23ac6cf965687a022c5ae5ba8c1ce690c39c45f9149076f36ab13bc2d222
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118349616"
---
# <a name="setservers-method-of-the-win32_tsgatewayloadbalancer-class"></a>SetServers-Methode der Win32 \_ TSGatewayLoadBalancer-Klasse

Legt die **Server-Eigenschaft** mit der Liste der Remotedesktop Gateway (RD-Gateway)-Lastenausgleichsserver fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetServers(
  [in] string Servers
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Server* \[ In\]
</dt> <dd>

Durch Semikolons getrennte Liste von RD-Gateway-Lastenausgleichsservern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter Remotedesktopdienste [WMI-Anbieterfehlercodes](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Hinweise

Wenn sich mehrere Server im *Serverparameter* befinden und einer der Server nicht verarbeitet werden kann, wird keiner der Server verarbeitet.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSGatewayLoadBalancer**](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 

