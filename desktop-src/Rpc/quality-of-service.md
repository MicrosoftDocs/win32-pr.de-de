---
title: Quality of Service (RPC)
description: Clientprogramme können die RpcBindingSetAuthInfoEx-Funktion anstelle der RpcBindingSetAuthInfo-Funktion verwenden, um eine authentifizierte Bindung zu erstellen.
ms.assetid: bc3d47ba-3c1b-4aba-8fe3-b4501a621931
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d7c68386a5d7db4f59b620bc998d628faa2969671ef99b5c5fc2c65aadeb96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927148"
---
# <a name="quality-of-service-rpc"></a>Quality of Service (RPC)

Clientprogramme können die [**RpcBindingSetAuthInfoEx-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) anstelle der [**RpcBindingSetAuthInfo-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) verwenden, um eine authentifizierte Bindung zu erstellen. Wenn sie dies tun, übergeben sie einen Zeiger auf eine [**RPC \_ SECURITY \_ QOS-Struktur**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_security_qos) als letzten Parameter von **RpcBindingSetAuthInfoEx.** Diese Struktur enthält Informationen zur Dienstqualität. Clientprogramme können auch die Identitätsnachverfolgung angeben und den Identitätswechseltyp auswählen.

Verwenden Sie das **Capabilities-Element** der [**RPC SECURITY \_ \_ QOS-Struktur,**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_security_qos) um festzulegen, welche Teile der Client-/Serveranwendung authentifiziert werden. Wenn RPC \_ C \_ QOS \_ CAPABILITIES DEFAULT ausgewählt \_ ist, authentifiziert die RPC-Laufzeitbibliothek den Client oder Server gemäß der Standardeinstellung für den SSP. Standardmäßig authentifiziert der Kerberos-Protokoll-SSP sowohl den Client als auch den Server. Die Standardeinstellung für alle anderen von Microsoft zur Verfügung gestellten SSPs ist die Authentifizierung des Clients beim Server, aber nicht die Authentifizierung des Servers beim Client.

Wenn sich client und server immer gegenseitig authentifizieren sollen, legen Sie den **Capabilities-Member** der [**RPC SECURITY \_ \_ QOS-Struktur**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_security_qos) auf RPC \_ C \_ QOS CAPABILITIES MUTUAL \_ \_ \_ AUTH fest. Einige Sicherheitsanbieter unterstützen möglicherweise keine gegenseitige Authentifizierung. Wenn RPC \_ C \_ QOS \_ CAPABILITIES MUTUAL \_ \_ AUTH für solche Sicherheitsanbieter angegeben wird, wird beim Aufrufen einer Remoteprozedur ein Fehler zurückgegeben. Wenn Sie den SCHANNEL-SSP verwenden, können Sie auch den **Capabilities-Member** auf RPC \_ C \_ QOS \_ CAPABILITIES ANY \_ \_ AUTHORITY festlegen. Diese Konstante gibt an, dass der SSP den Remoteprozeduraufruf auch dann überprüfen soll, wenn sich die Zertifizierungsstelle, die das Authentifizierungszertifikat des Clients ausgestellt hat, nicht im Stammzertifikatspeicher des SSP befindet. Standardmäßig wird das Zertifikat abgelehnt, wenn der SSP die Zertifizierungsstelle nicht erkennt. Die Zertifizierungsstelle ist ein unabhängiges Unternehmen oder eine unabhängige Organisation, z. B. VeriSign, das Authentifizierungszertifikate ausstellt.

Anwendungen können auch die Identitätsnachverfolgung festlegen, die von der RPC-Laufzeitbibliothek verwendet wird. Programme verwenden im Allgemeinen [*die statische Identitätsnachverfolgung.*](s-glos.md) Bei der statischen Nachverfolgung werden die Anmeldeinformationen des Clients festgelegt, wenn die [**RpcBindingSetAuthInfo-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) aufgerufen wird. Die RPC-Laufzeitbibliothek verwendet diese Anmeldeinformationen dann für alle RPC-Aufrufe der Bindung, unabhängig von Änderungen an der Identität des aufrufenden Threads oder des aufrufenden Prozesses. Anwendungen können auch [*dynamische Identitätsnachverfolgung*](d-glos.md)auswählen. Die dynamische Identitätsnachverfolgung weist die RPC-Laufzeitbibliothek an, die Anmeldeinformationen des aufrufenden Threads zum Zeitpunkt jedes Aufrufs anstelle des Bindungshandle zu verwenden. Die Standardidentitätsnachverfolgung ist statisch.

Wenn sich die Identität des Clients nicht ändert, kann die statische Identitätsnachverfolgung bessere Leistungsmerkmale aufweisen und die RPC-Laufzeit daran hindern, jedes Mal zu überprüfen, ob die Identität im aufrufenden Thread mit der identität für das Sicherheitssystem identisch ist. Wenn sich die Identität des aufrufenden Threads zwischen Aufrufen ändern kann und der Server diese Änderungen erkennen muss, empfiehlt es sich, die dynamische Identitätsnachverfolgung anzugeben. Die RPC-Laufzeit verfolgt die Identität für Sie still und effizient nach, und wenn sich die Identität ändert, wird diese Änderung in Ihrem Namen verwaltet.

> [!Note]  
> Bei **ncalrpc-Aufrufen** weist die statische und dynamische Identitätsnachverfolgung unterschiedliche Leistungsmerkmale auf und kann je nach Den Umständen schneller sein.

 

Im Rahmen der QOS-Spezifikation kann das Clientprogramm auch den Typ des Identitätswechsels festlegen, den ein Serverprogramm in seinem Namen ausführen kann. Weitere Informationen finden Sie unter [Clientidentitätswechsel.](client-impersonation.md)

Das Feld Versionsnummer der [**RPC \_ SECURITY \_ QOS-Struktur**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_security_qos) sollte immer auf RPC C SECURITY QOS VERSION festgelegt \_ \_ \_ \_ werden.

 

 




