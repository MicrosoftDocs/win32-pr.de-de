---
title: retval-Attribut
description: Das Attribut \retval\ gibt den Parameter an, der den Rückgabewert des -Mitglieds empfängt.
ms.assetid: 3a5f1469-7828-4c38-b58f-195a47b2a66f
keywords:
- MIDL-Attribut "retval"
topic_type:
- apiref
api_name:
- retval
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72655883b24c83890cf2f5604cb8f7335c6943b32e5e69611dba415689b03e22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146303"
---
# <a name="retval-attribute"></a>retval-Attribut

Das **\[ retval-Attribut \]** bestimmt den Parameter, der den Rückgabewert des -Member empfängt.

``` syntax
return-type function-name(
    [out, retval [, optional-attributes]] data-type * param-name,
    ...);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*return-type* 
</dt> <dd>

Der Datentyp des Rückgabewerts der Remoteprozedur.

</dd> <dt>

*Funktionsname* 
</dt> <dd>

Der Name, der zum Aufrufen der Remoteprozedur verwendet wird.

</dd> <dt>

*optional-attributes* 
</dt> <dd>

Null oder mehr MIDL-Attribute.

</dd> <dt>

*-Datentyp* 
</dt> <dd>

Der Typ der Daten, die durch den -Parameter übergeben werden.

</dd> <dt>

*param-name* 
</dt> <dd>

Der Bezeichnername des Parameters.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Sie können das **\[ retval-Attribut für Parameter \]** von Schnittstellenmitgliedern verwenden, die Methoden beschreiben oder Eigenschaften erhalten. (Das -Attribut ist für den letzten Parameter einer Methode erforderlich, die über das -Attribut verfügt. **\[** [**propget**](propget.md) **\]** -Attribut.) Der Parameter muss das **\[** [**out-Attribut**](out-idl.md) **\]** und einen Zeigertyp haben.

Sie können das **\[** [**optionale Attribut**](optional.md) **\]** nicht auf einen **\[ retval-Parameter \]** anwenden.

Der MIDL-Compiler akzeptiert die folgende Parameter reihenfolge (von links nach rechts):

1.  Erforderliche Parameter (Parameter, die nicht über den **\[** [**Standardwert oder**](defaultvalue.md) **\]** **\[** [**optionale**](optional.md) Attribute **\]** verfügen).
2.  Optionale Parameter mit oder ohne **\[** [**defaultvalue-Attribut.**](defaultvalue.md) **\]**
3.  Parameter mit dem **\[** [**optionalen**](optional.md) **\]** Attribut und ohne das **\[** [**defaultvalue-Attribut.**](defaultvalue.md) **\]**
4.  **\[**[](lcid.md) **\]** lcid-Parameter, sofern ein Parameter vorgibt.
5.  **\[ \] retval-Parameter.**

Parameter mit dem **\[ Retval-Attribut \]** werden in benutzerorientierten Browsern nicht angezeigt.

### <a name="flags"></a>Flags

IDLFLAG \_ FRETVAL

## <a name="examples"></a>Beispiele

``` syntax
HRESULT MyMethod([out, retval] InMyFace** ReturnVal);
HRESULT MyOtherMethod([out, retval] VARIANT_BOOL* ReturnVal);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Defaultvalue**](defaultvalue.md)
</dt> <dt>

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**Lcid**](lcid.md)
</dt> <dt>

[ODL-Dateibeispiel](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**Optional**](optional.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**Typeflags**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 