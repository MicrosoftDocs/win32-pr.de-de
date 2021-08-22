---
title: context_handle_noserialize-Attribut
description: Das \context \_ handle \_ noserialize\ACF-Attribut garantiert, dass ein Kontexthandle unabhängig vom Standardverhalten der Anwendung nie serialisiert wird.
ms.assetid: aff2484e-639b-41d2-94a9-f34ca4f2343c
keywords:
- context_handle_noserialize-Attribut MIDL
topic_type:
- apiref
api_name:
- context_handle_noserialize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40556db0d63441e42d46a0ed7f9bd45edb8b2ce65f8d4b9b84e3a848325ddbb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013998"
---
# <a name="context_handle_noserialize-attribute"></a>\_Kontexthandle \_ noserialize-Attribut

Das **\[ \_ Kontexthandle \_ noserialize \]** ACF-Attribut garantiert, dass ein Kontexthandle unabhängig vom Standardverhalten der Anwendung nie serialisiert wird.

``` syntax
typedef [context_handle_noserialize [ , type-acf-attribute-list ] ] context-handle-type

[context_handle_noserialize [, function-acf-attribute-list ] ] function-name( );

function-name (   [context_handle_noserialize 
  [ , parameter-acf-attribute-list ] ] param-name );
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*type-acf-attribute-list* 
</dt> <dd>

Alle anderen ACF-Attribute, die für den Typ gelten.

</dd> <dt>

*context-handle-type* 
</dt> <dd>

Der Bezeichner, der den Kontexthandletyp angibt, wie in einer [**typedef-Deklaration**](typedef.md) definiert. Dies ist der Typ, der das [**\[ \_ \] Kontexthandleattribut**](context-handle.md) in der IDL-Datei empfängt.

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

Das [**\[ \_ \] Kontexthandleatat**](context-handle.md) identifiziert ein Bindungshandle, das Kontext- oder Zustandsinformationen auf dem Server zwischen Remoteprozeduraufrufen verwaltet. Das Attribut kann als [**IDL-Typdefinitionstypattribut,**](typedef.md) als Funktionsrückgabetypattribut oder als Parameterattribut angezeigt werden.

Standardmäßig werden Aufrufe von Kontexthandles serialisiert. Eine Anwendung kann [**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) aufrufen, um dieses Standardverhalten zu überschreiben. Die Verwendung des [**\[ \_ \] Kontexthandleattributs**](context-handle.md) in einer ACF-Datei garantiert, dass Aufrufe für dieses bestimmte Kontexthandle unabhängig vom Verhalten der aufrufenden Anwendung nicht serialisiert werden. Das Bereitstellen einer Kontext-Rundownroutine ist optional.

Dieses Attribut ist in MIDL Version 5.0 verfügbar.

**Windows Server 2003 und Windows XP oder höher:** Eine einzelne Schnittstelle kann sowohl serialisierte als auch nicht serialisierte Kontexthandles aufnehmen, sodass eine Methode einer Schnittstelle ausschließlich auf ein Kontexthandle zugreifen kann (serialisiert), während andere Methoden im freigegebenen Modus (nicht serialisiert) auf dieses Kontexthandle zugreifen. Diese Zugriffsfunktionen sind vergleichbar mit Lese-/Schreibsperrmechanismen. -Methoden, die ein serialisiertes Kontexthandle verwenden, sind exklusive Benutzer (Writer), während Methoden, die ein nicht serialisiertes Kontexthandle verwenden, freigegebene Benutzer (Reader) sind. Methoden, die den Zustand eines Kontexthandle zerstören oder ändern, müssen serialisiert werden. Methoden, die den Zustand eines Kontexthandles nicht ändern, z. B. Methoden, die einfach aus einem Kontexthandle lesen, können nicht deserialisiert werden. Beachten Sie, dass Erstellungsmethoden implizit serialisiert werden.

## <a name="examples"></a>Beispiele

``` syntax
typedef [context_handle_noserialize] PCONTEXT_HANDLE_TYPE; 
HRESULT RemoteFunc([context_handle_noserialize] pCxHandle);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ACF-Attribute](acf-attributes.md)
</dt> <dt>

[**\_Kontexthandle \_ serialisieren**](context-handle-serialize.md)
</dt> <dt>

[**\_Kontexthandle**](context-handle.md)
</dt> <dt>

[Kontexthandles](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext)
</dt> <dt>

[Run-down-Routine für Serverkontext](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[Multithreadclients und Kontexthandles](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> </dl>

 

 