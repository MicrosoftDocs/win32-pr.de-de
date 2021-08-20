---
title: handle_t-Attribut
description: Das Handle-Schlüsselwort t deklariert ein Objekt als des \_ primitiven Handletyphand handle \_ t. Ein primitives Bindungshand handle ist ein Datenobjekt, das von der Anwendung zur Darstellung der Bindung verwendet werden kann.
ms.assetid: 94962ed6-5c17-43e7-853f-1e9c4b3118a7
keywords:
- handle_t MIDL-Attribut
topic_type:
- apiref
api_name:
- handle_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 251a2574908891d29baf9d4748943d0550f3f015eddccbdd123e31598b39b08c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117991328"
---
# <a name="handle_t-attribute"></a>handle \_ t-Attribut

Das **\_ Handle-Schlüsselwort t** deklariert ein Objekt als des primitiven Handletyphand **handle \_ t.** Ein primitives Bindungshand handle ist ein Datenobjekt, das von der Anwendung zur Darstellung der Bindung verwendet werden kann.

``` syntax
typedef RPC_BINDING_HANDLE handle_t;
```

## <a name="parameters"></a>Parameter

Dieses Attribut verfügt über keine Parameter.

## <a name="remarks"></a>Hinweise

Der **\_ T-Handletyp** ist einer der vordefinierten Typen der Schnittstellendefinitionssprache (Interface Definition Language, IDL). Sie kann als Typspezifizierer in Typedef-Deklarationen, allgemeinen Deklarationen und Funktionsdeklaratoren (als Funktions-Rückgabetypspezifizierer und Parametertypspezifizierer) angezeigt werden. [](typedef.md) Informationen zum Kontext, in dem Typspezifizierer angezeigt werden, finden Sie unter [Interface Definition (IDL)-Datei.](interface-definition-idl-file.md)

In Microsoft RPC können Parameter vom Typ **handle \_ t** nur wie **\[** [**in Parametern**](in.md) **\]** auftreten. Primitive Handles können nicht über das **\[** [**eindeutige Attribut oder**](unique.md) **\]** **\[** [**ptr-Attribut**](ptr.md) **\]** verfügen.

Parameter vom Typ **handle \_ t** (primitive Handleparameter) werden nicht im Netzwerk übertragen.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MIDL-Basistypen](midl-base-types.md)
</dt> <dt>

[Bindung und Handles](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> <dt>

[**in**](in.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> <dt>

[**Ptr**](ptr.md)
</dt> <dt>

[**Einzigartige**](unique.md)
</dt> </dl>

 

 