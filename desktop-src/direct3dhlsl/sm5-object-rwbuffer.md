---
title: Rwbuffer
description: Ein Lese-/Schreibpuffer.
ms.assetid: e9b60e63-5b2b-4f45-834b-269e692ba84c
keywords:
- Rwbuffer HLSL
topic_type:
- apiref
api_name:
- RWBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 765634da85fb74f2d3a3591bfe4767ccee1a80c8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312558"
---
# <a name="rwbuffer"></a>Rwbuffer

Ein Lese-/Schreibpuffer.



| Methode                                                     | BESCHREIBUNG                            |
|------------------------------------------------------------|----------------------------------------|
| [**GetDimensions**](sm5-object-rwbuffer-getdimensions.md) | Ruft die Ressourcen Dimensionen ab.          |
| [**Laden**](rwbuffer-load.md)                              | Ruft einen Wert in einem Puffer mit Lese-/Schreibzugriff ab. |
| [**KOM\[\]**](sm5-object-rwbuffer-operatorindex.md)  | Gibt eine Ressourcen Variable zurück.           |



 

Eine Ressourcen Variable kann auch an einen ungeordneten oder Interlocked-Vorgang übermittelt werden.

**Rwbuffer** -Objekten kann die Speicher Klasse **globallycoherent** vorangestellt werden. Diese Speicher Klasse bewirkt, dass Speicherbarrieren und Synchronisierungen Daten über die gesamte GPU leeren, sodass andere Gruppen Schreibvorgänge sehen können. Ohne diesen Spezifizierer leert eine Speicherbarriere oder Synchronisierung eine UAV nur innerhalb der aktuellen Gruppe.

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Dieses Objekt wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle | ja       |



 

Dieses Objekt wird für die folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Shader Model 5-Objekte](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




