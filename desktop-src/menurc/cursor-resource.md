---
title: Cursor Ressource
description: Definiert eine Bitmap, die die Form des Cursors auf dem Anzeige Bildschirm oder einen animierten Cursor definiert.
ms.assetid: c087abca-5502-4625-8c9b-464e1718571f
keywords:
- Cursor Ressourcen Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- CURSOR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 594f406420b3b18f88b8890ca4248345ba77fa8e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106341714"
---
# <a name="cursor-resource"></a>Cursor Ressource

Definiert eine Bitmap, die die Form des Cursors auf dem Anzeige Bildschirm oder einen animierten Cursor definiert.

``` syntax
nameID CURSOR filename
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*NameID*
</dt> <dd>

Eindeutiger Name oder eine 16-Bit-Ganzzahl ohne Vorzeichen, die die Ressource identifiziert.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Einfügen*
</dt> <dd>

Der Name der Datei, die die Ressource enthält. Der Name muss ein gültiger Dateiname sein. Es muss sich um einen vollständigen Pfad handeln, wenn sich die Datei nicht im aktuellen Arbeitsverzeichnis befindet. Der Pfad muss eine Zeichenfolge in Anführungszeichen sein.

</dd> </dl>

Bestimmte Attribute werden auch aus Gründen der Abwärtskompatibilität unterstützt. Weitere Informationen finden Sie unter [allgemeine Ressourcen Attribute](common-resource-attributes.md).

## <a name="remarks"></a>Bemerkungen

Symbol-und Cursor Ressourcen können mehr als ein Bild enthalten.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel werden zwei Cursor Ressourcen definiert: eine nach Namen (cursor1) und die andere nach Zahl (2):

``` syntax
cursor1 CURSOR "bullseye.cur"
2       CURSOR "d:\\cursor\\arrow.cur" 
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden von Cursors](./using-cursors.md)
</dt> </dl>

 

 