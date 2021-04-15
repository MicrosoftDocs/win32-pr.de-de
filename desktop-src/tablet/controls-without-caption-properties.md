---
description: Einführung in die Verwendung von Steuerelementen ohne Beschriftung-Eigenschaften für den Tablet PC.
ms.assetid: 8c44e1eb-8d57-4c3b-a329-c8ad77423cb7
title: Steuerelemente ohne Beschriftung-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f6c9a52d7c6c89e7233e32f7f5d7dc295bc289e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524379"
---
# <a name="controls-without-caption-properties"></a>Steuerelemente ohne Beschriftung-Eigenschaften

Wenn ein Steuerelement nicht über eine eigene Caption-Eigenschaft verfügt, führen Sie die folgenden Schritte aus, um sicherzustellen, dass Barrierefreiheits Hilfen die Steuerelemente identifizieren können:

-   Erstellen Sie ein statisches Text Steuerelement mit einem aussagekräftigen und beschreibenden Namen.
-   Platzieren Sie die statische Bezeichnung, sodass Sie unmittelbar vor dem Steuerelement in der Aktivier Reihenfolge steht.
-   Stellen Sie sicher, dass der Bezeichnungs Text mit einem Doppelpunkt endet, z. b. "Settings:"
-   Positionieren Sie den Bezeichnungs Text direkt links oder vor dem Steuerelement, auf das verwiesen wird.
-   Machen Sie den statischen Text unsichtbar, wenn er nicht für eine visuelle Darstellung geeignet ist. Dazu weisen Sie dem Ressourcen Skript das entsprechende Attribut zu. Dies kann sinnvoll sein, wenn der Name oder die Funktion eines Steuer Elements mit einem anderen Mittel als statischem Text Steuerelement visuell bereitgestellt wird, z. b. eine Grafik oder ein verknüpftes Optionsfeld.

Die richtige Verwendung statischer Steuerelemente ist die einzige Möglichkeit, unterstrichene Zugriffstasten für Steuerelemente, die keine intrinsischen Bezeichnungen aufweisen, ordnungsgemäß zu implementieren. Weitere Informationen zur Verwendung von Steuerelementen, die keine Beschriftungs Eigenschaften aufweisen, finden Sie im Abschnitt zur [Barrierefreiheit](/windows/desktop/accessibility) .

 

 
