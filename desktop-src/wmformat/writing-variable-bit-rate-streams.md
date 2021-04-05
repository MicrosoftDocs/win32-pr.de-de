---
title: Schreiben von variablenbitrate-Streams
description: Schreiben von variablenbitrate-Streams
ms.assetid: 9eccde59-8342-44ad-90e6-032db022d7c5
keywords:
- Advanced Systems Format (ASF), Schreiben von VBR-Streams
- ASF (Advanced Systems Format), Schreiben von VBR-Streams
- variablenbitrate (VBR), Schreiben von Streams
- VBR (Variable Bitrate), Schreiben von Streams
- Streams, Schreiben von VBR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6981cbae04085c4bf4f771d9dd29e30752427cdc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723392"
---
# <a name="writing-variable-bit-rate-streams"></a>Schreiben von variablenbitrate-Streams

VBR-Streams (Variable Bitrate) werden auf die gleiche Weise wie mit konstanten Bitrate (CBR) geschrieben. Der einzige Unterschied besteht in der vom Writer und den Codecs intern durchgeführten Verarbeitung. Allerdings erfordert die Bitrate-basierte VBR (sowohl eingeschränkt als auch nicht eingeschränkt) einen Vorverarbeitungs Durchlauf im Writer.

Überprüfen Sie für jeden Stream den Rückgabewert für den ersten-Befehl, den Sie für " [**iwmwriter:: Write tesample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) " vornehmen. Wenn der zurückgegebene Fehlercode NS \_ E \_ ungültige \_ NUM- \_ Pässe ist, erfordert der Stream einen Vorverarbeitungs Durchlauf.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden von Two-Pass Codierung**](using-two-pass-encoding.md)
</dt> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> </dl>

 

 




