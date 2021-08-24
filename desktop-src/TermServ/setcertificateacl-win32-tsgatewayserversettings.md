---
title: SetCertificateACL-Methode der Win32_TSGatewayServerSettings-Klasse
description: Legt das Zertifikat fest, das für den Zugriff auf den Remotedesktop Gatewayserver (RD Gateway) erforderlich ist.
ms.assetid: 274c24bf-4e44-42ea-a109-99d0249c2f78
ms.tgt_platform: multiple
keywords:
- SetCertificateACL-Methode Remotedesktopdienste
- SetCertificateACL-Methode Remotedesktopdienste , Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste , SetCertificateACL-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetCertificateACL
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc18dd0bf72ac63216e71e1a7db6a133d6a97f79d3a62876f8a9c9458007e25d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138033"
---
# <a name="setcertificateacl-method-of-the-win32_tsgatewayserversettings-class"></a>SetCertificateACL-Methode der Win32 \_ TSGatewayServerSettings-Klasse

Legt das Zertifikat fest, das für den Zugriff auf den Remotedesktop Gatewayserver (RD Gateway) erforderlich ist.

## <a name="syntax"></a>Syntax


```mof
uint32 SetCertificateACL(
  [in] uint8 CertHash[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*CertHash* \[ In\]
</dt> <dd>

Hash des Zertifikats, das vom RD-Gatewayserver verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufzurufen.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

