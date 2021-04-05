---
title: Schriftart Ressource
description: Definiert eine Datei, die eine Schriftart enthält.
ms.assetid: 0e19edd5-6cfc-44e6-add4-7413eb94867a
keywords:
- Schriftart Ressourcen Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- FONT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e205d80779a1a228ee50e062f6904c1ed4a4934
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718738"
---
# <a name="font-resource"></a>Schriftart Ressource

Definiert eine Datei, die eine Schriftart enthält.

``` syntax
nameID FONT filename
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*NameID*
</dt> <dd>

Eindeutiger ganzzahliger 16-Bit-Wert ohne Vorzeichen, der die Ressource identifiziert.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Einfügen*
</dt> <dd>

Der Name der Datei, die die Ressource enthält. Der Name muss ein gültiger Dateiname sein. Es muss sich um einen vollständigen Pfad handeln, wenn sich die Datei nicht im aktuellen Arbeitsverzeichnis befindet. Der Pfad muss eine Zeichenfolge in Anführungszeichen sein.

</dd> </dl>

Bestimmte Attribute werden auch aus Gründen der Abwärtskompatibilität unterstützt. Weitere Informationen finden Sie unter [allgemeine Ressourcen Attribute](common-resource-attributes.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird eine einzelne Schriftart Ressource definiert:

``` syntax
5 FONT  "cmroman.fnt"
```

 

 




