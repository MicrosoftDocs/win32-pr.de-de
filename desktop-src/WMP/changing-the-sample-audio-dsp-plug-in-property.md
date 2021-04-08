---
title: Ändern der Sample audiodsp-Plug-in-Eigenschaft
description: Ändern der Sample audiodsp-Plug-in-Eigenschaft
ms.assetid: 9e742bcd-cff8-422f-ad91-d8d46f15bdc4
keywords:
- Windows Media Player-Plug-ins, audiodsp
- Plug-ins, audiodsp
- Plug-Ins für die digitale Signalverarbeitung, Audioeigenschaften
- DSP-Plug-ins, Audioeigenschaften
- audiodsp-Plug-ins, Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbc27f58fa8c8903b54f9903797dcc32a7795841
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712185"
---
# <a name="changing-the-sample-audio-dsp-plug-in-property"></a>Ändern der Sample audiodsp-Plug-in-Eigenschaft

Sie möchten wahrscheinlich die Eigenschaft ändern, die der Assistent für den Windows Media Player-Plug-in standardmäßig erstellt. In der folgenden Liste sind die Elemente aufgeführt, die möglicherweise geändert werden müssen:

-   **Die Dialogfeld Ressource.** Klicken Sie im Fenster Arbeitsbereich des Projekts auf die Registerkarte **resourceview** . Erweitern Sie die Ordnerliste, um den Dialog Ordner zu öffnen. Doppelklicken Sie auf die Dialogfeld Ressource, um den Ressourcen-Editor zu öffnen. Sie können Änderungen am Eigenschaften Seiten Dialogfeld vornehmen, um Ihre Anforderungen zu erfüllen. Beispielsweise können Sie den Text in der Bezeichnung ändern oder das Bearbeitungs Steuerelement durch ein Kontrollkästchen ersetzen.
-   **Der Objektcode der Eigenschaften Seite.** Die Standard Implementierung verwendet eine Variable vom Typ Double, um den Skalierungsfaktor zu speichern. Möglicherweise benötigen Sie einen anderen Datentyp. Dies erfordert auch, dass Sie den Code, der die Daten persistent speichert, in die Registrierung ändern und die Daten aus der Registrierung lesen (einschließlich des Codes, der aus der Registrierung in *cprojectname*::**FinalConstruct** liest).
-   **Die Element Variable, die den Eigenschafts Wert speichert.** Diese Variable hat den Namen "m \_ f/alefactor" und ist als Typ "Double" deklariert. Möglicherweise möchten Sie den Namen und den Typ dieser Variablen im gesamten Projekt ändern.
-   **Die Get-und Property Put-Methode der Eigenschaft.** Möglicherweise möchten Sie die Namen, Parameter und Implementierungen dieser Methoden ändern. Vergessen Sie nicht, diese Änderungen auch an anderer Stelle im Projekt widerzuspiegeln. Beispielsweise ruft die Methode zum **anwenden** der Eigenschaften Seite " *cprojectname*::**Put \_ Scale**" auf.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren eines audiodsp-Plug-ins**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




