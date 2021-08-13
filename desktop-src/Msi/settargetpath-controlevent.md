---
description: Das SetTargetPath-Ereignis benachrichtigt das Installationsprogramm, den ausgewählten Pfad zu überprüfen und festzulegen. Wenn der Pfad nicht in geschrieben werden kann, blockiert das Installationsprogramm weitere ControlEvents, die dem Steuerelement zugeordnet sind.
ms.assetid: 5649da99-1541-47ab-9d2e-b33a705998ec
title: SetTargetPath ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40e49e9447d7d2e67dce85e7d60638c18a949ecbc87800d12a60bc94d971cb30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625070"
---
# <a name="settargetpath-controlevent"></a>SetTargetPath ControlEvent

Das SetTargetPath-Ereignis benachrichtigt das Installationsprogramm, den ausgewählten Pfad zu überprüfen und festzulegen. Wenn der Pfad nicht in geschrieben werden kann, blockiert das Installationsprogramm weitere ControlEvents, die dem Steuerelement zugeordnet sind.

Dieses Ereignis kann von einem [PushButton-Steuerelement](pushbutton-control.md)oder einem [SelectionTree-Steuerelement](selectiontree-control.md)veröffentlicht werden. Dieses Ereignis sollte in der [ControlEvent-Tabelle](controlevent-table.md)erstellt werden.

Für dieses ControlEvent muss die Benutzeroberfläche auf [*der vollständigen Benutzeroberflächenebene*](f-gly.md) ausgeführt werden. Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzeroberfläche*](r-gly.md) oder [*einer einfachen Benutzeroberfläche.*](b-gly.md) Weitere Informationen finden Sie unter [Benutzeroberfläche Ebenen.](user-interface-levels.md)

## <a name="published-by"></a>Veröffentlicht von

Dieses ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

Der Name der Eigenschaft, die den Pfad enthält. Wenn die Eigenschaft indirekt ist, wird der Eigenschaftenname in eckige Klammern eingeschlossen.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Keine.

## <a name="typical-use"></a>Typische Verwendung

Ein [PushButton-Steuerelement](pushbutton-control.md) in einem Dialogfeld zum Durchsuchen ist an dieses Ereignis in der [ControlEvent-Tabelle](controlevent-table.md) gebunden, um den ausgewählten Pfad zu überprüfen, bevor zum Auswahldialogfeld zurückzukehren.

## <a name="remarks"></a>Hinweise

Versuchen Sie nicht, den Zielpfad zu konfigurieren, wenn die Komponenten, die diese Pfade verwenden, bereits für den aktuellen Benutzer oder für einen anderen Benutzer installiert sind. Überprüfen Sie die [**ProductState-Eigenschaft,**](productstate.md) bevor Sie setTargetPath ControlEvent veröffentlichen, um zu ermitteln, ob das Produkt, das die Komponente enthält, installiert ist.

 

 



