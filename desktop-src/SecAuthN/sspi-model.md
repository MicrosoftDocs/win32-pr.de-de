---
description: Mithilfe der Security Support Provider-Schnittstelle (Security Support Provider Interface, SSPI) kann eine Anwendung verschiedene Sicherheitsmodelle verwenden, die auf einem Computer oder Netzwerk verfügbar sind, ohne die Schnittstelle zum Sicherheitssystem
ms.assetid: 86ffc8c0-727d-437f-ac36-10df6563b0be
title: SSPI-Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55cf79185693f40694d1bc6de319376b037fb853
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393353"
---
# <a name="sspi-model"></a>SSPI-Modell

Mithilfe der [*Security Support Provider-Schnittstelle (Security Support Provider Interface*](../secgloss/s-gly.md) , SSPI) kann eine Anwendung verschiedene Sicherheitsmodelle verwenden, die auf einem Computer oder Netzwerk verfügbar sind, ohne die Schnittstelle zum Sicherheitssystem SSPI richtet [*keine Anmelde Informationen ein, da dies*](../secgloss/c-gly.md) im Allgemeinen ein privilegierter Vorgang ist, der vom Betriebssystem behandelt wird.

Ein [*Security Support Provider*](../secgloss/s-gly.md) (SSP) ist in einer [*Dynamic Link Library*](../secgloss/d-gly.md) (dll) enthalten, die SSPI implementiert, indem ein oder mehrere [*Sicherheitspakete*](../secgloss/s-gly.md) für Anwendungen verfügbar gemacht werden. Jedes Sicherheitspaket stellt Zuordnungen zwischen den SSPI-Funktionsaufrufen einer Anwendung und den Funktionen eines tatsächlichen Sicherheitsmodells bereit. Sicherheitspakete unterstützen [*Sicherheitsprotokolle*](../secgloss/s-gly.md) wie die [*Kerberos*](../secgloss/k-gly.md) -Authentifizierung und den LAN-Manager.

Die SSPI-Schnittstelle ist im Kernel Modus und im Benutzermodus verfügbar. Um die SSPI-Funktionalität im Kernel Modus zu verwenden, müssen Sie das Windows installierbare Datei System-DDK installieren. Das Aufruf Modell bleibt unverändert, aber Überlegungen zum Kernel Modus werden auf Funktions Verweis Seiten vermerkt. Weitere Informationen finden Sie unter [SSPI-Funktionen](authentication-functions.md).

 

 
