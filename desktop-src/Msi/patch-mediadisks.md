---
description: Die Media Disks-Eigenschaft listet alle Medien Datenträger für diese Produkt Instanz auf. Diese Eigenschaft ruft msisourcelistenumschlag mediadisks auf. Gibt die Datenträger Informationen als Array von Datensatz-Objekten zurück.
ms.assetid: 02faf211-16c8-4d2f-b192-c2ce8f3f2c66
title: Patch. mediadisks (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.MediaDisks
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 40353ecce95cb0c4eb69228b004623bbb87c904e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369385"
---
# <a name="patchmediadisks-property"></a>Patch. mediadisks (Eigenschaft)

Die Media **Disks** -Eigenschaft listet alle Medien Datenträger für diese Produkt Instanz auf. Diese Eigenschaft ruft [**msisourcelistenumschlag mediadisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)auf. Gibt die Datenträger Informationen als Array von [**Datensatz**](record-object.md) -Objekten zurück.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Patch.MediaDisks
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

In jedem Datensatz enthält das erste Feld die Datenträger-ID, das zweite Feld enthält die Volumebezeichnung, und das dritte Feld enthält die für den Datenträger registrierte Datenträger Aufforderung.

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

[**Msisourcelistenumschlag mediadisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)
</dt> <dt>

[**Datensatz**](record-object.md)
</dt> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




