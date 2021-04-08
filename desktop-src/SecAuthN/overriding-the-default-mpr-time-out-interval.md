---
description: Der Multiple Provider Router (MPR) ruft NPgetCaps auf, um herauszufinden, wann die Netzwerkanbieter gestartet werden (nIndex ist auf wnnc Start festgelegt \_ ).
ms.assetid: f57bd8ff-647d-42f8-abaf-7937b24416dd
title: Überschreiben des standardmpr-Timeout Intervalls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b4308d94f4b16a7f67786c8a0856f23922e6f25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960334"
---
# <a name="overriding-the-default-mpr-time-out-interval"></a>Überschreiben des standardmpr-Timeout Intervalls

Der [*Multiple Provider Router*](../secgloss/m-gly.md) (MPR) ruft [**NPgetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) auf, um herauszufinden, wann die Netzwerkanbieter gestartet werden (*nIndex* ist auf wnnc Start festgelegt \_ ). Die MPR wartet dann auf den längsten Timeout Zeitraum, der von allen Netzwerkanbietern festgelegt wird, bevor das konsolidierte Netzwerk dem Benutzer präsentiert wird. Wenn einer der Netzwerkanbieter nicht weiß, wann er gestartet wird, verwendet MPR für diesen Anbieter ein Standard Timeout von 60 Sekunden.

Falls erforderlich, kann der Administrator das Standard Timeout überschreiben, indem er das folgende Registrierungs Timeout für " **reg \_ DWORD** " erstellt, wobei " *n* " das Timeout Intervall in Millisekunden ist:

**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Network Provider** \\ **restoretimeout**  =  *n*

Der folgende Pseudo Code zeigt den gesamten Logik Fluss für die Timeout Behandlung durch die MPR.


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



 

 
