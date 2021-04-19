---
description: Die Eigenschaft schreibgeschützte Komponenten gibt ein stringlist-Objekt zurück, das den Satz der installierten Komponenten für alle Produkte auflistet.
ms.assetid: c84e4329-428a-440a-bd65-097588a86932
title: Installer. Components (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Components
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e6767be5182b15836c071bf8b00ed8441f6031dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368651"
---
# <a name="installercomponents-property"></a>Installer. Components (Eigenschaft)

Die Eigenschaft schreibgeschützte **Komponenten** gibt ein [**stringlist**](stringlist-object.md) -Objekt zurück, das den Satz der installierten Komponenten für alle Produkte auflistet.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.Components
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

Zum Auflisten der Komponenten kann eine Anwendung das [**stringlist**](stringlist-object.md) -Objekt durchlaufen, indem ein-Objekt für jedes Konstrukt verwendet wird. Da Komponenten nicht geordnet sind, haben alle neuen Komponenten einen beliebigen Index. Dies bedeutet, dass die Funktion Komponenten in beliebiger Reihenfolge zurückgeben kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msienumschlag Components**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa)
</dt> </dl>

 

 




