---
title: Bufferaverage
description: Das bufferaverage-Attribut enthält die durchschnittliche Puffergröße, die für einen VBR-Stream (Variable Bitrate) benötigt wird.
ms.assetid: 5fd69534-6655-4c98-bf07-a694585fc9ae
keywords:
- Bufferaverage Windows Media-Format
topic_type:
- apiref
api_name:
- BufferAverage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce5767ed329fde43cc1022af54d937fc99e0e323
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104100987"
---
# <a name="bufferaverage"></a>Bufferaverage

Das **bufferaverage** -Attribut enthält die durchschnittliche Puffergröße, die für einen VBR-Stream (Variable Bitrate) benötigt wird.

## <a name="global-constant"></a>Globale Konstante

g \_ wszbufferaverage

## <a name="data-type"></a>Datentyp

**WMT- \_ Typ \_ DWORD**

## <a name="remarks"></a>Bemerkungen

Beim Zugriff auf die **IWMHeaderInfo3** -Schnittstelle des Writer-Objekts können Sie diesen Wert hinzufügen oder ändern. In anderen Objekten (Metadaten-Editor, Reader und synchroner Reader) ist dieser Wert schreibgeschützt.

Der Writer schreibt automatisch einen **bufferaverage** -Wert für jeden VBR-Stream.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




