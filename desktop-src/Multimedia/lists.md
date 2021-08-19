---
title: Listen
description: Listen
ms.assetid: 89fb4457-307a-4693-94d4-57f57c422d1e
keywords:
- Audiomixer, Steuerelemente
- Audiomixer,Listen
- Mixer, Steuerelemente
- Mixer, Listen
- List-Steuerelemente
- MIXERCONTROLDETAILS_BOOLEAN-Struktur
- MIXERCONTROLDETAILS_LISTTEXT-Struktur
- Steuerelement mit einmaliger Auswahl
- Mehrfachauswahl-Steuerelement
- Mixer-Steuerelement
- Multiplexer (MUX)
- MUX (Multiplexer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f15e1c89e564ddd3b6c263b91242a3e4dc0382fd36f86554ec6bd0556191ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139395"
---
# <a name="lists"></a>Listen

Die Listensteuerelemente bieten Einen-Auswahl- oder Mehrfachauswahlzustände für komplexe Audiolinien. Diese Steuerelemente verwenden die [**\_ BOOLEAN-Struktur MIXERCONTROLDETAILS**](/previous-versions//dd757295(v=vs.85)) zum Abrufen und Festlegen von Steuerelementeigenschaften. Die [**MIXERCONTROLDETAILS \_ LISTTEXT-Struktur**](/previous-versions//dd757296(v=vs.85)) wird auch verwendet, um alle Textbeschreibungen eines Steuerelements mit mehreren Element abzurufen. In der folgenden Tabelle werden die Typen von Listensteuerelementen beschrieben.



| Control           | Beschreibung                                                                                                                                                                                                                                                                      |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Einzelauswahl     | Schränkt die Steuerelementauswahl auf ein Element gleichzeitig ein. Im Gegensatz zum Multiplexer-Steuerelement kann dieses Steuerelement verwendet werden, um mehr als Audioquellenlinien zu steuern. Sie können dieses Steuerelement beispielsweise verwenden, um einen Low-Pass-Filter aus einer Liste von Filtern auszuwählen, die von einem Mixergerät unterstützt werden. |
| Multiplexer (MUX) | Schränkt die Zeilenauswahl auf eine Quellzeile gleichzeitig ein.                                                                                                                                                                                                                       |
| Mehrfachauswahl   | Ermöglicht dem Benutzer, mehrere Elemente gleichzeitig aus einer Liste auszuwählen. Im Gegensatz zum Mixer-Steuerelement kann das Mehrfachauswahl-Steuerelement verwendet werden, um mehr als Audioquellenlinien zu steuern.                                                                                                  |
| Mixer             | Ermöglicht dem Benutzer, Quellzeilen gleichzeitig aus einer Liste auszuwählen.                                                                                                                                                                                                               |



 

 

 