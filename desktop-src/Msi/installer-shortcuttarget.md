---
description: Die ShortcutTarget-Eigenschaft des Installer-Objekts untersucht eine Verknüpfung und gibt das Produkt, den Funktionsnamen und die Komponente zurück, sofern verfügbar.
ms.assetid: fd7a1d34-3013-4419-af92-0a0162c93494
title: Installer.ShortcutTarget-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ShortcutTarget
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b54e334314c0bfd0fb721b175d0a14894d8a509ea02ff36e324903bb1fdbffaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894000"
---
# <a name="installershortcuttarget-property"></a>Installer.ShortcutTarget-Eigenschaft

Die **ShortcutTarget-Eigenschaft** des [**Installer-Objekts**](installer-object.md) untersucht eine Verknüpfung und gibt das Produkt, den Funktionsnamen und die Komponente zurück, sofern verfügbar.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.ShortcutTarget
```



## <a name="property-value"></a>Eigenschaftswert

Vollständiger Pfad und Dateiname für die Datei.

## <a name="remarks"></a>Hinweise

ShortcutTarget gibt ein [**Record-Objekt**](record-object.md) zurück, das drei Felder enthält:

-   Feld 1 ist eine GUID für den Produktcode der Verknüpfung, sofern verfügbar. Dieses Feld kann NULL sein.
-   Feld 2 ist die Funktions-ID der Verknüpfung, sofern verfügbar. Dieses Feld kann NULL sein.
-   Feld 3 ist eine GUID für den Komponentencode, sofern verfügbar. Dieses Feld kann NULL sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)
</dt> <dt>

[**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)
</dt> </dl>

 

 




