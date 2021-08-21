---
title: What Can You Know, and When Can You Know It
description: Anwendungen, die auf latenzbedingte Zustände reagieren, müssen Problemzustände erkennen und entsprechende Maßnahmen ergreifen.
ms.assetid: d1d0135e-2d67-47dd-82ac-4869203ce85e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05845de7fe6f578627ced8c7acbc8e14065a779f67e6e8c6a5ce281514640be0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182244"
---
# <a name="what-can-you-know-and-when-can-you-know-it"></a>Was können Sie wissen, und wann können Sie es wissen?

Anwendungen, die auf latenzbedingte Zustände reagieren, müssen Problemzustände erkennen und entsprechende Maßnahmen ergreifen. Es gibt zwei Problemzustände: Versionsschiefe und Teilaktualisierung. Versionsschiefe lässt sich nicht erkennen, indem der Verzeichnisdienst untersucht wird (beachten Sie das Axiom des verteilten Computings, das unter [Why Active Directory Domain Services Use This Replication Model (Warum Active Directory Domain Services dieses Replikationsmodell verwenden)](why-active-directory-domain-services-uses-this-replication-model.md)angegeben ist. Teilaktualisierungen können erkannt werden, indem den Objekten, aus denen der verknüpfte Satz besteht, Metadaten hinzugefügt werden. Vorschläge für solche Metadaten werden in den nachfolgenden Abschnitten dieses Dokuments angezeigt. Es gibt Vermeidungsstrategien, die Anwendungen verwenden können, um die Wahrscheinlichkeit von Versionsschiefe und Teilupdates zu verringern. Diese Strategien werden auch in den nachfolgenden Abschnitten dieses Dokuments erläutert.

 

 




