---
title: AddServers-Methode der Win32_TSGatewayLoadBalancer Klasse
description: Fügt den Lastenausgleichsservern des Remotedesktop Gateways (RD-Gateway) in der Eigenschaft Server Server Server hinzu.
ms.assetid: ffcbe14b-5ada-4951-bf51-95db14af41d7
ms.tgt_platform: multiple
keywords:
- AddServers-Remotedesktopdienste
- AddServers-Methode Remotedesktopdienste , Win32_TSGatewayLoadBalancer-Klasse
- Win32_TSGatewayLoadBalancer klasse Remotedesktopdienste , AddServers-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer.AddServers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00bb232572c49b77f11de469f8e09fc536e73354f907d4070bc2281d42fc87fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117942268"
---
# <a name="addservers-method-of-the-win32_tsgatewayloadbalancer-class"></a>AddServers-Methode der Win32 \_ TSGatewayLoadBalancer-Klasse

Fügt den Lastenausgleichsservern des Remotedesktop Gateways (RD-Gateway) in der **Eigenschaft Server Server Server** hinzu.

## <a name="syntax"></a>Syntax


```mof
uint32 AddServers(
  [in] string Servers
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Server* \[ In\]
</dt> <dd>

Durch Semikolons getrennte Liste der RD-Gateway-Lastenausgleichsserver, die der **Server-Eigenschaft hinzugefügt werden** sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter Remotedesktopdienste [WMI-Anbieterfehlercodes](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Hinweise

Wenn sich mehrere Server im *Serverparameter* befinden und einer der Server nicht verarbeitet werden kann, wird keiner der Server verarbeitet.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSGatewayLoadBalancer**](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 

