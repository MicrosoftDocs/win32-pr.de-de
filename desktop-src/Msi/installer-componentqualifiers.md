---
description: Die ComponentQualifiers-Eigenschaft ist eine schreibgeschützte Eigenschaft, die ein StringList-Objekt zurückgibt, das den Satz registrierter Qualifizierer für die angegebene Komponente auflistet.
ms.assetid: 49b16c9a-ce84-42ff-af1d-f4ecf7dbe23a
title: Installer.ComponentQualifiers (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentQualifiers
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ff11302b87c144d59129b7041ab75129477e7925b3dd98ce7c740f0c4eda62e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118632604"
---
# <a name="installercomponentqualifiers-property"></a>Installer.ComponentQualifiers (Eigenschaft)

Die **ComponentQualifiers-Eigenschaft** ist eine schreibgeschützte Eigenschaft, die ein [**StringList-Objekt**](stringlist-object.md) zurückgibt, das den Satz registrierter Qualifizierer für die angegebene Komponente auflistet.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.ComponentQualifiers
```



## <a name="property-value"></a>Eigenschaftswert

Eine Zeichenfolgen-GUID, die die Kategorie der Komponente [darstellt.](publishcomponent-table.md)

## <a name="remarks"></a>Hinweise

Zum Auflisten von Qualifizierern durchgibt die Anwendung das [**StringList-Objekt**](stringlist-object.md) mithilfe eines For Each-Konstrukts. Da Qualifizierer nicht geordnet sind, verfügt jeder neue Qualifizierer über einen beliebigen Index, was bedeutet, dass die Funktion Qualifizierer in beliebiger Reihenfolge zurückgeben kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
</dt> </dl>

 

 




