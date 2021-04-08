---
description: In den Flussdiagrammen in den folgenden Abschnitten werden die Standardregeln für die Datei Versionsverwaltung veranschaulicht, die verwendet werden, wenn die Schlüsseldatei einer installierten Komponente den gleichen Namen wie eine Datei hat, die bereits am Ziel Speicherort installiert ist.
ms.assetid: a09e091c-ee82-4951-b129-d1d4c8948883
title: Standardmäßige Datei Versionsverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fad33a7af49c28b560d9d558abbc86b220c4cb42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866360"
---
# <a name="default-file-versioning"></a>Standardmäßige Datei Versionsverwaltung

In den Flussdiagrammen in den folgenden Abschnitten werden die Standardregeln für die Datei Versionsverwaltung veranschaulicht, die verwendet werden, wenn die Schlüsseldatei einer installierten Komponente den gleichen Namen wie eine Datei hat, die bereits am Ziel Speicherort installiert ist. Die Standarddatei Versionsverwaltung wird auch unter [Ersetzen vorhandener Dateien](replacing-existing-files.md)veranschaulicht.

Beachten Sie, dass mit Windows Installer Datei Hashwert zur Optimierung des Kopierens von Dateien verfügbar ist. Weitere Informationen finden Sie unter [**msigetflehash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) und in der [Tabelle msigetfash](msifilehash-table.md). Die msiflehash-Tabelle kann nur mit Dateien ohne Versions Angabe verwendet werden.

-   [Beide Dateien haben eine Version.](both-files-have-a-version.md)
-   [Keine der Dateien hat eine Version.](neither-file-has-a-version.md)
-   [Keine der Dateien weist eine Version mit Datei Hash Überprüfung auf.](neither-file-has-a-version-with-file-hash-check.md)
-   [Eine Datei hat eine Version.](one-file-has-a-version.md)

 

 



