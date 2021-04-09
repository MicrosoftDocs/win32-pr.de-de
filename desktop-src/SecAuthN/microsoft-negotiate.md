---
description: Microsoft aushandeln ist eine Security Support Provider, die als Anwendungsschicht zwischen der Security Support Provider-Schnittstelle und den anderen SSPs fungiert.
ms.assetid: 3aa7e979-8b55-416d-bed1-28296055d38e
title: Microsoft aushandeln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7ce57a8f8924120dcce51e50e05de90fd6774b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958873"
---
# <a name="microsoft-negotiate"></a>Microsoft aushandeln

Bei Microsoft Aushandlungen handelt es sich um einen [*Security Support Provider*](../secgloss/s-gly.md) (SSP), der als Anwendungsschicht zwischen [*Security Support Provider Interface*](../secgloss/s-gly.md) ([SSPI](sspi.md)) und den anderen SSPs fungiert. Wenn eine SSPI zur Anmeldung bei einem Netzwerk von einer Anwendung aufgerufen wird, kann ein SSP zur Verarbeitung der Anforderung angegeben werden. Wenn die Anwendung aushandeln angibt, analysiert aushandeln die Anforderung und wählt den besten SSP für die Verarbeitung der Anforderung basierend auf der vom Kunden konfigurierten Sicherheitsrichtlinie aus.

Derzeit wählt das Aushandlungs Sicherheitspaket zwischen [Kerberos](microsoft-kerberos.md) und [NTLM](microsoft-ntlm.md)aus. Aushandeln wählt Kerberos aus, es sei denn, Sie kann von einem der an der Authentifizierung beteiligten Systeme verwendet werden, oder die aufrufende Anwendung hat keine ausreichenden Informationen für die Verwendung von Kerberos bereitgestellt.

Damit der [Kerberos](microsoft-kerberos.md) -Sicherheitsanbieter von aushandeln ausgewählt werden kann, muss die Client Anwendung einen [*Dienst Prinzipal Namen*](../secgloss/s-gly.md) (SPN), einen Benutzer Prinzipal Namen (User Principal Name, UPN) oder einen NetBIOS-Kontonamen als Zielnamen bereitstellen. Andernfalls wählt aushandeln immer den [NTLM](microsoft-ntlm.md) -Sicherheitsanbieter aus.

Ein Server, der das Aushandlungs Paket verwendet, kann auf Client Anwendungen Antworten, die speziell den [Kerberos](microsoft-kerberos.md) -oder [NTLM](microsoft-ntlm.md) -Sicherheitsanbieter auswählen. Eine Client Anwendung muss jedoch wissen, dass ein Server das Aushandlungs Paket unterstützt, um die Authentifizierung mithilfe von aushandeln anzufordern. Ein Server, der keine Aushandlung unterstützt, kann nicht immer auf Anforderungen von Clients antworten, die aushandeln als SSP angeben.

## <a name="reasons-to-use-the-negotiate-package"></a>Gründe für die Verwendung des Aushandlungs Pakets

-   Ermöglicht dem System, das stärkste (sicherste) verfügbare Protokoll zu verwenden.
-   Gewährleistet die Vorwärtskompatibilität für Ihre Anwendung.
-   Stellt sicher, dass Ihre Anwendung ein Verhalten aufweist, das mit der vom Kunden festgelegten Sicherheitsrichtlinie übereinstimmt.

 

 
