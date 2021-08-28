---
description: Die UPGRADINGPRODUCTCODE-Eigenschaft wird von Windows Installer festgelegt, wenn eine Anwendung durch ein Upgrade entfernt wird.
ms.assetid: 903e4c22-e7ae-47bd-989b-d8c922de8d1a
title: UPGRADINGPRODUCTCODE-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4f5b0096878d06c4eb3880ab8d965265b04114bcf4e3d732d8243bb4fb02cc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809510"
---
# <a name="upgradingproductcode-property"></a>UPGRADINGPRODUCTCODE-Eigenschaft

Die **UPGRADINGPRODUCTCODE-Eigenschaft** wird von Windows Installer festgelegt, wenn eine Anwendung durch ein Upgrade entfernt wird. Das Installationsprogramm legt diese Eigenschaft fest, wenn die [RemoveExistingProducts-Aktion](removeexistingproducts-action.md)ausgeführt wird. Diese Eigenschaft wird nicht festgelegt, indem eine Anwendung mithilfe von Software in Systemsteuerung entfernt wird. Eine Anwendung bestimmt, ob sie durch ein Upgrade oder das Hinzufügen oder Entfernen von Programmen entfernt wird, indem **upgradingproductcode** aktiviert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zu den mindestens erforderlichen Windows Service Packs, die für eine Windows Installer-Version erforderlich sind, finden Sie unter Run-Time [Anforderungen](windows-installer-portal.md) für Windows Installer.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




