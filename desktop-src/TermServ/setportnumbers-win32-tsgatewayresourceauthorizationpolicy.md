---
title: Setportnumbers-Methode der Win32_TSGatewayResourceAuthorizationPolicy-Klasse
description: Legt die Portnummern fest, die über Remotedesktop Gateway (RD-Gateway) mit der Ressource verbunden werden können.
ms.assetid: f8237ec3-84dc-44f8-ad86-54c46be1fd03
ms.tgt_platform: multiple
keywords:
- Setportnumbers-Methode Remotedesktopdienste
- Setportnumbers-Methode Remotedesktopdienste, Win32_TSGatewayResourceAuthorizationPolicy-Klasse
- Win32_TSGatewayResourceAuthorizationPolicy-Klasse Remotedesktopdienste, setportnumbers-Methode
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
ms.openlocfilehash: b938435abab23e3ad27cf13dbe65e64b9ec859eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477721"
---
# <a name="setportnumbers-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Setportnumbers-Methode der Win32-Klasse "t- \_ gatewayresourceauthorizationpolicy"

Legt die Portnummern fest, die über Remotedesktop Gateway (RD-Gateway) mit der Ressource verbunden werden können.

## <a name="syntax"></a>Syntax


```mof
uint32 SetPortNumbers(
  [in] string PortNumbers
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Portnummern* \[ in\]
</dt> <dd>

Liste von durch Semikolons getrennten Portnummern, die für diese Remotedesktop Ressourcen Autorisierungs Richtlinie (RD-RAP) zulässig sind. Um eine beliebige Portnummer zuzulassen, legen Sie " \* " fest.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

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

[**Win32- \_ faigatewayresourceauthorizationpolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

