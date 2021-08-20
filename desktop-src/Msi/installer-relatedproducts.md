---
description: Die schreibgeschützte RelatedProducts-Eigenschaft gibt ein StringList-Objekt zurück, das den Satz aller Für den aktuellen Benutzer und Computer installierten oder angekündigten Produkte mit einer angegebenen UpgradeCode-Eigenschaft in der zugehörigen Property-Tabelle auflistet.
ms.assetid: 0316e536-ccd4-4d7a-9c49-66e6c4a07f1c
title: Installer.RelatedProducts-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RelatedProducts
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 15e84a063b8f094dbeee02f3000bdd1c69356f5fa664f6e6f6aff87d19d07dd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946138"
---
# <a name="installerrelatedproducts-property"></a>Installer.RelatedProducts-Eigenschaft

Die schreibgeschützte **RelatedProducts-Eigenschaft** gibt ein [**StringList-Objekt**](stringlist-object.md) zurück, das den Satz aller Für den aktuellen Benutzer und Computer installierten oder angekündigten Produkte mit einer angegebenen [**UpgradeCode-Eigenschaft**](upgradecode.md) in der [Property-Tabelle](property-table.md)auflistet.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.RelatedProducts
```



## <a name="property-value"></a>Eigenschaftswert

Der Upgradecode verwandter Produkte, die das Installationsprogramm aufzählt.

## <a name="remarks"></a>Hinweise

Um die zugehörigen Produkte aufzulisten, durchläuft eine Anwendung die [**StringList**](stringlist-object.md) mithilfe eines For Each-Konstrukts. Da verwandte Produkte nicht bestellt werden, verfügt jedes neue verwandte Produkt über einen beliebigen Index. Dies bedeutet, dass die Funktion verwandte Produkte in beliebiger Reihenfolge zurückgeben kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MsiEnumRelatedProducts**](/windows/desktop/api/Msi/nf-msi-msienumrelatedproductsa)
</dt> </dl>

 

 




