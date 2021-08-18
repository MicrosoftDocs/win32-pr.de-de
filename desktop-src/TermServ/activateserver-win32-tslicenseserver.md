---
title: ActivateServer-Methode der Win32_TSLicenseServer Klasse
description: Aktiviert den Remotedesktop Lizenzserver mithilfe eines Remotedesktop Lizenzserverbezeichners, der über das Telefon oder das Internet ermittelt wird.
ms.assetid: 628e87f0-600e-404d-a0b4-35f1570b4fc0
ms.tgt_platform: multiple
keywords:
- ActivateServer-Remotedesktopdienste
- ActivateServer-Methode Remotedesktopdienste , Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer klasse Remotedesktopdienste , ActivateServer-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ActivateServer
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86ba3e231da50c9103361b2cf22cbd44d7311a26a4ea36f9a32185ed0c32d408
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872070"
---
# <a name="activateserver-method-of-the-win32_tslicenseserver-class"></a>ActivateServer-Methode der Win32 \_ TSLicenseServer-Klasse

Aktiviert den Remotedesktop Lizenzserver mithilfe eines Remotedesktop Lizenzserverbezeichners, der über das Telefon oder das Internet ermittelt wird.

## <a name="syntax"></a>Syntax


```mof
uint32 ActivateServer(
  [in]  string sLicenseServerId,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sLicenseServerId* \[ In\]
</dt> <dd>

Remotedesktop Lizenzserver-ID, die über das Telefon oder das Internet erhalten wurde. Der *sLicenseServerId-Parameter* ist eine alphanumerische Zeichenfolge mit 35 Zeichen, die keine Bindestriche enthalten darf.

</dd> <dt>

*ActivationStatus* \[ out\]
</dt> <dd>

Der zurückgegebene Aktivierungsstatus kann einer der folgenden sein.

<dt>

0
</dt> <dd>

Der Remotedesktop Lizenzserver ist aktiviert.

</dd> <dt>

1
</dt> <dd>

Der Remotedesktop Lizenzserver ist nicht aktiviert.

</dd> <dt>

2
</dt> <dd>

Unbekannter Fehler aufgetreten. Es ist nicht bekannt, ob Remotedesktop Lizenzserver aktiviert ist.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter Remotedesktopdienste [WMI-Anbieterfehlercodes](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufrufen zu können.

Managed Object Format (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 

