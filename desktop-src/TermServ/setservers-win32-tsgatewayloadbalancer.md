---
title: Setservers-Methode der Win32_TSGatewayLoadBalancer-Klasse
description: Legt die Server-Eigenschaft mit der Liste der Remotedesktop Gateway-Server (RD-Gateway) für den Lastenausgleich fest.
ms.assetid: c82de8e2-301b-465d-b375-038b8a480cde
ms.tgt_platform: multiple
keywords:
- Setservers-Methode Remotedesktopdienste
- Setservers-Methode Remotedesktopdienste, Win32_TSGatewayLoadBalancer-Klasse
- Win32_TSGatewayLoadBalancer-Klasse Remotedesktopdienste, setservers-Methode
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
ms.openlocfilehash: b28d1123ce82844fb501f3562014b93337502b51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742369"
---
# <a name="setservers-method-of-the-win32_tsgatewayloadbalancer-class"></a>Setservers-Methode der Win32- \_ Klasse "segatewayloadbalancer"

Legt die **Server** -Eigenschaft mit der Liste der Remotedesktop Gateway-Server (RD-Gateway) für den Lastenausgleich fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetServers(
  [in] string Servers
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Server* \[ in\]
</dt> <dd>

Durch Semikolons getrennte Liste der RD-Gateway Lasten Ausgleichs Server.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Bemerkungen

Wenn sich mehrere Server im *Server* -Parameter befinden und einer der Server nicht verarbeitet werden kann, wird keiner der Server verarbeitet.

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

[**Win32-"t- \_ gatewayloadbalancer"**](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 

