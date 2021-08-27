---
title: type_strict_context_handle-Attribut
description: Verwenden Sie das \type \_ strict \_ context \_ handle\ in einer ACF-Datei, um Einschränkungen für Kontexthandles festzulegen.
ms.assetid: b67caad2-e87d-4eba-8555-8f347aadd515
keywords:
- type_strict_context_handle-Attribut MIDL
topic_type:
- apiref
api_name:
- type_strict_context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7e10c6231ac41287a08df7b9a0fa4e5361eddec9eb72bb6059b9f00dea5106
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105620"
---
# <a name="type_strict_context_handle-attribute"></a>Type \_ \_ Strict-Kontexthandleat \_

Verwenden Sie das **\[ \_ \_ Typ-Strict-Kontexthandle \_ \]** in einer ACF-Datei, um Einschränkungen für Kontexthandles festzulegen.

``` syntax
[ 
    type_strict_context_handle 
    [, interface-attribute-list] 
] 
interface interface-name
{
    interface-definition-statements
}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*interface-attribute-list* 
</dt> <dd>

Andere ACF-Attribute, die für die gesamte Schnittstelle gelten. Zu den gültigen Attributen gehören [**das automatische \_ Handle,**](auto-handle.md) [**das implizite \_ Handle,**](implicit-handle.md)das [**explizite \_ Handle**](explicit-handle.md)und [**das Optimieren**](optimize.md)von , [**Code**](code.md)oder [**Nocode**](nocode.md). Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*Schnittstellenname* 
</dt> <dd>

Der Name der Schnittstelle.

</dd> <dt>

*interface-definition-statements* 
</dt> <dd>

Eine oder mehrere MIDL-Anweisungen, die die Elemente der [**Schnittstelle**](interface.md)definieren.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Um dieses Attribut verwenden zu können, muss das Flag -target beim Ausführen von midl.exe auf NT60 (oder höher) festgelegt werden.

\[Type \_ \_ Strict-Kontexthandle \_ ist eine funktionale \] Obermenge des \[ \_ strict-Kontexthandle. \_ \] Im \[ \_ strict-Kontexthandle \_ \] ist die Typ-ID des Handles immer 0. Im \[ Typ \_ \_ strict-Kontexthandle \_ wird vom \] MIDL-Compiler eine eindeutige Typ-ID zugewiesen.

Es wird empfohlen, das \[ \_ Typ-Strict-Kontexthandle \_ \_ anstelle des \] \[ \_ strict-Kontexthandle zu \_ \] verwenden. Kontexthandles sind standardmäßig keinem bestimmten Typ zugeordnet. Wenn mehrere Typen von Kontexthandles im gleichen Prozess verwendet werden, kann ein böswilliger Client ein Kontexthandle anstelle eines anderen übergeben, um unerwünschte Ergebnisse zu erzeugen. Durch die Verwendung des \[ Typ \_ \_ \_ \] strict-Kontexthandle können Anwendungen die Kontexthandletypkonsistenz erzwingen und die Verwendung nicht übereinstimmender Kontexthandletypen verhindern.

Ein Kontexthandle, das mit \[ einem typ \_ \_ strict-Kontexthandle \_ \] attributiert wird, kann nicht auch mit \[ dem strict-Kontexthandle attributiert \_ \_ \] werden.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Anwendungskonfigurationsdatei (Application Configuration File, ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**Code**](code.md)
</dt> <dt>

[Kontexthandles](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[**\_Kontexthandle \_ serialisieren**](context-handle-serialize.md)
</dt> <dt>

[**context \_ handle \_ noserialize**](context-handle-noserialize.md)
</dt> <dt>

[**Explizites \_ Handle**](explicit-handle.md)
</dt> <dt>

[**Implizites \_ Handle**](implicit-handle.md)
</dt> <dt>

[**nocode**](nocode.md)
</dt> <dt>

[**Optimieren**](optimize.md)
</dt> <dt>

[Striktes \_ \_ Kontexthandle](strict-context-handle.md)
</dt> </dl>

 

 