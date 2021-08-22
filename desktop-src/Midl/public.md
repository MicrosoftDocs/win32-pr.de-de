---
title: Öffentliches Attribut
description: Das \public\-Attribut enthält einen Alias, der mit dem typedef-Schlüsselwort in der Typbibliothek deklariert wurde.
ms.assetid: d4e90165-8b0d-47bb-998d-e515226be935
keywords:
- öffentliches MidL-Attribut
topic_type:
- apiref
api_name:
- public
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f8e4944404bccc734594f3847c0ff9de17e54d0b5bcc444a56abe9b8f1e0eaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328720"
---
# <a name="public-attribute"></a>Öffentliches Attribut

Das **\[ öffentliche \]** Attribut enthält einen Alias, der mit dem [**typedef-Schlüsselwort**](typedef.md) in der Typbibliothek deklariert wurde.

``` syntax
typedef [public] data-type identifier;
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Datentyp* 
</dt> <dd>

Der Datentyp, für den der Bezeichner ein Alias sein soll.

</dd> <dt>

*identifier* 
</dt> <dd>

Ein anderer Name, mit dem der *Datentyp* in der Software bekannt ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Standardmäßig wird ein Alias, der mit [**typedef**](typedef.md) deklariert wird und über keine anderen Attribute verfügt, als **\# definiert** behandelt und ist nicht in der Typbibliothek enthalten. Die Verwendung des **\[ \] public-Attributs** stellt sicher, dass der Alias Teil der Typbibliothek wird.

> [!Note]  
> Der MIDL-Compiler erfordert, dass Sie das **\[ \] public-Attribut** explizit auf jede Typedef anwenden, die öffentlich sein soll.

 

## <a name="examples"></a>Beispiele

``` syntax
typedef [public] long MEMBERID;
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[BEISPIEL FÜR ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**Schnittstelle**](interface.md)
</dt> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> </dl>

 

 