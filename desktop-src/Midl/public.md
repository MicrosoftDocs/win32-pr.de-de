---
title: Öffentliches Attribut
description: Das \ Public \-Attribut enthält einen Alias, der mit dem typedef-Schlüsselwort in der Typbibliothek deklariert wurde.
ms.assetid: d4e90165-8b0d-47bb-998d-e515226be935
keywords:
- öffentliches Attribut, Mittel l
topic_type:
- apiref
api_name:
- public
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8451ddf77b5074dbea609bfed144340dc877c00
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106338255"
---
# <a name="public-attribute"></a>Öffentliches Attribut

Das **\[ Public \]** -Attribut enthält einen Alias, der mit dem [**typedef**](typedef.md) -Schlüsselwort in der Typbibliothek deklariert wurde.

``` syntax
typedef [public] data-type identifier;
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Datentyp* 
</dt> <dd>

Der Datentyp, für den der Bezeichner als Alias verwendet wird.

</dd> <dt>

*identifier* 
</dt> <dd>

Ein weiterer Name, nach dem der *Datentyp* in der Software bekannt ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Standardmäßig wird ein Alias, der mit [**typedef**](typedef.md) deklariert wird und keine anderen Attribute hat, als **\# define** behandelt und ist nicht in der Typbibliothek enthalten. Durch die Verwendung des **\[ Public \]** -Attributs wird sichergestellt, dass der Alias Teil der Typbibliothek ist.

> [!Note]  
> Der mittlerer l-Compiler erfordert, dass Sie das **\[ öffentliche \]** Attribut explizit auf jede typedef anwenden, die öffentlich sein soll.

 

## <a name="examples"></a>Beispiele

``` syntax
typedef [public] long MEMBERID;
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**berfläche**](interface.md)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 