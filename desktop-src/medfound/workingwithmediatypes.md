---
description: Arbeiten mit DMO-Medientypen
ms.assetid: 1aaf7554-1a5f-439a-afb1-a031607e1a1e
title: Arbeiten mit DMO-Medientypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db172538280a5dcdc6f4ffe91c19ac1d51e91ef9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961125"
---
# <a name="working-with-dmo-media-types"></a>Arbeiten mit DMO-Medientypen

Die von den Codec-DMOS verwendeten Eingabe-und Ausgabemedien Typen werden mithilfe der [**\_ \_ Medientyp Struktur von DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) definiert. Diese Struktur ist identisch mit dem im Windows Media SDK-SDK definierten [**Typ "WM- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type)" und [**" \_ am \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type)", der in der Microsoft DirectShow-® definiert ist. Abhängig von Ihrer Anwendung können Sie Variablen verwenden, die als einer dieser drei Typen definiert sind. Es ist sicher, einen Zeiger auf eine der Medientyp Strukturen als einen anderen umzuwandeln. Beispiel:


```
    DMO_MEDIA_TYPE MediaType;
    WM_MEDIA_TYPE* pMedia = NULL;
    pMedia = (WM_MEDIA_TYPE*)&MediaType;
```



Die von den Codecs verwendeten Format Typen sind in der Regel auf die von den **videoinfoheader** -und **WaveFormatEx** -Strukturen beschriebenen Typen beschränkt. Zur einfacheren Handhabung sind Konstanten für diese Format Typen in der Header Datei "wmcodeckonst. h" enthalten. Die Konstanten Namen lauten wmcformat \_ videoinfo bzw. wmcformat \_ WaveFormatEx. Die Audiocodecs können unter bestimmten Umständen mit der **WAVEFORMATEXTENSIBLE** -Struktur verwendet werden und müssen Sie in anderen verwenden. Der **DMO- \_ \_ Medientyp. formatType** wird jedoch auf denselben Wert festgelegt wie für **WaveFormatEx**. Weitere Informationen zur Verwendung von **WAVEFORMATEXTENSIBLE** finden Sie unter [Verwenden von High-Definition-Audiodaten](usinghighdefinitionaudio.md).

> [!Note]  
>    Sie müssen die Formattyp Struktur, die als encoderausgabe verwendet wird, in den Container einschließen, den Sie zum Speichern der komprimierten Daten verwenden. Die Decoder benötigen die ursprüngliche Format Struktur, um den Inhalt zu dekomprimieren. Zusätzlich zu den Elementen der Struktur erfordern komprimierte Windows Media Audio und Video Typen zusätzliche Formatinformationen, die an die Struktur angehängt werden. Weitere Informationen finden Sie unter [Arbeiten mit Audiodaten](workingwithaudio.md) und [Arbeiten mit Videos](workingwithvideo.md).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Codec-DMOS](workingwithcodecdmos.md)
</dt> </dl>

 

 
