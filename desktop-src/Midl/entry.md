---
title: Eingabeattribut
description: Das \entry\-Attribut gibt eine exportierte Funktion oder Konstante in einem Modul an, indem der Einstiegspunkt in der DLL identifiziert wird.
ms.assetid: 1d2d6429-d828-44ec-8b0a-cefb64c6e706
keywords:
- Entry-Attribut MIDL
topic_type:
- apiref
api_name:
- entry
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f6dab1681cb04adbd48c4a27c14a359c87624870a43c118c6dd1a589689c00f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013928"
---
# <a name="entry-attribute"></a>Eingabeattribut

Das **\[ \] Entry-Attribut** gibt eine exportierte Funktion oder Konstante in einem Modul an, indem der Einstiegspunkt in der DLL identifiziert wird.

``` syntax
[
    uuid(uuid-number), 
    entry(entry-id)
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

*entry-id* 
</dt> <dd>

Gibt den Funktionsnamen des Moduleinstiegspunkts oder die Ganzzahl-ID an.

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Gibt null oder mehr Attribute für den MIDL-Compiler an, die auf das Modul angewendet [**werden.**](module.md)

</dd> <dt>

*Modulename* 
</dt> <dd>

Gibt den Namen an, den andere Softwarekomponenten verwenden, um das Modul [**zu bezeichnen.**](module.md)

</dd> <dt>

*elementlist* 
</dt> <dd>

Gibt mindestens eine Modulelementdefinitions-Anweisung an.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn die *entryid-Variable* des **\[ \] Entry-Attributs** eine Zeichenfolge ist, ist dies ein benannter Einstiegspunkt. Wenn *entryid* eine Zahl ist, wird der Einstiegspunkt durch eine Ordnungszahl definiert. Dieses Attribut bietet eine Möglichkeit, die Adresse einer Funktion in einem Modul zu erhalten.

## <a name="examples"></a>Beispiele

``` syntax
[
    dllname("MyAppsFirst.dll")
] 
module MyModule
{
    [entry(20), bindable, requestedit, 
     propputref, defaultbind ] HRESULT Func1(
         [in]IUnknown * Param1, 
         [out] MyType * Param2);
    [entry("TwentyOne"), hidden, vararg] SAFEARRAY (int) Func2(
        [in, out] SAFEARRAY (variant) *varP) ;
    [entry(22)] Float Func3(
        [in] lpstr pName, [in] double dLevel,
        [out] short * sByte) ;
    } ;
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Dllname**](dllname-str-.md)
</dt> <dt>

[**Modul**](module.md)
</dt> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[ODL-Dateibeispiel](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 