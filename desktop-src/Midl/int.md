---
title: int-Attribut
description: Das Schlüsselwort int gibt eine 32-Bit-Ganzzahl mit Vorzeichen auf 32-Bit-Plattformen an. Auf 16-Bit-Plattformen ist das Schlüsselwort int ein optionales Schlüsselwort, das die Schlüsselwörter Small, Short und Long begleitet.
ms.assetid: ad6ce0ff-e87b-4701-b9d2-a69c34e0339b
keywords:
- int-Attribut-Mittel l
topic_type:
- apiref
api_name:
- int
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f916c4f03023c756b71a2e3cbb38acd9f41f1e8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718065"
---
# <a name="int-attribute"></a>int-Attribut

Das Schlüsselwort **int** gibt eine 32-Bit-Ganzzahl mit Vorzeichen auf 32-Bit-Plattformen an. Auf 16-Bit-Plattformen ist das Schlüsselwort **int** ein optionales Schlüsselwort, das die Schlüsselwörter [**Small**](small.md), [**Short**](short.md)und [**Long**](long.md)begleitet.

``` syntax
[ signed | unsigned ] integer-modifier [ int ] declarator-list;
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*ganzzahliger Modifizierer* 
</dt> <dd>

Gibt das Schlüsselwort [**Small**](small.md), [**Short**](short.md), [**Long**](long.md), [**Hyper**](hyper.md), [**\_ \_ int3264**](--int3264.md)oder [**\_ \_ Int64**](--int64.md)an, mit dem die Größe der ganzzahligen Daten ausgewählt wird. Auf 16-Bit-Plattformen muss der Größen Qualifizierer vorhanden sein.

</dd> <dt>

*Deklarator-List* 
</dt> <dd>

Gibt einen oder mehrere Standard-C-Deklaratoren an, z. b. Bezeichner, zeigerdeklaratoren und Array Deklaratoren. (Funktions Deklaratoren und Bitfeld Deklarationen sind in Strukturen, die in Remote Prozedur aufrufen übertragen werden, nicht zulässig. Diese Deklaratoren sind in Strukturen zulässig, die nicht übertragen werden.) Trennen Sie mehrere Deklaratoren durch Kommas.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Ganzzahlige Typen gehören zu den Basis Typen der Schnittstellen Definitions Sprache (IDL). Sie können als Typspezifizierer in [**typedef**](typedef.md) -Deklarationen, allgemeinen Deklarationen und Funktions Deklaratoren (als Funktionsrückgabetyp-Spezifizierer und als Parametertyp Spezifizierer) angezeigt werden. Informationen zu dem Kontext, in dem typspezifier angezeigt wird, finden Sie unter [Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md).

Wenn keine ganzzahlige Vorzeichen Angabe bereitgestellt wird, ist der ganzzahlige Typ standardmäßig [**signiert**](signed.md).

DCE-IDL-Compiler lassen nicht zu, dass das Schlüsselwort [**signiert**](signed.md) ist, um das Vorzeichen von ganzzahligen Typen anzugeben. Diese Funktion ist daher nicht verfügbar, wenn Sie den [**/OSF**](-osf.md) -Schalter für den Mittelwert Compiler verwenden.

Microsoft empfiehlt nicht die Verwendung von \_ \_ int3264 für Remoting, wenn dies vermieden werden kann. Weitere Informationen zur Verwendung und zu den Einschränkungen finden Sie im Thema zu [**\_ \_ int3264**](--int3264.md) .

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

[Mittel l-Basis Typen](midl-base-types.md)
</dt> <dt>

[**Enumeration**](enum.md)
</dt> <dt>

[**Hyper**](hyper.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**lange**](long.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**ebenes**](signed.md)
</dt> <dt>

[**zuletzt**](small.md)
</dt> <dt>

[**struct**](struct.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**Union**](union.md)
</dt> </dl>

 

 




