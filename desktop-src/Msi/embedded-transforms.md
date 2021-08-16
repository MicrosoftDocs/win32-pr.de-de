---
description: Eingebettete Transformationen werden in der .msi-Datei des Pakets gespeichert. Dadurch wird benutzern garantiert, dass die Transformation immer verfügbar ist, wenn das Installationspaket verfügbar ist. Alternativ können Transformationen für Benutzer als eigenständige MST-Dateien bereitgestellt werden.
ms.assetid: f7b265df-4b34-44ea-85ab-8dbca4797517
title: Eingebettete Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae8d7afb2b28599cb9ee2f10c4bc1fb25fbb0939fe68da5e817972eb8fc94236
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637462"
---
# <a name="embedded-transforms"></a>Eingebettete Transformationen

Eingebettete Transformationen werden in der .msi-Datei des Pakets gespeichert. Dadurch wird benutzern garantiert, dass die Transformation immer verfügbar ist, wenn das Installationspaket verfügbar ist. Alternativ können Transformationen für Benutzer als eigenständige MST-Dateien bereitgestellt werden.

Um der Transformationsliste eine eingebettete Transformation hinzuzufügen, fügen Sie einen Doppelpunkt (:) Präfix des Dateinamens. Da das Installationsprogramm die Transformation immer aus dem Speicher in der .msi abrufen kann, werden eingebettete Transformationen nicht auf dem Computer des Benutzers zwischengespeichert. Eingebettete Transformationen können in Kombination mit geschützten [Transformationen](secured-transforms.md) oder [ungesicherten Transformationen verwendet werden.](unsecured-transforms.md) Weitere Informationen finden Sie unter [Anwenden von Transformationen.](applying-transforms.md)

 

 



