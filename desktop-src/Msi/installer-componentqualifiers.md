---
description: Die componentqualifizierereigenschaft ist eine schreibgeschützte Eigenschaft, die ein stringlist-Objekt zurückgibt, das den Satz registrierter Qualifizierer für die angegebene Komponente auflistet.
ms.assetid: 49b16c9a-ce84-42ff-af1d-f4ecf7dbe23a
title: Installer. componentqualifizierereigenschaft
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
ms.openlocfilehash: 0e6f58850974eaa2021578f0d56015ea0ef6d9e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365478"
---
# <a name="installercomponentqualifiers-property"></a>Installer. componentqualifizierereigenschaft

Die **componentqualifizierereigenschaft** ist eine schreibgeschützte Eigenschaft, die ein [**stringlist**](stringlist-object.md) -Objekt zurückgibt, das den Satz registrierter Qualifizierer für die angegebene Komponente auflistet.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.ComponentQualifiers
```



## <a name="property-value"></a>Eigenschaftswert

Eine Zeichen folgen-GUID, die die Kategorie der [Komponente](publishcomponent-table.md)darstellt.

## <a name="remarks"></a>Bemerkungen

Zum Auflisten der Qualifizierer durchläuft die Anwendung das [**stringlist**](stringlist-object.md) -Objekt mithilfe eines for Each-Konstrukts. Da Qualifizierer nicht sortiert sind, verfügt jeder neue Qualifizierer über einen beliebigen Index, was bedeutet, dass die Funktion Qualifizierer in beliebiger Reihenfolge

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msienumschlag componentqualifizierer**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
</dt> </dl>

 

 




