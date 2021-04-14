---
title: Setsslbridging-Methode der Win32_TSGatewayServerSettings-Klasse
description: Legt den Typ des SSL-Bridging fest, der vom Remotedesktop Gateway-Server (RD-Gateway) verwendet werden soll.
ms.assetid: 11885b8b-491e-4d90-b4d4-f0a0fbe68cb1
ms.tgt_platform: multiple
keywords:
- Setsslbridging-Methode Remotedesktopdienste
- Setsslbridging-Methode Remotedesktopdienste, Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste, setsslbridging-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetSslBridging
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77181fb8d8661ec7ea7dc0ce70532281fb9c1bde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392016"
---
# <a name="setsslbridging-method-of-the-win32_tsgatewayserversettings-class"></a>Setsslbridging-Methode der Win32-Klasse "t- \_ gatewayserversettings"

Legt den Typ des SSL-Bridging fest, der vom Remotedesktop Gateway-Server (RD-Gateway) verwendet werden soll. Dieser Wert wird in der **sslbridging** -Eigenschaft gespeichert.

> [!IMPORTANT]
> Wenn der SSL-Bridging-Typ mit dieser Methode geändert wird, muss der RD-Gateway-Dienst neu gestartet werden, damit diese Änderung wirksam wird.

 

## <a name="syntax"></a>Syntax


```mof
uint32 SetSslBridging(
  [in] uint32 SslBridging
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Sslbridging* \[ in\]
</dt> <dd>

Typ: **UInt32**

Gibt den neuen SSL-Überbrückungs Wert an. Dies kann einer der folgenden Werte sein:

<dt>

0
</dt> <dd>

Keine SSL-Überbrückung.

</dd> <dt>

1
</dt> <dd>

HTTPS-zu-HTTP-Bridging.

</dd> <dt>

2
</dt> <dd>

HTTPS-zu-HTTPS-Bridging.

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

[**Win32-Datei- \_ gatewayserversettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

