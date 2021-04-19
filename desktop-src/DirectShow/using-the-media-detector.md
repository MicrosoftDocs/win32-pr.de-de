---
description: Verwenden des Medien Detektors
ms.assetid: 462150d5-7315-4c2b-81b0-964a788ec47d
title: Verwenden des Medien Detektors
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ebdb05eb47c7efabcc3234fb6ac2411a46e40d4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106355708"
---
# <a name="using-the-media-detector"></a>Verwenden des Medien Detektors

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

Der Medien Detektor ist ein Hilfsobjekt, das Informationen über eine Datei abrufen kann, z. b. die Anzahl der Streams, ihren Typ und ihre Dauer. Sie enthält auch Methoden zum Abrufen von Poster-Frames aus einem Videostream. Sie macht die [**imediadet**](imediadet.md) -Schnittstelle verfügbar.

Der Medien Detektor arbeitet in einem von zwei Modi. Wenn Sie eine Instanz des Medien Detektors erstellen, wird diese nicht an eine bestimmte Quelldatei angefügt. In diesem Modus können Sie Datenstrom Informationen aus mehreren Quelldateien abrufen. Nachdem Sie jedoch mithilfe des Medien Detektors einen Poster-Frame abgerufen haben, wechselt er in den *Bitmap*-Abruf Modus. Im bitmapingmodus wird der Medien Detektor an einen bestimmten Videostream angefügt, und die Datenstrom Informationsmethoden funktionieren nicht mehr. Außerdem gibt es keine Möglichkeit zum Wechsel des Medien Detektors in seinen Start Modus. Rufen Sie daher alle benötigten Datenströme ab, bevor Sie Poster-Frames abrufen, oder erstellen Sie für jeden Stream neue Instanzen des Medien Detektors.

Gehen Sie folgendermaßen vor, um streaminformationen zu erhalten:

1.  Nennen Sie [**imediadet::p UT \_ filename**](imediadet-put-filename.md) mit dem Namen der Quelldatei.
2.  Rufen Sie [**imediadet:: get \_ outputstreams**](imediadet-get-outputstreams.md) auf, um die Anzahl der Streams in der Quelle abzurufen.
3.  Geben Sie eine streamnummer mit [**imediadet an::p UT \_ currentstream**](imediadet-put-currentstream.md). Dann wenden Sie eine oder mehrere der folgenden Methoden an:
    -   [**Imediadet:: get \_ Streamtype**](imediadet-get-streamtype.md): Ruft den Medientyp des Streams ab.
    -   [**Imediadet:: get \_ Streamlength**](imediadet-get-streamlength.md): Ruft die Dauer des Streams ab.
    -   [**Imediadet:: get \_ Framerate: Ruft die Framerate**](imediadet-get-framerate.md)eines Videostreams ab.

Um einen Poster-Frame zu erhalten, geben Sie die Datenstrom Nummer an, wie im vorherigen Schritt. Anschließend wird entweder [**imediadet:: getbitmapbits**](imediadet-getbitmapbits.md)aufgerufen, mit dem ein Poster-Frame in einen Puffer kopiert wird, oder [**imediadet:: Beschreib tebitmapbits**](imediadet-writebitmapbits.md), der einen Poster-Frame in einer Datei speichert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Quellen](working-with-sources.md)
</dt> </dl>

 

 



