---
title: Primitive und benutzerdefinierte Bindungshandles
description: Alle Handles, die mit dem Handle t- oder \_ RPC BINDING HANDLE-Typ deklariert \_ \_ werden, sind primitive Bindungshandles.
ms.assetid: 7a948aad-02fa-421d-b32c-f5dab071bd04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e0e1d6f7cc2ad4d11e268e0f5c83b0275fcd2677a32303820507272f550b834
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019150"
---
# <a name="primitive-and-custom-binding-handles"></a>Primitive und benutzerdefinierte Bindungshandles

Alle Handles, die mit dem Handle [ \_ t-](/windows/desktop/Midl/handle-t) oder [**RPC BINDING \_ \_ HANDLE-Typ deklariert**](rpc-binding-handle.md) werden, sind primitive Bindungshandles. Sie können die [ \_ Handletypen t](/windows/desktop/Midl/handle-t) oder [**RPC BINDING \_ \_ HANDLE**](rpc-binding-handle.md) so erweitern, dass sie mehr oder andere Informationen enthalten, als der primitive Handletyp enthält. Wenn Sie dies tun, erstellen Sie ein benutzerdefiniertes Bindungshand handle.

Um ein benutzerdefiniertes Bindungshandl für Ihre verteilte Anwendung zu erstellen, müssen Sie einen eigenen Datentyp erstellen und das Handleattribut für eine Typdefinition in Ihrer \[ [](/windows/desktop/Midl/handle) \] IDL-Datei angeben. Letztendlich ordnen die Stubdateien benutzerdefinierte Bindungshandles primitiven Handles zu.

Wenn Sie einen eigenen Bindungshandpunkttyp erstellen, müssen Sie auch Bindungs- und Bindungsaufbindungsroutinen verwenden, die der Clientstub verwendet, um einem primitiven Handle ein benutzerdefiniertes Handle zu zuordnen. Der Stub ruft die Bindungs- und Bindungsroutinen am Anfang und Ende jedes Remoteprozeduraufrufs auf. Die Bindungs- und Bindungsaufbindungsroutinen müssen den folgenden Funktionsprototypen entsprechen.



| Funktionsprototyp                     | Beschreibung       |
|----------------------------------------|-------------------|
| handle \_ t type \_ bind(*type*)           | Bindungsroutine   |
| void type \_ unbind(*type*, *handle \_ t*) | Entbindungsroutine |



 

Das folgende Beispiel zeigt, wie ein benutzerdefiniertes Bindungshandl in der IDL-Datei definiert werden kann:

``` syntax
/* usrdef.idl */
[
  uuid(20B309B1-015C-101A-B308-02608C4C9B53),
  version(1.0),
  pointer_default(unique)
]
interface usrdef
{
  typedef struct _DATA_TYPE 
  {
      unsigned char * pszUuid;
      unsigned char * pszProtocolSequence;
      unsigned char * pszNetworkAddress;
      unsigned char * pszEndpoint;
      unsigned char * pszOptions;
  } DATA_TYPE;
 
  typedef [handle] DATA_TYPE * DATA_HANDLE_TYPE;
  void UsrdefProc([in] DATA_HANDLE_TYPE  hBinding,
                  [in, string] unsigned char *   pszString);
 
  void Shutdown([in] DATA_HANDLE_TYPE hBinding);
}
```

Wenn die Bindungsroutine auf einen Fehler stößt, sollte sie mithilfe der [**RpcRerklärexception-Funktion eine Ausnahme**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) auslösen. Der Clientstub wird dann bereinigt und lässt die Ausnahme bis zum Ausnahmeblock filtern, der den Remoteprozeduraufruf auf clientseitiger Seite umhing. Wenn die Bindungsroutine einfach **NULL zurückgibt,** erhält der Clientcode den Fehler RPC \_ S INVALID \_ \_ BINDING. Dies kann in bestimmten Situationen akzeptabel sein, aber andere Situationen (z. B. nicht genügend Arbeitsspeicher) reagieren nicht gut. Die Unbind-Routine sollte so entworfen werden, dass sie nicht fehlschlägt. Die Unbind-Routine sollte keine Ausnahmen auslösen.

Die vom Programmierer definierten Bindungs- und Bindungsaufbindungsroutinen werden in der Clientanwendung angezeigt. Im folgenden Beispiel ruft die Bindungsroutine [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) auf, um die Zeichenfolgenbindungsinformationen in ein Bindungshand handle zu konvertieren. Die Unbind-Routine ruft [**RpcBindingFree auf,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) um das Bindungshand handle frei zu geben.

Der Name des vom Programmierer definierten Bindungshandrs DATA HANDLE TYPE wird als Teil des \_ \_ Namens der Funktionen angezeigt. Sie wird auch als Parametertyp in den Funktionsparametern verwendet.

``` syntax
/* The client stub calls this _bind routine at the */
/* beginning of each remote procedure call                */
 
RPC_BINDING_HANDLE __RPC_USER DATA_HANDLE_TYPE_bind(
    DATA_HANDLE_TYPE dh1)
{
    RPC_BINDING_HANDLE hBinding;
    RPC_STATUS status;
 
    unsigned char *pszStringBinding;
 
    status = RpcStringBindingCompose(
          dh1.pszUuid,
          dh1.pszProtocolSequence,
          dh1.pszNetworkAddress,
          dh1.pszEndpoint,
          dh1.pszOptions,
          &pszStringBinding);
          ...
 
    status = RpcBindingFromStringBinding(
          pszStringBinding,
          &hBinding);
          ...
 
    status = RpcStringFree(&pszStringBinding); 
    ...
 
    return(hBinding);
}
 
/* The client stub calls this _unbind routine */
/* after each remote procedure call.                            */
void __RPC_USER DATA_HANDLE_TYPE_unbind(
    DATA_HANDLE_TYPE dh1, 
    RPC_BINDING_HANDLE h1)
{
    RPC_STATUS status;
    status = RpcBindingFree(&h1); 
    ...
}
```

Sowohl implizite als auch explizite Bindungshandles können primitive oder benutzerdefinierte Handles sein. Das heißt, ein Handle kann folgendes sein:

-   Primitiv und implizit
-   Benutzerdefiniert und implizit
-   Primitiv und explizit
-   Benutzerdefiniert und explizit

 

 