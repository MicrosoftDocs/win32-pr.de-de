---
description: Dieses modale Dialogfeld ermöglicht es Benutzern, bestimmte Elemente auszuwählen.
ms.assetid: 76e0f369-839e-4dc0-bb42-c48dbf1511f3
title: Auswahl Dialogfeld
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d5a6b8700bbbdefe2bd1b2270797b34b0cebfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349715"
---
# <a name="selection-dialog"></a>Auswahl Dialogfeld

Dieses modale Dialogfeld ermöglicht es Benutzern, bestimmte Elemente auszuwählen.

Ein Auswahl Dialogfeld enthält ein [SelectionTree-Steuer](selectiontree-control.md) Element, mit dem mehrere ControlEvents veröffentlicht werden. Häufig werden diese ControlEvents von [Text](text-control.md)-, [Symbol](icon-control.md)-oder [Bitmap](bitmap-control.md) -Steuerelementen abonniert, die eine Beschreibung, die Größe, den Pfad und das Symbol des hervorgehobenen Elements anzeigen.

Das Dialogfeld enthält ein [PUSHBUTTON-Steuer](pushbutton-control.md) Element, das den [selectionbrowse-ControlEvent](selectionbrowse-controlevent.md) veröffentlicht und ein [Dialogfeld zum Durchsuchen](browse-dialog.md)erzeugt. Das Browse-Steuerelement ermöglicht es dem Benutzer, ein Verzeichnis auszuwählen.

Die Auswahl Struktur wird erst aufgefüllt, nachdem die Aktion " [costinitialize](costinitialize-action.md) " und die [Aktion "costfinalize](costfinalize-action.md) " aufgerufen wurden.

Ein Auswahl Dialogfeld wird häufig verwendet, um Features auszuwählen. Die Funktionen werden in einem SelectionTree-Steuerelement als Elemente aufgeführt und mit der kurzen Text Zeichenfolge gekennzeichnet, die in der Spalte Titel der [Featuretabelle](feature-table.md)angezeigt wird. Die Text Zeichenfolge in der Spalte Beschreibung der Funktions Tabelle wird als [selectiondescription ControlEvent](selectiondescription-controlevent.md) veröffentlicht und durch ein [Text-Steuer](text-control.md) Element im Auswahl Dialogfeld angezeigt. Das Auswahl Struktur-Steuerelement veröffentlicht auch das Handle für das Symbol des hervorgehobenen Elements.

 

 



