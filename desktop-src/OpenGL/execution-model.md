---
title: Ausführungsmodell
description: Ausführungsmodell
ms.assetid: 1947eb24-3a55-4d30-924e-93f2eed2c7b6
keywords:
- OpenGL, Ausführungsmodell
- Ausführungsmodell OpenGL
- OpenGL,Client-/Servermodell
- Client-/Servermodell OpenGL
- OpenGL, netzwerktransparent
- Framepuffer, Ausführungsmodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7cb7c3c06baa0a56f4c59b14744b73962fced369d56f00cbf887b9ae6d09e2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082460"
---
# <a name="execution-model"></a>Ausführungsmodell

Das Modell für die Interpretation von OpenGL-Befehlen ist client/server. Anwendungscode (der Client) gibt Befehle aus, die von OpenGL (dem Server) interpretiert und verarbeitet werden. Der Server kann auf demselben Computer wie der Client ausgeführt werden. In diesem Sinne ist OpenGL netzwerktransparent. Ein Server kann mehrere OpenGL-Kontexte verwalten, von denen jeder ein gekapselter OpenGL-Zustand ist. Ein Client kann eine Verbindung mit einem dieser Kontexte herstellen. Das erforderliche Netzwerkprotokoll kann implementiert werden, indem ein bereits vorhandenes Protokoll (z. B. das des X-Fenstersystems) oder ein unabhängiges Protokoll erweitert wird. Es werden keine OpenGL-Befehle zum Abrufen von Benutzereingaben bereitgestellt.

Das Fenstersystem, das Framepufferressourcen zuordnet, steuert letztendlich die Auswirkungen von OpenGL-Befehlen auf den Framepuffer. Das Fenstersystem:

-   Bestimmt, auf welche Teile des Framepuffers OpenGL zu einem bestimmten Zeitpunkt zugreifen kann.
-   Kommuniziert OpenGL, wie diese Teile strukturiert sind.

Daher gibt es keine OpenGL-Befehle, um den Framepuffer zu konfigurieren oder OpenGL zu initialisieren. Die Framepufferkonfiguration erfolgt außerhalb von OpenGL in Verbindung mit dem Fenstersystem. Die OpenGL-Initialisierung erfolgt, wenn das Fenstersystem ein Fenster für das OpenGL-Rendering zuordnet.

 

 




