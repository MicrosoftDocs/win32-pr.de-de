---
title: UnpublishLS-Methode der Win32_TSLicenseServer-Klasse
description: Aufheben der Veröffentlichung Remotedesktop Lizenzservers Active Directory Domain Services.
ms.assetid: 275854e2-85f6-4142-8bce-8d633bfcff7d
ms.tgt_platform: multiple
keywords:
- UnpublishLS-Remotedesktopdienste
- UnpublishLS-Methode Remotedesktopdienste , Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer klasse Remotedesktopdienste , UnpublishLS-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.UnpublishLS
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4990488dba9610dc307878f09fdcf2faab6b61b452aebe9860668aee7d59111a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869000"
---
# <a name="unpublishls-method-of-the-win32_tslicenseserver-class"></a>UnpublishLS-Methode der Win32 \_ TSLicenseServer-Klasse

Aufheben der Veröffentlichung Remotedesktop Lizenzservers Active Directory Domain Services.

## <a name="syntax"></a>Syntax


```mof
uint32 UnpublishLS();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter Remotedesktopdienste [WMI-Anbieterfehlercodes](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Hinweise

Zum Aufrufen dieser Methode müssen Sie als Unternehmensadministrator bei der Gesamtstruktur angemeldet sein, in der der Lizenzserver Mitglied ist.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 

