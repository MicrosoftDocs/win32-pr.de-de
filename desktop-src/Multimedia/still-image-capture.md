---
title: Still-Image Capture
description: Still-Image Capture
ms.assetid: 9e84b385-aedb-4132-8a2d-72c32594083a
keywords:
- WM_CAP_GRAB_FRAME_NOSTOP-Nachricht
- WM_CAP_GRAB_FRAME Nachricht
- capGrabFrameNoStop-Makro
- capGrabFrame-Makro
- WM_CAP_EDIT_COPY Nachricht
- capEditCopy-Makro
- WM_CAP_FILE_SAVEDIB-Nachricht
- capFileSaveDIB-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c0d822292489be4093998ac18d70191dbe2b87327a33adaba26e8442420d93b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688600"
---
# <a name="still-image-capture"></a>Still-Image Capture

Wenn Sie einen einzelnen Frame als Stillbild erfassen möchten, können Sie die [**WM CAP GRAB FRAME \_ \_ \_ \_ NOSTOP-**](wm-cap-grab-frame-nostop.md) oder [**WM CAP GRAB \_ \_ \_ FRAME-Nachricht**](wm-cap-grab-frame.md) (oder das [**CapGrabFrameNoStop-**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) oder [**capGrabFrame-Makro)**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) verwenden, um das digitalisierte Bild in einem internen Framepuffer zu erfassen. Sie können die Anzeige auf dem erfassten Bild mithilfe von WM \_ CAP \_ GRAB FRAME \_ einfrieren. Verwenden Sie andernfalls WM \_ CAP \_ GRAB FRAME \_ \_ NOSTOP.

Nach der Erfassung können Sie das Image zur Verwendung durch andere Anwendungen kopieren. Sie können ein Bild aus dem Framepuffer in die Zwischenablage kopieren, indem Sie die [**WM \_ CAP EDIT \_ \_ COPY-Meldung**](wm-cap-edit-copy.md) (oder das [**Makro capEditCopy)**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) verwenden. Sie können das Bild auch mithilfe der [**WM \_ CAP FILE \_ \_ SAVEDIB-Nachricht**](wm-cap-file-savedib.md) (oder des [**Makros capFileSaveDIB)**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib) aus dem Framepuffer in eine geräteunabhängige Bitmap (DIB) kopieren.

Ihre Anwendung kann auch die beiden Einzelframe-Erfassungsnachrichten verwenden, um einen Sequenzrahmen nach Frame zu bearbeiten oder eine Zeitraffersequenz zu erstellen.

 

 




