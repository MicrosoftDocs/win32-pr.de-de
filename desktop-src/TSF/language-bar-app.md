---
title: Sprachleiste (TSF-Anwendungen)
description: Eine Anwendung kann der Sprachleiste keine Elemente hinzufügen. nur ein Textdienst kann der Sprachleiste Elemente hinzufügen.
ms.assetid: facb0da1-3f80-4745-b021-c026e7e5356c
keywords:
- Textdienstframework (TSF), Sprachleiste
- TSF (Textdienstframework),Sprachleiste
- TSF-fähige Anwendungen, Sprachleiste
- Sprachleiste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2f0adeacdfe105700efba761b0622432f4ac382d147bd82145242be9fdd71a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952108"
---
# <a name="language-bar-tsf-applications"></a>Sprachleiste (TSF-Anwendungen)

Eine Anwendung kann der Sprachleiste keine Elemente hinzufügen. nur ein Textdienst kann der Sprachleiste Elemente hinzufügen. Eine Anwendung kann beeinflussen, wie bestimmte Elemente auf der Sprachleiste angezeigt werden.

Das [ \_ GUID-Department "COMPARTMENT \_ SPEECH \_ DICTATIONSTAT"](predefined-compartments.md) wird verwendet, um den Typ der Spracheingabe anzugeben, den die Anwendung akzeptieren kann: direkte Texteingabe (Diktat) und/oder Sprachbefehle. Standardmäßig ist das Diktat aktiviert, und der Sprachbefehl ist deaktiviert. Wenn die Anwendung Sprachbefehle akzeptieren kann, sollte sie den [TF \_ COMMANDING \_ ENABLED-Wert](speech-recognition-constants.md) im GUID-COMPARTMENT \_ SPEECH \_ \_ DICTATIONSTAT-Abteil festlegen. Wenn die Anwendung Diktat akzeptieren kann, sollte sie den TF \_ DICTATION \_ ENABLED-Wert im \_ GUID-Compartment \_ SPEECH \_ DICTATIONSTAT-Abteil festlegen. Der TF-DICTATION ON- oder TF COMMANDING ON-Wert dieses Compartments bestimmt, in welchem Modus \_ \_ (Diktat- oder Befehlseingabe) sich die \_ \_ Spracheingabe derzeit befindet.

Wenn die Anwendung die persistente Speicherung von Eigenschaftsdaten unterstützt, sollte sie das [ \_ GUID-Compartment \_ PERSISTMENUENABLED](predefined-compartments.md) auf einen Wert ungleich 0 (null) festlegen. Dies bewirkt, dass der Sprachtextdienst das **Menüelement Speech-Daten speichern** aktiviert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einrichten von Textdienstframework](how-to-set-up-tsf.md)
</dt> <dt>

[Sprachleiste (Textdienste)](language-bar.md)
</dt> </dl>

 

 




