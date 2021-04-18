---
title: nicht signiertes Attribut
description: Das Ganzzahl ohne Vorzeichen-Schlüsselwort gibt an, dass das signifikanteste Bit einer ganzzahligen Variablen ein Daten Bit anstelle eines signierten Bits darstellt.
ms.assetid: bfcc6bec-895e-45e1-b162-b79651662aa6
keywords:
- Ganzzahl ohne Vorzeichen-Attribut, Mittel l
topic_type:
- apiref
api_name:
- unsigned
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 329d638f1b5be97e5b441aa4e84825fe59a4a3f0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106339248"
---
# <a name="unsigned-attribute"></a>nicht signiertes Attribut

Das **Ganzzahl ohne Vorzeichen** -Schlüsselwort gibt an, dass das signifikanteste Bit einer ganzzahligen Variablen ein Daten Bit anstelle eines signierten Bits darstellt.

``` syntax
[[ unsigned ]] type-qualifier [[ int ]]identifier-name;
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*type-qualifier* 
</dt> <dd>

Kann " [**char**](char-idl.md)", " [**WCHAR \_ t**](wchar-t.md)", " [**Long**](long.md)", " [**int**](int.md)", " [**Short**](short.md)" und [**klein**](small.md)sein.

</dd> <dt>

*Bezeichnername* 
</dt> <dd>

Gibt einen gültigen Mittell-Bezeichner an. Gültige Mittell-Bezeichner bestehen aus bis zu 31 alphanumerischen Zeichen und/oder unterstrichen und müssen mit einem Buchstaben oder einem Unterstrich beginnen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Dieses Schlüsselwort ist optional und kann mit jedem der Zeichen-und ganzzahligen Typen [**char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Long**](long.md), [**Short**](short.md)und [**Small**](small.md)verwendet werden. Sie können optional das Schlüsselwort [**int**](int.md) nach den typqualifizierern **Long**, **Short** und **Small** einschließen.

Wenn Sie den Compilerschalter [**/char**](-char.md)verwenden, können Zeichen-und ganzzahlige Typen, die in der IDL-Datei ohne explizite Vorzeichen vorkommen, mit dem Schlüsselwort [**Signed**](signed.md) oder **Ganzzahl ohne Vorzeichen** in der generierten Header Datei angezeigt werden. Um Verwirrung zu vermeiden, geben Sie das Vorzeichen der ganzzahligen und Zeichen Typen an.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mittel l-Basis Typen](midl-base-types.md)
</dt> <dt>

[**Char**](char-idl.md)
</dt> <dt>

[**/Char**](-char.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**INT**](int.md)
</dt> <dt>

[**lange**](long.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**ebenes**](signed.md)
</dt> <dt>

[**zuletzt**](small.md)
</dt> <dt>

[**WCHAR \_ t**](wchar-t.md)
</dt> </dl>

 

 




