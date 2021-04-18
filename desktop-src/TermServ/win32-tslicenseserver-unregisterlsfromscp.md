---
title: Unregisterlsfromscp-Methode der Win32_TSLicenseServer-Klasse
description: Entfernt den Remotedesktop-Lizenzserver als Dienst Verbindungspunkt in Active Directory Domain Services.
ms.assetid: 3EE6F272-A99F-49EF-BDED-D8C2C641D45B
ms.tgt_platform: multiple
keywords:
- Unregisterlsfromscp-Methode Remotedesktopdienste
- Unregisterlsfromscp-Methode Remotedesktopdienste, Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer-Klasse Remotedesktopdienste, unregisterlsfromscp-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.UnRegisterLSFromSCP
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d365b0f3e64c57fba9447d8658c3a955b6e92f73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340783"
---
# <a name="unregisterlsfromscp-method-of-the-win32_tslicenseserver-class"></a>Unregisterlsfromscp-Methode der Win32- \_ Klasse "zlicenseserver"

Entfernt den Remotedesktop-Lizenzserver als Dienst Verbindungspunkt in Active Directory Domain Services.

## <a name="syntax"></a>Syntax


```mof
uint32 UnRegisterLSFromSCP();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Bemerkungen

Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                         |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>Tltaumiprov. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ Lizenznehmer**](win32-tslicenseserver.md)
</dt> </dl>

 

