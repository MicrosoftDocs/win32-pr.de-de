---
title: Implizite Bindungshandles
description: Implizite Bindungshandles ermöglichen es Ihrer Anwendung, einen bestimmten Server auszuwählen, um ihre Remoteprozeduraufrufe auszuführen.
ms.assetid: cf4e179b-8d97-4597-89e6-c8967b9db6c7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d49618ec505cc776c346a504fb19b65db539dadb90d030e45efbabcf08371db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929075"
---
# <a name="implicit-binding-handles"></a>Implizite Bindungshandles

Implizite Bindungshandles ermöglichen es Ihrer Anwendung, einen bestimmten Server auszuwählen, um ihre Remoteprozeduraufrufe auszuführen. Weitere Informationen finden Sie unter [Clientseitige Bindung.](client-side-binding.md) Sie ermöglichen ihrem Client-/Serverprogramm auch die Verwendung authentifizierter Bindungen. Das heißt, der Client kann Authentifizierungsinformationen in einem impliziten Bindungshand handle angeben. Die RPC-Laufzeitbibliothek verwendet die Authentifizierungsinformationen, um eine authentifizierte RPC-Sitzung zwischen dem Client und dem Server herzustellen. Weitere Informationen finden Sie unter [Sicherheit](security.md).

> [!Note]  
> Implizite Bindungshandles sind nicht threadsicher. Multithreadanwendungen sollten daher die Verwendung impliziter Bindungshandles vermeiden.

 

Wenn ihre Anwendung implizite Bindungen verwendet, muss der Client die Bindungsinformationen festlegen, damit er die Bindung erstellen kann. Nachdem der Client eine implizite Bindung erstellt hat, muss er keine Bindungshandles an Remoteverfahren übergeben. Die RPC-Bibliothek übernimmt die restlichen Mechanismen der Kommunikationssitzung.

Der Client speichert die Bindungsinformationen für ein implizites Handle in einer globalen Variablen. Wenn der MIDL-Compiler den Clientstub und die Headerdatei aus der Schnittstellenspezifikation in Ihrer MIDL-Datei generiert, generiert er auch Code für eine globale Bindungshandlevariable. Ihr Clientprogramm initialisiert das Handle und bezieht sich erst dann erneut darauf, wenn es die Bindung zerstört.

Sie erstellen ein implizites Handle, indem Sie das implizite Handleattribut \[ [**\_**](/windows/desktop/Midl/implicit-handle) \] im ACF für eine Schnittstelle wie folgt angeben:

``` syntax
/* ACF file (complete) */
 
[
  implicit_handle(handle_t hHello)
]
interface hello
{
}
```

Der **\_ T-Handletyp,** der im vorherigen Beispiel verwendet wird, ist ein MIDL-Datentyp, der zum Definieren von Bindungshandles verwendet wird.

Nach dem Erstellen des impliziten Handles muss die Anwendung es als Parameter für die RPC-Laufzeitbibliotheksfunktionen verwenden. Verwenden Sie das implizite Handle nicht als Parameter für Remoteprozeduraufrufe. Im folgenden Codebeispiel wird die Verwendung impliziter Bindungshandles veranschaulicht.

``` syntax
RPC_STATUS status;
status = RpcBindingFromStringBinding(
            pszStringBinding,
            &hHello);
 
status = MyRemoteProcedure();
 
status = RpcBindingFree(hHello);
...
```

Im vorherigen Beispiel erforderten die RPC-Laufzeitbibliotheksfunktionen [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) und [**RpcBindingFree,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) dass das implizite Bindungshand handle in ihren Parameterlisten übergeben werden musste. Die Remoteprozedur MyRemoteProcedure hat dies jedoch nicht getan, da es sich nicht um eine RPC-Laufzeitbibliotheksfunktion handelt.

 

 