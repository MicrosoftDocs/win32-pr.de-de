---
title: Primitive und benutzerdefinierte Bindungs Handles
description: Alle Handles, die mit den Handle \_ t-oder RPC- \_ Bindungs handle-Typen deklariert werden, \_ sind primitive Bindungs Handles.
ms.assetid: 7a948aad-02fa-421d-b32c-f5dab071bd04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d496a9a54ba0ee7b9552326f7c4dc15792a72bce
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039491"
---
# <a name="primitive-and-custom-binding-handles"></a>Primitive und benutzerdefinierte Bindungs Handles

Alle Handles, die mit den [handle \_ t](/windows/desktop/Midl/handle-t) -oder [**RPC- \_ Bindungs \_ handle**](rpc-binding-handle.md) -Typen deklariert werden, sind primitive Bindungs Handles. Sie können die [handle \_ t](/windows/desktop/Midl/handle-t) -oder [**RPC- \_ Bindungs \_ handle**](rpc-binding-handle.md) -Typen so erweitern, dass mehr oder andere Informationen als der primitive Handle-Typ enthalten sind. Wenn Sie dies tun, erstellen Sie ein benutzerdefiniertes Bindungs handle.

Um ein benutzerdefiniertes Bindungs Handle für Ihre verteilte Anwendung zu erstellen, müssen Sie einen eigenen Datentyp erstellen und das \[ [handle](/windows/desktop/Midl/handle) - \] Attribut für eine Typdefinition in der IDL-Datei angeben. Letztendlich ordnen die Stub-Dateien primitive Handles benutzerdefinierte Bindungs Handles zu.

Wenn Sie einen eigenen Bindungs Handle-Typ erstellen, müssen Sie auch Bindungs-und Bindung-Routinen bereitstellen, die der Clientstub verwendet, um ein benutzerdefiniertes Handle einem primitiven handle zuzuordnen. Der Stub Ruft die BIND-und Bindung-Routinen am Anfang und am Ende jedes Remote Prozedur Aufrufs auf. Die Bindungs-und Bindung-Routinen müssen den folgenden Funktionsprototypen entsprechen.



| Funktionsprototyp                     | BESCHREIBUNG       |
|----------------------------------------|-------------------|
| Handle \_ t- \_ Typbindung (*Typ*)           | Bindungs Routine   |
| void Type \_ Unbind (*Type*, *handle \_ t*) | Bindung der Routine aufheben |



 

Im folgenden Beispiel wird gezeigt, wie ein benutzerdefiniertes Bindungs Handle in der IDL-Datei definiert werden kann:

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

Wenn die Bindungs Routine einen Fehler feststellt, sollte Sie mithilfe der [**rpcraiseexception**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) -Funktion eine Ausnahme auslöst. Der Clientstub wird dann bereinigt, und die Ausnahme wird durch den Ausnahme Block für den Remote Prozedur Aufrufe auf der Clientseite gefiltert. Wenn die Bindungs Routine einfach **null** zurückgibt, wird der Client Code Fehler-RPC \_ S \_ ungültige \_ Bindung erhalten. Dies kann in bestimmten Situationen akzeptabel sein, aber andere Situationen (z. b. nicht genügend Arbeitsspeicher) Antworten nicht gut. Die Bindung-Routine sollte so entworfen werden, dass Sie nicht fehlschlägt. Die Bindung-Routine sollte keine Ausnahmen ausgelöst werden.

Die vom Programmierer definierten Bindungs-und Bindung-Routinen werden in der Client Anwendung angezeigt. Im folgenden Beispiel ruft die BIND-Routine [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) auf, um die Zeichen folgen Bindungs Informationen in ein Bindungs Handle zu konvertieren. Die Bindung-Routine ruft [**rpcbindingfree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) auf, um das Bindungs Handle freizugeben.

Der Name des vom Programmierer definierten Bindungs Handles, Daten \_ handle \_ Type, wird als Teil des Namens der Funktionen angezeigt. Sie wird auch als Parametertyp in den Funktionsparametern verwendet.

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

Sowohl implizite als auch explizite Bindungs Handles können primitive oder benutzerdefinierte Handles sein. Das heißt, ein Handle kann sein:

-   Primitiv und implizit
-   Benutzer definiert und implizit
-   Primitiv und explizit
-   Benutzer definiert und explizit

 

 