---
title: Rwbuffer
description: Ein Lese-/Schreibpuffer.
ms.assetid: e9b60e63-5b2b-4f45-834b-269e692ba84c
keywords:
- RWBuffer HLSL
topic_type:
- apiref
api_name:
- RWBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 88992a60148b58e4a252770c2be65625130378d56837a8c8c93958b57a9a3980
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725175"
---
# <a name="rwbuffer"></a>Rwbuffer

Ein Lese-/Schreibpuffer.



| Methode                                                     | Beschreibung                            |
|------------------------------------------------------------|----------------------------------------|
| [**GetDimensions**](sm5-object-rwbuffer-getdimensions.md) | Ruft die Ressourcendimensionen ab.          |
| [**Laden**](rwbuffer-load.md)                              | Ruft einen Wert in einem Lese-/Schreibpuffer ab. |
| [**Operator\[\]**](sm5-object-rwbuffer-operatorindex.md)  | Gibt eine Ressourcenvariable zurück.           |



 

Eine Ressourcenvariable kann auch an jeden ungeordneten oder interlocked-Vorgang übergeben werden.

**RWBuffer-Objekten** kann die speicherklasse **globallycoherent vorangestellt werden.** Diese Speicherklasse bewirkt Speicherbarrieren und Synchronisierungen, um Daten über die gesamte GPU zu leeren, damit andere Gruppen Schreibvorgänge sehen können. Ohne diesen Bezeichner leert eine Speicherbarriere oder Synchronisierung einen UAV nur innerhalb der aktuellen Gruppe.

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Dieses Objekt wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höher– Shadermodelle | Ja       |



 

Dieses Objekt wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ShaderModell 5-Objekte](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




