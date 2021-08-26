---
title: SetPortNumbers-Methode der Win32_TSGatewayResourceAuthorizationPolicy-Klasse
description: Legt die Portnummern fest, die eine Verbindung mit der Ressource über Remotedesktop Gateway (RD-Gateway) herstellen dürfen.
ms.assetid: f8237ec3-84dc-44f8-ad86-54c46be1fd03
ms.tgt_platform: multiple
keywords:
- SetPortNumbers-Remotedesktopdienste
- SetPortNumbers-Methode Remotedesktopdienste , Win32_TSGatewayResourceAuthorizationPolicy-Klasse
- Win32_TSGatewayResourceAuthorizationPolicy der Remotedesktopdienste , SetPortNumbers-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetPortNumbers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c151302abfda0b6bc42566770c0e8b8fb10dbab789cf2ece886be557efb023e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987770"
---
# <a name="setportnumbers-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>SetPortNumbers-Methode der Win32 \_ TSGatewayResourceAuthorizationPolicy-Klasse

Legt die Portnummern fest, die eine Verbindung mit der Ressource über Remotedesktop Gateway (RD-Gateway) herstellen dürfen.

## <a name="syntax"></a>Syntax


```mof
uint32 SetPortNumbers(
  [in] string PortNumbers
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PortNumbers* \[ In\]
</dt> <dd>

Liste der durch Semikolons getrennten Portnummern, die für diese Richtlinie Remotedesktop Resource Authorization Policy (RD RD RD) zulässig sind. Um eine beliebige Portnummer zu ermöglichen, legen Sie " \* " fest.

</dd> </dl>

## <a name="remarks"></a>Hinweise

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

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

