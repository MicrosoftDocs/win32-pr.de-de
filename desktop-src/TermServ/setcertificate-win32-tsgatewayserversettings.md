---
title: SetCertificate-Methode der Win32_TSGatewayServerSettings-Klasse
description: Legt den Zertifikathash für die HTTPS-Bindung an Port 443 in IIS fest.
ms.assetid: b5f794bc-17b1-401a-92d8-c9bbe5d0d05f
ms.tgt_platform: multiple
keywords:
- SetCertificate-Methode Remotedesktopdienste
- SetCertificate-Methode Remotedesktopdienste , Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings Klasse Remotedesktopdienste , SetCertificate-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetCertificate
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54b11f87e3cdc8c5c211f67e03a067690ddeac5ab3bc342794e1e97a8f339117
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127475"
---
# <a name="setcertificate-method-of-the-win32_tsgatewayserversettings-class"></a>SetCertificate-Methode der Win32 \_ TSGatewayServerSettings-Klasse

Legt den Zertifikathash für die HTTPS-Bindung an Port 443 in IIS fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetCertificate(
  [in] uint8 CertHash[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*CertHash* \[ In\]
</dt> <dd>

Typ: **uint8 \[ \]**

Der neue Zertifikathash.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Hinweise

Nachdem der Zertifikathash mit dieser Methode festgelegt wurde, müssen Sie die [**Configure-Methode**](configure-win32-tsgatewayserversettings.md) aufrufen, um den Konfigurationsprozess abzuschließen.

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufzurufen.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

 

