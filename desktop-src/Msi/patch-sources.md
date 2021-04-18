---
description: Die Sources-Eigenschaft listet alle Quellen für die Patch-Instanz auf. Diese Eigenschaft ruft "msisourcelistenumschlag Sources" auf und gibt ein Array von Zeichen folgen zurück. der Quelltyp wird als Argument akzeptiert.
ms.assetid: 4a052518-4d76-4a95-be9e-7acae36db626
title: Patch. Sources (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.Sources
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 18b9e6ab867d68908bc8dd7e7f87f942f8cd015c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357991"
---
# <a name="patchsources-property"></a>Patch. Sources (Eigenschaft)

Die **Sources** -Eigenschaft listet alle Quellen für die Patch-Instanz auf. Diese Eigenschaft ruft " [**msisourcelistenumschlag sources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) " auf und gibt ein Array von Zeichen folgen zurück. der Quelltyp wird als Argument akzeptiert.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Patch.Sources
```



## <a name="property-value"></a>Eigenschaftswert

Der Typ der aufzuzählenden Quelle. Der Wert kann *msiinstallsourcetymessetwork* (1) oder *msiinstallsourcetypeurl* (2) sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer 3,0 oder höher unter Windows Server 2003, Windows XP und Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ iPatch ist definiert als 000c10a1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Patch**](patch-object.md)
</dt> <dt>

[**Msisourcelistenumschlag Quellen**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)
</dt> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




