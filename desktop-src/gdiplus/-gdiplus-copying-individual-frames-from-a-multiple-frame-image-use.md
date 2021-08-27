---
title: Kopieren einzelner Frames aus einem Bild mit mehreren Frames
description: Im folgenden Beispiel werden die einzelnen Frames aus einer TIFF-Datei mit mehreren Frames abgerufen.
ms.assetid: dfed0b61-2230-4911-a642-0a6e4beb08d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8398df806ad56b65114b0cc9a986ea53061183fa4658872b65b7d08ef7e38a9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115100"
---
# <a name="copy-individual-frames-from-a-multiple-frame-image"></a>Kopieren einzelner Frames aus einem Bild mit mehreren Frames

Im folgenden Beispiel werden die einzelnen Frames aus einer TIFF-Datei mit mehreren Frames abgerufen. Beim Erstellen der TIFF-Datei wurden die einzelnen Frames der Page-Dimension hinzugefügt (siehe [Erstellen und Speichern eines Multiple-Frame Bilds).](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md) Der Code zeigt jede der vier Seiten an und speichert jede Seite in einer separaten PNG-Datenträgerdatei.

Der Code erstellt ein [**Image-Objekt**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) aus der TIFF-Datei mit mehreren Frames. Um die einzelnen Frames (Seiten) abzurufen, ruft der Code die [**Image::SelectActiveFrame-Methode**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-selectactiveframe) dieses **Bildobjekts** auf. Das erste Argument, das an die **Image::SelectActiveFrame-Methode** übergeben wird, ist die Adresse einer GUID, die die Dimension angibt, in der die Frames zuvor der TIFF-Datei mit mehreren Frames hinzugefügt wurden. Die GUID FrameDimensionPage ist in Gdiplusimaging.h definiert. Andere GUIDs, die in dieser Headerdatei definiert sind, sind FrameDimensionTime und FrameDimensionResolution. Das zweite Argument, das an die **Image::SelectActiveFrame-Methode** übergeben wird, ist der nullbasierte Index der gewünschten Seite.

Der Code basiert auf der Hilfsfunktion GetEncoderClsid, die unter [Abrufen des Klassenbezeichners für einen Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)gezeigt wird.


```
GUID   pageGuid = FrameDimensionPage;
CLSID  encoderClsid;
Image  multi(L"Multiframe.tif");

// Get the CLSID of the PNG encoder.
GetEncoderClsid(L"image/png", &encoderClsid);

// Display and save the first page (index 0).
multi.SelectActiveFrame(&pageGuid, 0);
graphics.DrawImage(&multi, 10, 10);
multi.Save(L"Page0.png", &encoderClsid, NULL);

// Display and save the second page.
multi.SelectActiveFrame(&pageGuid, 1);
graphics.DrawImage(&multi, 200, 10);
multi.Save(L"Page1.png", &encoderClsid, NULL);

// Display and save the third page.
multi.SelectActiveFrame(&pageGuid, 2);
graphics.DrawImage(&multi, 10, 150);
multi.Save(L"Page2.png", &encoderClsid, NULL);

// Display and save the fourth page.
multi.SelectActiveFrame(&pageGuid, 3);
graphics.DrawImage(&multi, 200, 150);
multi.Save(L"Page3.png", &encoderClsid, NULL);
```



Die folgende Abbildung zeigt die einzelnen Seiten, wie sie im vorangehenden Code angezeigt werden.

![Abbildung einer geometrischen Form, eines Farbfotos, eines monocoloren Fotos und einer anderen geometrischen Form](images/multiframe1.png)

 

 



