---
description: Während einer gleichzeitigen Installation legt das Installationsprogramm die Eigenschaft "paramealdatabase" in der Sitzung der gleichzeitigen Installation auf denselben Wert wie die Eigenschaft "originaldatabase" in der übergeordneten Installationssitzung fest.
ms.assetid: 8af1c7e5-313c-47b7-be0f-0e31ef21f6a6
title: Eigenschaft ' genoriginaldatabase '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ab69dff7058336a5b68fd3373100f4789059ed7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360900"
---
# <a name="parentoriginaldatabase-property"></a>Eigenschaft ' genoriginaldatabase '

Während einer gleichzeitigen Installation legt das Installationsprogramm die Eigenschaft " **paramealdatabase** " in der Sitzung der gleichzeitigen Installation auf denselben Wert wie die Eigenschaft " [**originaldatabase**](originaldatabase.md) " in der übergeordneten Installationssitzung fest. Bei übergeordneten Installationen werden die parallelen Installations Aktionen verwendet, um eine gleichzeitige Installation auszuführen. Mithilfe eines Installationspakets kann festgestellt werden, ob es durch eine parallele Installations Aktion installiert wird, indem der Wert dieser Eigenschaft überprüft wird.

> [!Note]  
> Parallele Installationen werden nicht für die Installation von Anwendungen empfohlen, die für die öffentliche Veröffentlichung vorgesehen sind. Weitere Informationen zu gleichzeitigen Installationen finden Sie unter [parallele Installationen](concurrent-installations.md).

 

> [!Note]  
> Diese Eigenschaft ist nicht festgelegt, wenn die parallele Installation von der Aktion " [RemoveExistingProducts](removeexistingproducts-action.md) " ausgeführt wird.

 

## <a name="remarks"></a>Bemerkungen

Fügen Sie der [LaunchCondition](launchcondition-table.md) -Tabelle eine der folgenden Bedingungs Anweisungen hinzu, um zu verhindern, dass ein Paket jemals als gleichzeitige Installation installiert wird. Dadurch wird verhindert, dass das Paket jemals durch eine parallele Installations Aktion installiert wird, die von einer anderen Installation ausgeführt wird. Dies verhindert nicht, dass das Paket von der Aktion " [RemoveExistingProducts](removeexistingproducts-action.md) " installiert wird.

``` syntax
"Not ParentProductCode"
```

``` syntax
"Not ParentOriginalDatabase"
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[**"Parametriproductcode"**](parentproductcode.md)
</dt> </dl>

 

 




