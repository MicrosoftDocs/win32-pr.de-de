---
description: In diesem Thema wird beschrieben, wie eine Media Foundation Transformation (MFT) Formatänderungen beim Streaming behandeln soll.
ms.assetid: b0a94760-b4dd-4e50-a5ce-a1f674dde156
title: Verarbeiten von streamänderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2adf3cbc0504a37fe611b77047c73f85b9d1e742
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214967"
---
# <a name="handling-stream-changes"></a>Verarbeiten von streamänderungen

In diesem Thema wird beschrieben, wie eine Media Foundation Transformation (MFT) Formatänderungen beim Streaming behandeln soll.

> [!IMPORTANT]
>
> Dieses Thema gilt nicht für Encoder. Encoder sollten keine Formatänderungen weitergeben, wie in diesem Thema beschrieben. Encoder sollten nur einen Eingabetyp akzeptieren, der mit dem aktuell konfigurierten Ausgabetyp übereinstimmt.

 

## <a name="overview-of-format-changes"></a>Übersicht über Format Änderungen

Im Allgemeinen gibt es zwei Gründe dafür, dass ein Format während des Streamings geändert werden kann.

-   Der Client kann zu einem Stream mit einem neuen Format wechseln. Beispielsweise kann dies im digitalen Fernsehen aufgrund einer Kanal Änderung auftreten.
-   In einigen Videoformaten, z. b. H. 264, kann der Bitstrom eine Formatänderung signalisieren. Diese Änderungen können Änderungen an der Feld Dominanz, der Videoauflösung oder dem Pixel Seitenverhältnis einschließen.

Wenn sich der Codierungstyp ändert, muss der Client möglicherweise die MFT aus der Pipeline entfernen und durch eine andere MFT ersetzen. (Beispielsweise muss der Client möglicherweise einen neuen Decoder austauschen.) Diese Situation wird in diesem Thema nicht behandelt. In diesem Thema wird nur die Groß-/Kleinschreibung behandelt, in der das aktuelle MFT das neue Format verarbeiten kann

Wenn sich das Format ändert, erfordert die MFT möglicherweise einen neuen Eingabetyp, einen neuen Ausgabetyp oder beides.

-   Änderungen am Eingabetyp werden vom Client initiiert. Ein MFT ändert seinen eigenen Eingabetyp nie.
-   Änderungen am Ausgabetyp werden vom MFT initiiert. Der MFT signalisiert, dass ein neuer Ausgabetyp erforderlich ist, und der Client aushandiert den neuen Ausgabetyp mit dem MFT.

Daher sind drei verschiedene Fälle möglich:

-   Der Client legt einen neuen Eingabetyp fest. Der MFT nutzt das neue Format ohne Änderung des Ausgabe Typs.
-   Der Client legt einen neuen Eingabetyp fest, und dies löst eine Änderung im Ausgabetyp aus.
-   Der Eingabetyp ändert sich nicht, aber der MFT erkennt eine Formatänderung im Bitstream, die einen neuen Ausgabetyp erfordert.

## <a name="implementing-format-changes"></a>Implementieren von Format Änderungen

Im restlichen Teil dieses Themas wird beschrieben, wie der Client eine Formatänderung verarbeiten und Formatänderungen in einer MFT implementieren kann.

### <a name="output-type"></a>Ausgabetyp

Jede MFT kann wie folgt eine Änderung des Ausgabe Typs initiieren:

1.  Vom Client wird " [**IMF Transform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)" aufgerufen. Die MFT antwortet wie folgt:
    1.  Der MFT erzeugt kein Ausgabe Beispiel in " [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)".
    2.  Der MFT legt das Flag für die **Änderung des MFT- \_ Ausgabe \_ Daten \_ Puffer \_ \_ Formats** im **dwStatus** -Member der [**MFT- \_ Ausgabe \_ Daten \_ Puffer**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_data_buffer) Struktur fest.
    3.  Die [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) -Methode gibt den Fehlercode MF-E-Transform-Daten **\_ \_ \_ Strom \_ Änderung** zurück.
2.  Der Client ruft [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)auf. Diese Methode gibt einen aktualisierten Satz von Ausgabetypen zurück.
3.  Der Client ruft [**setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) auf, um einen neuen Ausgabetyp festzulegen.
4.  Der Client setzt das Aufrufen von [**ProcessInput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessinput) / [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)fort.

### <a name="input-type"></a>Eingabetyp

Änderungen am Eingabetyp werden vom Client initiiert, nie vom MFT. Wenn sich der Eingabetyp ändert, kann dies eine Änderung am Ausgabetyp auslöst.

Die genaue Reihenfolge der Ereignisse hängt vom Wert des MFT-Unterstützungs Attributs für das [**\_ \_ dynamische \_ Format \_**](mft-support-dynamic-format-change-attribute.md) ab.



| Wert     | BESCHREIBUNG                                                     |
|-----------|-----------------------------------------------------------------|
| **FALSE** | Bevor der Client einen neuen Eingabetyp festlegt, muss er die MFT entladen. |
| **TRUE**  | Der Client kann einen neuen Eingabetyp festlegen, ohne die MFT zu entleeren.   |



 

Ein MFT macht dieses Attribut über seine [**imftransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) -Methode verfügbar. Der Standardwert dieses Attributs ist **false**. Wenn das Attribut vom MFT nicht festgelegt wird, behandeln Sie den Wert als **false**.

**MFT- \_ Unterstützung der \_ dynamischen \_ Format \_ Änderung ist falsch**

1.  Der Client sendet die [**MFT \_ - \_ Nachrichten \_ Befehls**](mft-message-command-drain.md) Ausgleichs Nachricht.
2.  Der Client zieht die MFT durch Aufrufen von [**imftransform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) , bis **ProcessOutput** zurückgibt, **\_ dass MF E \_ Transform \_ \_ mehr \_ Eingaben benötigt**.
3.  Der Client ruft [**imftransform:: setinputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) auf, um den neuen Eingabetyp festzulegen.
4.  Der MFT überprüft den Eingabetyp. Wenn der Typ ungültig ist, gibt [**setinputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) **MF \_ E \_ invalidmediatype** oder einen anderen Fehlercode zurück. Andernfalls gibt "* **tinputtype** " "S OK" zurück \_ .
5.  Wenn der Eingabetyp gültig ist, wertet der MFT aus, ob der Ausgabetyp ebenfalls geändert wird. Andernfalls wird das Streaming fortgesetzt, und es ist keine weitere Aktion erforderlich.
6.  Wenn sich der Ausgabetyp ändert:
    1.  Der MFT macht seinen aktuellen Ausgabe Medientyp ungültig und aktualisiert die Liste der verfügbaren Ausgabemedien Typen.
    2.  Der nächste Rückruf von [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) gibt **die \_ \_ Änderungs Daten \_ Strom \_ Änderung von MF E** zurück, wie im vorherigen Abschnitt beschrieben.
    3.  Der Client ruft [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) auf, um die aktualisierte Liste der Ausgabetypen zu erhalten.
    4.  Der Client ruft [**setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)auf.

**MFT- \_ Unterstützung \_ \_ für dynamische Format \_ Änderung ist true**

1.  Der Client ruft [**imftransform:: setinputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) auf, um den neuen Eingabetyp festzulegen.
2.  Der MFT überprüft den Eingabetyp. Wenn der Typ ungültig ist, gibt [**setinputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) **MF \_ E \_ invalidmediatype** oder einen anderen Fehlercode zurück. Andernfalls gibt "* **tinputtype** " "S OK" zurück \_ .
3.  Wenn der Eingabetyp gültig ist, wertet der MFT aus, ob der Ausgabetyp ebenfalls geändert wird. Andernfalls wird das Streaming fortgesetzt, und es ist keine weitere Aktion erforderlich.
4.  Bevor der Ausgabetyp geändert wird, muss der MFT alle zwischengespeicherten Eingabe Beispiele wie folgt verarbeiten:
    1.  Der aktuelle Ausgabetyp wird vom MFT nicht für ungültig erklärt.
    2.  Der MFT erzeugt so viele Ausgaben wie aus den zwischengespeicherten Eingabe Beispielen.
    3.  Es ist optional, ob der MFT bei der Verarbeitung der zwischengespeicherten Beispiele neue Eingabe Beispiele akzeptiert. Wenn dies der Fall ist, wird in den neuen Eingabe Beispielen das neue Eingabeformat verwendet, sodass die MFT den Punkt nachverfolgen muss, an dem sich das Format geändert hat.
5.  Nachdem die MFT alle Abtastungen verarbeitet hat, die vor dem Eingabetyp empfangen wurden, gibt [**imftransform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) die **Änderung von MF \_ E \_ Transform \_ Stream \_** zurück.
6.  Der MFT macht seinen aktuellen Ausgabetyp ungültig und aktualisiert die Liste der verfügbaren Ausgabemedien Typen.
7.  Der Client aushandiert den neuen Ausgabetyp, wie zuvor beschrieben.

[Asynchrone MFTs](asynchronous-mfts.md) müssen den Wert **true** für das [**MFT-Unterstützungs Attribut für \_ \_ dynamische \_ Format \_ Änderungen**](mft-support-dynamic-format-change-attribute.md) zurückgeben. Wenn ein asynchroner MFT verwendet wird, kann der Client davon ausgehen, dass die **MFT- \_ Unterstützung des \_ dynamischen \_ Format \_ Änderungs** Attributs auf **true** festgelegt ist.

Wenn die [**MFT- \_ Unterstützung für die \_ dynamische \_ Format \_ Änderung**](mft-support-dynamic-format-change-attribute.md) **zutrifft**, besteht der Hauptunterschied darin, dass der Client die MFT nicht vor dem Festlegen eines neuen Eingabetyps entladen muss. Folglich ändert sich der Eingabetyp möglicherweise, während der MFT Eingabe Beispiele hält. Es ist wichtig, dass die MFT diese Beispiele nicht einfach löscht. Außerdem kann der Ausgabetyp erst geändert werden, wenn der MFT alle zwischengespeicherten Daten verarbeitet.

Der vorherige Absatz gilt besonders für Video-Decoders, die intercodierte Frames aus Temporaler Reihenfolge empfangen können und daher zwischengespeichert werden müssen. Wenn eine MFT keine Eingabe Beispiele zwischenspeichert, ist die Ableitung im Grunde kein op. In diesem Fall kann die MFT die [**MFT- \_ Unterstützung für das \_ dynamische \_ Format \_ ändern**](mft-support-dynamic-format-change-attribute.md) auf **false** festlegen (oder das Attribut nicht festlegen).

Beachten Sie außerdem, dass jedes MFT erwartet, dass Formatänderungen ordnungsgemäß verarbeitet werden, nachdem es entladen wurde. Das Change-Attribut für die [**MFT- \_ Unterstützung für das \_ dynamische \_ Format \_**](mft-support-dynamic-format-change-attribute.md) gibt an, ob die MFT Format Änderungen ohne Abbild

## <a name="change-in-interlace-mode"></a>Änderung im Interlace-Modus

Änderungen im Video-interschnür Modus sind ein Sonderfall, da Sie den aktuellen Medientyp nicht für ungültig erklären. Stattdessen wird der damit-Modus für jeden Video Frame durch Festlegen von Attributen für das Medien Beispiel angegeben. Ein Video-MFT sollte jedes Eingabe Beispiel auf das vorhanden sein dieser Flags überprüfen.

Der damit-Modus kann sich ändern, wenn die Feld Dominanz von oben nach unten Feld wechselt oder wenn das Video zwischen progressiven und Zeilen Sprung Bildern wechselt.

Weitere Informationen finden Sie unter [Interlace Flags on Samples](video-interlacing.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben eines benutzerdefinierten MFT](writing-a-custom-mft.md)
</dt> </dl>

 

 



