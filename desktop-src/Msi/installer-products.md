---
description: Die Products-Eigenschaft ist eine schreibgeschützte Eigenschaft, die ein stringlist-Objekt zurückgibt, das den Satz aller Produkte auflistet, die für den aktuellen Benutzer und Computer installiert oder angekündigt wurden.
ms.assetid: 5c210827-a7cc-4358-bfe6-4d8e9767bd8c
title: Installer. Products (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Products
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8d5b20a770154382e7e7a68cc3fe4d81c350fb1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354183"
---
# <a name="installerproducts-property"></a>Installer. Products (Eigenschaft)

Die **Products** -Eigenschaft ist eine schreibgeschützte Eigenschaft, die ein [**stringlist**](stringlist-object.md) -Objekt zurückgibt, das den Satz aller Produkte auflistet, die für den aktuellen Benutzer und Computer installiert oder angekündigt wurden.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.Products
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

Zum Auflisten der Produkte durchläuft eine Anwendung das [**stringlist**](stringlist-object.md) -Objekt mithilfe eines for Each-Konstrukts. Da Produkte nicht geordnet sind, weist jedes neue Produkt einen beliebigen Index auf. Dies bedeutet, dass die Funktion Produkte in beliebiger Reihenfolge zurückgeben kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msienumschlag Produkte**](/windows/desktop/api/Msi/nf-msi-msienumproductsa)
</dt> </dl>

 

 




