---
title: Auswählen von QOS-Sicherheitsoptionen
description: Die QOS-Sicherheitsoptionen werden als Teil des SecurityQOS-Parameters übergeben, der an die RpcBindingSetAuthInfoEx-Funktion übergeben wird. Verwenden Sie die folgenden bewährten Methoden.
ms.assetid: 43befe3d-079a-4389-a1ff-6bda90935769
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44c943fd9e2b4104de87a24c6078499fa38acdf1b6d1ea2122bf9d3063cd80f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932196"
---
# <a name="choosing-security-qos-options"></a>Auswählen von QOS-Sicherheitsoptionen

Die QOS-Sicherheitsoptionen werden als Teil des *SecurityQOS-Parameters* übergeben, der an die [**RpcBindingSetAuthInfoEx-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) übergeben wird. Verwenden Sie die folgenden bewährten Methoden.

## <a name="use-mutual-authentication"></a>Verwenden der gegenseitigen Authentifizierung

Die echte gegenseitige Authentifizierung ist nur für bestimmte Sicherheitsanbieter verfügbar: Aushandeln (beim Aushandeln von Kerberos), Kerberos und Schannel. NTLM unterstützt keine gegenseitige Authentifizierung. Die Verwendung der gegenseitigen Authentifizierung erfordert, dass ein wohlgeformte Serverprinzipalname angegeben wird. Viele Entwickler verwenden die folgende fehlerhafte Sicherheitsmethode: Der Server wird aufgerufen, um nach seinem Prinzipalnamen [**(RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname)) zu fragen, und dann wird blind nach gegenseitiger Authentifizierung mit diesem Prinzipalnamen gefragt. Dieser Ansatz unterbricht die gesamte Idee der gegenseitigen Authentifizierung. Die Idee der gegenseitigen Authentifizierung besteht darin, dass nur bestimmte Server aufgerufen werden, da sie als vertrauenswürdig eingestuft werden, um Ihre Daten zu analysieren und zu verarbeiten. Mithilfe der soeben beschriebenen fehlerhaften Sicherheitsmaßnahmen geben Entwickler ihre Daten an alle Benutzer weiter, die intelligent genug sind, um ihren Namen zurückzugeben.

Wenn die Clientsoftware beispielsweise nur einen Server aufrufen soll, der unter den Konten von Joe, Pete oder Alice ausgeführt wird, sollte die [**RpcMgmtInqServerPrincName-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname) aufgerufen und der zurückgesendete Name überprüft werden. Wenn es sich um Joe, Pete oder Alice handelt, sollte die gegenseitige Authentifizierung mit dem Serverprinzipalnamen angefordert werden. Dadurch wird sichergestellt, dass beide Hälften der Konversation an denselben Prinzipal gehen.

Wenn die Clientsoftware einen Dienst aufrufen soll, der nur unter dem Konto von Joe ausgeführt wird, erstellen Sie den Serverprinzipalnamen von Joe direkt, und führen Sie den Aufruf aus. Wenn der Server nicht Joe ist, schlägt der Aufruf einfach fehl.

Häufig werden Dienste als Windows Systemdienste ausgeführt, was bedeutet, dass sie unter dem Computerkonto ausgeführt werden. Die gegenseitige Authentifizierung und Erstellung eines Serverprinzipalnamens wird weiterhin empfohlen.

## <a name="use-the-lowest-impersonationtype-that-allows-the-call-to-go-through"></a>Verwenden Sie den niedrigsten Identitätswechseltyp, der dem Aufruf das Durchlaufen ermöglicht.

Diese bewährte Methode ist relativ selbsterklärend. Auch wenn die gegenseitige Authentifizierung verwendet wird, erteilen Sie dem Server nicht mehr Rechte als nötig. Ein legitimer Server wurde möglicherweise kompromittiert, und obwohl die von Ihnen gesendeten Daten in solchen Fällen in die falschen Hände fallen, kann zumindest der Server nicht in Ihrem Namen auf andere Daten im Netzwerk zugreifen. Einige Server lehnt einen Aufruf ab, der nicht über ausreichende Informationen verfügt, um den Aufrufer zu bestimmen und möglicherweise die Identität zu annehmen. Beachten Sie außerdem, dass einige Protokollsequenzen die Sicherheit auf Transportebene unterstützen ([**ncacn \_ np**](/windows/desktop/Midl/ncacn-np) und [**ncalrpc**](/windows/desktop/Midl/ncalrpc)). In solchen Fällen kann der Server immer die Identität von Ihnen annehmen, wenn Sie beim Erstellen des Bindungshandle über den *Parameter NetworkOptions* eine ausreichend hohe Identitätswechselebene angeben.

Schließlich können einige Sicherheitsanbieter oder Transporte impersonationType transparent auf eine höhere Ebene als die angegebene erhöhen. Stellen Sie beim Entwickeln eines Programms sicher, dass Sie versuchen, Aufrufe mit dem beabsichtigten ImpersonationType-Wert vorzunehmen, und überprüfen Sie, ob sie auf dem Server einen höheren ImpersonationType-Wert erhalten.

 

 