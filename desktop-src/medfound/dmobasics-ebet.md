---
description: DMO-Grundlagen
ms.assetid: eaf453d2-69f8-432a-8a58-1ed70778f182
title: DMO-Grundlagen (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b1aca2fcd7e70cf78e2e95135aee73c454b910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214312"
---
# <a name="dmo-basics-microsoft-media-foundation"></a>DMO-Grundlagen (Microsoft Media Foundation)

Dieses Thema enthält eine kurze Übersicht über DMOS im Zusammenhang mit Windows Media Codecs. Weitere Informationen zu DMOS finden Sie unter [DirectX-Medienobjekte](../directshow/directx-media-objects.md).

Ein DMO ist ein COM-Objekt, das Daten transformiert. Sie übergeben Daten an Sie und geben die transformierten Daten zurück. Bei einem Codec-Encoder-DMO geben Sie unkomprimierte Mediendaten ein, und der DMO liefert komprimierte Mediendaten. Der Hauptvorteil der Verwendung von dmos besteht darin, dass alle die gleiche Basisschnittstelle ( [**imediaobject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)) implementieren, was die Arbeit mit Ihnen vereinfacht, da Sie das gleiche Objekt unabhängig vom Typ der Transformation, die ausgeführt wird, verwenden können.

Da es Variablen gibt, die an einer beliebigen Art von Datentransformation beteiligt sind, muss die Transformation für Audiodaten und Videos die verschiedensten möglichen Medien Konfigurationen berücksichtigen. Die Windows Media Audio-und Video Codecs unterstützen außerdem eine Reihe spezieller Features, die Sie mit dem DMO konfigurieren können.

Im Allgemeinen werden die Variablen Informationen, die vom Codec-DMOS zum Komprimieren und Dekomprimieren digitaler Medien benötigt werden, auf eine von drei Arten übermittelt:

-   Legen Sie den Eingabetyp für den DMO fest, um die Merkmale der nicht komprimierten Medien zu übermitteln, die Sie an einen DMO-Encoder übergeben, sowie die Merkmale der komprimierten Medien, die Sie an einen DMO-Decoder übergeben.
-   Legen Sie den Ausgabetyp für den DMO fest, um die Merkmale der von einem Encoder-DMO gelieferten komprimierten Medien und die Merkmale der nicht komprimierten Medien zu übermitteln, die von einem Decoder-DMO übermittelt werden.
-   Konfigurieren Sie mithilfe der Methoden der **IPropertyBag** -Schnittstelle andere Einstellungen, die die verschiedenen Funktionen der Codec-DMOS als Eigenschaften unterstützen. **IPropertyBag** ist eine Standard-COM-Schnittstelle, die von allen Codec-DMOS unterstützt wird.

Darüber hinaus werden einige Codec-Features über andere Schnittstellen verwaltet, die für die Codec-DMOS spezifisch sind. Diese Schnittstellen werden für jeden Codec im Abschnitt [Codec-Objekte](codecobjects.md)aufgelistet.

Eingabe-und Ausgabetypen sind spezifisch für Eingabe-und Ausgabestreams. Jeder Stream stellt eine diskrete Darstellung des Inhalts dar. Der Windows Media Video Encoder DMO verfügt z. b. über einen einzelnen Eingabestream und zwei Ausgabedaten Ströme. Der Eingabestream akzeptiert nicht komprimierte Videobeispiele. Der erste der beiden Ausgabedaten Ströme liefert komprimierte Beispiele. der andere stellt nicht komprimierte Beispiele bereit. Die einzelnen Beispiele in einem Ausgabestream repräsentieren denselben Inhalt wie die entsprechenden Beispiele im anderen Stream, aber jeder Stream liefert diese Beispiele in einem anderen Format.

Jeder Stream (Eingabe oder Ausgabe) unterstützt einen oder mehrere Medientypen. Ein Medientyp oder-Format wird durch eine [**DMO- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) Struktur beschrieben. Sie können den DMO nach den Typen Abfragen, die von einem Ausgabestream unterstützt werden, indem Sie [**imediaobject:: getoutputtype**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype)aufrufen. Diese Methode gibt einen gültigen Ausgabetyp (in einigen Fällen teilweise unvollständig) für diesen Stream zurück. Sie können die unterstützten Medientypen für einen Ausgabestream auflisten, indem Sie wiederholte Aufrufe von **getoutputtype** ausführen und den Typparameter bei jedem Aufruf erhöhen. Wenn der übergebene Typindex außerhalb des gültigen Bereichs liegt, gibt die Methode **DMO \_ E \_ nicht \_ mehr \_ Elemente** zurück. Eingabeformate können mithilfe der [**imediaobject:: getinputtype**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype) -Methode auf die gleiche Weise aufgezählt werden.

Die Typen, die vom DMO aufgelistet werden, sind nur die "bevorzugten" Typen. andere Typen werden jedoch möglicherweise unterstützt. Sie können einen Ausgabetyp überprüfen, indem Sie [**imediaobject:: setoutputtype**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype)aufrufen. Verwenden Sie [**imediaobject:: setinputtype**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) , um einen Eingabetyp zu validieren. Beide Methoden geben den **DMO \_ E- \_ Typ \_ nicht \_ akzeptiert** zurück, wenn die übergebenen [**DMO- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) Struktur ungültig ist. Einige DMOS erfordern, dass Sie einen Ausgabetyp vor dem Auflisten von Eingabetypen festlegen. Die Windows Media Audio-und Videocodec-DMOS haben alle Eingaben und Ausgaben, die über eine abhängige Validierung verfügen. Das heißt, der von Ihnen festgelegte Ausgabetyp legt die Überprüfungs Kriterien für den Eingabetyp fest. Es gibt auch einige Eigenschaften, die die gültigen Eingabe-und Ausgabetypen ändern, wenn Sie festgelegt sind. Aus diesem Grund sollten Sie alle gewünschten Eigenschaften für das DMO festlegen, bevor Sie Typen aufzählen.

Wenn Sie die Ausgabe-und Eingabetypen für den DMO festgelegt haben, können Sie mit der Verarbeitung von Beispielen beginnen. Jedes Eingabe Beispiel wird mithilfe eines [**imediaobject::P rocessinput-Objekts**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput)an den Codec übergeben, und jedes Ausgabe Beispiel wird vom Codec übermittelt, wenn Sie [**imediaobject aufrufen::P rocess Output**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Codec-DMOS](workingwithcodecdmos.md)
</dt> </dl>

 

 
