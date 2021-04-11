---
description: .
ms.assetid: 43cca5bc-6675-4f29-925e-19d3fb19ef0f
title: 'Microsoft Message Queuing (MSMQ): SHA 2 ist der Standard Hash Algorithmus.'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f0d2476133ca7939bc90effa3842c0b90482ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217413"
---
# <a name="microsoft-message-queuing-msmq---sha-2-is-the-default-hash-algorithm"></a>Microsoft Message Queuing (MSMQ): SHA 2 ist der Standard Hash Algorithmus.

## <a name="affected-platforms"></a>Betroffene Plattformen

 **Clients** -Windows XP \| Windows Vista \| Windows 7  
**Server** -Windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2  










## <a name="feature-impact"></a>Auswirkungen von Features

 **Schweregrad** -niedrig  
**Häufigkeit** -niedrig  





## <a name="description"></a>BESCHREIBUNG

In Windows 7 verwendet MSMQ SHA-2 als Standard beim Signieren einer ausgehenden Nachricht. Außerdem müssen alle eingehenden Nachrichten mit SHA-2 signiert werden. Sie können die Unterstützung für einen niedrigeren Verschlüsselungsalgorithmus über einen vom Administrator zugänglichen Registrierungsschlüssel aktivieren.

## <a name="manifestation-of-impact"></a>Erscheinung der Auswirkung

-   MSMQ in Windows 2003 oder unten akzeptiert keine signierten Nachrichten, die von MSMQ in Windows 7 stammen
-   MSMQ in Windows 7 akzeptiert keine signierten Nachrichten, die von Windows 2008 oder niedriger stammen

## <a name="mitigation"></a>Minderung

Benutzer sollten ein Upgrade auf Windows 7 in Erwägung nehmen, um den stärkeren Signatur Algorithmus zu nutzen. Um einen nahtlosen signierten Nachrichtenaustausch zwischen Windows 7 und einem Betriebssystem auf Betriebssystemebene zu aktivieren, muss der Administrator auf den MSMQ-Computern entsprechende Ausnahmen hinzufügen.

 

 



