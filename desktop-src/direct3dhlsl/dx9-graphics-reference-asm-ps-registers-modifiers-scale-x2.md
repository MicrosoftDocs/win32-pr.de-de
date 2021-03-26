---
title: Quell Register Skala x 2
description: Multiplizieren Sie den Wert mit zwei, bevor Sie ihn in der-Anweisung verwenden.
ms.assetid: a02c9572-e03d-410b-8b65-7ea1a0bfaa0f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7e88127e4027767d23a2ab576e94802019068dc3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104976161"
---
# <a name="source-register-scale-x-2"></a>Quell Register Skala x 2

Multiplizieren Sie den Wert mit zwei, bevor Sie ihn in der-Anweisung verwenden.

## <a name="syntax"></a>Syntax


```
register_x2
```



## <a name="register"></a>Register

Quell Register. Weitere Informationen zu Register Typen finden Sie unter [PS \_ 1 1 PS 1 \_ \_ \_ \_ \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 Registern](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="remarks"></a>Bemerkungen

Der Inhalt des Registers wird nicht geändert. Der-Modifizierer wird nur auf die aus dem Register gelesenen Daten angewendet.

Dieser Modifizierer schließt sich mit dem [Quell Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md)gegenseitig aus und kann daher nicht auf dasselbe Register angewendet werden.

Dieser Modifizierer ist nur für arithmetische Anweisungen in Version 1 \_ 4 verfügbar.

## <a name="example"></a>Beispiel

Dieses Beispiel veranschaulicht eine Textur, konvertiert Daten in den Bereich von-1 bis + 1 und berechnet ein Punktprodukt.


```
mul r0, r0, r1_x2;
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixel-Shader-quellregistrierungs Modifizierern](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




