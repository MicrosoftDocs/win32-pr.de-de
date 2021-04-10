---
description: Eingebettete Transformationen werden in der MSI-Datei des Pakets gespeichert. Dadurch wird Benutzern gewährleistet, dass die Transformation immer verfügbar ist, wenn das Installationspaket verfügbar ist. Alternativ können Transformationen als eigenständige MST-Dateien für Benutzer bereitgestellt werden.
ms.assetid: f7b265df-4b34-44ea-85ab-8dbca4797517
title: Eingebettete Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301e7f188da1a46411636ef90b7e6ae327a06c22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042390"
---
# <a name="embedded-transforms"></a>Eingebettete Transformationen

Eingebettete Transformationen werden in der MSI-Datei des Pakets gespeichert. Dadurch wird Benutzern gewährleistet, dass die Transformation immer verfügbar ist, wenn das Installationspaket verfügbar ist. Alternativ können Transformationen als eigenständige MST-Dateien für Benutzer bereitgestellt werden.

Um der Liste Transformationen eine eingebettete Transformation hinzuzufügen, fügen Sie einen Doppelpunkt (:) Präfix des Datei namens. Da das Installationsprogramm die Transformation immer aus dem Speicher in der MSI-Datei abrufen kann, werden eingebettete Transformationen nicht auf dem Computer des Benutzers zwischengespeichert. Eingebettete Transformationen können in Kombination mit [gesicherten Transformationen](secured-transforms.md) oder [ungesicherten Transformationen](unsecured-transforms.md)verwendet werden. Weitere Informationen finden Sie unter [Anwenden von Transformationen](applying-transforms.md).

 

 



