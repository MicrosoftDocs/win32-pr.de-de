---
title: SetSecurityLayer-Methode der Win32_TSGeneralSetting Klasse
description: Die SetSecurityLayer-Methode legt die Sicherheitsschicht fest.
ms.assetid: 3b894494-2180-4f1d-8e67-a66c679d286c
ms.tgt_platform: multiple
keywords:
- SetSecurityLayer-Remotedesktopdienste
- SetSecurityLayer-Methode Remotedesktopdienste , Win32_TSGeneralSetting-Klasse
- Win32_TSGeneralSetting klasse Remotedesktopdienste , SetSecurityLayer-Methode
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetSecurityLayer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e01f761b63be028e2c507644f160b6742f9d781e517ea03ce549e3ac84419c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513870"
---
# <a name="setsecuritylayer-method-of-the-win32_tsgeneralsetting-class"></a>SetSecurityLayer-Methode der Win32 \_ TSGeneralSetting-Klasse

Die **SetSecurityLayer-Methode** legt die Sicherheitsschicht fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetSecurityLayer(
  [in] uint32 SecurityLayer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SecurityLayer* \[ In\]
</dt> <dd>

Die sicherheitsschicht, die festgelegt werden soll. Wenn die aktuelle Verschlüsselungsstufe 1 ist, ist der Wert 2 für *SecurityLayer* ungültig.

<dt>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**RDP-Sicherheitsschicht** (0)


</dt> <dd>

Für die Kommunikation zwischen dem Server und dem Client wird die native RDP-Verschlüsselung verwendet.

</dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Aushandeln** (1)


</dt> <dd>

Die sicherste Ebene, die vom Client unterstützt wird, wird verwendet. Falls unterstützt, wird SSL (TLS 1.0) verwendet.

</dd> <dt>

<span id="SSL"></span><span id="ssl"></span>

<span id="SSL"></span><span id="ssl"></span>**SSL** (2)


</dt> <dd>

SSL (TLS 1.0) wird für die Serverauthentifizierung sowie für die Verschlüsselung aller Daten verwendet, die zwischen dem Server und dem Client übertragen werden. Für diese Einstellung muss der Server über ein SSL-kompatibles Zertifikat verfügen. Diese Einstellung ist nicht mit dem **MinEncryptionLevel-Wert** 1 kompatibel.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt Success bei Erfolg zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Remotedesktopdienste finden Sie unter [Fehlercodes](terminal-services-wmi-provider-error-codes.md) für WMI-Anbieter.

## <a name="remarks"></a>Hinweise

Managed Object Format (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md)
</dt> <dt>

[**SetEncryptionLevel**](win32-tsgeneralsetting-setencryptionlevel.md)
</dt> </dl>

 

