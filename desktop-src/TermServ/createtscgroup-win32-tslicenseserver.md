---
title: CreateTSCGroup-Methode der Win32_TSLicenseServer Klasse
description: CreateTSCGroup ist ab diesem Zeitraum nicht mehr Windows Server 2012.
ms.assetid: 31751da7-263b-4911-a328-246457a606f0
ms.tgt_platform: multiple
keywords:
- CreateTSCGroup-Remotedesktopdienste
- CreateTSCGroup-Methode Remotedesktopdienste , Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer klasse Remotedesktopdienste , CreateTSCGroup-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.CreateTSCGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf363d86cf663a3f9b626d9586140eb4c00f86e9750070f8a2000149b655bb34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737870"
---
# <a name="createtscgroup-method-of-the-win32_tslicenseserver-class"></a>CreateTSCGroup-Methode der Win32 \_ TSLicenseServer-Klasse

\[**CreateTSCGroup** ist ab diesem Zeitraum nicht mehr Windows Server 2012.\]

Diese Methode wird nicht unterstützt.

**Windows Server 2008 R2 und Windows Server 2008:** Erstellt die lokale Gruppe Terminalservercomputer auf dem Remotedesktop Lizenzserver.

## <a name="syntax"></a>Syntax


```mof
uint32 CreateTSCGroup();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt **WBEM \_ E NOT SUPPORTED \_ \_ zurück.**

**Windows Server 2008 R2 und Windows Server 2008:** Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter Remotedesktopdienste [WMI-Anbieterfehlercodes](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufrufen zu können.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> <dt>

[**IsTSCGroupPresent**](istscgrouppresent-win32-tslicenseserver.md)
</dt> </dl>

 

