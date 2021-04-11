---
title: immediatebind-Attribut
description: Das Attribut \ unmittelatebind \ gibt an, dass die Datenbank sofort über alle Änderungen an einer Eigenschaft eines Daten gebundenen Objekts benachrichtigt wird.
ms.assetid: 1c08ddca-e273-43b3-a8f6-ed7f552e4e0e
keywords:
- unmittel-BIND-Attribut (Mittel l)
topic_type:
- apiref
api_name:
- immediatebind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc8a797514c15f8d4c46bb6161946d5d0b6bd10b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104208823"
---
# <a name="immediatebind-attribute"></a>immediatebind-Attribut

Das **\[ unmittelatebind \]** -Attribut gibt an, dass die Datenbank sofort über alle Änderungen an einer Eigenschaft eines Daten gebundenen Objekts benachrichtigt wird.

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable, immediatebind[, optional-attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Interface-Attribute-List* 
</dt> <dd>

Gibt eine Liste mit einem oder mehreren Attributen an, die auf die gesamte Schnittstelle angewendet werden.

</dd> <dt>

*Schnittstellen Name* 
</dt> <dd>

Gibt den Namen der [**Schnittstelle**](interface.md) oder der " [**dispinterface**](dispinterface.md)" an.

</dd> <dt>

*optional-Attribut-List* 
</dt> <dd>

NULL oder mehr Funktions Attribute.

</dd> <dt>

*ReturnType* 
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

Das **\[ unmittelatebind \]** -Attribut ermöglicht es Steuerelementen, zwischen Eigenschaften zu unterscheiden, die die Datenbank über jede Änderung benachrichtigen müssen. So sollte beispielsweise jede Änderung an einem CheckBox-Steuerelement sofort an die zugrunde liegende Datenbank gesendet werden, auch wenn das Steuerelement den Fokus nicht verliert. Bei einem ListBox-Steuerelement tritt jedoch eine Änderung auf, wenn eine andere Auswahl hervorgehoben wird. Das Benachrichtigen der Datenbank über eine Änderung, bevor das Steuerelement den Fokus verliert, wäre ineffizient und unnötig. Mit dem Attribut " **\[ unmittelatebind \]** " können Sie angeben, indem Sie das unmittelatebind-Bit festlegen, einzelne Eigenschaften auf einem Formular, dessen Änderungen sofort gemeldet werden sollen.

Eigenschaften, die über das **\[ unmittelatebind \]** -Attribut verfügen, müssen auch über das **\[** [**bindbare**](bindable.md) **\]** Attribut verfügen.

### <a name="flags"></a>Flags

funkflag " \_ smediatebind", varflag " \_ fmmediatebind"

## <a name="examples"></a>Beispiele

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, immediatebind] long Size(void);

        [id(1), propput, bindable, 
         immediatebind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**bindable**](bindable.md)
</dt> <dt>

[**FUNCFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**berfläche**](interface.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 