---
description: Die Features-Eigenschaft ist eine schreibgeschützte Eigenschaft, die ein stringlist-Objekt zurückgibt, das den Satz veröffentlichter Funktionen für das angegebene Produkt auflistet.
ms.assetid: feb8f09a-fa97-4fee-9082-8f04288af22f
title: Installer. Features (Eigenschaft)
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
ms.openlocfilehash: 4f63ce80249fb8bd24d70f92e72c44420a13d798
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360285"
---
# <a name="installerfeatures-property"></a>Installer. Features (Eigenschaft)

Die **Features** -Eigenschaft ist eine schreibgeschützte Eigenschaft, die ein [**stringlist**](stringlist-object.md) -Objekt zurückgibt, das den Satz veröffentlichter Funktionen für das angegebene Produkt auflistet.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.Features
```



## <a name="property-value"></a>Eigenschaftswert

Gibt den Produktcode des Produkts an.

## <a name="remarks"></a>Bemerkungen

Um die Funktionen aufzulisten, durchläuft eine Anwendung das [**stringlist**](stringlist-object.md) -Objekt mithilfe eines for Each-Konstrukts. Da Features nicht sortiert sind, verfügt jede neue Funktion über einen beliebigen Index, was bedeutet, dass die Funktion Funktionen in beliebiger Reihenfolge zurückgeben kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msienumschlag-Features**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa)
</dt> <dt>

[System Status Funktionen](installer-function-reference.md)
</dt> </dl>

 

 




