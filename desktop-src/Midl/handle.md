---
title: handle-Attribut
description: Das \handle\-Attribut gibt ein benutzerdefiniertes oder \0034;angepasstes \ 0034; an. handle-Typ.
ms.assetid: db5c6ea6-6081-4cea-9265-5e2f67fd8c14
keywords:
- Handleattribut MIDL
topic_type:
- apiref
api_name:
- handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aacdb3611a12873a6e828c33606bb9c970747555c285f8612be2b43bc3f51adf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895290"
---
# <a name="handle-attribute"></a>handle-Attribut

Das \[  \] Handleattribut gibt einen benutzerdefinierten oder "angepassten" Handletyp an.

``` syntax
typedef [handle] typename;  
handle_t __RPC_USER typename_bind (typename);
void __RPC_USER typename_unbind (typename, handle_t);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Typename* 
</dt> <dd>

Gibt den Namen des benutzerdefinierten Bindungshandletyps an.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Benutzerdefinierte Handles ermöglichen Entwicklern das Entwerfen von Handles, die für die Anwendung von Bedeutung sind. Ein benutzerdefiniertes Handle kann nur in einer Typdeklaration definiert werden, nicht in einem Funktionsdeklarator.

Ein Parameter eines vom Handleattribut definierten Typs \[  \] wird verwendet, um die Bindung für den Aufruf zu bestimmen, und wird an die aufgerufene Prozedur übertragen.

Der Benutzer muss Bindungs- und Bindungsroutinen bereitstellen, um zwischen primitiven und benutzerdefinierten Handletypen zu konvertieren. Bei einem benutzerdefinierten Handle vom Typ *typname* muss der Benutzer die Routinen *typename* \_ **bind** und *typename* \_ **unbind** bereitstellen. Wenn der benutzerdefinierte Handletyp z. B. MYHANDLE heißt, heißen die Routinen MYHANDLE \_ **bind** und MYHANDLE \_ **unbind**.

Bei Erfolg sollte die *Bindungsroutine typename* \_  ein gültiges primitives Bindungshandle zurückgeben. Wenn dies nicht erfolgreich ist, sollte die Routine einen **NULL-Wert** zurückgeben. Wenn die Routine **NULL** zurückgibt, wird die  \_ **Unbind-Routine** typename nicht aufgerufen. Wenn die Bindungsroutine ein ungültiges Bindungshandle zurückgibt, das sich von **NULL** unterscheidet, ist das Stubverhalten nicht definiert.

Wenn die Remoteprozedur über ein benutzerdefiniertes Handle als Parameter oder als implizites Handle verfügt, rufen die Clientstubs die Bindungsroutine auf, bevor sie die Remoteprozedur aufrufen. Die Clientstubs rufen die Bindungsroutine nach dem Remoteaufruf auf.

In DCE IDL muss ein Parameter mit dem \[ **handle-Attribut** \] als erster Parameter in der Argumentliste der Remoteprozedur angezeigt werden. Nachfolgende Parameter, einschließlich anderer \[  \] Handleattribute, werden als normale Parameter behandelt. Microsoft unterstützt eine Erweiterung für DCE IDL, mit der der benutzerdefinierte \[ **Handleparameter** \] an anderen Positionen als dem ersten Parameter angezeigt werden kann.

## <a name="examples"></a>Beispiele

``` syntax
typedef [handle] struct 
{ 
    char machine[8]; 
    char nmpipe[256]; 
} h_service; 
 
handle_t __RPC_USER h_service_bind(h_service); 
void __RPC_USER h_service_unbind(h_service, handle_t);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Bindung und Handles](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> <dt>

[**Implizites \_ Handle**](implicit-handle.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> </dl>

 

 