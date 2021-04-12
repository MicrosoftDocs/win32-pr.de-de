---
title: defaultvalue-Attribut
description: Mit dem Attribut "\ DefaultValue \" können Sie einen Standardwert für einen eingegebenen optionalen Parameter angeben.
ms.assetid: a974a0f7-7b08-4f17-bb28-0e23e6aa97db
keywords:
- DefaultValue-Attribut (Mitte)
topic_type:
- apiref
api_name:
- defaultvalue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04f4efaac16325ec77721665a4dee14c9514a192
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314979"
---
# <a name="defaultvalue-attribute"></a>defaultvalue-Attribut

Mit dem **\[ DefaultValue \]** -Attribut können Sie einen Standardwert für einen eingegebenen optionalen Parameter angeben.

``` syntax
interface interface-name
{
  return-type function-name(
        mandatory-param-list, 
        [[attribute-list,] defaultvalue(value)] param-type param-name
        [ , optional-param-list]);
}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Schnittstellen Name* 
</dt> <dd>

Gibt den Namen der Schnittstelle an.

</dd> <dt>

*Rückgabetyp* 
</dt> <dd>

Gibt den Rückgabetyp der Funktion an.

</dd> <dt>

*function-name* 
</dt> <dd>

Gibt den Namen der Funktion an, auf die das **\[ DefaultValue \]** -Attribut angewendet wird.

</dd> <dt>

*obligatorisch-param-List* 
</dt> <dd>

Gibt ein oder mehrere erforderliche Parameter an.

</dd> <dt>

*Attribut-List* 
</dt> <dd>

Gibt eine Liste mit einem oder mehreren Attributen, die durch Kommas getrennt sind, an, die auf den-Parameter angewendet werden.

</dd> <dt>

*param-Typ* 
</dt> <dd>

Gibt den Typ des optionalen Parameters an.

</dd> <dt>

*Param-Name* 
</dt> <dd>

Gibt den Namen des optionalen Parameters an.

</dd> <dt>

*optional-param-List* 
</dt> <dd>

Gibt 0 (null) oder mehr zusätzliche Parameter an, von denen jeder über einen Standardwert verfügen muss.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Standardwert, den Sie für den-Parameter angeben, kann eine beliebige Konstante oder ein Ausdruck sein, der zu einer Konstante aufgelöst wird, der durch eine **Variante** dargestellt werden kann. Insbesondere kann das **\[ DefaultValue \]** -Attribut nicht auf einen Parameter angewendet werden, bei dem es sich um eine Struktur, ein Array oder einen **SAFEARRAY** -Typ handelt.

Der mittlerer l-Compiler akzeptiert die folgende Parameter Reihenfolge (von links nach rechts):

1.  Erforderliche Parameter (Parameter, die nicht über das **\[ DefaultValue \]** - **\[** Attribut oder [**optionale**](optional.md) **\]** Attribute verfügen)
2.  optionale Parameter mit oder ohne das **\[ DefaultValue \]** -Attribut
3.  Parameter mit dem **\[ optionalen \]** -Attribut und ohne das **\[ DefaultValue \]** -Attribut
4.  **\[**[**LCID**](lcid.md) - **\]** Parameter (falls vorhanden)
5.  **\[**[**retval**](retval.md) **\]** Parame

## <a name="examples"></a>Beispiele

``` syntax
interface IFace : IUnknown
{
    HRESULT Ex1([defaultvalue(44)] LONG i);
    HRESULT Ex2([defaultvalue(44)] SHORT i);
...
};

interface QueryDef : IUnknown
{
    HRESULT OpenRecordset( [in, defaultvalue(DBOPENTABLE)]
    LONG Type,
    [out,retval] Recordset **pprst);
}
//  Type is now known to be a LONG type (good for browser in VBA and
//  good for a C/C++ programmer) and has a default value of
//  DBOPENTABLE
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**berfläche**](interface.md)
</dt> <dt>

[**LCID**](lcid.md)
</dt> <dt>

[**optionale**](optional.md)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**retval**](retval.md)
</dt> <dt>

[FUNCFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 