---
description: Die schreibgeschützte componentclients-Eigenschaft gibt ein stringlist-Objekt zurück, das den Satz von Clients einer angegebenen Komponente auflistet.
ms.assetid: 47553360-298f-4be8-819d-18f4df96667c
title: Installer. componentclients (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentClients
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2241babae283f367a15c8f742b51af280ed1a3b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371154"
---
# <a name="installercomponentclients-property"></a>Installer. componentclients (Eigenschaft)

Die schreibgeschützte **componentclients** -Eigenschaft gibt ein [**stringlist**](stringlist-object.md) -Objekt zurück, das den Satz von Clients einer angegebenen Komponente auflistet.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.ComponentClients
```



## <a name="property-value"></a>Eigenschaftswert

Eine Zeichen folgen-GUID, die den Komponenten Code der Komponente darstellt. Die Komponenten Codes werden in der ComponentID-Spalte der [Component-Tabelle](component-table.md)angegeben.

## <a name="remarks"></a>Bemerkungen

Um die Komponenten Clients aufzulisten, kann eine Anwendung das [**stringlist**](stringlist-object.md) -Objekt durchlaufen, indem ein-Objekt für jedes Konstrukt verwendet wird. Da Clients nicht geordnet sind, haben alle neuen Komponenten einen beliebigen Index. Dies bedeutet, dass die Funktion Clients in beliebiger Reihenfolge zurückgeben kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msienumschlag Clients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa)
</dt> </dl>

 

 




