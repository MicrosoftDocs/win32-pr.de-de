---
description: 'Die Image:: Save Methods-Methode und die Image:: SaveAdd Methods-Methode der Image-Klasse erhalten ein EncoderParameters-Objekt, das ein Array von EncoderParameter-Objekten enthält.'
ms.assetid: babc89f0-aea5-4341-8cf9-40d11e73fb10
title: Bild Encoder Konstanten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8130b90ad7f1d559ca480a581a0b157ff152fc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215598"
---
# <a name="image-encoder-constants"></a>Bild Encoder Konstanten

Die [Image:: Save Methods](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) -Methode und die [Image:: SaveAdd Methods](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) -Methode der [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) -Klasse erhalten ein [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) -Objekt, das ein Array von [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) -Objekten enthält. Jedes **EncoderParameter** -Objekt verfügt über einen GUID-Datenmember, der die Parameter Kategorie angibt. Die folgenden Konstanten, die in "gdiplusimaging. h" definiert sind, stellen GUIDs dar, die die verschiedenen Parameter Kategorien angeben.

-   Encoderchrominancetable
-   Encodercolortiefe
-   Encodercolorspace
-   Encodercompression
-   Encoderluminancetable
-   Encoderquality
-   Encoderrendermethod
-   Encodersaveflag
-   Encoderscanmethod
-   Encodertransformation
-   EncoderVersion
-   Encoderimageitems
-   Encodersaveascmyk

 

 
