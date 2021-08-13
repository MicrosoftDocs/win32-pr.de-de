---
description: Die schreibgeschützte ComponentClients-Eigenschaft gibt ein StringList-Objekt zurück, das den Satz von Clients einer angegebenen Komponente auflistet.
ms.assetid: 47553360-298f-4be8-819d-18f4df96667c
title: Installer.ComponentClients-Eigenschaft
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
ms.openlocfilehash: c94a30247bbfc39675308308457c369785bd9a67413a5b0b62af143e17e2112b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118632712"
---
# <a name="installercomponentclients-property"></a>Installer.ComponentClients-Eigenschaft

Die schreibgeschützte **ComponentClients-Eigenschaft** gibt ein [**StringList-Objekt**](stringlist-object.md) zurück, das den Satz von Clients einer angegebenen Komponente auflistet.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.ComponentClients
```



## <a name="property-value"></a>Eigenschaftswert

Eine Zeichenfolgen-GUID, die den Komponentencode der Komponente darstellt. Die Komponentencodes werden in der ComponentId -Spalte der [Component-Tabelle](component-table.md)angegeben.

## <a name="remarks"></a>Hinweise

Um die Komponentenclients aufzulisten, kann eine Anwendung das [**StringList-Objekt**](stringlist-object.md) mithilfe eines For Each-Konstrukts durchlaufen. Da Clients nicht sortiert sind, verfügen alle neuen Komponenten über einen beliebigen Index. Dies bedeutet, dass die Funktion Clients in beliebiger Reihenfolge zurückgeben kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa)
</dt> </dl>

 

 




