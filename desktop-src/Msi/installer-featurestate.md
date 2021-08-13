---
description: Die schreibgeschützte FeatureState-Eigenschaft gibt den installierten Zustand eines Features zurück.
ms.assetid: a3d30296-191e-4446-b5b1-a92f8991926a
title: Installer.FeatureState-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 989abe860848b943e77b02910e9760f8fcaecc97fd8a2634f8147605577613d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118631274"
---
# <a name="installerfeaturestate-property"></a>Installer.FeatureState-Eigenschaft

Die schreibgeschützte **FeatureState-Eigenschaft** gibt den installierten Zustand eines Features zurück.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.FeatureState
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Hinweise

Diese Eigenschaft gibt einen der folgenden Werte zurück.



| Wert                     | Beschreibung                                      |
|---------------------------|--------------------------------------------------|
| msiInstallStateAbsent     | Das Feature ist nicht installiert.                    |
| msiInstallStateAdvertised | Das Feature wird angekündigt.                       |
| msiInstallStateLocal      | Das Feature wird installiert, um lokal ausgeführt zu werden.         |
| msiInstallStateSource     | Das Feature wird installiert, um von der Quelle aus ausgeführt zu werden.     |
| msiInstallStateInvalidArg | Ein ungültiger Parameter wurde an die Funktion übergeben. |
| msiInstallStateUnknown    | Der Produktcode oder die Feature-ID ist unbekannt.       |
| msiInstallStateBadConfig  | Die Konfigurationsdaten sind beschädigt.               |



 

 

Die **FeatureState-Eigenschaft** überprüft nicht, ob auf das Feature zugegriffen werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea)
</dt> </dl>

 

 




