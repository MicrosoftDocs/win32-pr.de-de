---
title: ADSI-LDAP-Anbieter
description: Der ADSI LDAP-Anbieter implementiert eine Reihe von ADSI-Objekten, die verschiedene ADSI-Schnittstellen unterstützen. Um auf den LDAP-Anbieter zuzugreifen, binden Sie mithilfe des LDAP-ADsPath an eines der ADSI LDAP-Objekte.
ms.assetid: 3c13ea2f-fe40-4fd4-8540-422f277e07c1
ms.tgt_platform: multiple
keywords:
- ADSI-LDAP-Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8edbca53708a46c2f788c328a78bd2488973486
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855360"
---
# <a name="adsi-ldap-provider"></a>ADSI-LDAP-Anbieter

Der ADSI LDAP-Anbieter implementiert eine Reihe von ADSI-Objekten, die verschiedene ADSI-Schnittstellen unterstützen. Um auf den LDAP-Anbieter zuzugreifen, binden Sie mithilfe des LDAP-ADsPath an eines der ADSI LDAP-Objekte.

Adsldp.dll, Adsldpc.dll, Adsmsext.dll und Activeds.dll müssen auf dem Client Computer installiert sein, um mit dem Anbieter zusammenarbeiten zu können.

> [!Note]  
> Der standardmäßige ADSI LDAP-Anbieter kann nicht als vollständig Thread sicher angesehen werden. Writer von Multithreadanwendungen sollten den Zugriff zwischen Threads durch die ordnungsgemäße Verwendung von Synchronisierungs Objekten, wie z. b. Semaphore, Mutexen, kritischen Abschnitten usw., ordnungsgemäß koordinieren.

 

 

 




