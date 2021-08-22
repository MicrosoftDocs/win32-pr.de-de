---
description: Die schreibgeschützte Components-Eigenschaft gibt ein StringList-Objekt zurück, das den Satz installierter Komponenten für alle Produkte auflistet.
ms.assetid: c84e4329-428a-440a-bd65-097588a86932
title: Installer.Components (Eigenschaft)
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
ms.openlocfilehash: b8538e594ed02a1bc355ed4cf57db1befb1443e58d7afe2038b16e08eb9e4659
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118632408"
---
# <a name="installercomponents-property"></a>Installer.Components (Eigenschaft)

Die schreibgeschützte **Components-Eigenschaft** gibt ein [**StringList-Objekt**](stringlist-object.md) zurück, das den Satz installierter Komponenten für alle Produkte auflistet.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.Components
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Hinweise

Um die Komponenten aufzählen zu können, kann eine Anwendung das [**StringList-Objekt**](stringlist-object.md) mithilfe eines For Each-Konstrukts iterieren. Da Komponenten nicht geordnet sind, haben alle neuen Komponenten einen beliebigen Index. Dies bedeutet, dass die Funktion Komponenten in beliebiger Reihenfolge zurückgeben kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa)
</dt> </dl>

 

 




