---
description: Das Installationsprogramm verwendet dieses Ereignis, um eine Informations Zeichenfolge anzuzeigen, während das Ausführungs Skript der Installation kompiliert wird.
ms.assetid: 088e91e0-734a-4f18-8ceb-cfa4f904f75c
title: Scriptinprogress ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788fdc9c0acec5979a835a6cd2a0ec09cc6f0c38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347372"
---
# <a name="scriptinprogress-controlevent"></a>Scriptinprogress ControlEvent

Das Installationsprogramm verwendet dieses Ereignis, um eine Informations Zeichenfolge anzuzeigen, während das Ausführungs Skript der Installation kompiliert wird. Die Informations Zeichenfolge kann in einem Dialogfeld durch ein [Text Steuer](text-control.md) Element angezeigt werden, das diese ControlEvent abonniert. Dieses Ereignis sollte in der [Tabelle EventMapping](eventmapping-table.md)erstellt werden.

Diese ControlEvent kann von einer Benutzeroberfläche verarbeitet werden, die auf der [*grundlegenden*](b-gly.md)Benutzeroberfläche, der [*reduzierten*](r-gly.md)Benutzeroberfläche oder der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird. Weitere Informationen zu UI-Ebenen finden Sie unter [Benutzeroberflächen](user-interface-levels.md)Ebenen.

## <a name="published-by"></a>Veröffentlicht von

Diese ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

Keine.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Ein [Text Steuer](text-control.md) Element, das scriptinprogress abonniert, zeigt die in der [UIText-Tabelle](uitext-table.md)angegebene Text Zeichenfolge an.

## <a name="typical-use"></a>Typische Verwendung

Während das Ausführungs Skript kompiliert wird, zeigt das Installationsprogramm eine ProgressBar an, die die verbleibende Zeit vor dem Beginn der Skriptausführung angibt. Der Paket Ersteller kann zu diesem Zeitpunkt eine vorläufige Meldung anzeigen, in der die ProgressBar erläutert wird. Um eine vorläufige Meldung anzuzeigen, schließen Sie ein [Text Steuer](text-control.md) Element in dasselbe nicht Modaldialogfeld wie die ProgressBar ein. Legen Sie fest, dass dieses Text Steuerelement den scriptinprogress-ControlEvent über die [EventMapping-Tabelle](eventmapping-table.md)abonniert. Fügen Sie einen Eintrag in der [UIText-Tabelle](uitext-table.md) mit scriptinprogress ein, der im Schlüsselfeld angegeben ist. Geben Sie die vorläufige Nachricht als Text Zeichenfolge im Textfeld der UIText-Tabelle an. Während der Skript Kompilierung zeigt das Installationsprogramm diese Zeichenfolge im Text Steuerelement an. Der angezeigte Text verschwindet, sobald die Skript Kompilierung abgeschlossen ist.

Das gleiche Text Steuerelement, das den scriptinprogress-ControlEvent abonniert, kann auch das [timeremainingcontrolevent](timeremaining-controlevent.md)abonnieren. In diesem Fall wird der Text der vorläufigen scriptinprogress-Zeichenfolge durch die Zeichenfolge "verbleibende Zeit: XX Minuten" ersetzt.

 

 



