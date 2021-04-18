---
description: Der Wert der ProductVersion-Eigenschaft ist die Version des Produkts im Zeichen folgen Format.
ms.assetid: 551fca7e-a827-482d-bc56-ff2fe5a17025
title: ProductVersion-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01f82fcbd28c4a4132e4c3f76adfd68e33c43b36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354678"
---
# <a name="productversion-property"></a>ProductVersion-Eigenschaft

Der Wert der **ProductVersion** -Eigenschaft ist die Version des Produkts im Zeichen folgen Format. Diese Eigenschaft ist erforderlich.

Das Format der Zeichenfolge lautet wie folgt:

<dl> Hauptversion.Nebenversion.Build  
</dl>

Das erste Feld ist die Hauptversion und hat einen maximalen Wert von 255. Das zweite Feld ist die neben Version und hat einen maximalen Wert von 255. Das dritte Feld wird als Buildversion oder Update Version bezeichnet und hat den maximalen Wert 65.535.

## <a name="remarks"></a>Bemerkungen

Mindestens eines der drei Felder von **ProductVersion** muss sich bei einem Upgrade mithilfe der [upgradetabelle](upgrade-table.md)ändern. Alle Updates, die nur den Paketcode ändern, aber " **ProductVersion** " und " [**ProductCode**](productcode.md) " unverändert bleiben, werden als [kleines Update](small-updates.md)bezeichnet. Die drei Versions Felder werden hauptsächlich zur einfacheren Bereitstellung bereitgestellt. Wenn Sie z. **b. ProductVersion** ändern, aber weder die Haupt-noch die neben Version ändern möchten, können Sie die Buildversion ändern.

Beachten Sie, dass Windows Installer nur die ersten drei Felder der Produktversion verwendet. Wenn Sie ein viertes Feld in Ihre Produktversion einschließen, wird das vierte Feld vom Installationsprogramm ignoriert.

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

[kleines Update](small-updates.md)
</dt> </dl>

 

 




