---
description: Microsoft Negotiate ist ein Sicherheitssupportanbieter, der als Anwendungsschicht zwischen der Security Support Provider-Schnittstelle und den anderen SSPs fungiert.
ms.assetid: 3aa7e979-8b55-416d-bed1-28296055d38e
title: Microsoft Negotiate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebd223267a2e7d0e4dc23ae356a6fa2e6224c742c491e428369f15fb6d46ff73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786952"
---
# <a name="microsoft-negotiate"></a>Microsoft Negotiate

Microsoft Negotiate ist ein [*Sicherheitssupportanbieter (Security Support Provider,*](../secgloss/s-gly.md) SSP), der als Anwendungsschicht zwischen der [*Security Support Provider Interface*](../secgloss/s-gly.md) [(SSPI)](sspi.md)und den anderen SSPs fungiert. Wenn eine SSPI zur Anmeldung bei einem Netzwerk von einer Anwendung aufgerufen wird, kann ein SSP zur Verarbeitung der Anforderung angegeben werden. Wenn die Anwendung Negotiate angibt, analysiert Negotiate die Anforderung und wählt den besten SSP aus, um die Anforderung basierend auf der vom Kunden konfigurierten Sicherheitsrichtlinie zu verarbeiten.

Derzeit wählt das Sicherheitspaket Negotiate zwischen [Kerberos](microsoft-kerberos.md) und [NTLM](microsoft-ntlm.md)aus. Negotiate wählt Kerberos aus, es sei denn, es kann nicht von einem der an der Authentifizierung beteiligten Systeme verwendet werden, oder die aufrufende Anwendung hat nicht genügend Informationen für die Verwendung von Kerberos angegeben.

Damit Negotiate den [Kerberos-Sicherheitsanbieter](microsoft-kerberos.md) auswählen kann, muss die Clientanwendung einen [*Dienstprinzipalnamen (Service Principal Name,*](../secgloss/s-gly.md) SPN), einen Benutzerprinzipalnamen (USER Principal Name, UPN) oder einen NetBIOS-Kontonamen als Zielnamen angeben. Andernfalls wählt Negotiate immer den [NTLM-Sicherheitsanbieter](microsoft-ntlm.md) aus.

Ein Server, der das Negotiate-Paket verwendet, kann auf Clientanwendungen reagieren, die entweder den [Kerberos-](microsoft-kerberos.md) oder [NTLM-Sicherheitsanbieter](microsoft-ntlm.md) auswählen. Eine Clientanwendung muss jedoch wissen, dass ein Server das Negotiate-Paket unterstützt, um die Authentifizierung mit negotiate anzufordern. Ein Server, der Negotiate nicht unterstützt, kann nicht immer auf Anforderungen von Clients reagieren, die Negotiate als SSP angeben.

## <a name="reasons-to-use-the-negotiate-package"></a>Gründe für die Verwendung des Aushandlungspakets

-   Ermöglicht dem System die Verwendung des stärksten (sichersten) verfügbaren Protokolls.
-   Stellt die Vorwärtskompatibilität für Ihre Anwendung sicher.
-   Stellt sicher, dass Ihre Anwendung ein Verhalten aufweist, das mit der vom Kunden festgelegten Sicherheitsrichtlinie in Einklang steht.

 

 
