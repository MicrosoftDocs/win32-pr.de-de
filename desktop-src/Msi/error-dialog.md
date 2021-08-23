---
description: Ein Fehlerdialogfeld ist ein modales Dialogfeld, in dem eine Fehlermeldung angezeigt wird. In jeder Installation kann mehr als ein Fehlerdialogfeld vorhanden sein.
ms.assetid: 11d4fe8b-ec5f-4576-95e5-c86344f0195c
title: Fehlerdialogfeld
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff8582996ad4380d8adc62f684f638092857b45d464e7e8ef150c1fed141027f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692500"
---
# <a name="error-dialog"></a>Fehlerdialogfeld

Ein Fehlerdialogfeld ist ein modales Dialogfeld, in dem eine Fehlermeldung angezeigt wird. In jeder Installation kann mehr als ein Fehlerdialogfeld vorhanden sein.

Eine ErrorDialog-Eigenschaft muss festgelegt werden, die angibt, welches Dialogfeld verwendet werden soll. Wenn diese Eigenschaft nicht festgelegt ist oder nicht auf ein gültiges Dialogfeld Fehler zeigt, werden die Fehlermeldungen nicht angezeigt. In diesem Fall wird der Fehler nur mit einer Warnung zum fehlenden Dialogfeld protokolliert.

Für ein Dialogfeld Fehler muss das [Bit im Format Fehlerdialogfeld festgelegt](error-dialog-style-bit.md) sein. Das Dialogfeld muss über ein [Text-Steuerelement mit dem Namen](text-control.md) ErrorText verfügen. Für den Datensatz für das Dialogfeld Fehler in der [Tabelle Dialog](dialog-table.md) muss das ErrorText-Steuerelement in das Feld Control First \_ eingegeben werden.

Das Dialogfeld muss sieben [PushButtons enthalten.](pushbutton-control.md) Alle diese Schaltflächen geben das [EndDialog](enddialog-controlevent.md) ControlEvent in der [ControlEvent-Tabelle an.](controlevent-table.md) Jede Schaltfläche gibt eines der folgenden Attribute an: **ErrorAbort**, **ErrorCancel**, **ErrorIgnore**, **ErrorNo**, **ErrorOk**, **ErrorRetry**, **ErrorYes**.

> [!Note]  
> Der Fokus dieser Steuerelemente sollte nicht über die Verwendung der Control Next -Spalte \_ in der [Control-Tabelle verknüpft werden.](control-table.md)

 

Diese Schaltflächen sollten ungefähr an derselben Position im Dialogfeld platziert werden, da bei derEntstellung je nach Meldung nur eine Teilmenge dieser sieben Schaltflächen erstellt wird. Die X-Koordinate der Schaltflächen wird so geändert, dass die angezeigten Schaltflächen gleichmäßig zwischen den Schaltflächen stehen. Die Y-Koordinate, Höhe und Breite der Schaltflächen bleiben unverändert. Da die Schaltflächen horizontal angeordnet sind, kann kein anderes Steuerelement im gleichen horizontalen Bereich des Dialogfelds platziert werden.

Bei einem Fehlerdialogfeld werden die Felder Standard steuern und Abbrechen steuern \_ in der Tabelle \_ [Dialog](dialog-table.md) ignoriert. Das Feld Control \_ First für ein Fehlerdialogfeld muss das ErrorText-Steuerelement angeben.

Wenn in [diesem Dialogfeld ein](icon-control.md) Symbol-Steuerelement mit dem Namen ErrorIcon enthalten ist, werden Windows Standardsymbole angezeigt:

-   IDI \_ ERROR als Reaktion auf imtFatalExit-Meldungen.
-   IDI \_ WARNING als Reaktion auf imtError- und imtWarning-Meldungen.
-   IDI \_ INFORMATION als Reaktion auf imtOutOfDiskSpace-Meldungen.

Das ErrorIcon-Steuerelement sollte mit dem [FixedSize-Steuerelementattribut](fixedsize-control-attribute.md) erstellt werden, um eine falsche Größengröße der Standardsymbole Windows vermeiden.

 

 



