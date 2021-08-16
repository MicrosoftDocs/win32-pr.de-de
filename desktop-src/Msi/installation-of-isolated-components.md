---
description: Windows Das Installationsprogramm führt während der Installation einer Anwendung die folgenden Aktionen aus, wenn das Paket isolierte Komponenten enthält. In der Regel ist Die \_ freigegebene Komponente eine DLL, die von der Komponentenanwendung und anderen \_ ausführbaren Clientdateien gemeinsam genutzt wird.
ms.assetid: fbc5dd86-5d38-4ce8-ab38-03c84cc77e80
title: Installation isolierter Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f842f626775dce436abedace96549fd55079c577885aad81492df861cd1a68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118634125"
---
# <a name="installation-of-isolated-components"></a>Installation isolierter Komponenten

Windows Das Installationsprogramm führt während der Installation einer Anwendung die folgenden Aktionen aus, wenn das Paket isolierte Komponenten enthält. In der Regel ist Die \_ freigegebene Komponente eine DLL, die von der Komponentenanwendung und anderen \_ ausführbaren Clientdateien gemeinsam genutzt wird.

## <a name="installation"></a>Installation

-   Kopieren Sie die Dateien von Component Shared nur dann in den gleichen Ordner wie \_ die \_ Komponentenanwendung, wenn die \_ Komponentenanwendung ebenfalls installiert wird.
-   Erstellen Sie eine Null-Byte-Datei mit dem kurzen Dateinamen der Schlüsseldatei der \_ Komponentenanwendung. Suchen Sie diese Datei im gleichen Ordner wie \_ Komponentenanwendung. Fügen Sie die Erweiterung an. LOCAL für diesen Dateinamen.
-   Erhöhen Sie die SharedDLL-Refcount, wenn das Bit msidbComponentAttributesSharedDllRefCount in der Spalte Attribute der [Component-Tabelle festgelegt ist.](component-table.md)
-   Registrieren Sie die Komponentenanwendung als Client von Component Shared, und registrieren Sie einen Schlüsselpfad, der auf den freigegebenen Speicherort von \_ \_ Component Shared (Freigegebene Komponente) \_ verweisen soll.
-   Installieren Sie wie gewohnt alle Ressourcen \_ der Komponentenanwendung.

Wenn die Freigegebene Komponente oder ihre Schlüsseldatei bereits auf dem Computer installiert ist, kopieren Sie keine Dateien an den freigegebenen \_ Speicherort der Freigegebenen \_ Komponente.

Wenn die \_ Freigegebene Komponente oder ihre Schlüsseldatei noch nicht auf dem Computer installiert ist:

-   Kopieren Sie die Dateien von Component \_ Shared an den freigegebenen Speicherort.
-   Verarbeiten Sie alle Installationsaktionen für Freigegebene \_ Komponenten.
-   Wenn Component Shared eine COM-Komponente ist, registrieren Sie den vollständigen COM-Pfad, damit die Syntax $Component und FileKey auf den freigegebenen Speicherort von \_ \[ Component Shared \] \[ \# \] \_ zeigen.

 

 



