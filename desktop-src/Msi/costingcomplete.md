---
description: Die CostingComplete-Eigenschaft gibt an, ob das Installationsprogramm die Kosten für den Speicherplatz auf dem Datenträger abgeschlossen hat.
ms.assetid: 23688f1e-3ae8-4cd9-824c-36077cc7838f
title: CostingComplete(Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5a512621e187be9897c07106ade8c6012d4ac4fa43543d71cb856e90027d549
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948357"
---
# <a name="costingcomplete-property"></a>CostingComplete(Eigenschaft)

Die **CostingComplete-Eigenschaft** gibt an, ob das Installationsprogramm die Kosten für den Speicherplatz auf dem Datenträger abgeschlossen hat. Diese Eigenschaft kann verwendet werden, um ein Dialogfeld zu erstellen, das ausgelöst wird, wenn die Kosten nicht abgeschlossen wurden. Die -Eigenschaft wird dynamisch während der Speicherplatzkosten festgelegt und auf 1 festgelegt, sobald die Kosten abgeschlossen sind. Diese Eigenschaft wird mit der [CostFinalize-Aktion](costfinalize-action.md)auf 0 initialisiert.

## <a name="remarks"></a>Hinweise

Ein Beispiel für die Erstellung eines "Please wait . . . " (Dialogfeld), das während der Speicherplatzkosten angezeigt wird, finden Sie im Abschnitt Erstellen eines bedingten ["Please wait . . ". Meldungsfeld](authoring-a-conditional-please-wait-------message-box.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Anforderungen.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




