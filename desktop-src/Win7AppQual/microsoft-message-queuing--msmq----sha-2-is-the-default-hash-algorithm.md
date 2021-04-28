---
description: 'Microsoft Message Queuing (MSMQ): SHA 2 ist der Standardhashalgorithmus.'
ms.assetid: 43cca5bc-6675-4f29-925e-19d3fb19ef0f
title: 'Microsoft Message Queuing (MSMQ): SHA 2 ist der Standardhashalgorithmus.'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e2b73e347f5d5a768780afc5d2153909c6f5a9a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088098"
---
# <a name="microsoft-message-queuing-msmq---sha-2-is-the-default-hash-algorithm"></a>Microsoft Message Queuing (MSMQ): SHA 2 ist der Standardhashalgorithmus.

## <a name="affected-platforms"></a>Betroffene Plattformen

 **Clients:** Windows XP, Windows Vista, Windows 7  
**Server:** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2  










## <a name="feature-impact"></a>Auswirkungen auf Das Feature

 **Schweregrad –** Niedrig  
**Häufigkeit** : Niedrig  





## <a name="description"></a>BESCHREIBUNG

In Windows 7 verwendet MSMQ SHA-2 als Standard beim Signieren einer ausgehenden Nachricht. Darüber hinaus müssen alle eingehenden Nachrichten mit SHA-2 signiert werden. Sie können die Unterstützung für einen niedrigeren Verschlüsselungsalgorithmus über einen vom Administrator zugänglichen Registrierungsschlüssel aktivieren.

## <a name="manifestation-of-impact"></a>Wirkungserz weiter

-   MSMQ unter Windows 2003 oder darunter akzeptiert keine signierten Nachrichten, die von MSMQ in Windows 7 stammen.
-   MSMQ in Windows 7 akzeptiert keine signierten Nachrichten, die von Windows 2008 oder darunter stammen.

## <a name="mitigation"></a>Minderung

Benutzer sollten ein Upgrade auf Windows 7 in Betracht ziehen, um den verstärkten Signaturalgorithmus zu nutzen. Um den nahtlosen Austausch signierter Nachrichten zwischen Windows 7 und einem beliebigen Downlevelbetriebssystem zu ermöglichen, muss der Administrator auf den MSMQ-Computern entsprechende Ausnahmen hinzufügen.

 

 



