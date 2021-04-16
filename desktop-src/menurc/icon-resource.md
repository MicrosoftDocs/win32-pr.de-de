---
title: Symbol Ressource
description: Definiert eine Bitmap, die die Form des Symbols definiert, das für eine bestimmte Anwendung oder ein animiertes Symbol verwendet werden soll.
ms.assetid: a8e3205e-e17a-4daf-a599-4dc89cb1e640
keywords:
- Symbol Ressourcen Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- ICON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d5f762c4f4b459d51a0243a9cdbd7367deda7b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104516733"
---
# <a name="icon-resource"></a>Symbol Ressource

Definiert eine Bitmap, die die Form des Symbols definiert, das für eine bestimmte Anwendung oder ein animiertes Symbol verwendet werden soll.

``` syntax
nameID ICON filename
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*NameID*
</dt> <dd>

Eindeutiger Name oder ein 16-Bit-Ganzzahl-Wert ohne Vorzeichen, der die Ressource identifiziert.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Einfügen*
</dt> <dd>

Der Name der Datei, die die Ressource enthält. Der Name muss ein gültiger Dateiname sein. Es muss sich um einen vollständigen Pfad handeln, wenn sich die Datei nicht im aktuellen Arbeitsverzeichnis befindet. Der Pfad muss eine Zeichenfolge in Anführungszeichen sein.

</dd> </dl>

Bestimmte Attribute werden auch aus Gründen der Abwärtskompatibilität unterstützt. Weitere Informationen finden Sie unter [allgemeine Ressourcen Attribute](common-resource-attributes.md).

## <a name="remarks"></a>Bemerkungen

Symbol-und Cursor Ressourcen können mehr als ein Bild enthalten.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel werden zwei Symbol Ressourcen definiert:

``` syntax
desk1   ICON "desk.ico"
11      ICON "custom.ico"
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden von Symbolen](./using-icons.md)
</dt> </dl>

 

 