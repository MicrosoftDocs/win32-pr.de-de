---
description: Die schreibgeschützte RelatedProducts-Eigenschaft gibt ein stringlist-Objekt zurück, das den Satz aller Produkte auflistet, die für den aktuellen Benutzer und Computer mit einer angegebenen UpgradeCode-Eigenschaft in der Eigenschaften Tabelle installiert oder angekündigt wurden.
ms.assetid: 0316e536-ccd4-4d7a-9c49-66e6c4a07f1c
title: Installer. RelatedProducts (Eigenschaft)
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
ms.openlocfilehash: fb30be6ea5250a90ef8aa18065e9be679946e503
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361678"
---
# <a name="installerrelatedproducts-property"></a>Installer. RelatedProducts (Eigenschaft)

Die schreibgeschützte **RelatedProducts** -Eigenschaft gibt ein [**stringlist**](stringlist-object.md) -Objekt zurück, das den Satz aller Produkte auflistet, die für den aktuellen Benutzer und Computer mit einer angegebenen [**UpgradeCode**](upgradecode.md) -Eigenschaft in der [Eigenschaften Tabelle](property-table.md)installiert oder angekündigt wurden.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.RelatedProducts
```



## <a name="property-value"></a>Eigenschaftswert

Der UpgradeCode verwandter Produkte, die das Installationsprogramm auflistet.

## <a name="remarks"></a>Bemerkungen

Zum Auflisten der zugehörigen Produkte durchläuft eine Anwendung die [**stringlist**](stringlist-object.md) mithilfe eines for Each-Konstrukts. Da Verwandte Produkte nicht geordnet sind, weist jedes neue verwandte Produkt einen beliebigen Index auf. Dies bedeutet, dass die Funktion Verwandte Produkte in beliebiger Reihenfolge zurückgeben kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msienumrelatedproducts**](/windows/desktop/api/Msi/nf-msi-msienumrelatedproductsa)
</dt> </dl>

 

 




