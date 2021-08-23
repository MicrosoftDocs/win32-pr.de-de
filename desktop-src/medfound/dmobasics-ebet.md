---
description: DMO Grundlagen
ms.assetid: eaf453d2-69f8-432a-8a58-1ed70778f182
title: DMO Grundlagen (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f24c7fb988d5e5225f292585a5562cce22e67c007175fa7ddc4cd86e40ec1d18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742359"
---
# <a name="dmo-basics-microsoft-media-foundation"></a>DMO Grundlagen (Microsoft Media Foundation)

Dieses Thema bietet eine kurze Übersicht über DMOs im Zusammenhang mit Windows Mediencodecs. Weitere Informationen zu DMOs finden Sie unter [DirectX Media Objects](../directshow/directx-media-objects.md).

Ein DMO ist ein COM-Objekt, das Daten transformiert. Sie übergeben Daten an sie und geben die transformierten Daten zurück. Bei einem Codecencoder DMO geben Sie unkomprimierte Mediendaten ein, und der DMO übermittelt komprimierte Mediendaten. Der Hauptvorteil der Verwendung von DMOs besteht darin, dass alle die gleiche Basisschnittstelle , [**IMediaObject,**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)implementieren, die die Arbeit mit ihnen vereinfacht, da Sie das gleiche Objekt verwenden können, unabhängig vom Typ der transformation, die ausgeführt wird.

Da an jeder Art von Datentransformation Variablen beteiligt sind, muss die Audio- und Videotransformation die vielzahl möglicher Medienkonfigurationen berücksichtigen. Die Windows Medienaudio- und Videocodecs unterstützen auch eine Reihe von speziellen Features, die Sie mithilfe der DMO konfigurieren müssen.

Im Allgemeinen werden die Variableninformationen, die von den Codec-DMOs zum Komprimieren und Dekomprimieren digitaler Medien benötigt werden, auf eine von drei Arten vermittelt:

-   Legen Sie den Eingabetyp auf dem DMO fest, um die Merkmale der unkomprimierten Medien, die Sie an einen Encoder übergeben DMO, und die Merkmale der komprimierten Medien zu vermitteln, die Sie an einen Decoder übergeben DMO.
-   Legen Sie den Ausgabetyp auf dem DMO fest, um die Merkmale der komprimierten Medien, die von einem Encoder DMO bereitgestellt werden, und die Merkmale der nicht komprimierten Medien zu vermitteln, die von einem Decoder DMO.
-   Konfigurieren Sie mithilfe der Methoden der **IPropertyBag-Schnittstelle** andere Einstellungen, die die verschiedenen Features der Codec-DMOs als Eigenschaften unterstützen. **IPropertyBag** ist eine COM-Standardschnittstelle, die von allen Codec-DMOs unterstützt wird.

Darüber hinaus werden einige Codecfeatures mit anderen Schnittstellen verwaltet, die für die Codec-DMOs spezifisch sind. Diese Schnittstellen sind für jeden Codec im Abschnitt [CodecObjekte](codecobjects.md)aufgeführt.

Eingabe- und Ausgabetypen sind spezifisch für Eingabe- und Ausgabestreams. Jeder Stream stellt eine diskrete Darstellung des Inhalts dar. Beispielsweise verfügt der Windows Media Video Encoder DMO über einen einzelnen Eingabestream und zwei Ausgabestreams. Der Eingabestream akzeptiert unkomprimierte Videobeispiele. Der erste der beiden Ausgabestreams liefert komprimierte Beispiele. der andere enthält unkomprimierte Beispiele. Die einzelnen Beispiele in einem Ausgabestream stellen den gleichen Inhalt wie die entsprechenden Beispiele im anderen Stream dar, aber jeder Stream stellt diese Beispiele in einem anderen Format bereit.

Jeder Stream (Eingabe oder Ausgabe) unterstützt einen oder mehrere Medientypen. Ein Medientyp oder -format wird durch eine [**DMO \_ MEDIA \_ TYPE-Struktur**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) beschrieben. Sie können die DMO nach den Typen abfragen, die von einem Ausgabestream unterstützt werden, indem [**Sie IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype)aufrufen. Diese Methode gibt einen gültigen (in einigen Fällen teilweise unvollständigen) Ausgabetyp für diesen Stream zurück. Sie können die unterstützten Medientypen für einen Ausgabestream aufzählen, indem Sie wiederholt **GetOutputType** aufrufen und den Typparameter mit jedem Aufruf erhöhen. Wenn der übergebene Typindex außerhalb der Grenzen liegt, gibt die Methode **DMO E NO MORE \_ \_ \_ \_ ITEMS** zurück. Eingabeformate können auf die gleiche Weise mithilfe der [**IMediaObject::GetInputType-Methode**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype) aufzählt werden.

Die Typen, die vom DMO aufzählt werden, sind nur die "bevorzugten" Typen, andere Typen können jedoch unterstützt werden. Sie können einen Ausgabetyp überprüfen, indem Sie [**IMediaObject::SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype)aufrufen. Verwenden Sie [**IMediaObject::SetInputType,**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) um einen Eingabetyp zu überprüfen. Beide Methoden geben **DMO \_ E TYPE NOT \_ ACCEPTED \_ \_ zurück,** wenn die [**übergebene \_ DMO MEDIA \_ TYPE-Struktur**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) ungültig ist. Für einige DMOs müssen Sie einen Ausgabetyp festlegen, bevor Sie Eingabetypen aufzählen. Die WINDOWS Medienaudio- und Videocodec-DMOs verfügen alle über Eingaben und Ausgaben, die eine voneinander abhängige Überprüfung aufweisen. Das heißt, der von Ihnen festgelegte Ausgabetyp legt die Validierungskriterien für den Eingabetyp fest. Es gibt auch einige Eigenschaften, die beim Festlegen die gültigen Eingabe- und Ausgabetypen ändern. Aus diesem Grund sollten Sie alle gewünschten Eigenschaften für die DMO festlegen, bevor Sie Typen aufzählen.

Wenn Sie die Ausgabe- und Eingabetypen für die DMO festgelegt haben, können Sie mit der Verarbeitung von Beispielen beginnen. Jedes Eingabebeispiel wird mithilfe eines Aufrufs von [**IMediaObject::P rocessInput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput)an den Codec übergeben, und jedes Ausgabebeispiel wird vom Codec übermittelt, wenn Sie [**IMediaObject::P rocessOutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput)aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Codec-DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 
