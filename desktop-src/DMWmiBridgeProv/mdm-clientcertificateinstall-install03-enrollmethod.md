---
title: Methode der Registrierungsmethode der MDM_ClientCertificateInstall_Install03-Klasse
description: Hiermit wird das Gerät ausgelöst, um die Zertifikat Registrierung zu starten.
ms.assetid: 21a31574-0b19-44bf-90db-4bb9e2611364
keywords:
- Methode der Registrierungsmethode
- Methode der Registrierungsmethode, MDM_ClientCertificateInstall_Install03-Klasse
- MDM_ClientCertificateInstall_Install03-Klasse, Methode der Registrierungsmethode
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_Install03.EnrollMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7903407d5a97f056835e529eb21408bdcbe800ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742640"
---
# <a name="enrollmethod-method-of-the-mdm_clientcertificateinstall_install03-class"></a>Methode der Registrierungsmethode der MDM \_ \_ clientcertifiInstall03-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Hiermit wird das Gerät ausgelöst, um die Zertifikat Registrierung zu starten. Das Gerät benachrichtigt den MDM-Server nicht, nachdem die Zertifikat Registrierung durchgeführt wurde. Der MDM-Server könnte das Gerät später Abfragen, um herauszufinden, ob ein neues Zertifikat hinzugefügt wird. Siehe auch, [**registrieren**](/windows/client-management/mdm/clientcertificateinstall-csp).

## <a name="syntax"></a>Syntax


```mof
uint32 EnrollMethod();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Erforderlich. Hiermit wird das Gerät ausgelöst, um die Zertifikat Registrierung zu starten. Das Gerät benachrichtigt den MDM-Server nicht, nachdem die Zertifikat Registrierung durchgeführt wurde. Der MDM-Server könnte das Gerät später Abfragen, um herauszufinden, ob ein neues Zertifikat hinzugefügt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                      |
| Namespace<br/>                | Root \\ CIMV2 \\ MDM- \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>Dmwmibridgeprov. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MDM \_ clientcertifi-einstall \_ Install03**](mdm-clientcertificateinstall-install03.md)
</dt> <dt>

[Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

