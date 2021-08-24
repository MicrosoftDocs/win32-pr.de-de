---
title: ReactivateServerAutomatic-Methode der Win32_TSLicenseServer-Klasse
description: Reaktiviert den Remotedesktop Lizenzserver mithilfe einer automatischen Verbindung mit dem Internet.
ms.assetid: 98b9b8e5-4de4-418c-9175-58e8b84784d5
ms.tgt_platform: multiple
keywords:
- ReactivateServerAutomatic-Methode Remotedesktopdienste
- ReactivateServerAutomatic-Methode Remotedesktopdienste , Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer-Klasse Remotedesktopdienste , ReactivateServerAutomatic-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ReactivateServerAutomatic
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4e822c441410ae3757f7cdb0a4a714b435facbb20e171646c889e2ea53ec82b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866040"
---
# <a name="reactivateserverautomatic-method-of-the-win32_tslicenseserver-class"></a>ReactivateServerAutomatic-Methode der Win32 \_ TSLicenseServer-Klasse

Reaktiviert den Remotedesktop Lizenzserver mithilfe einer automatischen Verbindung mit dem Internet.

## <a name="syntax"></a>Syntax


```mof
uint32 ReactivateServerAutomatic(
  [in]  uint32 Reason,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Grund* \[ In\]
</dt> <dd>

Grund für die Aktivierung. Dieses Argument einen der folgenden Werte annehmen.

<dt>

0
</dt> <dd>

Der Server wurde erneut bereitgestellt.

</dd> <dt>

1
</dt> <dd>

Das Zertifikat war beschädigt.

</dd> <dt>

2
</dt> <dd>

Der private Schlüssel wurde kompromittiert.

</dd> <dt>

3
</dt> <dd>

Der Aktivierungsschlüssel ist abgelaufen.

</dd> <dt>

4
</dt> <dd>

Der Server wurde aktualisiert.

</dd> </dl> </dd> <dt>

*ActivationStatus* \[ out\]
</dt> <dd>

Der zurückgegebene Aktivierungsstatus kann einer der folgenden Werte sein.

<dt>

0
</dt> <dd>

Der Remotedesktop Lizenzserver wird aktiviert.

</dd> <dt>

1
</dt> <dd>

Der Remotedesktop Lizenzserver ist nicht aktiviert.

</dd> <dt>

2
</dt> <dd>

Unbekannter Fehler aufgetreten. Es ist nicht bekannt, ob der Remotedesktop Lizenzserver aktiviert ist.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufzurufen.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

 

