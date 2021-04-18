---
title: requestedit-Attribut
description: Das Attribut \ requestedit \ gibt an, dass die Eigenschaft die OnRequestEdit-Benachrichtigung unterstützt.
ms.assetid: 63f38d83-596b-4031-bb6a-972374cd0c60
keywords:
- requestedit-Attribut-Mittel l
topic_type:
- apiref
api_name:
- requestedit
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18d83beea34f008e6e96fcd493d8410d7d2c5b88
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106338254"
---
# <a name="requestedit-attribute"></a>requestedit-Attribut

Das **\[ requestedit \]** -Attribut gibt an, dass die Eigenschaft die **OnRequestEdit** -Benachrichtigung unterstützt.

``` syntax
[requestedit [,optional-attributes]] return-type function-name(params)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*optionale Attribute* 
</dt> <dd>

NULL oder mehr mittlere Attribute.

</dd> <dt>

*Rückgabetyp* 
</dt> <dd>

Gibt den Rückgabetyp der Funktion an.

</dd> <dt>

*function-name* 
</dt> <dd>

Gibt den Namen der Funktion in der IDL-Datei an.

</dd> <dt>

*params* 
</dt> <dd>

NULL oder mehr Funktionsparameter.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Unterstützung der **OnRequestEdit** -Benachrichtigung bedeutet, dass das-Objekt vor einer Änderung dem Client eine Anforderung zur Berechtigung zum Ändern einer Eigenschaft sendet. Ein Objekt kann die Datenbindung unterstützen, aber nicht über dieses Attribut verfügen.

### <a name="flags"></a>Flags

funcflag \_ frequestedit, varflag \_ frequestedit

## <a name="examples"></a>Beispiele

``` syntax
properties:
    [propget, helpstring("A useful comment"), bindable, defaultbind,
     displaybind, requestedit] long Func1(void);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[FUNCFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 