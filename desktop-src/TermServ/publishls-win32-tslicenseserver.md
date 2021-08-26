---
title: PublishLS-Methode der Win32_TSLicenseServer-Klasse
description: Veröffentlicht den Remotedesktop Lizenzserver in Active Directory Domain Services.
ms.assetid: 726d5dec-e438-455e-adb8-56d646d65d13
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der PublishLS-Methode
- PublishLS-Methode Remotedesktopdienste , Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer-Klasse Remotedesktopdienste , PublishLS-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.PublishLS
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5559fc41e08535142642c64658234902aea22d2a47e6b43add30427fdaec0778
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988830"
---
# <a name="publishls-method-of-the-win32_tslicenseserver-class"></a>PublishLS-Methode der Win32 \_ TSLicenseServer-Klasse

Veröffentlicht den Remotedesktop Lizenzserver in Active Directory Domain Services.

## <a name="syntax"></a>Syntax


```mof
uint32 PublishLS();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Hinweise

Um diese Methode aufzurufen, müssen Sie als Unternehmensadministrator bei der Gesamtstruktur angemeldet sein, in der der Lizenzserver Mitglied ist.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

 

