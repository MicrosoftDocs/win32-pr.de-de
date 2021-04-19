---
description: Die ShortcutTarget-Eigenschaft des Installer-Objekts überprüft eine Verknüpfung und gibt, sofern verfügbar, das Produkt, den Funktionsnamen und die Komponente zurück.
ms.assetid: fd7a1d34-3013-4419-af92-0a0162c93494
title: Installer. ShortcutTarget-Eigenschaft
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
ms.openlocfilehash: 1c53d43188af9ed8f58ddd54916761e346f1bad1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370784"
---
# <a name="installershortcuttarget-property"></a>Installer. ShortcutTarget-Eigenschaft

Die **ShortcutTarget** -Eigenschaft des [**Installer**](installer-object.md) -Objekts überprüft eine Verknüpfung und gibt, sofern verfügbar, das Produkt, den Funktionsnamen und die Komponente zurück.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.ShortcutTarget
```



## <a name="property-value"></a>Eigenschaftswert

Vollständiger Pfad und Dateiname für die Datei.

## <a name="remarks"></a>Bemerkungen

ShortcutTarget gibt ein [**Daten Satz Objekt**](record-object.md) zurück, das drei Felder enthält:

-   Field 1 ist eine GUID für den Produktcode der Verknüpfung, falls verfügbar. Dieses Feld kann NULL sein.
-   Feld 2 ist die Funktions-ID der Verknüpfung, falls verfügbar. Dieses Feld kann NULL sein.
-   Field 3 ist eine GUID für den Komponenten Code, falls verfügbar. Dieses Feld kann NULL sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)
</dt> <dt>

[**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)
</dt> </dl>

 

 




