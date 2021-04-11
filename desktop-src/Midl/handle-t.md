---
title: handle_t-Attribut
description: Das Handle \_ t-Schlüsselwort deklariert ein Objekt, das dem primitiven handle-Handle \_ t entspricht. Ein Primitives Bindungs Handle ist ein Datenobjekt, das von der Anwendung zur Darstellung der Bindung verwendet werden kann.
ms.assetid: 94962ed6-5c17-43e7-853f-1e9c4b3118a7
keywords:
- handle_t Attribut-Mittel l
topic_type:
- apiref
api_name:
- handle_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 435dcfcf620bd33043d8c8c7d948bccd74eb4e77
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314822"
---
# <a name="handle_t-attribute"></a>Handle \_ t-Attribut

Das **handle \_ t** -Schlüsselwort deklariert ein Objekt, das dem primitiven handle-Handle **\_ t** entspricht. Ein Primitives Bindungs Handle ist ein Datenobjekt, das von der Anwendung zur Darstellung der Bindung verwendet werden kann.

``` syntax
typedef RPC_BINDING_HANDLE handle_t;
```

## <a name="parameters"></a>Parameter

Dieses Attribut hat keine Parameter.

## <a name="remarks"></a>Bemerkungen

Der **handle \_ t** -Typ ist einer der vordefinierten Typen der IDL (Interface Definition Language). Sie kann als Typspezifizierer in [**typedef**](typedef.md) -Deklarationen, allgemeinen Deklarationen und Funktions Deklaratoren (als Funktions Rückgabetyp-Spezifizierer und Parametertyp Spezifizierer) angezeigt werden. Informationen zu dem Kontext, in dem typspezifier angezeigt wird, finden Sie unter [Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md).

In Microsoft RPC können Parameter des Typs **handle \_ t** nur als in- **\[** [](in.md) **\]** Parametern auftreten. Primitive Handles können nicht über das **\[** [**Unique**](unique.md) - **\]** oder **\[** [**ptr**](ptr.md) - **\]** Attribut verfügen.

Parameter vom Typ **handle \_ t** (primitive handle Parameters) werden nicht im Netzwerk übertragen.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mittel l-Basis Typen](midl-base-types.md)
</dt> <dt>

[Bindung und Handles](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**in**](in.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**gem**](unique.md)
</dt> </dl>

 

 