---
title: context_handle_serialize-Attribut
description: Das Attribut \ Kontext \_ handle \_ serialize \ ACF stellt sicher, dass ein Kontext Handle unabhängig vom Standardverhalten der Anwendung immer serialisiert wird.
ms.assetid: e2f48582-228a-4725-9543-1e638d86ff6b
keywords:
- context_handle_serialize Attribut-Mittel l
topic_type:
- apiref
api_name:
- context_handle_serialize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c74e364c3ae8bf0439e50ae53130542762f37484
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106340260"
---
# <a name="context_handle_serialize-attribute"></a>\_Attribut zum \_ Serialisieren des Kontext Handles

Das Kontext Handle-Attribut für die **\[ \_ \_ Serialisierung \]** von ACF stellt sicher, dass ein Kontext Handle unabhängig vom Standardverhalten der Anwendung immer serialisiert wird.

``` syntax
typedef [context_handle_serialize [ , type-acf-attribute-list ] ] context-handle-type;

[context_handle_serialize [, function-acf-attribute-list ] ] function-name( );

function-name(
    [context_handle_serialize [ , parameter-acf-attribute-list ] ] param-name );
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Type-ACF-Attribute-List* 
</dt> <dd>

Alle anderen ACF-Attribute, die auf den Typ angewendet werden.

</dd> <dt>

*Context-Handle-type* 
</dt> <dd>

Der Bezeichner, der den Typ des Kontext Handles angibt, wie in einer [**typedef**](typedef.md) -Deklaration definiert. Dies ist der Typ, der das **\[ \_ \_ serialisierungsattribut \] des Kontext Handles** in der IDL-Datei empfängt.

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

Das Attribut zum **\[ \_ \_ serialisieren \] des Kontext Handles** identifiziert ein Bindungs handle, das Kontext-oder Zustandsinformationen auf dem Server zwischen Remote Prozedur aufrufen verwaltet. Das Attribut kann als IDL [**typedef**](typedef.md) Type-Attribut, als Funktions Rückgabetyp Attribut oder als Parameter Attribut angezeigt werden.

Standardmäßig werden Aufrufe für Kontext Handles serialisiert, aber eine Anwendung kann [**rpcssdontserializecontext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) aufrufen, um dieses Standardverhalten zu überschreiben. Durch die Verwendung des **\[ Kontext \_ Handles \_ serialisieren \]** -Attributs in einer ACF-Datei wird sichergestellt, dass Aufrufe für dieses Kontext Handle serialisiert werden, auch wenn die aufrufende Anwendung die Standardserialisierung überschrieben hat. Eine Context-Rundown-Routine ist optional.

Dieses Attribut ist in der mittleren l-Version 5,0 verfügbar.

**Windows Server 2003 und Windows XP oder höher:** Eine einzelne Schnittstelle kann sowohl serialisierte als auch nicht serialisierte Kontext Handles aufnehmen, sodass eine Methode in einer Schnittstelle ausschließlich auf ein Kontext Handle (serialisiert) zugreifen kann, während andere Methoden auf dieses Kontext Handle im freigegebenen Modus zugreifen (nicht serialisiert). Diese Zugriffs Funktionen sind mit Lese-/schreibsperrungs-Mechanismen vergleichbar. Methoden, die ein serialisiertes Kontext Handle verwenden, sind exklusive Benutzer (Writer), während Methoden, die ein nicht serialisiertes Kontext Handle verwenden, freigegebene Benutzer (Reader) sind. Methoden, die den Zustand eines Kontext Handles zerstören oder ändern, müssen serialisiert werden. Methoden, die den Zustand eines Kontext Handles nicht ändern, wie z. b. die Methoden, die einfach aus einem Kontext Handle lesen, können nicht serialisiert werden. Beachten Sie, dass Erstellungs Methoden implizit serialisiert werden.

## <a name="examples"></a>Beispiele

``` syntax
typedef [context_handle_serialize] PCONTEXT_HANDLE_TYPE; 
HRESULT RemoteFunc([context_handle_serialize] pCxHandle);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Anwendungs Konfigurationsdatei (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[ACF-Attribute](acf-attributes.md)
</dt> <dt>

[**Kontext \_ handle \_ noserialize**](context-handle-noserialize.md)
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

 

 