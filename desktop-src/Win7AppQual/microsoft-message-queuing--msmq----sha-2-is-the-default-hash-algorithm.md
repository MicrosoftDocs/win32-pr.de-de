---
description: 'Microsoft Message Queuing (MSMQ): SHA 2 ist der Standardhashalgorithmus.'
ms.assetid: 43cca5bc-6675-4f29-925e-19d3fb19ef0f
title: 'Microsoft Message Queuing (MSMQ): SHA 2 ist der Standardhashalgorithmus.'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3c54832d953e50f3b912fdf36374faa8ff9ed0466587f7ac3fed2572eb3b85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053038"
---
# <a name="microsoft-message-queuing-msmq---sha-2-is-the-default-hash-algorithm"></a>Microsoft Message Queuing (MSMQ): SHA 2 ist der Standardhashalgorithmus.

## <a name="affected-platforms"></a>Betroffene Plattformen

 **Clients** – Windows XP, Windows Vista, Windows 7  
**Server** – Windows Server 2003, Windows Server 2008, Windows Server 2008 R2  










## <a name="feature-impact"></a>Auswirkungen auf Features

 **Schweregrad –** Niedrig  
**Häufigkeit** : Niedrig  





## <a name="description"></a>Beschreibung

In Windows 7 verwendet MSMQ SHA-2 als Standard beim Signieren einer ausgehenden Nachricht. Darüber hinaus müssen alle eingehenden Nachrichten mit SHA-2 signiert werden. Sie können die Unterstützung für einen niedrigeren Verschlüsselungsalgorithmus über einen vom Administrator zugänglichen Registrierungsschlüssel aktivieren.

## <a name="manifestation-of-impact"></a>Auswirkungen

-   MSMQ in Windows 2003 oder darunter akzeptiert keine signierten Nachrichten, die von MSMQ in Windows 7 stammen.
-   MSMQ in Windows 7 akzeptiert keine signierten Nachrichten, die von Windows 2008 oder darunter stammen.

## <a name="mitigation"></a>Minderung

Benutzer sollten ein Upgrade auf Windows 7 in Betracht ziehen, um den verstärkten Signaturalgorithmus zu nutzen. Um den nahtlosen Austausch signierter Nachrichten zwischen Windows 7 und einem beliebigen Downlevelbetriebssystem zu ermöglichen, muss der Administrator auf den MSMQ-Computern entsprechende Ausnahmen hinzufügen.

 

 



