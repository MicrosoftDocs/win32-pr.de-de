---
description: Die State-Eigenschaft gibt den Installationsstatus dieser patchinstanz zurück.
ms.assetid: b01b2839-d867-4353-99d0-8c612cd1eb0c
title: Patch. State (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.State
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f903ec66c2d55567fee9ccbc123e018e1dc7bacb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354754"
---
# <a name="patchstate-property"></a>Patch. State (Eigenschaft)

Die **State** -Eigenschaft gibt den Installationsstatus dieser patchinstanz zurück.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Patch.State
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gibt einen der folgenden Werte zurück.



| Installationsstatus        | Bedeutung                                                      |
|---------------------------|--------------------------------------------------------------|
| msipatchstate \_ angewendet    | Patch wird auf diese Produkt Instanz angewendet.                   |
| msipatchstate \_ abgelöst | Patch wird auf diese Produkt Instanz angewendet, aber ersetzt. |
| "msipatchstate" ist \_ veraltet.  | Patch wird in dieser Produkt Instanz, aber veraltet, angewendet.      |



 

Diese Methode kann den Fehler "Unbekannter Patch" zurückgeben \_ \_ , wenn das [**Patch**](patch-object.md) -Objekt mit einer leeren Zeichenfolge für " *ProductCode*" initialisiert wird.

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

[**Msigetpatchinfoex**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




