---
description: Die schreibgeschützte featurestate-Eigenschaft gibt den installierten Zustand einer Funktion zurück.
ms.assetid: a3d30296-191e-4446-b5b1-a92f8991926a
title: Installer. featurestate (Eigenschaft)
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
ms.openlocfilehash: cf6fe61899ea1daac37fd678e9f0e70dfcc3af69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365185"
---
# <a name="installerfeaturestate-property"></a>Installer. featurestate (Eigenschaft)

Die schreibgeschützte **featurestate** -Eigenschaft gibt den installierten Zustand einer Funktion zurück.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.FeatureState
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gibt einen der folgenden Werte zurück.



| Wert                     | BESCHREIBUNG                                      |
|---------------------------|--------------------------------------------------|
| msiinstallstatemissing     | Das Feature ist nicht installiert.                    |
| msiinstallstateangekündigten | Die Funktion wird angekündigt.                       |
| msiinstallstatuelocal      | Das Feature wird für die lokale Installation installiert.         |
| msiinstallstaatource     | Das Feature wird zum Ausführen von der Quelle installiert.     |
| msiinstallstatueingevalidarg | An die Funktion wurde ein ungültiger Parameter übergeben. |
| msiinstallstateunknown    | Der Produktcode oder die featurekennung ist unbekannt.       |
| msiinstallstatebadconfig  | Die Konfigurationsdaten sind beschädigt.               |



 

 

Die **featurestate** -Eigenschaft überprüft nicht, ob auf die Funktion zugegriffen werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea)
</dt> </dl>

 

 




