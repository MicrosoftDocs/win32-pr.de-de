---
title: Handle-Attribut
description: Das \ handle \-Attribut gibt eine benutzerdefinierte oder \ 0034; angepasste \ 0034; an. behandlertyp.
ms.assetid: db5c6ea6-6081-4cea-9265-5e2f67fd8c14
keywords:
- Handle-Attribut-Mittel l
topic_type:
- apiref
api_name:
- handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d4560de53bf3f24238e9ff96e01c74716729749
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858252"
---
# <a name="handle-attribute"></a>Handle-Attribut

Das \[ **handle** - \] Attribut gibt einen benutzerdefinierten oder "angepassten" Handlertyp an.

``` syntax
typedef [handle] typename;  
handle_t __RPC_USER typename_bind (typename);
void __RPC_USER typename_unbind (typename, handle_t);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*typeName* 
</dt> <dd>

Gibt den Namen des benutzerdefinierten Bindungs Handle Typs an.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Benutzerdefinierte Handles ermöglichen Entwicklern das Entwerfen von Handles, die für die Anwendung von Bedeutung sind. Ein benutzerdefiniertes Handle kann nur in einer Typdeklaration definiert werden, nicht in einem funktionsdeklarator.

Ein Parameter eines Typs, der durch das \[ **handle** \] -Attribut definiert wird, wird verwendet, um die Bindung für den Aufruf zu bestimmen und wird an die aufgerufene Prozedur übertragen.

Der Benutzer muss Bindungs-und unbindungs Routinen bereitstellen, um zwischen primitiven und benutzerdefinierten handle-Typen zu konvertieren. Wenn ein benutzerdefiniertes Handle des Typs *Typname* angegeben ist, muss der Benutzer die Routinen *tykame* \_ **Bind** und *tykame* \_ **Bindung** angeben. Wenn z. b. der benutzerdefinierte Handlertyp myhandle lautet, werden die Routinen mit myhandle \_ **Bind** und myhandle \_ **Bindung** benannt.

Wenn der Vorgang erfolgreich ist, sollte die Bindungs Routine *Typname* \_  ein gültiges Primitives Bindungs Handle zurückgeben. Wenn nicht erfolgreich, sollte die Routine einen **null**-Wert zurückgeben. Wenn die Routine **null** zurückgibt, wird die Bindung-Routine von *typame* \_  nicht aufgerufen. Wenn die Bindungs Routine ein ungültiges Bindungs handle zurückgibt, das nicht **null** ist, ist das stubverhalten nicht definiert.

Wenn die Remote Prozedur ein benutzerdefiniertes Handle als Parameter oder als implizites handle aufweist, rufen die Client-stubdie Bindungs Routine auf, bevor Sie die Remote Prozedur aufrufen. Die Client-stubzeichen nennen die aufheben-Routine nach dem Remote-Befehl.

In DCE IDL muss ein Parameter mit dem \[ **handle** - \] Attribut als erster Parameter in der Liste der Remote Prozedur Argumente angezeigt werden. Nachfolgende Parameter, einschließlich anderer \[ **handle** - \] Attribute, werden als normale Parameter behandelt. Microsoft unterstützt eine Erweiterung der DCE-IDL, die es ermöglicht, dass der benutzerdefinierte \[ **handle** - \] Parameter in anderen Positionen als dem ersten Parameter angezeigt wird.

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

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**implizites \_ handle**](implicit-handle.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 