---
title: defaultbind-Attribut
description: Das Attribut "\ Defaultbind \" gibt die einzelne, bindbare Eigenschaft an, die das Objekt am besten darstellt.
ms.assetid: 8cf0922a-3d7c-404d-b4fd-edbd772987bf
keywords:
- Defaultbind-Attribut-Mittel l
topic_type:
- apiref
api_name:
- defaultbind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 518c11da8d5f9b0762843c5b69292562a94b80c4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038963"
---
# <a name="defaultbind-attribute"></a>defaultbind-Attribut

Das **\[ Defaultbind \]** -Attribut gibt die einzelne, bindbare Eigenschaft an, die das Objekt am besten darstellt.

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable, defaultbind [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Interface-Attribute-List* 
</dt> <dd>

Gibt eine Liste mit einem oder mehreren Attributen an, die auf die gesamte Schnittstelle angewendet werden. Wenn zwei oder mehr Schnittstellen Attribute vorhanden sind, müssen diese durch Kommas getrennt werden.

</dd> <dt>

*Schnittstellen Name* 
</dt> <dd>

Gibt den Namen der Schnittstelle an.

</dd> <dt>

*Attribut-List* 
</dt> <dd>

Gibt eine Liste mit mindestens einem Attribut an, das für die Funktion gilt. Wenn zwei oder mehr Schnittstellen Attribute vorhanden sind, müssen diese durch Kommas getrennt werden.

</dd> <dt>

*ReturnType* 
</dt> <dd>

Gibt den Rückgabetyp der Funktion an.

</dd> <dt>

*function-name* 
</dt> <dd>

Gibt den Namen der Funktion an, auf die das **\[ Defaultbind \]** -Attribut angewendet wird.

</dd> <dt>

*params* 
</dt> <dd>

Funktionsparameter Liste.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Eigenschaften, die über das **\[ Defaultbind \]** -Attribut verfügen, müssen auch über das **\[** [**bindbare**](bindable.md) **\]** Attribut verfügen. Nur eine Eigenschaft in einer Schnittstelle oder einem Dispinterface-Attribut kann das **\[ Defaultbind \]** -Attribut aufweisen.

Dieses Attribut wird von Containern verwendet, die ein Benutzer Modell enthalten, das die Bindung an ein Objekt und nicht die Bindung an eine Eigenschaft eines Objekts umfasst. Ein Objekt kann die Datenbindung unterstützen, aber nicht über dieses Attribut verfügen.

### <a name="flags"></a>Flags

funcflag " \_ sdefaultbind", varflag " \_ sdefaultbind"

## <a name="examples"></a>Beispiele

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, 
         defaultbind, displaybind] long Size(void);

        [id(1), propput, bindable, 
         defaultbind, displaybind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**bindable**](bindable.md)
</dt> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[FUNCFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 