---
description: Das Ereignis settargetpath benachrichtigt den Installer, den ausgewählten Pfad zu überprüfen und festzulegen. Wenn der Pfad für den Schreibzugriff nicht gültig ist, blockiert der Installer weitere ControlEvents, die dem Steuerelement zugeordnet sind.
ms.assetid: 5649da99-1541-47ab-9d2e-b33a705998ec
title: Settargetpath ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36812d291ab4410b08c577e6d118c3ff9e5dc0b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216933"
---
# <a name="settargetpath-controlevent"></a>Settargetpath ControlEvent

Das Ereignis settargetpath benachrichtigt den Installer, den ausgewählten Pfad zu überprüfen und festzulegen. Wenn der Pfad für den Schreibzugriff nicht gültig ist, blockiert der Installer weitere ControlEvents, die dem Steuerelement zugeordnet sind.

Dieses Ereignis kann von einem [PUSHBUTTON-Steuer](pushbutton-control.md)Element oder einem [SelectionTree-Steuer](selectiontree-control.md)Element veröffentlicht werden. Dieses Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden.

Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird. Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md). Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).

## <a name="published-by"></a>Veröffentlicht von

Diese ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

Der Name der Eigenschaft, die den Pfad enthält. Wenn die Eigenschaft deretendiert ist, wird der Eigenschaftsname in eckige Klammern eingeschlossen.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Keine.

## <a name="typical-use"></a>Typische Verwendung

Ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement in einem Dialogfeld zum Durchsuchen ist an dieses Ereignis in der Tabelle [ControlEvent](controlevent-table.md) gebunden, um den ausgewählten Pfad vor der Rückgabe zum Auswahl Dialogfeld zu überprüfen.

## <a name="remarks"></a>Bemerkungen

Versuchen Sie nicht, den Zielpfad zu konfigurieren, wenn die Komponenten, die diese Pfade verwenden, für den aktuellen Benutzer oder für einen anderen Benutzer bereits installiert sind. Überprüfen Sie die Eigenschaft [**productstate**](productstate.md) vor dem Veröffentlichen von settargetpath ControlEvent, um zu bestimmen, ob das Produkt, das die Komponente enthält, installiert ist.

 

 



