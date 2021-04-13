---
title: Eingabeattribut
description: Das Attribut \ Entry \ gibt eine exportierte Funktion oder Konstante in einem Modul an, indem der Einstiegspunkt in der DLL identifiziert wird.
ms.assetid: 1d2d6429-d828-44ec-8b0a-cefb64c6e706
keywords:
- Eingabe Attribut-Mittel l
topic_type:
- apiref
api_name:
- entry
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e596284a83c48bcfc84ef4f7985aed7c33ba7da
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314744"
---
# <a name="entry-attribute"></a>Eingabeattribut

Das Attribut **\[ Entry \]** gibt eine exportierte Funktion oder Konstante in einem Modul an, indem der Einstiegspunkt in der DLL identifiziert wird.

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

*UUID-Nummer* 
</dt> <dd>

Gibt eine universell eindeutige ID für das [**Modul**](module.md)an.

</dd> <dt>

*Eintrags-ID* 
</dt> <dd>

Gibt den Funktionsnamen oder die ganzzahlige Identifikationsnummer des Modul Einstiegs Punkts an.

</dd> <dt>

*optional-Attribut-List* 
</dt> <dd>

Gibt 0 (null) oder mehr Attribute an, die der mittlerer l-Compiler auf das [**Modul**](module.md)anwenden soll.

</dd> <dt>

*ModuleName* 
</dt> <dd>

Gibt den Namen an, den andere Softwarekomponenten verwenden, um das [**Modul**](module.md)zu kennzeichnen.

</dd> <dt>

*Elementliste* 
</dt> <dd>

Gibt mindestens eine Modul Element Definitions-Anweisung an.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn die *EntryID* -Variable des **\[ Entry \]** -Attributs eine Zeichenfolge ist, ist dies ein benannter Einstiegspunkt. Wenn *EntryID* eine Zahl ist, wird der Einstiegspunkt durch eine Ordinalzahl definiert. Dieses Attribut bietet eine Möglichkeit zum Abrufen der Adresse einer Funktion in einem Modul.

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

[**dllname**](dllname-str-.md)
</dt> <dt>

[**Mond**](module.md)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 