---
title: Schachtelung im gemischten Modus
description: In diesem Thema werden die Einschränkungen von Sicherheitsgruppen in einer Domäne im gemischten Modus aufgeführt.
ms.assetid: e9f50485-db09-4d8c-8cf4-0ee7e78cb133
ms.tgt_platform: multiple
keywords:
- Schachteln im gemischten Modus (AD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e54d63d475edf77398a69a519a08f3803f69d67d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855400"
---
# <a name="nesting-in-mixed-mode"></a>Schachtelung im gemischten Modus

In diesem Thema werden die Einschränkungen von Sicherheitsgruppen in einer Domäne im gemischten Modus aufgeführt.

Für Sicherheitsgruppen in einer Domäne im gemischten Modus gelten die folgenden Einschränkungen:

-   Universelle Gruppen können nicht in Domänen mit gemischtem Modus erstellt werden, da der universelle Bereich nur in Windows 2000-Domänen im einheitlichen Modus unterstützt wird
-   Eine globale Gruppe kann Konten aus derselben Domäne enthalten, zu der die Gruppe gehört. Eine globale Gruppe darf keine universellen Gruppen, keine globale Gruppe oder kein Konto aus einer anderen Domäne enthalten.
-   Eine lokale Gruppe der Domäne kann globale Gruppen und Konten aus beliebigen Domänen oder Gesamtstrukturen enthalten. Eine lokale Domänen Gruppe darf keine andere lokale Domänen Gruppe enthalten.

Beachten Sie, dass Verteiler Gruppen gemäß den Schachtelungs Regeln für den einheitlichen Modus geschachtelt werden können.

 

 




