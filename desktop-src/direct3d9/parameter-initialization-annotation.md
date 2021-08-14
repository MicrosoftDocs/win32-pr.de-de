---
description: Verwenden Sie diese Anmerkung, um den Inhalt einer externen Datei als Initialisierungswert für einen Effect-Parameter zu definieren.
ms.assetid: 3da1f951-cb8b-49ce-aba2-0badb3178093
title: Initialisierungsanmerkung für Parameter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2d66d0cc18782d97a5a56c73ab12cd9222d33827930d60023fccf73cd2a8455
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798661"
---
# <a name="parameter-initialization-annotation"></a>Initialisierungsanmerkung für Parameter

Verwenden Sie diese Anmerkung, um den Inhalt einer externen Datei als Initialisierungswert für einen Effect-Parameter zu definieren. Beispiel:


```
string SasResourceAddress = "Value";
```



Dabei ist Value eine ASCII-Textzeichenfolge, die einen absoluten oder relativen Pfad enthalten kann. Ein relativer Pfad ist relativ zu dem Verzeichnis, das die Effektdatei enthält.

Beispiel:


```
texture2D DetailTexture
<
    string SasResourceAddress = "noise.dds";
>;
```



Der Standardwert ist eine leere Zeichenfolge.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectX-Standardanmerkungen und Semantikreferenz](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



