---
title: Addservers-Methode der Win32_TSGatewayLoadBalancer-Klasse
description: Fügt dem Remotedesktop Gateway-Server (RD-Gateway) Lasten Ausgleichs Server in der Server-Eigenschaft hinzu.
ms.assetid: ffcbe14b-5ada-4951-bf51-95db14af41d7
ms.tgt_platform: multiple
keywords:
- Addservers-Methode Remotedesktopdienste
- Addservers-Methode Remotedesktopdienste, Win32_TSGatewayLoadBalancer-Klasse
- Win32_TSGatewayLoadBalancer-Klasse Remotedesktopdienste, addservers-Methode
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
ms.openlocfilehash: a510fd6ecee12b5251ec84773327d6217463240f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103175"
---
# <a name="addservers-method-of-the-win32_tsgatewayloadbalancer-class"></a>Addservers-Methode der Win32-Klasse "t- \_ gatewayloadbalancer"

Fügt dem Remotedesktop Gateway-Server (RD-Gateway) Lasten Ausgleichs Server in der **Server** -Eigenschaft hinzu.

## <a name="syntax"></a>Syntax


```mof
uint32 AddServers(
  [in] string Servers
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Server* \[ in\]
</dt> <dd>

Durch Semikolons getrennte Liste der RD-Gateway Lasten Ausgleichs Server, die der **Server** -Eigenschaft hinzugefügt werden sollen.

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

 

