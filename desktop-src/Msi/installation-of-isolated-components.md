---
description: Windows Das Installationsprogramm führt während der Installation einer Anwendung die folgenden Aktionen aus, wenn das Paket isolierte Komponenten enthält. In der Regel ist "Komponente \_ freigegeben" eine DLL, die von der \_ Komponentenanwendung und anderen ausführbaren Clientdateien gemeinsam genutzt wird.
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

Windows Das Installationsprogramm führt während der Installation einer Anwendung die folgenden Aktionen aus, wenn das Paket isolierte Komponenten enthält. In der Regel ist "Komponente \_ freigegeben" eine DLL, die von der \_ Komponentenanwendung und anderen ausführbaren Clientdateien gemeinsam genutzt wird.

## <a name="installation"></a>Installation

-   Kopieren Sie die Dateien von Komponente \_ freigegeben nur dann in denselben Ordner wie \_ Komponentenanwendung, wenn \_ die Komponentenanwendung ebenfalls installiert wird.
-   Erstellen Sie eine 0-Byte-Datei mit dem kurzen Dateinamen der Schlüsseldatei der \_ Komponentenanwendung. Suchen Sie diese Datei im gleichen Ordner wie \_ komponentenanwendung. Fügen Sie die Erweiterung an. LOCAL für diesen Dateinamen.
-   Erhöhen Sie den SharedDLL-Refcount, wenn das Bit msidbComponentAttributesSharedDllRefCount in der Attributes -Spalte der [Component-Tabelle](component-table.md)festgelegt ist.
-   Registrieren Sie die \_ Komponentenanwendung als Client der \_ Komponente Freigegeben, und registrieren Sie einen Schlüsselpfad, der auf den freigegebenen Speicherort von Komponente \_ Freigegeben verweist.
-   Installieren Sie wie gewohnt alle Ressourcen der \_ Komponentenanwendung.

Wenn Komponente \_ freigegeben oder die zugehörige Schlüsseldatei bereits auf dem Computer installiert ist, kopieren Sie keine Dateien an den freigegebenen Speicherort von Komponente \_ freigegeben.

Wenn Komponente \_ freigegeben oder ihre Schlüsseldatei noch nicht auf dem Computer installiert ist:

-   Kopieren Sie die Dateien der Komponente \_ Freigegeben an den freigegebenen Speicherort.
-   Verarbeiten Sie alle Installationsaktionen für \_ Komponenten freigegeben.
-   Wenn Component \_ Shared eine COM-Komponente ist, registrieren Sie den vollständigen COM-Pfad, sodass die Syntax \[ $Component und \] \[ \# FileKey auf den \] freigegebenen Speicherort der Komponente Shared \_ verweisen.

 

 



