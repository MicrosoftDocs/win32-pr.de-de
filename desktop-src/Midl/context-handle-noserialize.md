---
title: context_handle_noserialize-Attribut
description: Das \ Context \_ handle \_ noserialize \ ACF-Attribut stellt sicher, dass ein Kontext Handle unabhängig vom Standardverhalten der Anwendung niemals serialisiert wird.
ms.assetid: aff2484e-639b-41d2-94a9-f34ca4f2343c
keywords:
- context_handle_noserialize Attribut-Mittel l
topic_type:
- apiref
api_name:
- context_handle_noserialize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1394f3f2a72837df5efa3b74bd2672e39c3c3b12
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724961"
---
# <a name="context_handle_noserialize-attribute"></a>Kontext \_ handle- \_ noserialize-Attribut

Das **\[ Kontext \_ \_ handle \]** -ACF-Attribut stellt sicher, dass ein Kontext Handle unabhängig vom Standardverhalten der Anwendung niemals serialisiert wird.

``` syntax
typedef [context_handle_noserialize [ , type-acf-attribute-list ] ] context-handle-type

[context_handle_noserialize [, function-acf-attribute-list ] ] function-name( );

function-name (   [context_handle_noserialize 
  [ , parameter-acf-attribute-list ] ] param-name );
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Type-ACF-Attribute-List* 
</dt> <dd>

Alle anderen ACF-Attribute, die auf den Typ angewendet werden.

</dd> <dt>

*Context-Handle-type* 
</dt> <dd>

Der Bezeichner, der den Typ des Kontext Handles angibt, wie in einer [**typedef**](typedef.md) -Deklaration definiert. Dies ist der Typ, der das [**\[ Kontext \_ handle \]**](context-handle.md) -Attribut in der IDL-Datei empfängt.

</dd> <dt>

*Function-ACF-Attribute-List* 
</dt> <dd>

Alle zusätzlichen ACF-Attribute, die auf die Funktion angewendet werden.

</dd> <dt>

*function-name* 
</dt> <dd>

Der Name der Funktion, wie in der IDL-Datei definiert.

</dd> <dt>

*Parameter-ACF-Attribute-List* 
</dt> <dd>

Alle anderen ACF-Attribute, die auf den-Parameter angewendet werden.

</dd> <dt>

*Param-Name* 
</dt> <dd>

Der Name des Parameters, wie er in der IDL-Datei definiert ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das [**\[ Kontext \_ handle \]**](context-handle.md) -Attribut identifiziert ein Bindungs handle, das Kontext-oder Zustandsinformationen auf dem Server zwischen Remote Prozedur aufrufen verwaltet. Das Attribut kann als IDL [**typedef**](typedef.md) Type-Attribut, als Funktions Rückgabetyp Attribut oder als Parameter Attribut angezeigt werden.

Standardmäßig werden Aufrufe für Kontext Handles serialisiert. Eine Anwendung kann [**rpcssdontserializecontext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) aufgerufen werden, um dieses Standardverhalten zu überschreiben. Durch die Verwendung des [**\[ Kontext \_ handle \]**](context-handle.md) -Attributs in einer ACF-Datei wird sichergestellt, dass Aufrufe für dieses Kontext Handle unabhängig vom Verhalten der aufrufenden Anwendung nicht serialisiert werden. Das Bereitstellen einer Kontext-Rundown-Routine ist optional.

Dieses Attribut ist in der mittleren l-Version 5,0 verfügbar.

**Windows Server 2003 und Windows XP oder höher:** Eine einzelne Schnittstelle kann sowohl serialisierte als auch nicht serialisierte Kontext Handles aufnehmen, sodass eine Methode in einer Schnittstelle ausschließlich auf ein Kontext Handle (serialisiert) zugreifen kann, während andere Methoden auf dieses Kontext Handle im freigegebenen Modus zugreifen (nicht serialisiert). Diese Zugriffs Funktionen sind mit Lese-/schreibsperrungs-Mechanismen vergleichbar. Methoden, die ein serialisiertes Kontext Handle verwenden, sind exklusive Benutzer (Writer), während Methoden, die ein nicht serialisiertes Kontext Handle verwenden, freigegebene Benutzer (Reader) sind. Methoden, die den Zustand eines Kontext Handles zerstören oder ändern, müssen serialisiert werden. Methoden, die den Zustand eines Kontext Handles nicht ändern, wie z. b. die Methoden, die einfach aus einem Kontext Handle lesen, können nicht serialisiert werden. Beachten Sie, dass Erstellungs Methoden implizit serialisiert werden.

## <a name="examples"></a>Beispiele

``` syntax
typedef [context_handle_noserialize] PCONTEXT_HANDLE_TYPE; 
HRESULT RemoteFunc([context_handle_noserialize] pCxHandle);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ACF-Attribute](acf-attributes.md)
</dt> <dt>

[**Kontext \_ handle- \_ Serialisierung**](context-handle-serialize.md)
</dt> <dt>

[**Kontext \_ handle**](context-handle.md)
</dt> <dt>

[Kontext Handles](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[**Rpcssdontserializecontext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext)
</dt> <dt>

[Server Kontext-Lauf-ab-Routine](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[Multithread-Clients und Kontext Handles](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 