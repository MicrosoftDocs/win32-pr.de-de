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
# <a name="obtaining-a-volume-handle-for-change-journal-operations"></a><span data-ttu-id="69ef5-103">Abrufen eines Volumehandles für Änderungs Journal Vorgänge</span><span class="sxs-lookup"><span data-stu-id="69ef5-103">Obtaining a Volume Handle for Change Journal Operations</span></span>

<span data-ttu-id="69ef5-104">Rufen Sie zum Abrufen eines Handles für ein Volume zur Verwendung mit Aktualisierungs Zeichenfolgenvorgängen (Update Sequence Number, Aktualisierungs Sequenznummer) die Funktion "| [**atefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) " mit dem Parameter " *lpFileName* " auf, die auf eine Zeichenfolge in der folgenden Form \\ \\ \\ *X*:</span><span class="sxs-lookup"><span data-stu-id="69ef5-104">To obtain a handle to a volume for use with update sequence number (USN) change journal operations, call the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function with the *lpFileName* parameter set to a string of the following form: \\\\.\\*X*:</span></span>

<span data-ttu-id="69ef5-105">Beachten Sie, dass *X* der Buchstabe ist, der das Laufwerk identifiziert, auf dem das NTFS-Volume angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="69ef5-105">Note that *X* is the letter that identifies the drive on which the NTFS volume appears.</span></span>

<span data-ttu-id="69ef5-106">Wenn das Volume keinen Laufwerk Buchstaben aufweist, verwenden Sie die unter [Benennen eines](naming-a-volume.md)Volumes beschriebene Syntax.</span><span class="sxs-lookup"><span data-stu-id="69ef5-106">If the volume does not have a drive letter, use the syntax described in [Naming a Volume](naming-a-volume.md).</span></span>

 

 



