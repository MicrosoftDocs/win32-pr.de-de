---
title: Implizite Bindungs Handles
description: Implizite Bindungs Handles ermöglichen der Anwendung, einen bestimmten Server für die Ausführung der Remote Prozedur Aufrufe auszuwählen.
ms.assetid: cf4e179b-8d97-4597-89e6-c8967b9db6c7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5fda8501224d66518ad2e86f13fb769c4b2fa0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039100"
---
# <a name="implicit-binding-handles"></a>Implizite Bindungs Handles

Implizite Bindungs Handles ermöglichen der Anwendung, einen bestimmten Server für die Ausführung der Remote Prozedur Aufrufe auszuwählen. Weitere Informationen finden Sie unter [Client seitige Bindung](client-side-binding.md). Außerdem können Sie mit dem Client/Server-Programm authentifizierte Bindungen verwenden. Das heißt, der Client kann Authentifizierungsinformationen in einem impliziten Bindungs Handle angeben. Die RPC-Lauf Zeit Bibliothek verwendet die Authentifizierungsinformationen, um eine authentifizierte RPC-Sitzung zwischen dem Client und dem Server einzurichten. Weitere Informationen finden Sie unter [Sicherheit](security.md).

> [!Note]  
> Implizite Bindungs Handles sind nicht Thread sicher. Multithreadanwendungen sollten daher die Verwendung impliziter Bindungs Handles vermeiden.

 

Wenn Ihre Anwendung implizite Bindungen verwendet, muss der Client die Bindungs Informationen so festlegen, dass die Bindung erstellt werden kann. Nachdem der Client eine implizite Bindung erstellt hat, muss er keine Bindungs Handles an Remote Prozeduren übergeben. Die RPC-Bibliothek behandelt die restlichen Mechanismen der Kommunikationssitzung.

Der Client speichert die Bindungs Informationen für ein implizites Handle in einer globalen Variablen. Wenn der Mittell-Compiler den Clientstub und die Header Datei aus der Schnittstellen Spezifikation in der mittleren l-Datei generiert, generiert er auch Code für eine globale Bindungs handle-Variable. Das Client Programm initialisiert das Handle und verweist erst wieder auf das Handle, wenn die Bindung zerstört wird.

Sie erstellen ein implizites handle, indem Sie das \[ [**implizite \_ handle**](/windows/desktop/Midl/implicit-handle) - \] Attribut in der ACF für eine Schnittstelle wie folgt angeben:

``` syntax
/* ACF file (complete) */
 
[
  implicit_handle(handle_t hHello)
]
interface hello
{
}
```

Der **handle \_ t** -Typ, der im vorherigen Beispiel verwendet wird, ist ein mittlerer Datentyp, der zum Definieren von Bindungs Handles verwendet wird.

Nachdem Sie das implizite Handle erstellt haben, muss es von der Anwendung als Parameter für die RPC-Lauf Zeit Bibliotheksfunktionen verwendet werden. Verwenden Sie das implizite Handle nicht als Parameter für Remote Prozedur Aufrufe. Im folgenden Codebeispiel wird die Verwendung impliziter Bindungs Handles veranschaulicht.

``` syntax
RPC_STATUS status;
status = RpcBindingFromStringBinding(
            pszStringBinding,
            &hHello);
 
status = MyRemoteProcedure();
 
status = RpcBindingFree(hHello);
...
```

Im vorherigen Beispiel mussten die RPC-Lauf Zeit Bibliotheksfunktionen [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) und [**rpcbindingfree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) den impliziten Bindungs Handle in ihren Parameterlisten übergeben. Bei der Remote Prozedur myremoteprocedure ist dies jedoch nicht der Fall, da es sich nicht um eine RPC-Lauf Zeit Bibliotheksfunktion handelt.

 

 