---
description: In diesem Thema wird beschrieben, wie eine Media Foundation Transform (MFT) Formatänderungen während des Streamings verarbeiten soll.
ms.assetid: b0a94760-b4dd-4e50-a5ce-a1f674dde156
title: Behandeln von Streamänderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e238073bf518bc875b7b2d536c758eab48c8502278aae6780999c7616430337e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974429"
---
# <a name="handling-stream-changes"></a>Behandeln von Streamänderungen

In diesem Thema wird beschrieben, wie eine Media Foundation Transform (MFT) Formatänderungen während des Streamings verarbeiten soll.

> [!IMPORTANT]
>
> Dieses Thema gilt nicht für Encoder. Encoder sollten formatierte Änderungen nicht wie in diesem Thema beschrieben weiter geben. Encoder sollten nur einen Eingabetyp akzeptieren, der dem aktuell konfigurierten Ausgabetyp entspricht.

 

## <a name="overview-of-format-changes"></a>Übersicht über Formatänderungen

Im Allgemeinen gibt es zwei Gründe, warum sich ein Format während des Streamings ändern kann.

-   Der Client kann zu einem Stream mit einem neuen Format wechseln. Im digitalen Fernsehgerät kann dies beispielsweise aufgrund einer Kanaländerung auftreten.
-   In einigen Videoformaten, z. B. H.264, kann der Bitstream eine Formatänderung signalisieren. Solche Änderungen können Änderungen der Felddominanz, videoauflösung oder des Pixel-Seitenverhältnisses umfassen.

Wenn sich der Codierungstyp ändert, muss der Client möglicherweise den MFT aus der Pipeline entfernen und durch einen anderen MFT ersetzen. (Beispielsweise muss der Client möglicherweise in einem neuen Decoder austauschen.) In diesem Thema wird diese Situation nicht beschrieben. In diesem Thema wird nur der Fall behandelt, in dem der aktuelle MFT das neue Format verarbeiten kann.

Wenn sich das Format ändert, erfordert MFT möglicherweise einen neuen Eingabetyp, einen neuen Ausgabetyp oder beides.

-   Änderungen am Eingabetyp werden vom Client initiiert. Ein MFT ändert nie seinen eigenen Eingabetyp.
-   Änderungen am Ausgabetyp werden vom MFT initiiert. Der MFT signalisiert, dass ein neuer Ausgabetyp erforderlich ist, und der Client handelt den neuen Ausgabetyp mit dem MFT aus.

Daher sind drei unterschiedliche Fälle möglich:

-   Der Client legt einen neuen Eingabetyp fest. MFT verwendet das neue Format ohne Änderung des Ausgabetyps.
-   Der Client legt einen neuen Eingabetyp fest, und dies löst eine Änderung des Ausgabetyps aus.
-   Der Eingabetyp ändert sich nicht, aber MFT erkennt eine Formatänderung im Bitstream, die einen neuen Ausgabetyp erfordert.

## <a name="implementing-format-changes"></a>Implementieren von Formatänderungen

Im weiteren Verlauf dieses Themas wird beschrieben, wie der Client eine Formatänderung verarbeiten und Formatänderungen in einem MFT implementieren soll.

### <a name="output-type"></a>Ausgabetyp

Jeder MFT kann wie folgt eine Änderung des Ausgabetyps initiieren:

1.  Der Client ruft [**DIETTRANSFORM::P rocessOutput auf.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) MFT antwortet wie folgt:
    1.  MFT erzeugt kein Ausgabebeispiel in [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).
    2.  MFT legt das **MFT \_ OUTPUT DATA BUFFER FORMAT \_ \_ \_ \_ CHANGE-Flag** im **dwStatus-Member** der [**MFT OUTPUT DATA \_ \_ \_ BUFFER-Struktur**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_data_buffer) fest.
    3.  Die [**ProcessOutput-Methode**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) gibt den Fehlercode **MF \_ E TRANSFORM STREAM CHANGE \_ \_ \_ zurück.**
2.  Der Client ruft [**DIETTRANSFORM::GetOutputAvailableType auf.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) Diese Methode gibt einen aktualisierten Satz von Ausgabetypen zurück.
3.  Der Client ruft [**SetOutputType auf,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) um einen neuen Ausgabetyp zu festlegen.
4.  Der Client setzt den Aufruf von [**ProcessInput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessinput) / [**ProcessOutput wieder ein.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)

### <a name="input-type"></a>Eingabetyp

Änderungen am Eingabetyp werden vom Client initiiert, nie vom MFT. Wenn sich der Eingabetyp ändert, wird möglicherweise eine Änderung des Ausgabetyps ausgelöst.

Die genaue Abfolge der Ereignisse hängt vom Wert des [**MFT \_ SUPPORT DYNAMIC FORMAT \_ \_ \_ CHANGE-Attributs**](mft-support-dynamic-format-change-attribute.md) ab.



| Wert     | BESCHREIBUNG                                                     |
|-----------|-----------------------------------------------------------------|
| **FALSE** | Bevor der Client einen neuen Eingabetyp fest legt, muss er den MFT leeren. |
| **TRUE**  | Der Client kann einen neuen Eingabetyp festlegen, ohne den MFT zu leeren.   |



 

Ein MFT macht dieses Attribut über seine [**METHODE ZUM ÜBERTRAGEN::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) verfügbar. Der Standardwert dieses Attributs ist **FALSE.** Wenn MFT das Attribut nicht festgelegt, behandeln Sie den Wert als **FALSE.**

**MFT SUPPORT DYNAMIC FORMAT CHANGE is FALSE (MFT-UNTERSTÜTZUNG \_ \_ FÜR DYNAMISCHE \_ \_ FORMATÄNDERUNG IST FALSE)**

1.  Der Client sendet die [**MFT \_ MESSAGE COMMAND \_ \_ DRAIN-Nachricht.**](mft-message-command-drain.md)
2.  Der Client entleert den MFT durch Aufrufen [**vonGEFTransform::P rocessOutput,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) bis **ProcessOutput** **MF \_ E TRANSFORM NEED MORE INPUT \_ \_ \_ \_ zurückgibt.**
3.  Der Client ruft [**DEN TYP DERTRANSFORM::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) auf, um den neuen Eingabetyp zu festlegen.
4.  Der MFT überprüft den Eingabetyp. Wenn der Typ ungültig ist, gibt [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) **MF \_ E \_ INVALIDMEDIATYPE** oder einen anderen Fehlercode zurück. Andernfalls **gibt SetInputType** S \_ OK zurück.
5.  Wenn der Eingabetyp gültig ist, wertet MFT aus, ob sich auch der Ausgabetyp ändert. Ander denn, das Streaming wird fortgesetzt, und es ist keine weitere Aktion erforderlich.
6.  Wenn sich der Ausgabetyp ändert:
    1.  Der MFT macht seinen aktuellen Ausgabemedientyp ungültig und aktualisiert die Liste der verfügbaren Ausgabemedientypen.
    2.  Der nächste Aufruf von [**ProcessOutput gibt**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) **MF \_ E TRANSFORM \_ STREAM \_ \_ CHANGE** zurück, wie im vorherigen Abschnitt beschrieben.
    3.  Der Client ruft [**DIETTRANSFORM::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) auf, um die aktualisierte Liste der Ausgabetypen zu erhalten.
    4.  Der Client ruft [**SetOutputType auf.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)

**MFT \_ SUPPORT \_ DYNAMIC \_ FORMAT \_ CHANGE is TRUE**

1.  Der Client ruft [**DEN TYP DERTRANSFORM::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) auf, um den neuen Eingabetyp zu festlegen.
2.  Der MFT überprüft den Eingabetyp. Wenn der Typ ungültig ist, gibt [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) **MF \_ E \_ INVALIDMEDIATYPE** oder einen anderen Fehlercode zurück. Andernfalls **gibt SetInputType** S \_ OK zurück.
3.  Wenn der Eingabetyp gültig ist, wertet MFT aus, ob sich auch der Ausgabetyp ändert. Ander denn, das Streaming wird fortgesetzt, und es ist keine weitere Aktion erforderlich.
4.  Bevor sich der Ausgabetyp ändert, muss MFT alle zwischengespeicherten Eingabebeispiele wie folgt verarbeiten:
    1.  Der aktuelle Ausgabetyp des MFT wird nicht ungültig.
    2.  MFT erzeugt so viel Ausgabe wie möglich aus den zwischengespeicherten Eingabebeispielen.
    3.  Es ist optional, ob MFT neue Eingabebeispiele akzeptiert, während die zwischengespeicherten Stichproben verarbeitet werden. Wenn ja, verwenden die neuen Eingabebeispiele das neue Eingabeformat, sodass der MFT den Zeitpunkt nachverfolgen muss, an dem sich das Format geändert hat.
5.  Nachdem der MFT alle Stichproben verarbeitet hat, die er vor der Änderung des Eingabetyps erhalten hat, gibt [**DER EINGABETRANSFORM::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) **MF \_ E TRANSFORM STREAM \_ CHANGE \_ \_ zurück.**
6.  Der MFT macht seinen aktuellen Ausgabetyp ungültig und aktualisiert die Liste der verfügbaren Ausgabemedientypen.
7.  Der Client handelt den neuen Ausgabetyp aus, wie zuvor beschrieben.

[Asynchrone MFTs](asynchronous-mfts.md) müssen den Wert **TRUE für** das [**MFT SUPPORT DYNAMIC FORMAT \_ \_ \_ \_ CHANGE-Attribut**](mft-support-dynamic-format-change-attribute.md) zurückgeben. Bei Verwendung eines asynchronen MFT kann der Client davon ausgehen, dass das **MFT \_ SUPPORT DYNAMIC \_ FORMAT \_ \_ CHANGE-Attribut** auf TRUE festgelegt **ist.**

Wenn [**MFT \_ SUPPORT DYNAMIC \_ FORMAT \_ \_ CHANGE**](mft-support-dynamic-format-change-attribute.md) **true** ist, besteht der Hauptunterschied in dem, dass der Client den MFT vor dem Festlegen eines neuen Eingabetyps nicht leeren muss. Daher kann sich der Eingabetyp ändern, während MFT Eingabebeispiele bei sich hält. Es ist wichtig, dass MFT diese Beispiele nicht einfach ausmustert. Außerdem kann sich der Ausgabetyp erst ändern, wenn der MFT alle zwischengespeicherten Daten verarbeitet.

Der vorherige Absatz gilt insbesondere für Videodecoder, die intercodierte Frames in temporaler Reihenfolge empfangen und daher zwischenspeichern müssen. Wenn ein MFT keine Eingabebeispiele zwischenspeichert, ist das Leeren im Wesentlichen kein Op. In diesem Fall kann MFT SUPPORT [**\_ DYNAMIC FORMAT \_ \_ \_ CHANGE**](mft-support-dynamic-format-change-attribute.md) auf **FALSE** festlegen (oder das Attribut nicht festlegen).

Beachten Sie außerdem, dass von jedem MFT erwartet wird, dass Formatänderungen nach dem Leeren ordnungsgemäß verarbeitet werden. Das [**MFT \_ SUPPORT DYNAMIC \_ FORMAT \_ \_ CHANGE-Attribut**](mft-support-dynamic-format-change-attribute.md) gibt an, ob MFT Formatänderungen ohne Leerung unterstützt.

## <a name="change-in-interlace-mode"></a>Änderung im Interlace-Modus

Änderungen im Video interlacing-Modus sind ein Sonderfall, da sie den aktuellen Medientyp nicht ungültig machen. Stattdessen wird der Interlace-Modus für jeden Videoframe angegeben, indem Attribute für das Medienbeispiel festgelegt werden. Ein Video-MFT sollte jedes Eingabebeispiel auf das Vorhandensein dieser Flags überprüfen.

Der Interlace-Modus kann sich ändern, wenn die Felddominanz vom oberen feld zum unteren Feld wechselt oder wenn das Video zwischen progressiven und interlaced-Bildern wechselt.

Weitere Informationen finden Sie unter [Interlace-Flags unter Beispiele.](video-interlacing.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben eines benutzerdefinierten MFT](writing-a-custom-mft.md)
</dt> </dl>

 

 



