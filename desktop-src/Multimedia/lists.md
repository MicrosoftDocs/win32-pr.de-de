---
title: Listen
description: Listen
ms.assetid: 89fb4457-307a-4693-94d4-57f57c422d1e
keywords:
- Audiomischungen, Steuerelemente
- Audiomixer, Listen
- Mischungen, Steuerelemente
- Mixer, Listen
- List-Steuerelemente
- MIXERCONTROLDETAILS_BOOLEAN Struktur
- MIXERCONTROLDETAILS_LISTTEXT Struktur
- Steuerelement für die einfache Auswahl
- Mehrfachauswahl-Steuerelement
- Mixer-Steuerelement
- Multiplexer (MUX)
- MUX (Multiplexer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d475816d7090ee241a1508cc054b12742c4ab27
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314780"
---
# <a name="lists"></a>Listen

Die Listen-Steuerelemente stellen die einzelnen SELECT-und Multiple-Select-Zustände für komplexe audiozeilen bereit. Diese Steuerelemente verwenden die [**\_ boolesche "mixercontroldetails**](/previous-versions//dd757295(v=vs.85)) "-Struktur zum Abrufen und Festlegen von Steuerelement Eigenschaften. Die " [**mixercontroldetails"- \_ listtext**](/previous-versions//dd757296(v=vs.85)) -Struktur wird auch verwendet, um alle Textbeschreibungen eines Steuer Elements mit mehreren Elementen abzurufen. In der folgenden Tabelle werden die Typen von Listen Steuerelementen beschrieben.



| Control           | BESCHREIBUNG                                                                                                                                                                                                                                                                      |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Einfache Auswahl     | Schränkt die Auswahl des Steuer Elements auf ein Element gleichzeitig ein. Anders als das Multiplexer-Steuerelement kann dieses Steuerelement verwendet werden, um mehr als audioquellzeilen zu steuern. Beispielsweise können Sie mit diesem Steuerelement einen Tiefpass Filter aus einer Liste von Filtern auswählen, die von einem Mischungs Gerät unterstützt werden. |
| Multiplexer (MUX) | Schränkt die Zeilenauswahl auf jeweils eine Quellzeile ein.                                                                                                                                                                                                                       |
| Mehrfachauswahl   | Ermöglicht es dem Benutzer, mehrere Elemente gleichzeitig aus einer Liste auszuwählen. Anders als das Mixer-Steuerelement kann das Mehrfachauswahl-Steuerelement verwendet werden, um mehr als audioquellzeilen zu steuern.                                                                                                  |
| Mixer             | Ermöglicht dem Benutzer das gleichzeitige Auswählen von Quellzeilen aus einer Liste.                                                                                                                                                                                                               |



 

 

 