---
description: Die upgradingproductcode-Eigenschaft wird Windows Installer festgelegt, wenn ein Upgrade eine Anwendung entfernt.
ms.assetid: 903e4c22-e7ae-47bd-989b-d8c922de8d1a
title: Upgradingproductcode-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7a256ade7f03275752ad4d176e64cd9d0fa12ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358088"
---
# <a name="upgradingproductcode-property"></a>Upgradingproductcode-Eigenschaft

Die **upgradingproductcode** -Eigenschaft wird Windows Installer festgelegt, wenn ein Upgrade eine Anwendung entfernt. Das Installationsprogramm legt diese Eigenschaft fest, wenn die [RemoveExistingProducts-Aktion](removeexistingproducts-action.md)ausgeführt wird. Diese Eigenschaft wird nicht festgelegt, indem eine Anwendung mithilfe der Option Software in der Systemsteuerung entfernt wird. Eine Anwendung bestimmt mithilfe von " **upgradingproductcode**", ob Sie durch ein Upgrade oder die Software zum Hinzufügen oder entfernen entfernt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




