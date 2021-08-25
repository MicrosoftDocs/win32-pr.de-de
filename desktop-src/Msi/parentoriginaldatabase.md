---
description: Während einer gleichzeitigen Installation legt das Installationsprogramm die ParentOriginalDatabase-Eigenschaft in der Sitzung der gleichzeitigen Installation auf den gleichen Wert wie die OriginalDatabase-Eigenschaft in der Sitzung der übergeordneten Installation fest.
ms.assetid: 8af1c7e5-313c-47b7-be0f-0e31ef21f6a6
title: ParentOriginalDatabase-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f31d022aa4ec7274d464943d8b3ec059ce11142f06e0e09c22bbb42ec40a2e5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913270"
---
# <a name="parentoriginaldatabase-property"></a>ParentOriginalDatabase-Eigenschaft

Während einer gleichzeitigen Installation legt das Installationsprogramm die **ParentOriginalDatabase-Eigenschaft** in der Sitzung der gleichzeitigen Installation auf den gleichen Wert wie die [**OriginalDatabase-Eigenschaft**](originaldatabase.md) in der Sitzung der übergeordneten Installation fest. Übergeordnete Installationen verwenden die gleichzeitigen Installationsaktionen, um eine gleichzeitige Installation durchzuführen. Ein Installationspaket kann ermitteln, ob es von einer gleichzeitigen Installationsaktion installiert wird, indem der Wert dieser Eigenschaft überprüft wird.

> [!Note]  
> Gleichzeitige Installationen werden für die Installation von Anwendungen, die für die Veröffentlichung in der Öffentlichkeit vorgesehen sind, nicht empfohlen. Informationen zu gleichzeitigen Installationen finden Sie unter [Gleichzeitige Installationen.](concurrent-installations.md)

 

> [!Note]  
> Diese Eigenschaft wird nicht festgelegt, wenn die gleichzeitige Installation von der [RemoveExistingProducts-Aktion](removeexistingproducts-action.md) ausgeführt wird.

 

## <a name="remarks"></a>Hinweise

Um zu verhindern, dass ein Paket jemals als gleichzeitige Installation installiert wird, fügen Sie der [LaunchCondition-Tabelle](launchcondition-table.md) eine der folgenden bedingten Anweisungen hinzu. Dadurch wird verhindert, dass das Paket jemals von einer gleichzeitigen Installationsaktion installiert wird, die von einer anderen Installation ausgeführt wird. Dies verhindert nicht, dass das Paket von der [RemoveExistingProducts-Aktion](removeexistingproducts-action.md) installiert wird.

``` syntax
"Not ParentProductCode"
```

``` syntax
"Not ParentOriginalDatabase"
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Unter [Windows Installer Run-Time Requirements (Anforderungen für](windows-installer-portal.md) Windows Installer) finden Sie Informationen zu den mindest erforderlichen Windows Service Packs für eine Windows Installer-Version.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[**ParentProductCode**](parentproductcode.md)
</dt> </dl>

 

 




