---
title: Ändern der Beispieleigenschaft des Audio-DSP-Plug-Ins
description: Ändern der Beispieleigenschaft des Audio-DSP-Plug-Ins
ms.assetid: 9e742bcd-cff8-422f-ad91-d8d46f15bdc4
keywords:
- Windows Media Player-Plug-Ins,Audio-DSP
- Plug-Ins, Audio-DSP
- Plug-Ins für die digitale Signalverarbeitung, Audioeigenschaften
- DSP-Plug-Ins, Audioeigenschaften
- Audio-DSP-Plug-Ins,Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8aac1cf385f41e966bec51f19454308cf52697c995db4962a45486999ebae9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342623"
---
# <a name="changing-the-sample-audio-dsp-plug-in-property"></a>Ändern der Beispieleigenschaft des Audio-DSP-Plug-Ins

Sie sollten die Eigenschaft ändern, die der Windows Media Player-Plug-In-Assistent standardmäßig erstellt. In der folgenden Liste sind die Elemente aufgeführt, die möglicherweise geändert werden müssen:

-   **Die Dialogressource.** Klicken Sie **im Fenster Arbeitsbereich** auf Project ResourceView. Erweitern Sie die Ordnerliste, um den Ordner Dialog zu öffnen. Doppelklicken Sie auf die Dialogfeldressource, um den Ressourcen-Editor zu öffnen. Sie können Änderungen am Dialogfeld der Eigenschaftenseite vornehmen, um Ihre Anforderungen zu erfüllen. Beispielsweise können Sie den Text in der Bezeichnung ändern oder das Bearbeitungssteuerfeld durch ein Kontrollkästchen ersetzen.
-   **Der Objektcode der Eigenschaftenseite.** Die Standardimplementierung verwendet eine Variable vom Typ double, um den Skalierungsfaktor zu speichern. Möglicherweise benötigen Sie einen anderen Datentyp. Dazu müssten Sie auch den Code ändern, der die Daten in der Registrierung beibehält und die Daten aus der Registrierung liest (einschließlich des Codes, der in *CProjectName*::**FinalConstruct** aus der Registrierung liest).
-   **Die Membervariable, die den Eigenschaftswert speichert.** Diese Variable heißt "m \_ fScaleFactor" und wird als Typ double deklariert. Möglicherweise möchten Sie den Namen und Typ dieser Variablen im gesamten Projekt ändern.
-   **Die get- und property put-Methoden der Eigenschaft.** Möglicherweise möchten Sie die Namen, Parameter und Implementierungen dieser Methoden ändern. Vergessen Sie nicht, diese Änderungen auch an anderer Stelle im Projekt widerzu spiegelten. Die Eigenschaftenseite Apply-Methode **ruft** *beispielsweise CProjectName* auf:**put \_ scale**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren eines Audio-DSP-Plug-Ins**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




