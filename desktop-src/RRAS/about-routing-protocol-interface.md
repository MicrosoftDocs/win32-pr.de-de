---
title: Informationen zur Routing Protokoll Schnittstelle
description: In der folgenden Dokumentation wird die Integration von Routing Protokollen von Drittanbietern in den Routing-und RAS-Dienst (RRAS) beschrieben.
ms.assetid: 593e3b8a-6f26-47c6-aa93-520d36db7a6f
keywords:
- RRAS für Routing-und RAS-Dienst, Routing Protokoll Schnittstelle
- Routing-und RAS-Dienst RRAS, Routing Protokoll Schnittstelle, beschrieben
- Routing Protokoll Schnittstelle RRAS
- RRAS-Routing Protokoll Schnittstelle, beschrieben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bc663f249ca42ebbae509c164a828d603a9b968
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711838"
---
# <a name="about-routing-protocol-interface"></a>Informationen zur Routing Protokoll Schnittstelle

In der folgenden Dokumentation wird die Integration von Routing Protokollen von Drittanbietern in den Routing-und RAS-Dienst (RRAS) beschrieben. RRAS ist eine Funktion von Windows, die als Multiprotokollrouter fungiert. RRAS definiert die Schnittstelle zwischen dem routermanager und dem Routing Protokoll. Das Routing Protokoll wird in einer Dynamic Link Library (dll) implementiert.

Verwenden Sie diese Schnittstelle, um Routing Protokolle, wie z. b. IGRP, nlsp und BGP, als benutzermodusdlls zu implementieren, die mit RRAS funktionieren.

In dieser Dokumentation werden die folgenden Themen beschrieben:

-   [Adapter](adapters.md)
-   [Schnittstellen](interfaces.md)
-   [Statische und automatische statische Routen](static-and-autostatic-routes.md)

 

 




