---
title: Ändern der DSP-Plug-In-Eigenschaft für Beispielaudio
description: Ändern der DSP-Plug-In-Eigenschaft für Beispielaudio
ms.assetid: 9e742bcd-cff8-422f-ad91-d8d46f15bdc4
keywords:
- Windows Media Player-Plug-Ins, Audio-DSP
- Plug-Ins, Audio-DSP
- Digitale Signalverarbeitungs-Plug-Ins, Audioeigenschaften
- DSP-Plug-Ins, Audioeigenschaften
- Audio-DSP-Plug-Ins, Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8aac1cf385f41e966bec51f19454308cf52697c995db4962a45486999ebae9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342623"
---
# <a name="changing-the-sample-audio-dsp-plug-in-property"></a>Ändern der DSP-Plug-In-Eigenschaft für Beispielaudio

Sie möchten wahrscheinlich die Eigenschaft ändern, die der Windows Media Player Plug-In-Assistent standardmäßig erstellt. In der folgenden Liste sind die Elemente aufgeführt, die möglicherweise geändert werden müssen:

-   **Die Dialogressource.** Klicken Sie im Fenster Project Arbeitsbereich auf die Registerkarte **ResourceView.** Erweitern Sie die Ordnerliste, um den Ordner Dialog zu öffnen. Doppelklicken Sie auf die Dialogfeldressource, um den Ressourcen-Editor zu öffnen. Sie können Änderungen am Eigenschaftenseitendialogfeld vornehmen, um Ihre Anforderungen zu erfüllen. Beispielsweise können Sie den Text in der Bezeichnung ändern oder das Bearbeitungssteuerelement durch ein Kontrollkästchen ersetzen.
-   **Der Objektcode der Eigenschaftenseite.** Die Standardimplementierungen verwenden eine Variable vom Typ double, um den Skalierungsfaktor zu speichern. Möglicherweise benötigen Sie einen anderen Datentyp. Dies erfordert auch, dass Sie den Code ändern, der die Daten in der Registrierung beibehält und die Daten aus der Registrierung liest (einschließlich des Codes, der aus der Registrierung in *CProjectName*::**FinalConstruct** liest).
-   **Die Membervariable, die den Eigenschaftswert speichert.** Diese Variable heißt "m \_ fScaleFactor" und wird als Double-Typ deklariert. Möglicherweise möchten Sie den Namen und Typ dieser Variablen im gesamten Projekt ändern.
-   **Die get- und property put-Methoden der Eigenschaft.** Möglicherweise möchten Sie die Namen, Parameter und Implementierungen dieser Methoden ändern. Vergessen Sie nicht, diese Änderungen auch an anderer Stelle im Projekt widerzuspiegeln. Die Apply-Methode  der Eigenschaftenseite ruft z. B. *CProjectName*::**put \_ scale** auf.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren eines Audio-DSP-Plug-Ins**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




