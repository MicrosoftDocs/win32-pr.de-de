---
title: defaultvalue-Attribut
description: Mit dem Attribut \defaultvalue\ können Sie einen Standardwert für einen typisierten optionalen Parameter angeben.
ms.assetid: a974a0f7-7b08-4f17-bb28-0e23e6aa97db
keywords:
- defaultvalue-Attribut MIDL
topic_type:
- apiref
api_name:
- defaultvalue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f38fe7dfc99c5c9c1c6a7cae1a5fdd5750c5f3e9af37e56706b27300876da1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067350"
---
# <a name="defaultvalue-attribute"></a>defaultvalue-Attribut

Mit **\[ dem \] defaultvalue-Attribut** können Sie einen Standardwert für einen typisierten optionalen Parameter angeben.

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

*Schnittstellenname* 
</dt> <dd>

Gibt den Namen der Schnittstelle an.

</dd> <dt>

*rückgabetyp* 
</dt> <dd>

Gibt den Rückgabetyp der Funktion an.

</dd> <dt>

*Funktionsname* 
</dt> <dd>

Gibt den Namen der Funktion an, auf die das **\[ defaultvalue-Attribut \]** angewendet wird.

</dd> <dt>

*mandatory-param-list* 
</dt> <dd>

Gibt für oder mehrere erforderliche Parameter an.

</dd> <dt>

*Attributliste* 
</dt> <dd>

Gibt eine Durch Kommas getrennte Liste von attributen an, die für den -Parameter gelten.

</dd> <dt>

*param-type* 
</dt> <dd>

Gibt den Typ des optionalen Parameters an.

</dd> <dt>

*param-name* 
</dt> <dd>

Gibt den Namen des optionalen Parameters an.

</dd> <dt>

*optional-param-list* 
</dt> <dd>

Gibt null oder mehr zusätzliche Parameter an, von denen jeder einen Standardwert aufweisen muss.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Standardwert, den Sie für den Parameter angeben, kann eine beliebige Konstante oder ein Ausdruck sein, der in eine Konstante aufgelöst wird, die durch eine **VARIANT** dargestellt werden kann. Insbesondere können Sie das **\[ \] defaultvalue-Attribut** nicht auf einen Parameter anwenden, der eine Struktur, ein Array oder ein **SAFEARRAY-Typ** ist.

Der MIDL-Compiler akzeptiert die folgende Parameterreihenfolge (von links nach rechts):

1.  Erforderliche Parameter (Parameter ohne **\[ defaultvalue- \]** oder **\[** [**optionale**](optional.md) **\]** Attribute)
2.  optionale Parameter mit oder ohne das **\[ \] defaultvalue-Attribut,**
3.  Parameter mit dem **\[ optionalen \]** Attribut und ohne das **\[ \] defaultvalue-Attribut,**
4.  **\[**[](lcid.md) **\]** lcid-Parameter, falls vorhanden,
5.  **\[**[**retval**](retval.md) **\]** Parameter

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

[**Dispatchschnittstelle**](dispinterface.md)
</dt> <dt>

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**Schnittstelle**](interface.md)
</dt> <dt>

[**Lcid**](lcid.md)
</dt> <dt>

[**Optional**](optional.md)
</dt> <dt>

[BEISPIEL FÜR ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**Retval**](retval.md)
</dt> <dt>

[Typeflags](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 