---
title: Verbunddateien
description: Obwohl Sie eigene strukturierte Speicher Objekte und Schnittstellen implementieren können, stellt com eine Standard Implementierung namens Verbund Dateien bereit.
ms.assetid: 23b425e6-dfe5-403b-8f43-de6843a03dcd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62be79f09afd23e53a569b76ad3e0af46cae2f9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206374"
---
# <a name="compound-files"></a>Verbunddateien

Obwohl Sie eigene strukturierte Speicher Objekte und Schnittstellen implementieren können, stellt com eine Standard Implementierung namens Verbund Dateien bereit. Durch die Verwendung von Verbund Dateien können Sie Ihre eigene Implementierung von strukturiertem Speicher codieren und einige zusätzliche Vorteile nutzen, die von der Einhaltung eines definierten Standards abgeleitet werden. Dazu gehören folgende Vorteile:

-   **Dateisystem-und Plattformunabhängigkeit**. Da die Implementierung der Verbund Dateien von com auf vorhandenen Flatfile-Systemen ausgeführt wird, können Verbund Dateien, die im FAT-Dateisystem, im NTFS-Dateisystem oder im Macintosh-Dateisystem gespeichert sind, von Anwendungen geöffnet werden, die eines der anderen Dateisysteme verwenden.
-   Durch **suchbar**. Da die separaten Objekte in einer Verbund Datei in einem Standardformat gespeichert werden und über Standard-COM-Schnittstellen und APIs auf Sie zugegriffen werden kann, können alle Browser Dienstprogrammen, die diese Schnittstellen und APIs verwenden, die Objekte in der Datei auflisten, auch wenn die Daten in einem bestimmten Objekt ein proprietäres Format aufweisen können.
-   **Zugriff auf bestimmte interne Daten**. Da die Implementierung von Verbund Dateien Standardmethoden zum Schreiben bestimmter Datentypen bietet – zusammenfassende Informationen, z. –. Anwendungen können diese Daten mithilfe von COM-Schnittstellen und APIs lesen.

 

 




