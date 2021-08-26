---
description: Während einer gleichzeitigen Installation legt das Installationsprogramm die ParentProductCode-Eigenschaft in der Sitzung der gleichzeitigen Installation auf den gleichen Wert wie die ProductCode-Eigenschaft in der Sitzung der übergeordneten Installation fest.
ms.assetid: 7bf2b9b1-9efd-4d47-9fa3-253421f1ba4f
title: ParentProductCode(Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a56e7a120455723eb95f2bd7f5ea08c59894d3a1951aeb042afb30e3b0e2fdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042450"
---
# <a name="parentproductcode-property"></a>ParentProductCode(Eigenschaft)

Während einer gleichzeitigen Installation legt das Installationsprogramm die **ParentProductCode-Eigenschaft** in der Sitzung der gleichzeitigen Installation auf den gleichen Wert wie die [**ProductCode-Eigenschaft**](productcode.md) in der Sitzung der übergeordneten Installation fest. Übergeordnete Installationen führen die gleichzeitigen Installationsaktionen aus, um eine gleichzeitige Installation durchzuführen. Ein Installationspaket kann ermitteln, ob es durch eine gleichzeitige Installationsaktion installiert wird, indem der Wert dieser Eigenschaft überprüft wird.

> [!Note]  
> Gleichzeitige Installationen werden nicht für die Installation von Anwendungen empfohlen, die für die Veröffentlichung an die Öffentlichkeit vorgesehen sind. Informationen zu gleichzeitigen Installationen finden Sie unter [Gleichzeitige Installationen.](concurrent-installations.md)

 

> [!Note]  
> Diese Eigenschaft wird nicht festgelegt, wenn die gleichzeitige Installation durch die [RemoveExistingProducts-Aktion ausgeführt](removeexistingproducts-action.md) wird.

 

## <a name="remarks"></a>Hinweise

Um zu verhindern, dass ein Paket jemals als gleichzeitige Installation installiert wird, fügen Sie eine der folgenden Bedingungsanweisungen zur [LaunchCondition-Tabelle](launchcondition-table.md) hinzu. Dadurch wird verhindert, dass das Paket durch eine gleichzeitige Installationsaktion installiert wird, die von einer anderen Installation ausgeführt wird. Dies verhindert nicht, dass das Paket von der [RemoveExistingProducts-Aktion installiert](removeexistingproducts-action.md) wird.

``` syntax
"Not ParentProductCode"
```

``` syntax
"Not ParentOriginalDatabase"
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Anforderungen.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[**ParentOriginalDatabase**](parentoriginaldatabase.md)
</dt> </dl>

 

 




