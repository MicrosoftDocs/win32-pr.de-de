---
title: dllname (Str)-Attribut
description: Das Attribut \ dllName \ definiert den Namen der dll, die die Einstiegspunkte für ein Modul enthält.
ms.assetid: dbf062ce-9dcc-4cc6-b7cd-cdc5945e399b
keywords:
- dllname (Str)-Attribut (Mittel l)
topic_type:
- apiref
api_name:
- dllname(str)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 990d277db855c2988021d19a0a756c49454546f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038975"
---
# <a name="dllnamestr-attribute"></a>dllname (Str)-Attribut

Das **\[ dllName \]** -Attribut definiert den Namen der dll, die die Einstiegspunkte für ein Modul enthält.

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

*UUID-Nummer* 
</dt> <dd>

Gibt eine universell eindeutige ID für das [**Modul**](module.md)an.

</dd> <dt>

*filename* 
</dt> <dd>

Gibt eine NULL-terminierte Zeichenfolge an, die den vollständigen Pfad zur DLL-Datei enthält.

</dd> <dt>

*optional-Attribut-List* 
</dt> <dd>

Gibt eine Liste von 0 (null) oder mehr Attributen der Mittelwert Schnittstelle an.

</dd> <dt>

*ModuleName* 
</dt> <dd>

Gibt den Namen an, den andere Softwarekomponenten verwenden können, um auf das Modul zu verweisen.

</dd> <dt>

*Elementliste* 
</dt> <dd>

Gibt mindestens eine Modul Element Definitions-Anweisung an.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das **\[ dllName \]** -Attribut ist in einem Modul erforderlich.

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

[**Mond**](module.md)
</dt> <dt>

[**ein**](entry.md)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 