---
title: retval-Attribut
description: Das Attribut \ retval \ gibt den Parameter an, der den Rückgabewert des Members empfängt.
ms.assetid: 3a5f1469-7828-4c38-b58f-195a47b2a66f
keywords:
- retval-Attribut-Mittel l
topic_type:
- apiref
api_name:
- retval
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04b53aa2b8ab66737bd4d97710fe942ee73bf0b8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858173"
---
# <a name="retval-attribute"></a>retval-Attribut

Das **\[ retval \]** -Attribut bestimmt den Parameter, der den Rückgabewert des Members empfängt.

``` syntax
return-type function-name(
    [out, retval [, optional-attributes]] data-type * param-name,
    ...);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Rückgabetyp* 
</dt> <dd>

Der Datentyp des Rückgabewerts der Remote Prozedur.

</dd> <dt>

*function-name* 
</dt> <dd>

Der Name, der verwendet wird, um die Remote Prozedur aufzurufen.

</dd> <dt>

*optionale Attribute* 
</dt> <dd>

NULL oder mehr mittlere Attribute.

</dd> <dt>

*Datentyp* 
</dt> <dd>

Der Typ der Daten, die durch den-Parameter übergeben werden.

</dd> <dt>

*Param-Name* 
</dt> <dd>

Der Bezeichnername des Parameters.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Sie können das **\[ retval \]** -Attribut für Parameter von Schnittstellenmembern verwenden, die Methoden oder Get-Eigenschaften beschreiben. (Das-Attribut ist für den letzten Parameter einer Methode erforderlich, die über das **\[** [**propget**](propget.md) **\]** -Attribut.) Der-Parameter muss das **\[** [**out**](out-idl.md) **\]** -Attribut aufweisen und muss ein Zeigertyp sein.

Sie können das **\[** [**optionale**](optional.md) - **\]** Attribut nicht auf einen **\[ retval \]** -Parameter anwenden.

Der mittlerer l-Compiler akzeptiert die folgende Parameter Reihenfolge (von links nach rechts):

1.  Erforderliche Parameter (Parameter, die nicht über das **\[** [**DefaultValue**](defaultvalue.md) **\]** - **\[** Attribut oder [**optionale**](optional.md) **\]** Attribute verfügen).
2.  Optionale Parameter mit oder ohne das **\[** [**DefaultValue**](defaultvalue.md) - **\]** Attribut.
3.  Parameter mit dem **\[** [**optionalen**](optional.md) **\]** -Attribut und ohne das **\[** [**DefaultValue**](defaultvalue.md) - **\]** Attribut.
4.  **\[**[**LCID**](lcid.md) - **\]** Parameter (sofern vorhanden).
5.  **\[ retval \]** -Parameter.

Parameter mit dem **\[ retval \]** -Attribut werden in benutzerorientierten Browsern nicht angezeigt.

### <a name="flags"></a>Flags

IDLFLAG \_ fretval

## <a name="examples"></a>Beispiele

``` syntax
HRESULT MyMethod([out, retval] InMyFace** ReturnVal);
HRESULT MyOtherMethod([out, retval] VARIANT_BOOL* ReturnVal);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DefaultValue**](defaultvalue.md)
</dt> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**LCID**](lcid.md)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**optionale**](optional.md)
</dt> <dt>

[**vorgenommen**](out-idl.md)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**FUNCFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 