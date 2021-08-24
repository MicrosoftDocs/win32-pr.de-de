---
description: Bereitstellen eines benutzerdefinierten Video resizer
ms.assetid: 4009f93f-cd50-440f-b943-7e3700e0e2cb
title: Bereitstellen eines benutzerdefinierten Video resizer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a006f4620accc3917ae3072846f99f7537a1eadfaab21da36aab17f17d94e433
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747900"
---
# <a name="providing-a-custom-video-resizer"></a>Bereitstellen eines benutzerdefinierten Video resizer

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

> [!Note]  
> Für dieses Feature ist DirectX 9.0 oder höher erforderlich.

 

Wenn [DirectShow Editing Services](directshow-editing-services.md) (DES) die Größe eines Videoquellenclips geändert, ist das Standardverhalten *stretchBlt*, das schnell, aber nicht gegen Aliase ist. Sie können das Größenänderungsverhalten ändern, indem Sie einen benutzerdefinierten Resizer als DirectShow-Transformationsfilter implementieren. Der Filter muss die [**IResize-Schnittstelle**](iresize.md) verfügbar machen, mit der DES die Größe des Eingabe- und Ausgabevideos angeben kann. Informationen zum Schreiben eines Transformationsfilters finden Sie unter [Schreiben von Transformationsfiltern.](writing-transform-filters.md) Die **CTransformFilter-Basisklasse** wird als Ausgangspunkt empfohlen. Beachten Sie beim Implementieren des Filters Folgendes:

-   Unterstützen Sie **die IResize-Schnittstelle** für den Filter (nicht die Stecknadeln).
-   Der Filter sollte nur [**VIDEOINFOHEADER-Formate**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) (FORMAT \_ VideoInfo) akzeptieren. Lehnen Sie andere Formattypen ab.
-   Das Videoformat von DES kann ein beliebiger nicht komprimierter RGB-Typ sein, einschließlich 32-Bit-RGB mit Alpha (MEDIASUBTYPE \_ ARGB32). Ihr Filter kann Formate mit **biHeight** < 0 problemlos ablehnen.
-   Bevor die Render-Engine eine Verbindung mit dem Ausgabepin des Filters herstellt, ruft sie [**IResize::p ut \_ MediaType**](iresize-put-mediatype.md) auf, um den Ausgabetyp fest zu legen. Sie kann auch [**IResize::p ut \_ Size aufrufen,**](iresize-put-size.md) um die Ausgabegröße anzupassen. Sie kann diese beiden Methoden in beliebiger Reihenfolge und so oft aufrufen, bevor der Ausgabepin miteinander verknüpft wird.
-   Nachdem die Render-Engine die Verbindung mit dem Ausgabepin herstellt, kann sie **put \_ Size erneut** aufrufen. Der Größenfilter sollte seine Ausgabepins erneut mit der neuen Größe verbinden.
-   Strecken Sie in der [**CTransformFilter::Transform-Methode**](ctransformfilter-transform.md) des Filters das Eingabevideo auf die Ausgabegröße.
-   Ihr Filter sollte niemals das Flag für die Diskontinuität im Ausgabebeispiel festlegen oder einen Medientyp an das Ausgabebeispiel anfügen.
-   Implementieren Sie die **IPersistStream-Schnittstelle,** um den Zustand des Filters in einer GraphEdit-Datei (.grf) zu speichern. (Dies ist optional, aber nützlich für Tests.)

Um den Größenfilter verwenden zu können, muss der Filter als COM-Objekt im System des Benutzers registriert werden. Bevor die Anwendung das Videoprojekt rendert, fragen Sie die Render-Engine nach der [**IRenderEngine2-Schnittstelle**](irenderengine2.md) ab, und rufen [**Sie IRenderEngine2::SetResizerGUID**](irenderengine2-setresizerguid.md) mit der CLSID des Resizerfilters auf.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rendern eines Project](rendering-a-project.md)
</dt> </dl>

 

 



