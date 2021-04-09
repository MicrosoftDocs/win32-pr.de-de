---
title: signiertes Attribut
description: Das Schlüsselwort signed gibt an, dass das signifikanteste Bit einer ganzzahligen Variablen ein Signier Bit anstelle eines Datenbits darstellt.
ms.assetid: 6116089a-647e-485b-8f79-9c9267aa4810
keywords:
- signiertes Attribut "Mittel l"
topic_type:
- apiref
api_name:
- signed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 500b87c849f31082a036d605db0947650e914bed
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857084"
---
# <a name="signed-attribute"></a>signiertes Attribut

Das Schlüsselwort **Signed** gibt an, dass das signifikanteste Bit einer ganzzahligen Variablen ein Signier Bit anstelle eines Datenbits darstellt.

``` syntax
[[ signed ]] type-qualifier [[ int ]]identifier-name;
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*type-qualifier* 
</dt> <dd>

Kann " [**char**](char-idl.md)", " [**WCHAR \_ t**](wchar-t.md)", " [**Long**](long.md)", " [**Short**](short.md)" und " [**Small**](small.md)" lauten.

</dd> <dt>

*Bezeichnername* 
</dt> <dd>

Gibt einen gültigen Mittell-Bezeichner an. Gültige Mittell-Bezeichner bestehen aus bis zu 31 alphanumerischen Zeichen und/oder unterstrichen und müssen mit einem Buchstaben oder einem Unterstrich beginnen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Dieses Schlüsselwort ist optional und kann mit jedem der Zeichen-und ganzzahligen Typen [**char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Long**](long.md), [**Short**](short.md)und [**Small**](small.md)verwendet werden. Sie können optional das Schlüsselwort [**int**](int.md) nach den typqualifizierern **Long**, **Short** und **Small** einschließen.

Wenn Sie den-Compilerschalter [**char**](char-idl.md)verwenden, können Zeichen-und ganzzahlige Typen, die in der IDL-Datei ohne explizite Vorzeichen vorkommen, mit den Schlüsselwörtern **Signed** oder [**Ganzzahl ohne Vorzeichen**](unsigned.md) in der generierten Header Datei angezeigt werden. Um Verwirrung zu vermeiden, geben Sie das Vorzeichen der ganzzahligen und Zeichen Typen an.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mittel l-Basis Typen](midl-base-types.md)
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

[**zuletzt**](small.md)
</dt> <dt>

[**Ganzzahl ohne Vorzeichen**](unsigned.md)
</dt> <dt>

[**WCHAR \_ t**](wchar-t.md)
</dt> </dl>

 

 




