---
title: AddLStoTSLSGroup-Methode der Win32_TSLicenseServer-Klasse
description: Fügt den Remotedesktop Lizenzserver der Lizenzservergruppe Remotedesktopverbindung Broker (RD-Verbindungsbroker) auf einem Domänencontroller in derselben Domäne wie der Remotedesktop Lizenzserver hinzu.
ms.assetid: 65c6b7cf-324a-44f1-8dfc-40e35ed45d4f
ms.tgt_platform: multiple
keywords:
- AddLStoTSLSGroup-Methode Remotedesktopdienste
- AddLStoTSLSGroup-Methode Remotedesktopdienste , Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer-Klasse Remotedesktopdienste , AddLStoTSLSGroup-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.AddLStoTSLSGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf3d0464b42159ca1827caf579e21982c08d066495cd664ec1adfcaa883a4b16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610405"
---
# <a name="addlstotslsgroup-method-of-the-win32_tslicenseserver-class"></a>AddLStoTSLSGroup-Methode der Win32 \_ TSLicenseServer-Klasse

Fügt den Remotedesktop Lizenzserver der Lizenzservergruppe Remotedesktopverbindung Broker (RD-Verbindungsbroker) auf einem Domänencontroller in derselben Domäne wie der Remotedesktop Lizenzserver hinzu.

## <a name="syntax"></a>Syntax


```mof
uint32 AddLStoTSLSGroup();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Domänenadministratoren sein, um diese Methode aufzurufen.

Der Lizenzserver sollte Mitglied der Gruppe Remotedesktop Lizenzserver sein, wenn der Server für die Verwendung des Domänen- oder Gesamtstrukturermittlungsbereichs konfiguriert ist.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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
</dt> <dt>

[**IsLSinTSLSGroup**](islsintslsgroup-win32-tslicenseserver.md)
</dt> </dl>

 

