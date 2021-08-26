---
description: Windows Das Installationsprogramm führt die folgenden Aktionen während der Neuinstallation einer Anwendung aus, wenn das Paket isolierte Komponenten enthält. In der Regel ist Die \_ freigegebene Komponente eine DLL, die von der Komponentenanwendung und anderen \_ ausführbaren Clientdateien gemeinsam genutzt wird.
ms.assetid: 65909b47-dc09-4e9a-920a-9cb3f55b2e67
title: Neuinstallation isolierter Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c624777647ab9e5023cd6c78d9aaa4d20951563f915afcd800ba60ca3b233174
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086010"
---
# <a name="reinstallation-of-isolated-components"></a>Neuinstallation isolierter Komponenten

Windows Das Installationsprogramm führt die folgenden Aktionen während der Neuinstallation einer Anwendung aus, wenn das Paket isolierte Komponenten enthält. In der Regel ist Die \_ freigegebene Komponente eine DLL, die von der Komponentenanwendung und anderen \_ ausführbaren Clientdateien gemeinsam genutzt wird.

## <a name="reinstallation"></a>Neuinstallation

-   Installieren Sie die Dateien von Component Shared nur dann erneut im gleichen Ordner wie die Komponentenanwendung, wenn die \_ \_ \_ Komponentenanwendung ebenfalls neu installiert wird.
-   Erhöhen Sie die Clientliste von Component Shared nicht, und erhöhen Sie nicht \_ die SharedDLL-Anzahl.
-   Erstellen Sie die Null-Byte-Datei mit dem kurzen Dateinamen der Schlüsseldatei der \_ Komponentenanwendung neu. Diese Datei muss sich im gleichen Ordner wie die Komponentenanwendung befinden \_ und die Erweiterung haben. lokal.
-   Installieren Sie alle Ressourcen der \_ Komponentenanwendung wie gewohnt neu.

Wenn der SharedDLL-Refcount für Freigegebene Komponente größer als 1 ist oder andere Produkte in der Clientliste von \_ Component Shared (Freigegebene Komponente) \_ verbleiben:

-   Installieren Sie keine Dateien am freigegebenen Speicherort der Freigegebenen \_ Komponente neu.

Wenn der SharedDLL-Refcount für Die freigegebene Komponente gleich 1 ist oder keine anderen clients von \_ Component Shared (Freigegebene Komponente) noch nicht \_ mehr zur Verfügung stehen:

-   Installieren Sie die Dateien von Component Shared erneut am freigegebenen \_ Speicherort, indem Sie die [Dateiversionsregeln verwenden.](file-versioning-rules.md)
-   Verarbeiten Sie alle Neuinstallationsaktionen für Freigegebene \_ Komponenten.
-   Wenn component Shared eine COM-Komponente ist, registrieren Sie den vollständigen COM-Pfad, damit die Installersyntaxen $Component und FileKey auf den freigegebenen Speicherort von \_ \[ Component Shared \] \[ \# \] \_ zeigen.

 

 



