---
description: Der Multiple Provider Router (MPR) ruft NPGetCaps auf, um herauszufinden, wann die Netzwerkanbieter gestartet werden (nIndex ist auf WNNC \_ START festgelegt).
ms.assetid: f57bd8ff-647d-42f8-abaf-7937b24416dd
title: Überschreiben des MPR-Standardzeitintervalls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51c2c9db2fb892b7c2fc9646a9328fb9de4b7f9782ff5204ed261b16471ca4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921134"
---
# <a name="overriding-the-default-mpr-time-out-interval"></a>Überschreiben des MPR-Standardzeitintervalls

Der [*Multiple Provider Router*](../secgloss/m-gly.md) (MPR) ruft [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) auf, um herauszufinden, wann die Netzwerkanbieter gestartet werden (*nIndex* ist auf WNNC \_ START festgelegt). Die MPR wartet dann für den längsten time out-Zeitraum, der von allen Netzwerkanbietern angegeben wurde, bevor sie dem Benutzer das konsolidierte Netzwerk präsentiert. Wenn einer der Netzwerkanbieter nicht weiß, wann er gestartet wird, verwendet MPR ein Standard-Time out von 60 Sekunden für diesen Anbieter.

Bei Bedarf kann der Administrator das Standard-Time out überschreiben, indem er das folgende **REG \_ DWORD-Registrierungs-Time** out erstellt, wobei *n* das Time out-Intervall in Millisekunden ist:

**HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Control** \\ **NetworkProvider** \\ **RestoreTimeout**  =  *n*

Der folgende Pseudocode zeigt den vollständigen Logikfluss für die Time out-Behandlung durch mpr.


```C++
If there is a RegistryTimeout,
Then MaxTimeout = RegistryTimeout.
Otherwise,
MaxTimeout = 0.
For each provider,
if the provider does not supply a time-out and
if there is a RegistryTimeout,
ProviderTimeout is set to RegistryTimeout.
Otherwise,
ProviderTimeout is set to DefaultTimeout.
Otherwise,
If the ProviderTimeout is longer than MaxTimeout,
MaxTimeout = ProviderTimeout.
```



 

 
