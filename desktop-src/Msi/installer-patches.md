---
description: Die Eigenschaft schreibgeschützte Patches des Installer-Objekts gibt ein stringlist-Objekt zurück, das alle auf das Produkt angewendeten Patches enthält.
ms.assetid: a8d46073-399b-480e-b4b0-a7a2f832e160
title: Installer. Patches (Eigenschaft)
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
ms.openlocfilehash: fd94c5853b3e455cf4d814dfb3c4078705ac727b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370306"
---
# <a name="installerpatches-property"></a>Installer. Patches (Eigenschaft)

Die Eigenschaft schreibgeschützte **Patches** des [**Installer**](installer-object.md) -Objekts gibt ein [**stringlist**](stringlist-object.md) -Objekt zurück, das alle auf das Produkt angewendeten Patches enthält.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.Patches
```



## <a name="property-value"></a>Eigenschaftswert

Gibt den Produktcode an.

## <a name="remarks"></a>Bemerkungen

Zum Auflisten der Patches durchläuft eine Anwendung das [**stringlist**](stringlist-object.md) -Objekt mithilfe eines for Each-Konstrukts. Da Patches nicht geordnet sind, weist jeder neue Patch einen beliebigen Index auf. Dies bedeutet, dass die Funktion Patches in beliebiger Reihenfolge zurückgeben kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msienumschlag**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> </dl>

 

 




