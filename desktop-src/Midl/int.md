---
title: int-Attribut
description: Das Schlüsselwort int gibt eine 32-Bit-Ganzzahl mit Vorzeichen auf 32-Bit-Plattformen an. Auf 16-Bit-Plattformen ist das Schlüsselwort int ein optionales Schlüsselwort, das die Schlüsselwörter klein, kurz und lang begleiten kann.
ms.assetid: ad6ce0ff-e87b-4701-b9d2-a69c34e0339b
keywords:
- int-Attribut MIDL
topic_type:
- apiref
api_name:
- int
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 640eae8bfbadcba07f67d244edd78726269ede9eee2f14e9af06e851bb5cac92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807198"
---
# <a name="int-attribute"></a>int-Attribut

Das Schlüsselwort **int gibt** eine 32-Bit-Ganzzahl mit Vorzeichen auf 32-Bit-Plattformen an. Auf 16-Bit-Plattformen ist das Schlüsselwort **int** ein optionales Schlüsselwort, das die Schlüsselwörter [**small,**](small.md) [**short**](short.md)und [**long unterstützen kann.**](long.md)

``` syntax
[ signed | unsigned ] integer-modifier [ int ] declarator-list;
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Integermodifizierer* 
</dt> <dd>

Gibt das Schlüsselwort [**small**](small.md), [**short**](short.md), [**long**](long.md), [**hyper**](hyper.md), [**\_ \_ int3264**](--int3264.md)oder [**\_ \_ int64**](--int64.md)an, das die Größe der ganzzahligen Daten auswählt. Auf 16-Bit-Plattformen muss der Größenqualifizierer vorhanden sein.

</dd> <dt>

*declarator-list* 
</dt> <dd>

Gibt einen oder mehrere C-Standarddeklaratoren an, z. B. Bezeichner, Zeigerdeklaratoren und Arraydeklaratoren. (Funktionsdeklaratoren und Bitfelddeklarationen sind in Strukturen, die in Remoteprozeduraufrufen übertragen werden, nicht zulässig. Diese Deklaratoren sind in Strukturen zulässig, die nicht übertragen werden.) Trennen Sie mehrere Deklaratoren durch Kommas.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Ganzzahltypen gehören zu den Basistypen der Schnittstellendefinitionssprache (Interface Definition Language, IDL). Sie können als Typspezifizierer in TypeDef-Deklarationen, allgemeinen Deklarationen und Funktionsdeklaratoren (als Funktions-Rückgabetypspezifizierer und als Parametertypspezifizierer) angezeigt werden. [](typedef.md) Informationen zum Kontext, in dem Typspezifizierer angezeigt werden, finden Sie unter [Interface Definition (IDL)-Datei.](interface-definition-idl-file.md)

Wenn keine Ganzzahlzeichenspezifikation angegeben wird, wird der Ganzzahltyp standardmäßig mit [**Vorzeichen verwendet.**](signed.md)

DCE-IDL-Compiler lassen nicht zu, dass das Schlüsselwort [**signed**](signed.md) das Vorzeichen von ganzzahligen Typen angibt. Daher ist dieses Feature nicht verfügbar, wenn Sie den MIDL-Compilerschalter [**/osf**](-osf.md) verwenden.

Microsoft empfiehlt die Verwendung von \_ \_ int3264 für Remoting nicht, wenn dies vermieden werden kann. Weitere Informationen zu Verwendung und Einschränkungen finden Sie im Thema zu [**\_ \_ int3264.**](--int3264.md)

## <a name="examples"></a>Beispiele

``` syntax
signed short int i = 0; 
int j = i; 
typedef struct 
{ 
    small int         i1; 
    short             i2; 
    unsigned long int i3; 
} INTSIZETYPE; 
 
HRESULT MyFunc([in] long int lCount);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[MIDL-Basistypen](midl-base-types.md)
</dt> <dt>

[**Enum**](enum.md)
</dt> <dt>

[**Hyper**](hyper.md)
</dt> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**Unterzeichnet**](signed.md)
</dt> <dt>

[**klein**](small.md)
</dt> <dt>

[**Struktur**](struct.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> <dt>

[**Union**](union.md)
</dt> </dl>

 

 




