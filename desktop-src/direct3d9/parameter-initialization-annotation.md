---
description: Verwenden Sie diese Anmerkung, um den Inhalt einer externen Datei als Initialisierungs Wert für einen Effektparameter zu definieren.
ms.assetid: 3da1f951-cb8b-49ce-aba2-0badb3178093
title: Initialisierungs Anmerkung für Parameter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c564b5b5e273b320fdc5de6148ef5ba5dd9f1b78
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213840"
---
# <a name="parameter-initialization-annotation"></a>Initialisierungs Anmerkung für Parameter

Verwenden Sie diese Anmerkung, um den Inhalt einer externen Datei als Initialisierungs Wert für einen Effektparameter zu definieren. Beispiel:


```
string SasResourceAddress = "Value";
```



Dabei ist value eine ASCII-Text Zeichenfolge, die einen absoluten oder relativen Pfad enthalten kann. Ein relativer Pfad bezieht sich auf das Verzeichnis, das die Effekt Datei enthält.

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

[DirectX-Standard Anmerkungen und Semantik Referenz](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



