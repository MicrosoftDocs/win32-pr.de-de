---
title: requestedit-Attribut
description: Das Attribut \requestedit\ gibt an, dass die Eigenschaft die OnRequestEdit-Benachrichtigung unterstützt.
ms.assetid: 63f38d83-596b-4031-bb6a-972374cd0c60
keywords:
- requestedit attribute MIDL
topic_type:
- apiref
api_name:
- requestedit
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51a894e5d4a09e7535e10a73e1bd118245e5886e0cdbb23b0f0645e588ab4adf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146353"
---
# <a name="requestedit-attribute"></a>requestedit-Attribut

Das **\[ requestedit-Attribut \]** gibt an, dass die Eigenschaft die **OnRequestEdit-Benachrichtigung** unterstützt.

``` syntax
[requestedit [,optional-attributes]] return-type function-name(params)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*optional-attributes* 
</dt> <dd>

Null oder mehr MIDL-Attribute.

</dd> <dt>

*return-type* 
</dt> <dd>

Gibt den Rückgabetyp der Funktion an.

</dd> <dt>

*Funktionsname* 
</dt> <dd>

Gibt den Namen der Funktion in der IDL-Datei an.

</dd> <dt>

*params* 
</dt> <dd>

Null oder mehr Funktionsparameter.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Unterstützung der OnRequestEdit-Benachrichtigung** bedeutet, dass das -Objekt dem Client vor dem Ändern einer Eigenschaft eine Berechtigungsanforderung sendet. Ein Objekt kann die Datenbindung unterstützen, aber nicht über dieses Attribut verfügen.

### <a name="flags"></a>Flags

FUNCFLAG \_ FREQUESTEDIT, VARFLAG \_ FREQUESTEDIT

## <a name="examples"></a>Beispiele

``` syntax
properties:
    [propget, helpstring("A useful comment"), bindable, defaultbind,
     displaybind, requestedit] long Func1(void);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Typeflags](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[ODL-Dateibeispiel](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 