---
title: Auswählen von Sicherheits-QoS-Optionen
description: Die sicherheitsqos-Optionen werden als Teil des securityqos-Parameters übergeben, der an die rpcbindingsetauthinfoex-Funktion übergeben wird. Verwenden Sie die folgenden bewährten Methoden.
ms.assetid: 43befe3d-079a-4389-a1ff-6bda90935769
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c286b516438eae78117ef8d73939c3b4bed396d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341961"
---
# <a name="choosing-security-qos-options"></a>Auswählen von Sicherheits-QoS-Optionen

Die sicherheitsqos-Optionen werden als Teil des *securityqos* -Parameters übergeben, der an die [**rpcbindingsetauthinfoex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) -Funktion übergeben wird. Verwenden Sie die folgenden bewährten Methoden.

## <a name="use-mutual-authentication"></a>Gegenseitige Authentifizierung verwenden

Die echte gegenseitige Authentifizierung ist nur für bestimmte Sicherheitsanbieter verfügbar: Aushandeln (bei Aushandlung von Kerberos), Kerberos und Schannel. NTLM unterstützt keine gegenseitige Authentifizierung. Für die Verwendung der gegenseitigen Authentifizierung muss ein wohlgeformter Server Prinzipal Name angegeben werden. Viele Entwickler verwenden die folgende fehlerhafte Sicherheitsübung: der Server wird aufgerufen, um nach seinem Prinzipal Namen ([**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname)) zu Fragen, und dann Fragen Sie mithilfe dieses Prinzipal namens Blind die gegenseitige Authentifizierung. Diese Vorgehensweise unterbricht die gesamte Idee der gegenseitigen Authentifizierung. die Idee der gegenseitigen Authentifizierung besteht darin, dass nur bestimmte Server aufgerufen werden, da sie vertrauenswürdig sind, Ihre Daten zu analysieren und zu verarbeiten. Mithilfe der soeben beschriebenen fehlerhaften Sicherheitsübung geben Entwickler Ihre Daten an alle intelligenten genug, um Ihren Namen zurückzugeben.

Wenn die Client Software z. b. nur einen Server aufrufen soll, der unter den Konten Joe, Pete oder Alice ausgeführt wird, sollte die [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname) -Funktion aufgerufen werden, und der zurück gesendete Name sollte geprüft werden. Wenn er Joe, Pete oder Alice ist, muss die gegenseitige Authentifizierung mit dem Server Prinzipal Namen angefordert werden. Dadurch wird sichergestellt, dass beide Hälften der Konversation zum gleichen Prinzipal wechseln.

Wenn die Client Software einen Dienst anrufen soll, der nur unter dem Joe-Konto ausgeführt wird, verfassen Sie den Server Prinzipal Namen von Joe direkt, und nehmen Sie den- Wenn der Server nicht Joe ist, kann der-Befehl einfach nicht ausgeführt werden.

Häufig werden Dienste als Windows-Systemdienste ausgeführt. Dies bedeutet, dass Sie unter dem Computer Konto ausgeführt werden. Die gegenseitige Authentifizierung und Erstellung eines Server Prinzipal namens wird weiterhin empfohlen.

## <a name="use-the-lowest-impersonationtype-that-allows-the-call-to-go-through"></a>Verwenden Sie den niedrigsten Identitäts ationstyp, mit dem der Aufruf durchlaufen werden kann.

Diese bewährte Vorgehensweise ist recht selbsterklärend. Selbst wenn die gegenseitige Authentifizierung verwendet wird, sollten Sie dem Server nicht mehr Rechte als notwendig einräumen. Möglicherweise wurde ein legitimer Server kompromittiert, und auch wenn die von Ihnen gesendeten Daten in diesen Fällen in die falschen Hände geraten, kann zumindest der Server in Ihrem Namen nicht auf andere Daten im Netzwerk zugreifen. Einige Server lehnen einen Aufruf ab, der nicht über genügend Informationen zum Ermitteln und ggf. annehmen des Aufrufers verfügt. Beachten Sie außerdem, dass einige Protokoll Sequenzen die Sicherheit auf Transport Ebene ([**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np) und [**Ncalrpc**](/windows/desktop/Midl/ncalrpc)) unterstützen. In solchen Fällen kann der Server jederzeit einen Identitätswechsel durchführen, wenn Sie eine ausreichend hohe Identitätswechsel Ebene durch den *networkoptions* -Parameter angeben, wenn Sie das Bindungs Handle erstellen.

Schließlich können einige Sicherheitsanbieter oder Transporte den Identitäts ationstyp transparent auf eine höhere Ebene als die angegebene Ebene über stoßen. Wenn Sie ein Programm entwickeln, stellen Sie sicher, dass Sie versuchen, Aufrufe mit dem vorgesehenen Identitäts ationstyp auszuführen, und prüfen Sie, ob Sie einen höheren Identitäts ationstyp auf dem Server erhalten.

 

 