---
description: Die costingcomplete-Eigenschaft gibt an, ob das Installationsprogramm den Speicherplatz auf dem Datenträger abgeschlossen hat
ms.assetid: 23688f1e-3ae8-4cd9-824c-36077cc7838f
title: Costingcomplete (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 817b4d38b71e377bbf9b51588efef33e4fd6e93e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352924"
---
# <a name="costingcomplete-property"></a>Costingcomplete (Eigenschaft)

Die **costingcomplete** -Eigenschaft gibt an, ob das Installationsprogramm den Speicherplatz auf dem Datenträger abgeschlossen hat Diese Eigenschaft kann verwendet werden, um ein Dialogfeld zu erstellen, das ausgelöst wird, wenn die Kosten nicht abgeschlossen wurden. Die-Eigenschaft wird während der Kosten für den Speicherplatz dynamisch festgelegt, und wird auf 1 festgelegt, sobald die Kosten erfüllt sind. Diese Eigenschaft wird von der [costfinalize-Aktion](costfinalize-action.md)auf 0 (null) initialisiert.

## <a name="remarks"></a>Bemerkungen

Ein Beispiel für das Erstellen eines "Bitte warten. . . "das Dialogfeld, das während der Speicherplatz Kosten angezeigt wird, finden Sie im Abschnitt [Erstellen einer bedingten" Bitte warten... " ](authoring-a-conditional-please-wait-------message-box.md)Meldungs Feld.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




