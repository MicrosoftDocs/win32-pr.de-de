---
title: IsLSSecGrpGPEnabled-Methode der Win32_TSLicenseServer-Klasse
description: Ruft ab, ob die \0034;Lizenzserver-Sicherheitsgruppe \ 0034; Die Gruppenrichtlinieneinstellung ist auf dem Remotedesktop Lizenzserver aktiviert.
ms.assetid: 715b619b-f082-4fed-ac4c-70d5e286e37c
ms.tgt_platform: multiple
keywords:
- IsLSSecGrpGPEnabled-Methode Remotedesktopdienste
- IsLSSecGrpGPEnabled-Methode Remotedesktopdienste , Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer-Klasse Remotedesktopdienste , IsLSSecGrpGPEnabled-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSSecGrpGPEnabled
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 688843106583ea0ca32a3cc8ac7142d51aac737ad6722ab4ef95621b63b66eb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138363"
---
# <a name="islssecgrpgpenabled-method-of-the-win32_tslicenseserver-class"></a>IsLSSecGrpGPEnabled-Methode der Win32 \_ TSLicenseServer-Klasse

Ruft ab, ob die Gruppenrichtlinieneinstellung "Lizenzserversicherheitsgruppe" auf dem Remotedesktop Lizenzserver aktiviert ist.

## <a name="syntax"></a>Syntax


```mof
uint32 IsLSSecGrpGPEnabled(
  [out] boolean Enabled
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Aktiviert* \[ out\]
</dt> <dd>

Boolescher Wert, der angibt, ob die Richtlinieneinstellung "Lizenzserversicherheitsgruppe" aktiviert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufzurufen.

Mit der Richtlinieneinstellung "Lizenzserversicherheitsgruppe" können Sie die Remotedesktop-Sitzungshost -Server (RD-Sitzungshost) angeben, die den Lizenzserver kontaktieren dürfen, um Remotedesktopdienste Clientzugriffslizenzen (RDS CALs) zu erhalten. Wenn die Richtlinieneinstellung auf dem Lizenzserver aktiviert ist, antwortet der Server nur auf RDS CAL-Anforderungen von RD-Sitzungshost Servern, deren Computerkonten Mitglieder der lokalen Gruppe Terminalservercomputer auf dem Lizenzserver sind.

Die Richtlinieneinstellung befindet sich im folgenden Knoten des editors für lokale Gruppenrichtlinien:

TS-Lizenzierung für \\ \\ Computerkonfiguration Administrative Vorlagen Windows-Komponententerminaldienste \\ \\

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
</dt> </dl>

 

