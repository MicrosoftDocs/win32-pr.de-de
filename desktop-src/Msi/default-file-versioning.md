---
description: Die Flussdiagramme in den folgenden Abschnitten veranschaulichen die Standardregeln für die Dateiversionsversion, die verwendet werden, wenn die Schlüsseldatei einer komponente, die installiert wird, den gleichen Namen hat wie eine Datei, die bereits am Zielspeicherort installiert ist.
ms.assetid: a09e091c-ee82-4951-b129-d1d4c8948883
title: Standarddateiversionseinstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c239cd7989308e79dbb0ee621241560ac33a7a049c83c0a44d2cb1c3c32f5fb0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039990"
---
# <a name="default-file-versioning"></a>Standarddateiversionseinstellungen

Die Flussdiagramme in den folgenden Abschnitten veranschaulichen die Standardregeln für die Dateiversionsversion, die verwendet werden, wenn die Schlüsseldatei einer komponente, die installiert wird, den gleichen Namen hat wie eine Datei, die bereits am Zielspeicherort installiert ist. Die Standarddateiversionsierung wird auch unter [Ersetzen vorhandener Dateien veranschaulicht.](replacing-existing-files.md)

Beachten Sie, dass Windows Installer dateihashing verfügbar ist, um das Kopieren von Dateien zu optimieren. Weitere Informationen finden Sie unter [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) und in der [MsiFileHash-Tabelle.](msifilehash-table.md) Die MsiFileHash-Tabelle kann nur mit Nichtversionsdateien verwendet werden.

-   [Beide Dateien verfügen über eine Version](both-files-have-a-version.md)
-   [Keine der Dateien verfügt über eine Version](neither-file-has-a-version.md)
-   [Keine der Dateien verfügt über eine Version mit Dateihashüberprüfung](neither-file-has-a-version-with-file-hash-check.md)
-   [Eine Datei verfügt über eine Version](one-file-has-a-version.md)

 

 



