---
description: Die UpgradeCode-Eigenschaft ist eine GUID, die einen zusammenhängenden Satz von Produkten darstellt. Der UpgradeCode wird in der upgradetabelle verwendet, um nach verwandten Versionen des Produkts zu suchen, die bereits installiert sind. Diese Eigenschaft wird von der registerproduct-Aktion verwendet.
ms.assetid: 6cdee5d8-8aa0-4fad-9338-152ee33b8077
title: UpgradeCode-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac1e5493ad651e609f6ef9d7ae14e07c0c15b5b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370695"
---
# <a name="upgradecode-property"></a>UpgradeCode-Eigenschaft

Die **UpgradeCode** -Eigenschaft ist eine GUID, die einen zusammenhängenden Satz von Produkten darstellt. Der **UpgradeCode** wird in der [upgradetabelle](upgrade-table.md) verwendet, um nach verwandten Versionen des Produkts zu suchen, die bereits installiert sind.

Diese Eigenschaft wird von der [registerproduct-Aktion](registerproduct-action.md)verwendet.

## <a name="remarks"></a>Bemerkungen

Es wird dringend empfohlen, dass Autoren von Installationspaketen einen **UpgradeCode** für Ihre Anwendung angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Patchen und Upgrades](patching-and-upgrades.md)
</dt> <dt>

[Vorbereiten einer Anwendung für zukünftige größere Upgrades](preparing-an-application-for-future-major-upgrades.md)
</dt> </dl>

 

 




