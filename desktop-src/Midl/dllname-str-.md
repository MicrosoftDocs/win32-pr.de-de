---
title: dllname(str)-Attribut
description: Das \dllname\-Attribut definiert den Namen der DLL, die die Einstiegspunkte für ein Modul enthält.
ms.assetid: dbf062ce-9dcc-4cc6-b7cd-cdc5945e399b
keywords:
- dllname(str) attribute MIDL
topic_type:
- apiref
api_name:
- dllname(str)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7db6f70fb65822a63bd2bf0f9919ac1b9554a664d1ac7ec9775c611b5b4e7f73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067290"
---
# <a name="dllnamestr-attribute"></a>dllname(str)-Attribut

Das **\[ dllname-Attribut \]** definiert den Namen der DLL, die die Einstiegspunkte für ein Modul enthält.

``` syntax
[
    uuid(uuid-number), 
    dllname("filename")
    [, optional-attribute-list]
]
module modulename
{
    elementlist
};
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*uuid-number* 
</dt> <dd>

Gibt eine universell eindeutige ID für das Modul [**an.**](module.md)

</dd> <dt>

*filename* 
</dt> <dd>

Gibt eine auf NULL beendete Zeichenfolge an, die den vollständigen Pfad zur DLL-Datei enthält.

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Gibt eine Liste von null oder mehr MIDL-Schnittstellenattributen an.

</dd> <dt>

*Modulename* 
</dt> <dd>

Gibt den Namen an, mit dem andere Softwarekomponenten auf das Modul verweisen können.

</dd> <dt>

*elementlist* 
</dt> <dd>

Gibt mindestens eine Modulelementdefinitions-Anweisung an.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das **\[ dllname-Attribut \]** ist für ein Modul erforderlich.

## <a name="examples"></a>Beispiele

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("A meaningful comment"),   
    dllname("HANDY.DLL")
] 
module HandyStuff
{
    /* Module content definitions */
};
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Modul**](module.md)
</dt> <dt>

[**Eintrag**](entry.md)
</dt> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[ODL-Dateibeispiel](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 