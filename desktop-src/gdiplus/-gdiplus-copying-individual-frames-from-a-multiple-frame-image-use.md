---
title: Einzelne Frames aus einem Bild mit mehreren Frames kopieren
description: Im folgenden Beispiel werden die einzelnen Frames aus einer TIFF-Datei mit mehreren Frames abgerufen.
ms.assetid: dfed0b61-2230-4911-a642-0a6e4beb08d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d6bdb5668bcebb9babcbcb7d07839694750aec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215592"
---
# <a name="copy-individual-frames-from-a-multiple-frame-image"></a>Einzelne Frames aus einem Bild mit mehreren Frames kopieren

Im folgenden Beispiel werden die einzelnen Frames aus einer TIFF-Datei mit mehreren Frames abgerufen. Beim Erstellen der TIFF-Datei wurden die einzelnen Frames der Seiten Dimension hinzugefügt (Weitere Informationen finden Sie unter [Erstellen und Speichern eines Multiple-Frame Bilds](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)). Der Code zeigt jede der vier Seiten an und speichert jede Seite in einer separaten PNG-Datenträger Datei.

Der Code erstellt ein [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Objekt aus der TIFF-Datei mit mehreren Frames. Um die einzelnen Frames (Seiten) abzurufen, ruft der Code die [**Image:: SelectActiveFrame**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-selectactiveframe) -Methode dieses **Bild** Objekts auf. Das erste Argument, das an die **Image:: SelectActiveFrame** -Methode übermittelt wird, ist die Adresse einer GUID, die die Dimension angibt, in der die Frames zuvor der TIFF-Datei mit mehreren Frames hinzugefügt wurden. Die GUID ' framedimensionpage ' ist in ' gdiplusimaging. h ' definiert. Andere GUIDs, die in der Header Datei definiert sind, sind framedimensiontime und framedimensionresolution. Das zweite Argument, das an die Methode **Image:: SelectActiveFrame** übermittelt wird, ist der null basierte Index der gewünschten Seite.

Der Code basiert auf der Hilfsfunktion getencoderclsid, die unter [Abrufen des Klassen Bezeichners für einen Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)angezeigt wird.


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



In der folgenden Abbildung werden die einzelnen Seiten dargestellt, die im vorangehenden Code angezeigt werden.

![Darstellung einer geometrischen Form, eines Farbfotos, eines monochrome Fotos und einer anderen geometrischen Form](images/multiframe1.png)

 

 



