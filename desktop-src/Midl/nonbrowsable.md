---
title: nonbrowsable-Attribut
description: Verwenden Sie das \ NonBrowsable \-Attribut, um eine Schnittstelle oder einen dispinterface-Member zu kennzeichnen, der nicht in einem Eigenschaften Browser angezeigt werden soll.
ms.assetid: 94e868cc-8d9c-4b8a-ac18-1ea513a103da
keywords:
- nicht durchsuchbares Attribut, Mittel l
topic_type:
- apiref
api_name:
- nonbrowsable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e24c39511df9637c352245b98b237fe8fd451eb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948639"
---
# <a name="nonbrowsable-attribute"></a>nonbrowsable-Attribut

Verwenden Sie das nicht **\[ \] browsefähige** Attribut, um eine Schnittstelle oder einen dispinterface-Member zu kennzeichnen, der nicht in einem Eigenschaften Browser angezeigt werden soll.

``` syntax
[property-attribute-list, nonbrowsable]return-type property-name(prop-param-list)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Property-Attribute-List* 
</dt> <dd>

Andere Attribute, die auf die-Eigenschaft angewendet werden.

</dd> <dt>

*Rückgabetyp* 
</dt> <dd>

Der Typ der Daten, die von der-Methode zurückgegeben werden.

</dd> <dt>

*Eigenschaftsname* 
</dt> <dd>

Der Name der Eigenschaft oder Methode.

</dd> <dt>

*Prop-param-List* 
</dt> <dd>

NULL oder mehr Parameter, die an die Methode weitergegeben werden sollen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Bestimmte Eigenschaften sollten nicht in einem Eigenschaften Browser angezeigt werden. Dies liegt möglicherweise daran, dass das Abrufen des Werts sehr viel Zeit in Anspruch nehmen würde. Im Beispiel wird verhindert, dass der Benutzer versucht, die *count* -Eigenschaft abzurufen, die die Anzahl der Zeilen im Dynaset zurückgibt. Diese Zahl kann die Ergebnisse einer sehr großen Abfrage darstellen.

Andere Eigenschaften können unerwartete Auswirkungen auf den Browser haben. Stellen Sie sich z. b. ein Steuerelement mit der Eigenschaft "issselected" vor, um zu bestimmen, ob das Steuerelement ausgewählt ist Wenn "issgewählt" auf "false" festgelegt ist, durchsucht ein Auswahl basierter Eigenschaften Browser ein anderes Objekt.

Beachten Sie, dass eine Eigenschaft, die als **\[ nicht \]** suchbar markiert ist, immer noch in einem Objektkatalog angezeigt wird, in dem keine Eigenschaftswerte angezeigt werden.

### <a name="typeflag-representation"></a>TYPEFLAG-Darstellung

Das vorhanden sein von funkflag, das \_ nicht browsetierbar ist, oder das varflag-Element \_ .

## <a name="examples"></a>Beispiele

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IDynaset:IDispatch
{
    [propget, nonbrowsable]HRESULT Count([out, retval] long *Value);
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 