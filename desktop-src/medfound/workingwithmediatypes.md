---
description: Arbeiten mit DMO Medientypen
ms.assetid: 1aaf7554-1a5f-439a-afb1-a031607e1a1e
title: Arbeiten mit DMO Medientypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a75d7eb65e92a89d5d413d8cc04a7dbb9f1891d6b23a9cc3c1242fbae46f1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100917"
---
# <a name="working-with-dmo-media-types"></a>Arbeiten mit DMO Medientypen

Die von den Codec-DMOs verwendeten Eingabe- und Ausgabemedientypen werden mithilfe der [**DMO \_ MEDIA \_ TYPE-Struktur**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) definiert. Diese Struktur ist identisch mit [**WM \_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type), das im Windows Media Format SDK definiert ist, und [**AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type), das in Microsoft DirectShow® definiert ist. Je nach Anwendung können Sie Variablen verwenden, die als einer dieser drei Typen definiert sind. Es ist sicher, einen Zeiger auf eine der Medientypstrukturen als eine andere zu casten. Beispiel:


```
    DMO_MEDIA_TYPE MediaType;
    WM_MEDIA_TYPE* pMedia = NULL;
    pMedia = (WM_MEDIA_TYPE*)&MediaType;
```



Die von den Codecs verwendeten Formattypen sind im Allgemeinen auf die von den **VIDEOINFOHEADER-** und **WAVEFORMATEX-Strukturen** beschriebenen Typen beschränkt. Der Einfachheit halber sind Konstanten für diese Formattypen in der Headerdatei wmcodecconst.h enthalten. Die konstanten Namen sind WMCFORMAT \_ VideoInfo bzw. WMCFORMAT \_ WaveFormatEx. Die Audiocodecs können unter bestimmten Umständen mit der **WAVEFORMATEXTENSIBLE-Struktur** funktionieren und müssen sie in anderen verwenden. allerdings wird **DMO \_ MEDIA \_ TYPE.formattype** auf den gleichen Wert wie für **WAVEFORMATEX** festgelegt. Weitere Informationen zur Verwendung von **WAVEFORMATEXTENSIBLE** finden Sie unter [Verwenden von High-Definition Audio](usinghighdefinitionaudio.md).

> [!Note]  
>    Sie müssen die Formattypstruktur, die als Encoderausgabe verwendet wird, in den Container einschließen, den Sie zum Speichern der komprimierten Daten verwenden. Die Decoder erfordern die ursprüngliche Formatstruktur, um den Inhalt zu dekomprimieren. Zusätzlich zu den Membern der -Struktur erfordern komprimierte Windows Medienaudio- und Videotypen zusätzliche Formatinformationen, die an die Struktur angefügt werden. Weitere Informationen finden Sie unter [Working with Audio (Arbeiten mit Audio)](workingwithaudio.md) und [Working with Video (Arbeiten mit Video).](workingwithvideo.md)

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Codec-DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 
