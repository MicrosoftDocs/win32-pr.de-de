---
title: Die Methode "sstiessiontimeout" der Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
description: Legt die Eigenschaften sessiontimeout und sessiontimeoutaction fest.
ms.assetid: 11491c97-3ef8-46c1-9504-696c613e374e
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode "
- Methode Remotedesktopdienste der Methode "Win32_TSGatewayConnectionAuthorizationPolicy"
- Win32_TSGatewayConnectionAuthorizationPolicy-Klasse Remotedesktopdienste, Methode "-Methode"
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetSessionTimeout
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8e544b59ae4fe0b74d0c120e6884ab81743cac6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518161"
---
# <a name="setsessiontimeout-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Die Methode "stionessiontimeout" der Win32-Klasse "t- \_ gatewayconnectionauthorizationpolicy"

Legt die Eigenschaften **sessiontimeout** und **sessiontimeoutaction** fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetSessionTimeout(
  [in] uint32 SessionTimeout,
  [in] uint32 SessionTimeoutAction
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Sessiontimeout* \[ in\]
</dt> <dd>

Typ: **UInt32**

Der neue Timeout Wert in Minuten. Der Wert 0 bedeutet, dass kein Timeout vorliegt.

</dd> <dt>

*Sessiontimeoutaction* \[ in\]
</dt> <dd>

Typ: **UInt32**

Gibt die Aktion an, die bei einem Sitzungs Timeout durchgeführt werden soll. Dies kann einer der folgenden Werte sein:

<dt>

0
</dt> <dd>

Trennen Sie die Sitzung.

</dd> <dt>

1
</dt> <dd>

Versuchen Sie, die Sitzung erneut zu autorisieren.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Bemerkungen

Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                        |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>"T-Gateway. mof"</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ faigatewayconnectionauthorizationpolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

