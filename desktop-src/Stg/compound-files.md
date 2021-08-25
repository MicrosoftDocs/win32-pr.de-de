---
title: Verbunddateien
description: Obwohl Sie Ihre eigenen strukturierten Speicherobjekte und Schnittstellen implementieren können, bietet COM eine Standardimplementierung namens Verbunddateien.
ms.assetid: 23b425e6-dfe5-403b-8f43-de6843a03dcd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 302f7587817f07ec18900f537189a2571c883b0fc43a58eddb823a40fe1c0db3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867460"
---
# <a name="compound-files"></a>Verbunddateien

Obwohl Sie Ihre eigenen strukturierten Speicherobjekte und Schnittstellen implementieren können, bietet COM eine Standardimplementierung namens Verbunddateien. Die Verwendung von Verbunddateien erspart Ihnen das Programmieren Ihrer eigenen Implementierung von strukturiertem Speicher und bietet mehrere zusätzliche Vorteile, die sich aus der Einhaltung eines definierten Standards ableiten. Dazu gehören folgende Vorteile:

-   **Dateisystem- und Plattformunabhängigkeit**. Da die Com-Verbunddateiimplementierung auf vorhandenen Flatfilesystemen ausgeführt wird, können Verbunddateien, die im FAT-Dateisystem, NTFS-Dateisystem oder Macintosh-Dateisystem gespeichert sind, von Anwendungen geöffnet werden, die eines der anderen Dateisysteme verwenden.
-   **Durchsuchbar.** Da die separaten Objekte in einer Verbunddatei in einem Standardformat gespeichert werden und über COM-Standardschnittstellen und -APIs auf sie zugegriffen werden kann, kann jedes Browser-Hilfsprogramm, das diese Schnittstellen und APIs verwendet, die Objekte in der Datei auflisten, obwohl die Daten innerhalb eines bestimmten Objekts in einem proprietären Format vorliegen können.
-   **Zugriff auf bestimmte interne Daten.** Da die Verbunddateienimplementierung Standardverfahren zum Schreiben bestimmter Datentypen ( z. B. Zusammenfassungsinformationen) bietet, können Anwendungen diese Daten mithilfe von COM-Schnittstellen und APIs lesen.

 

 




