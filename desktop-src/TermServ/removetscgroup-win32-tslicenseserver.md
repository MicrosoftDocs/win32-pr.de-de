---
title: RemoveTSCGroup-Methode der Win32_TSLicenseServer-Klasse
description: RemoveTSCGroup ist ab Windows Server 2012 nicht mehr für die Verwendung verfügbar.
ms.assetid: e5e3eca9-4990-4322-b41d-c6b6b3356272
ms.tgt_platform: multiple
keywords:
- RemoveTSCGroup-Methode Remotedesktopdienste
- RemoveTSCGroup-Methode Remotedesktopdienste , Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer Klasse Remotedesktopdienste , RemoveTSCGroup-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.RemoveTSCGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebcd3c0eacb54a14675d2794f1c42f8e7a18cd9ea78c7f6369ef883cc3d9fad3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127505"
---
# <a name="removetscgroup-method-of-the-win32_tslicenseserver-class"></a>RemoveTSCGroup-Methode der Win32 \_ TSLicenseServer-Klasse

\[**RemoveTSCGroup** ist ab Windows Server 2012 nicht mehr für die Verwendung verfügbar.\]

Diese Methode wird nicht unterstützt.

**Windows Server 2008 R2 und Windows Server 2008:** Entfernt die lokale Gruppe Terminalservercomputer vom Remotedesktop Lizenzserver.

## <a name="syntax"></a>Syntax


```mof
uint32 RemoveTSCGroup();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt **WBEM \_ E NICHT UNTERSTÜTZT \_ \_ zurück.**

**Windows Server 2008 R2 und Windows Server 2008:** Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufzurufen.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Ende des Supports (Client)<br/>    | Nicht unterstützt<br/>                                                                 |
| Ende des Supports (Server)<br/>    | Windows Server 2008 R2<br/>                                                         |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> <dt>

[**IsTSCGroupPresent**](istscgrouppresent-win32-tslicenseserver.md)
</dt> </dl>

 

