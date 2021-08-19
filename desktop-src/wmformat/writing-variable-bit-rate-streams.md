---
title: Schreiben variabler Bitraten Streams
description: Schreiben variabler Bitraten Streams
ms.assetid: 9eccde59-8342-44ad-90e6-032db022d7c5
keywords:
- Advanced Systems Format (ASF), Schreiben von VBR-Streams
- ASF (Advanced Systems Format), Schreiben von VBR-Streams
- Variable Bitrate (VBR), Schreiben von Streams
- VBR (variable Bitrate), Schreiben von Streams
- Streams,Schreiben von VBR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 694774613ada8b4be05eab55be3213898d423d3b6ac4438204d149a0bd606c90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930257"
---
# <a name="writing-variable-bit-rate-streams"></a>Schreiben variabler Bitraten Streams

Datenströme mit variabler Bitrate (VBR) werden auf die gleiche Weise geschrieben wie CBR-Streams (Constant Bit Rate). Der einzige Unterschied besteht in der internen Verarbeitung durch den Writer und die Codecs. Allerdings erfordert die bitratenbasierte VBR (sowohl eingeschränkte als auch nicht gestützte) einen Vorverarbeitungspass im Writer.

Sie sollten den Rückgabewert für den ersten Aufruf von [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) für jeden Stream überprüfen. Wenn der zurückgegebene Fehlercode NS E INVALID NUM PASSES ist, erfordert der Stream \_ \_ einen \_ \_ Vorverarbeitungspass.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden der Two-Pass Codierung**](using-two-pass-encoding.md)
</dt> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> </dl>

 

 




