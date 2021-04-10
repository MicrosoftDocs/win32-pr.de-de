---
title: Setsecuritylayer-Methode der Win32_TSGeneralSetting-Klasse
description: Die setsecuritylayer-Methode legt die Sicherheitsebene fest.
ms.assetid: 3b894494-2180-4f1d-8e67-a66c679d286c
ms.tgt_platform: multiple
keywords:
- Setsecuritylayer-Methode Remotedesktopdienste
- Setsecuritylayer-Methode Remotedesktopdienste, Win32_TSGeneralSetting-Klasse
- Win32_TSGeneralSetting-Klasse Remotedesktopdienste, setsecuritylayer-Methode
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
ms.openlocfilehash: b5e04c3f7e5a58ec8de345d570e36b35c7eb1e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956567"
---
# <a name="setsecuritylayer-method-of-the-win32_tsgeneralsetting-class"></a>Setsecuritylayer-Methode der Win32- \_ Klasse "zgeneralsetting"

Die **setsecuritylayer** -Methode legt die Sicherheitsebene fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetSecurityLayer(
  [in] uint32 SecurityLayer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Securitylayer* \[ in\]
</dt> <dd>

Die festzulegende Sicherheitsebene. Wenn die aktuelle Verschlüsselungs Stufe 1 ist, ist der Wert 2 für *securitylayer* ungültig.

<dt>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**RDP-Sicherheitsebene** (0)


</dt> <dd>

Bei der Kommunikation zwischen dem Server und dem Client wird die Native RDP-Verschlüsselung verwendet.

</dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Aushandeln** (1)


</dt> <dd>

Die sicherste Ebene, die vom Client unterstützt wird, wird verwendet. Wenn unterstützt, wird SSL (TLS 1,0) verwendet.

</dd> <dt>

<span id="SSL"></span><span id="ssl"></span>

<span id="SSL"></span><span id="ssl"></span>**SSL** (2)


</dt> <dd>

SSL (TLS 1,0) wird für die Server Authentifizierung sowie für die Verschlüsselung aller Daten verwendet, die zwischen dem Server und dem Client übertragen werden. Diese Einstellung erfordert, dass der Server über ein SSL-kompatibles Zertifikat verfügt. Diese Einstellung ist nicht kompatibel mit dem **minverschlüsseltionlevel** -Wert 1.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg Erfolg zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .

## <a name="remarks"></a>Bemerkungen

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tscsgwmi. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32-Einstellung für "" \_**](win32-tsgeneralsetting.md)
</dt> <dt>

[**Setencryptionlevel**](win32-tsgeneralsetting-setencryptionlevel.md)
</dt> </dl>

 

