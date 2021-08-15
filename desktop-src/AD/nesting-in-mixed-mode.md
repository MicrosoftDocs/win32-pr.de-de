---
title: Schachteln im gemischten Modus
description: In diesem Thema werden die Einschränkungen von Sicherheitsgruppen in einer Domäne im gemischten Modus aufgelistet.
ms.assetid: e9f50485-db09-4d8c-8cf4-0ee7e78cb133
ms.tgt_platform: multiple
keywords:
- Schachteln in AD im gemischten Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54c53fd79cb10c452dbb363c3d6803071e6e52871f0ce87b03f9d06a61eaece8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185822"
---
# <a name="nesting-in-mixed-mode"></a>Schachteln im gemischten Modus

In diesem Thema werden die Einschränkungen von Sicherheitsgruppen in einer Domäne im gemischten Modus aufgelistet.

Für Sicherheitsgruppen in einer Domäne im gemischten Modus gelten die folgenden Einschränkungen:

-   Universelle Gruppen können nicht in Domänen im gemischten Modus erstellt werden, da der universelle Bereich nur in Domänen im einheitlichen Modus Windows 2000 unterstützt wird.
-   Eine globale Gruppe kann Konten aus derselben Domäne enthalten, zu der die Gruppe gehört. Eine globale Gruppe darf keine universellen Gruppen, globale Gruppen oder ein Konto aus einer anderen Domäne enthalten.
-   Eine lokale Domänengruppe kann globale Gruppen und Konten aus einer beliebigen Domäne oder Gesamtstruktur enthalten. Eine lokale Domänengruppe darf keine andere lokale Domänengruppe enthalten.

Beachten Sie, dass Verteilergruppen gemäß den Schachtelungsregeln für den einheitlichen Modus geschachtelt werden können.

 

 




