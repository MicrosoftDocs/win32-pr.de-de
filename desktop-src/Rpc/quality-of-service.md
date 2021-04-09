---
title: Quality of Service (RPC)
description: Client Programme können die Funktion rpcbindingsetauthinfoex anstelle der rpcbindingsetauthinfo-Funktion verwenden, um eine authentifizierte Bindung zu erstellen.
ms.assetid: bc3d47ba-3c1b-4aba-8fe3-b4501a621931
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee93b1aa376c9d6f4e2b3eedab73c91471d42498
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103858591"
---
# <a name="quality-of-service-rpc"></a>Quality of Service (RPC)

Client Programme können die Funktion [**rpcbindingsetauthinfoex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) anstelle der [**rpcbindingsetauthinfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) -Funktion verwenden, um eine authentifizierte Bindung zu erstellen. Wenn dies der Fall ist, übergeben Sie einen Zeiger auf eine [**RPC- \_ Sicherheits- \_ QoS**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_security_qos) -Struktur als letzten Parameter von **rpcbindingsetauthinfoex**. Diese Struktur enthält Informationen über die Quality of Service. Client Programme können auch die Identitäts Überwachung angeben und den Identitätswechsel auswählen.

Verwenden Sie das Element **Funktionen** der [**RPC- \_ Sicherheits- \_ QoS**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_security_qos) -Struktur, um festzulegen, welche Teile der Client/Server-Anwendung authentifiziert werden. Wenn die RPC- \_ C \_ -QoS- \_ Funktionen \_ standardmäßig ausgewählt ist, wird der Client oder Server von der RPC-Lauf Zeit Bibliothek entsprechend der Standardeinstellung für den SSP authentifiziert. Standardmäßig authentifiziert der Kerberos-Protokoll-SSP sowohl den Client als auch den Server. Der Standardwert für alle anderen SSPs, die Microsoft bereitstellt, ist die Authentifizierung des Clients beim Server, aber nicht der Authentifizieren des Servers für den Client.

Wenn sich der Client und der Server immer untereinander authentifizieren sollen, legen Sie den **Funktions Mitglied der** [**RPC- \_ Sicherheits- \_ QoS**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_security_qos) -Struktur auf die gegenseitige Authentifizierung von RPC- \_ C- \_ QoS- \_ Funktionen fest \_ \_ . Einige Sicherheitsanbieter unterstützen möglicherweise keine gegenseitige Authentifizierung. Wenn \_ eine gegenseitige Authentifizierung der RPC-C- \_ QoS- \_ Funktionen \_ \_ für solche Sicherheitsanbieter festgelegt ist, wird beim Ausführen eines Remote Prozedur Aufrufs ein Fehler zurückgegeben. Bei der Verwendung des Schannel-SSP ist es möglich, auch das Element " **Funktionen** " auf RPC- \_ C- \_ QoS-Funktionen für beliebige Berechtigungen festzulegen \_ \_ \_ . Diese Konstante gibt an, dass der SSP den Remote Prozedur Rückruf überprüfen soll, auch wenn sich die Zertifizierungsstelle, die das Authentifizierungszertifikat des Clients ausgestellt hat, nicht im Stamm Zertifikat Speicher des SSP befindet. Der Standardwert besteht darin, das Zertifikat abzulehnen, wenn der SSP die Zertifizierungsstelle nicht erkennt. Die Zertifizierungsstelle ist ein unabhängiges Unternehmen oder eine unabhängige Organisation, z. b. VeriSign, das Authentifizierungs Zertifikate ausgibt.

Anwendungen können auch die Identitäts Überwachung festlegen, die von der RPC-Lauf Zeit Bibliothek verwendet wird. Programme verwenden im Allgemeinen die [*statische Identitäts Überwachung*](s-glos.md). Bei der statischen Nachverfolgung werden die Anmelde Informationen des Clients festgelegt, wenn die [**rpcbindingsetauthinfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) -Funktion aufgerufen wird. Die RPC-Lauf Zeit Bibliothek verwendet dann diese Anmelde Informationen für alle RPC-Aufrufe der Bindung, unabhängig von Änderungen in der Identität des aufrufenden Threads oder des aufrufenden Prozesses. Anwendungen können auch [*dynamische Identitäts Nachverfolgung*](d-glos.md)auswählen. Die dynamische Identitäts Verfolgung weist die RPC-Lauf Zeit Bibliothek an, die Anmelde Informationen des aufrufenden Threads zum Zeitpunkt des Aufrufs zu verwenden, anstatt das Bindungs Handle zu verwenden. Die Standard-Identitäts Überwachung ist statisch.

Wenn die Identität des Clients nicht geändert wird, kann die statische Identitäts Überwachung bessere Leistungsmerkmale aufweisen und die RPC-Laufzeit aus der Überprüfung speichern, wenn die Identität des aufrufenden Threads mit der Identität des Sicherheitssystems übereinstimmt. Wenn die Identität des aufrufenden Threads zwischen den Aufrufen geändert werden kann und der Server diese Änderungen erkennen muss, empfiehlt es sich, die dynamische Identitäts Überwachung anzugeben – die RPC-Laufzeit wird in Echtzeit und effizient die Identität für Sie nachverfolgt. wenn sich die Identität ändert, verwaltet diese Änderung in Ihrem Namen.

> [!Note]  
> Bei **Ncalrpc** -aufrufen weisen die statische und dynamische Identitäts Verfolgung unterschiedliche Leistungsmerkmale auf. abhängig von den jeweiligen Umständen sind beide möglicherweise schneller.

 

Im Rahmen der QoS-Spezifikation kann das Client Programm auch den Typ des Identitäts Wechsels festlegen, der von einem Serverprogramm in seinem Auftrag durchgeführt werden kann. Weitere Informationen finden Sie unter [Client](client-impersonation.md)Identitätswechsel.

Das Feld Versionsnummer der [**RPC- \_ Sicherheits- \_ QoS**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_security_qos) -Struktur sollte immer auf RPC- \_ C-Sicherheits- \_ \_ QoS- \_ Version festgelegt sein.

 

 




