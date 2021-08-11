---
title: FONT-Ressource
description: Definiert eine Datei, die eine Schriftart enthält.
ms.assetid: 0e19edd5-6cfc-44e6-add4-7413eb94867a
keywords:
- FONT-Ressourcenmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- FONT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf08abd68d5d99640435d355609d5647c71116f9fa29c137ba67a311d41f493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235272"
---
# <a name="font-resource"></a>FONT-Ressource

Definiert eine Datei, die eine Schriftart enthält.

``` syntax
nameID FONT filename
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Eindeutiger 16-Bit-Ganzzahlwert ohne Vorzeichen, der die Ressource identifiziert.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Dateiname*
</dt> <dd>

Name der Datei, die die Ressource enthält. Der Name muss ein gültiger Dateiname sein. Es muss sich um einen vollständigen Pfad handeln, wenn sich die Datei nicht im aktuellen Arbeitsverzeichnis befindet. Der Pfad sollte eine Zeichenfolge in Anführungszeichen sein.

</dd> </dl>

Bestimmte Attribute werden auch aus Gründen der Abwärtskompatibilität unterstützt. Weitere Informationen finden Sie unter [Allgemeine Ressourcenattribute.](common-resource-attributes.md)

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird eine einzelne Schriftartressource definiert:

``` syntax
5 FONT  "cmroman.fnt"
```

 

 




