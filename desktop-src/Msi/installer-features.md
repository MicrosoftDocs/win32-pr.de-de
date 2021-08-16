---
description: Die Features-Eigenschaft ist eine schreibgeschützte Eigenschaft, die ein StringList-Objekt zurückgibt, das den Satz veröffentlichter Features für das angegebene Produkt auflistet.
ms.assetid: feb8f09a-fa97-4fee-9082-8f04288af22f
title: Installer.Features-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Features
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e31dfe2c487a151280a10c4fa7222c005f94c0eeb4ac4f3f5145d67ab600fe9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118631472"
---
# <a name="installerfeatures-property"></a>Installer.Features-Eigenschaft

Die **Features-Eigenschaft** ist eine schreibgeschützte Eigenschaft, die ein [**StringList-Objekt**](stringlist-object.md) zurückgibt, das den Satz veröffentlichter Features für das angegebene Produkt auflistet.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.Features
```



## <a name="property-value"></a>Eigenschaftswert

Gibt den Produktcode des Produkts an.

## <a name="remarks"></a>Hinweise

Um die Features aufzulisten, durchläuft eine Anwendung das [**StringList-Objekt**](stringlist-object.md) mithilfe eines For Each-Konstrukts. Da Features nicht sortiert sind, verfügt jedes neue Feature über einen beliebigen Index, was bedeutet, dass die Funktion Features in beliebiger Reihenfolge zurückgeben kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa)
</dt> <dt>

[Systemstatusfunktionen](installer-function-reference.md)
</dt> </dl>

 

 




