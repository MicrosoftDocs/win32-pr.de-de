---
description: Die schreibgeschützte Patches-Eigenschaft des Installer-Objekts gibt ein StringList-Objekt zurück, das alle auf das Produkt angewendeten Patches enthält.
ms.assetid: a8d46073-399b-480e-b4b0-a7a2f832e160
title: Installer.Patches (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Patches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 33576b92924493a99c058196639faa34f5b42e388b9e30b6e300c17444ddeeff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430780"
---
# <a name="installerpatches-property"></a>Installer.Patches (Eigenschaft)

Die schreibgeschützte **Patches-Eigenschaft** des [**Installer-Objekts**](installer-object.md) gibt ein [**StringList-Objekt**](stringlist-object.md) zurück, das alle auf das Produkt angewendeten Patches enthält.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.Patches
```



## <a name="property-value"></a>Eigenschaftswert

Gibt den Produktcode an.

## <a name="remarks"></a>Hinweise

Um die Patches aufzählen zu können, durchgibt eine Anwendung das [**StringList-Objekt**](stringlist-object.md) mithilfe eines For Each-Konstrukts. Da Patches nicht geordnet sind, verfügt jeder neue Patch über einen beliebigen Index. Dies bedeutet, dass die Funktion Patches in beliebiger Reihenfolge zurückgeben kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MsiEnumPatches**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> </dl>

 

 




