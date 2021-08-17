---
title: BufferAverage
description: Das BufferAverage-Attribut enthält die durchschnittliche Puffergröße, die für einen VBR-Datenstrom (Variable Bit Rate) benötigt wird.
ms.assetid: 5fd69534-6655-4c98-bf07-a694585fc9ae
keywords:
- BufferAverage windows Media Format
topic_type:
- apiref
api_name:
- BufferAverage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd839bff96f5ba327e585f8608bd4612fc047d354c24fee972e507ea5ca681f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117656120"
---
# <a name="bufferaverage"></a>BufferAverage

Das **BufferAverage-Attribut** enthält die durchschnittliche Puffergröße, die für einen VBR-Datenstrom (Variable Bit Rate) benötigt wird.

## <a name="global-constant"></a>Globale Konstante

g \_ wszBufferAverage

## <a name="data-type"></a>Datentyp

**\_WMT-TYP \_ DWORD**

## <a name="remarks"></a>Hinweise

Wenn Sie auf die **IWMHeaderInfo3-Schnittstelle** des Writerobjekts zugreifen, können Sie diesen Wert hinzufügen oder ändern. In anderen Objekten (Metadaten-Editor, Reader und synchroner Reader) ist dieser Wert schreibgeschützt.

Der Writer schreibt automatisch einen **BufferAverage-Wert** für jeden VBR-Stream.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




