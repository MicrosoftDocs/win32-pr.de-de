---
title: Source Register Negate
description: Führt ein Negat (y -x) für alle Registerkomponenten aus.
ms.assetid: fe11f7a7-81be-4237-8194-15704f6fe43c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 94898dbbf193254165850ee696d2fea72d6d446908021dfbb5fd32f1920b7010
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118512951"
---
# <a name="source-register-negate"></a>Source Register Negate

Führt ein Negat (y = -x) für alle Registerkomponenten aus.

## <a name="syntax"></a>Syntax


```
- register
```



## <a name="registers"></a>Register

Quellregister. Weitere Informationen zu Registertypen finden Sie unter [ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 ps \_ \_ \_ 1 \_ 3 ps \_ \_ \_ 1 \_ 4 Register .](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)

## <a name="remarks"></a>Hinweise

Der Inhalt des Registers wird nicht geändert. Der Modifizierer wird nur auf die aus dem Register gelesenen Daten angewendet. Der Negationsvorgang wird auf alle vier Farbkanäle (RGBA) angewendet.

Dieser Vorgang wird nach allen anderen Modifizierern ausgeführt, die für dasselbe Argument vorhanden sind.

Dieser Modifizierer ist mit [der Quellregister-Umkehrung](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) gegenseitig ausschließend, sodass er nicht auf dasselbe Register angewendet werden kann.

Dieser Modifizierer ist nur für die Verwendung mit arithmetischen Anweisungen vorgesehen.

## <a name="example"></a>Beispiel

Im folgenden Beispiel wird die Verwendung dieses Modifizierer veranschaulicht.


```
mul r0, r0, -v1;
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Quellregistermodifizierer für Pixelshader](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




