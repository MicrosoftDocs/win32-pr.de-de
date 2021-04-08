---
description: Das Installationsprogramm verwendet das setProgress-Ereignis, um Informationen über den Fortschritt der Installation zu veröffentlichen.
ms.assetid: be597c90-7222-4542-b0f7-e9f4cdfc08b9
title: SetProgress ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd7523f03dd8fc8216991ae16b05a731e9f38f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960152"
---
# <a name="setprogress-controlevent"></a>SetProgress ControlEvent

Das Installationsprogramm verwendet das setProgress-Ereignis, um Informationen über den Fortschritt der Installation zu veröffentlichen. Ein [ProgressBar-Steuer](progressbar-control.md) Element oder ein [Billboard-Steuer](billboard-control.md) Element sollte das Ereignis über die [EventMapping-Tabelle](eventmapping-table.md) abonnieren, indem er die Aktion benennt, deren Status angezeigt wird. Dieses Ereignis sollte in der [Tabelle EventMapping](eventmapping-table.md)erstellt werden.

Diese ControlEvent kann von einer Benutzeroberfläche verarbeitet werden, die auf der [*grundlegenden*](b-gly.md)Benutzeroberfläche, der [*reduzierten*](r-gly.md)Benutzeroberfläche oder der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird. Weitere Informationen zu UI-Ebenen finden Sie unter [Benutzeroberflächen](user-interface-levels.md)Ebenen.

## <a name="published-by"></a>Veröffentlicht von

Diese ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

Keine.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Keine.

## <a name="typical-use"></a>Typische Verwendung

Ein [ProgressBar](progressbar-control.md) -Steuerelement in einem nicht modaldialog Feld abonniert dieses Ereignis mithilfe des [Progress](progress-control-attribute.md) -Attributs, um die Statusinformationen zu erhalten.

 

 



