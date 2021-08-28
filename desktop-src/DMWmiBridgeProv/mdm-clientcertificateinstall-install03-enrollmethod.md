---
title: EnrollMethod-Methode der MDM_ClientCertificateInstall_Install03-Klasse
description: Löst das Gerät aus, um die Zertifikatregistrierung zu starten.
ms.assetid: 21a31574-0b19-44bf-90db-4bb9e2611364
keywords:
- EnrollMethod-Methode
- EnrollMethod-Methode, MDM_ClientCertificateInstall_Install03-Klasse
- MDM_ClientCertificateInstall_Install03-Klasse, EnrollMethod-Methode
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
ms.openlocfilehash: 1ddeca621f58015aa3806212c1250aeb43554a51cbb28e15414e779571b9c102
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109400"
---
# <a name="enrollmethod-method-of-the-mdm_clientcertificateinstall_install03-class"></a>EnrollMethod-Methode der \_ MDM-Klasse "ClientCertificateInstall \_ Install03"

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Löst das Gerät aus, um die Zertifikatregistrierung zu starten. Das Gerät benachrichtigt den MDM-Server nicht, nachdem die Zertifikatregistrierung abgeschlossen ist. Der MDM-Server kann das Gerät später abfragen, um herauszufinden, ob ein neues Zertifikat hinzugefügt wird. Weitere Informationen finden Sie unter [**Registrieren von**](/windows/client-management/mdm/clientcertificateinstall-csp).

## <a name="syntax"></a>Syntax


```mof
uint32 EnrollMethod();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Erforderlich. Löst das Gerät aus, um die Zertifikatregistrierung zu starten. Das Gerät benachrichtigt den MDM-Server nicht, nachdem die Zertifikatregistrierung abgeschlossen ist. Der MDM-Server kann das Gerät später abfragen, um herauszufinden, ob ein neues Zertifikat hinzugefügt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                      |
| Namespace<br/>                | Root \\ cimv2 \\ mdm \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MDM \_ ClientCertificateInstall \_ Install03**](mdm-clientcertificateinstall-install03.md)
</dt> <dt>

[Verwenden von PowerShell-Skripts mit dem WMI-Bridge-Anbieter](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

