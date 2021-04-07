---
title: pointer_default-Attribut
description: Das Attribut \ Zeiger \_ default \ gibt das Standard Zeiger Attribut für alle Zeiger außer der Spitze der obersten Ebene an, die in Parameterlisten angezeigt werden.
ms.assetid: a6e83034-8adb-483d-8d1e-432a1aed22c6
keywords:
- Pointer_default Attribut-Mittel l
topic_type:
- apiref
api_name:
- pointer_default
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08555358eb0abd42957d60527e18a4fd4f49165a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038844"
---
# <a name="pointer_default-attribute"></a>Zeiger- \_ Standard Attribut

Das **\[ \_ Default \] -Zeiger** Attribut gibt das Standard Zeiger Attribut für alle Zeiger außer der Spitze der obersten Ebene an, die in Parameterlisten angezeigt werden.

``` syntax
pointer_default ( ptr | ref | unique )
```

## <a name="parameters"></a>Parameter

Dieses Attribut hat keine Parameter.

## <a name="examples"></a>Beispiele

``` syntax
[
    uuid(6B29FC40-CA47-1067-B31D-00DD010662DA), 
    version(3.3), 
    pointer_default(unique)
] 
interface dictionary 
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**berfläche**](interface.md)
</dt> <dt>

[Array-und Sized-Pointer Attribute](array-and-sized-pointer-attributes.md)
</dt> <dt>

[**Mikro**](arrays-1.md)
</dt> <dt>

[Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**gem**](unique.md)
</dt> <dt>

[Standard Zeiger Typen](/windows/desktop/Rpc/default-pointer-types)
</dt> </dl>

 

 