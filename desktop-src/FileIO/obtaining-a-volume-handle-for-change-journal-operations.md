---
description: Rufen Sie zum Abrufen eines Handles für ein Volume zur Verwendung mit Aktualisierungs Zeichenfolgenvorgängen (Update Sequence Number, Aktualisierungs Sequenznummer) die Funktion "| atefile" mit dem Parameter "lpFileName" auf, die auf eine Zeichenfolge in der folgenden Form \\ \\ \\ Stuben.
ms.assetid: a4f4dac5-76fd-4e9e-a71e-665684840d74
title: Abrufen eines Volumehandles für Änderungs Journal Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8036fc642de52aa2d7f9bab66dd2e380dcc070c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360880"
---
# <a name="obtaining-a-volume-handle-for-change-journal-operations"></a>Abrufen eines Volumehandles für Änderungs Journal Vorgänge

Rufen Sie zum Abrufen eines Handles für ein Volume zur Verwendung mit Aktualisierungs Zeichenfolgenvorgängen (Update Sequence Number, Aktualisierungs Sequenznummer) die Funktion "| [**atefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) " mit dem Parameter " *lpFileName* " auf, die auf eine Zeichenfolge in der folgenden Form \\ \\ \\ *X*:

Beachten Sie, dass *X* der Buchstabe ist, der das Laufwerk identifiziert, auf dem das NTFS-Volume angezeigt wird.

Wenn das Volume keinen Laufwerk Buchstaben aufweist, verwenden Sie die unter [Benennen eines](naming-a-volume.md)Volumes beschriebene Syntax.

 

 



