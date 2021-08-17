---
description: Die State-Eigenschaft gibt den Installationsstatus dieser Instanz des Patches zurück.
ms.assetid: b01b2839-d867-4353-99d0-8c612cd1eb0c
title: Patch.State-Eigenschaft
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
ms.openlocfilehash: b28eee03cfc74537c8be7669124a4f70db40ca88196678889553978232c934c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942290"
---
# <a name="patchstate-property"></a>Patch.State-Eigenschaft

Die **State-Eigenschaft** gibt den Installationsstatus dieser Instanz des Patches zurück.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Patch.State
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Hinweise

Diese Eigenschaft gibt einen der folgenden Werte zurück.



| Installationsstatus        | Bedeutung                                                      |
|---------------------------|--------------------------------------------------------------|
| MSIPATCHSTATE \_ ANGEWENDET    | Patch wird auf diese Produktinstanz angewendet.                   |
| MSIPATCHSTATE \_ ABGELÖST | Patch wird auf diese Produktinstanz angewendet, aber ersetzt. |
| MSIPATCHSTATE \_ VERALTET  | Patch wird in dieser Produktinstanz angewendet, ist aber veraltet.      |



 

Diese Methode kann ERROR \_ UNKNOWN \_ PATCH zurückgeben, wenn das [**Patch-Objekt**](patch-object.md) mit einer leeren Zeichenfolge für *ProductCode* initialisiert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm 3.0 oder höher auf Windows Server 2003, Windows XP und Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IPatch ist als 000C10A1-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Patch**](patch-object.md)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




