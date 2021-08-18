---
title: context_handle_serialize-Attribut
description: Das Attribut \context handle serialize\ ACF garantiert, dass ein Kontexthand handle unabhängig vom Standardverhalten der Anwendung immer \_ \_ serialisiert wird.
ms.assetid: e2f48582-228a-4725-9543-1e638d86ff6b
keywords:
- context_handle_serialize MIDL-Attribut
topic_type:
- apiref
api_name:
- context_handle_serialize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c91bf9ab1610585001b1380b15ba5a89433f80194596e26cbae84692ff3a872a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013958"
---
# <a name="context_handle_serialize-attribute"></a>context \_ handle \_ serialize-Attribut

Das **\[ Context Handle \_ \_ serialize \]** ACF-Attribut garantiert, dass ein Kontexthand handle immer serialisiert wird, unabhängig vom Standardverhalten der Anwendung.

``` syntax
typedef [context_handle_serialize [ , type-acf-attribute-list ] ] context-handle-type;

[context_handle_serialize [, function-acf-attribute-list ] ] function-name( );

function-name(
    [context_handle_serialize [ , parameter-acf-attribute-list ] ] param-name );
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*type-acf-attribute-list* 
</dt> <dd>

Alle anderen ACF-Attribute, die für den Typ gelten.

</dd> <dt>

*context-handle-type* 
</dt> <dd>

Der Bezeichner, der den Kontexthand handle-Typ angibt, wie in einer [**Typedef-Deklaration**](typedef.md) definiert. Dies ist der Typ, der das **\[ Serialisierungsattribut \_ des \_ Kontexthandpunkts \]** in der IDL-Datei empfängt.

</dd> <dt>

*function-acf-attribute-list* 
</dt> <dd>

Alle zusätzlichen ACF-Attribute, die für die Funktion gelten.

</dd> <dt>

*Funktionsname* 
</dt> <dd>

Der Name der Funktion, wie in der IDL-Datei definiert.

</dd> <dt>

*parameter-acf-attribute-list* 
</dt> <dd>

Alle anderen ACF-Attribute, die für den Parameter gelten.

</dd> <dt>

*param-name* 
</dt> <dd>

Der Name des Parameters, wie in der IDL-Datei definiert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das **\[ \_ \_ Serialisierungsattribut \]** des Kontexthandpunkts identifiziert ein Bindungshand handle, das Kontext- oder Zustandsinformationen auf dem Server zwischen Remoteprozeduraufrufen verwaltet. Das Attribut kann als [](typedef.md) IDL Typedef-Typattribut, als Funktions-Rückgabetypattribut oder als Parameterattribut angezeigt werden.

Standardmäßig werden Aufrufe von Kontexthandles serialisiert, aber eine Anwendung kann [**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) aufrufen, um dieses Standardverhalten zu überschreiben. Durch die **\[ Verwendung des \_ Serialisierungsattributs \_ \]** des Kontexthandpunkts in einer ACF-Datei wird sichergestellt, dass Aufrufe für dieses bestimmte Kontexthand handle serialisiert werden, auch wenn die aufrufende Anwendung die Standardserialisierung außer Kraft gesetzt hat. Eine Kontext-Rundownroutine ist optional.

Dieses Attribut ist in MIDL Version 5.0 verfügbar.

**Windows Server 2003 und Windows XP oder höher:** Eine einzelne Schnittstelle kann sowohl serialisierte als auch nicht serialisierte Kontexthandles aufnehmen, sodass eine Methode auf einer Schnittstelle ausschließlich (serialisiert) auf ein Kontexthandle zugreifen kann, während andere Methoden im freigegebenen Modus (nicht serialisiert) auf dieses Kontexthandle zugreifen. Diese Zugriffsfunktionen sind vergleichbar mit Lese-/Schreibsperrmechanismen. -Methoden, die ein serialisiertes Kontexthandle verwenden, sind exklusive Benutzer (Writer), während Methoden, die ein nicht serialisiertes Kontexthandle verwenden, freigegebene Benutzer (Reader) sind. Methoden, die den Zustand eines Kontexthandpunkts zerstören oder ändern, müssen serialisiert werden. Methoden, die den Zustand eines Kontexthandles nicht ändern, z. B. methoden, die einfach aus einem Kontexthandle lesen, können nicht serialisiert werden. Beachten Sie, dass Erstellungsmethoden implizit serialisiert werden.

## <a name="examples"></a>Beispiele

``` syntax
typedef [context_handle_serialize] PCONTEXT_HANDLE_TYPE; 
HRESULT RemoteFunc([context_handle_serialize] pCxHandle);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Anwendungskonfigurationsdatei (Application Configuration File, ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[ACF-Attribute](acf-attributes.md)
</dt> <dt>

[**context \_ handle \_ noserialize**](context-handle-noserialize.md)
</dt> <dt>

[**Kontexthand \_ handle**](context-handle.md)
</dt> <dt>

[Kontexthandles](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext)
</dt> <dt>

[Run-down-Routine für Den Serverkontext](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[Multithreadclients und Kontexthandles](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> </dl>

 

 