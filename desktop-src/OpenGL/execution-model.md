---
title: Ausführungs Modell
description: Ausführungs Modell
ms.assetid: 1947eb24-3a55-4d30-924e-93f2eed2c7b6
keywords:
- OpenGL, Ausführungs Modell
- Ausführungs Modell OpenGL
- OpenGL, Client/Server-Modell
- Client/Server-Modell OpenGL
- OpenGL, netzwerktransparent
- Framebuffers, Ausführungs Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86012912f9bd963da0489b83cc4a5c1e7e1722ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947977"
---
# <a name="execution-model"></a>Ausführungs Modell

Das Modell für die Interpretation von OpenGL-Befehlen ist Client/Server. Der Anwendungscode (der Client) gibt Befehle aus, die von OpenGL (dem Server) interpretiert und verarbeitet werden. Der Server kann auf demselben Computer wie der Client ausgeführt werden. In diesem Sinne ist OpenGL netzwerktransparent. Ein Server kann mehrere OpenGL-Kontexte verwalten, von denen jeder ein gekapselter OpenGL-Zustand ist. Ein Client kann eine Verbindung mit einem dieser Kontexte herstellen. Das erforderliche Netzwerkprotokoll kann implementiert werden, indem ein bereits vorhandenes Protokoll (z. b. das des X-Fenstersystems) erweitert oder ein unabhängiges Protokoll verwendet wird. Zum Abrufen von Benutzereingaben werden keine OpenGL-Befehle bereitgestellt.

Das Fenstersystem, das Frame Puffer-Ressourcen ordnet, steuert letztendlich die Auswirkungen von OpenGL-Befehlen auf den Frame Puffer. Das Fenstersystem:

-   Bestimmt, auf welche Teile des Frame Puffer OpenGL zu einem beliebigen Zeitpunkt zugreifen können.
-   Kommuniziert mit OpenGL, wie diese Teile strukturiert sind.

Daher sind keine OpenGL-Befehle zum Konfigurieren von Frame Puffer oder zum Initialisieren von OpenGL vorhanden. Die Frame Puffer Konfiguration erfolgt außerhalb von OpenGL in Verbindung mit dem Fenstersystem. Die OpenGL-Initialisierung findet statt, wenn das Fenstersystem ein Fenster für das OpenGL-Rendering bereitstellt.

 

 




