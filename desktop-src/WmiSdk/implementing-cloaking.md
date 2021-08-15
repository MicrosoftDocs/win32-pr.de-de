---
description: Cloaking ist eine Erweiterung für den Identitätswechsel, die eine bessere Kontrolle darüber ermöglicht, wie COM einen Client über einen Proxy identitätswechselt. Wie bei vielen Formen der WMI-Sicherheit legen Sie das Cloaking über die Schnittstellen CoSetProxyBlanket und CoInitializeSecurity fest.
ms.assetid: e094aecc-e940-43aa-87c2-ea8cc86d1051
ms.tgt_platform: multiple
title: Implementieren von Cloaking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8d32333250bc37d8ccbfdb17421fed635f0da77e6394229220b2b36a1ce57f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118318895"
---
# <a name="implementing-cloaking"></a>Implementieren von Cloaking

Cloaking ist eine Erweiterung für den Identitätswechsel, die eine bessere Kontrolle darüber ermöglicht, wie COM einen Client über einen Proxy identitätswechselt. Wie bei vielen Formen der WMI-Sicherheit legen Sie das Cloaking über die Schnittstellen [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) und [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) fest.

COM stellt die folgenden Formen der Verleumdung bereit:

-   statischen

    COM richtet die Tokenidentität durch den Thread oder das Prozesstoken beim ersten Aufruf des Proxys ein. Wenn Sie statisches Cloaking mit [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)verwenden, legen Sie die Identität des Proxys für die Lebensdauer des Proxys fest.

-   Dynamisch

    COM reestablishes the token identity from the thread or process token on each call to the proxy. Da COM die Identität bei jedem Aufruf überprüft, ermöglicht die dynamische Verleumdung eine feineren Kontrolle über die Clientidentität. Die dynamische Verleumdung ist jedoch weniger effizient als die statische Verleumdung.

Wenn Sie die Verleumdung in Verbindung mit der Delegierungsebene des Identitätswechsels festlegen, kann ein Server die Identität eines Clients serverübergreifend verteilen, auch wenn die Server remote sind. Wenn Sie die Verleumdung nicht aktivieren, ruft COM jeden Aufruf von einem lokalen Server an einen Remoteserver im Kontext des eigentlichen Serverprozesses ab.

Durch die Verleumdung kann WMI die Identität eines Clients annehmen, um auf lokale und Remotenetzwerkressourcen über mehrere Computergrenzen hinweg zuzugreifen. WMI kann die Identität des Clients an lokale und Remoteserver übergeben, z. B. an andere Remoteinstanzen von WMI. Diese Remoteserver können dann Vorgänge im ursprünglichen Clientkontext ausführen.

Im folgenden Verfahren wird beschrieben, wie Sie die Verleumdung und Delegierung zusammen verwenden.

**So verwenden Sie Verleumdung und Delegierung zusammen**

1.  Legen Sie den Authentifizierungsdienst auf Kerberos fest.

    Kerberos ist der einzige Authentifizierungsdienst, der remote cloaking und delegierung unterstützt. Dies bedeutet, dass Verleumdung und Delegierung nur auf Remoteservern verwendet werden können.

2.  Markieren Sie das Serveranmeldungskonto in den Active Directory-Diensten als "Vertrauenswürdig für delegierung".
3.  Markieren Sie das Clientanmeldungskonto in Active Directory-Diensten als "Konto ist vertraulich und kann nicht delegiert werden".

Beispielsweise kann ein Aufruf des Ansichtsanbieters, der Objekte von mehreren WMI-Instanzen auf mehreren Computern zurückgeben kann, von delegierung und versieht.

 

 
