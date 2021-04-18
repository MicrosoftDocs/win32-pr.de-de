---
description: Sie können einem lokalen Volume einen Laufwerk Buchstaben (z. b. X:) zuweisen \) , indem Sie die setvolumemountpoint-Funktion verwenden, vorausgesetzt, dass diesem Laufwerk Buchstaben nicht bereits ein Volume zugeordnet ist.
ms.assetid: 8c78b2e8-199a-4934-a9c4-6f3913f44efe
title: Zuweisen eines Laufwerk Buchstabens zu einem Volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f31b9446cc41ad26f14a34874c59e153e1db8ce5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343416"
---
# <a name="assigning-a-drive-letter-to-a-volume"></a><span data-ttu-id="96ab8-103">Zuweisen eines Laufwerk Buchstabens zu einem Volume</span><span class="sxs-lookup"><span data-stu-id="96ab8-103">Assigning a Drive Letter to a Volume</span></span>

<span data-ttu-id="96ab8-104">Sie können einem lokalen Volume einen Laufwerk Buchstaben (z. b. X:) zuweisen \) , indem Sie die [**setvolumemountpoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) -Funktion verwenden, vorausgesetzt, dass diesem Laufwerk Buchstaben nicht bereits ein Volume zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="96ab8-104">You can assign a drive letter (for example, X:\) to a local volume by using the [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) function, provided there is no volume already assigned to that drive letter.</span></span> <span data-ttu-id="96ab8-105">, Wenn das lokale Volume bereits über einen Laufwerk Buchstaben verfügt.</span><span class="sxs-lookup"><span data-stu-id="96ab8-105">If the local volume already has a drive letter.</span></span> <span data-ttu-id="96ab8-106">[**setvolumemountpoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="96ab8-106">then [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) will fail.</span></span> <span data-ttu-id="96ab8-107">Um dies zu behandeln, löschen Sie zuerst den Laufwerk Buchstaben mithilfe der [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="96ab8-107">To handle this, first delete the drive letter by using the [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) function.</span></span> <span data-ttu-id="96ab8-108">Beispielcode finden Sie unter [Bearbeiten von Laufwerk Buchstaben Zuweisungen](editing-drive-letter-assignments.md).</span><span class="sxs-lookup"><span data-stu-id="96ab8-108">For example code, see [Editing Drive Letter Assignments](editing-drive-letter-assignments.md).</span></span>

<span data-ttu-id="96ab8-109">Das System unterstützt höchstens einen Laufwerk Buchstaben pro Volume.</span><span class="sxs-lookup"><span data-stu-id="96ab8-109">The system supports at most one drive letter per volume.</span></span> <span data-ttu-id="96ab8-110">Daher ist es nicht möglich, dass C: \\ und F: \\ dasselbe Volume darstellen.</span><span class="sxs-lookup"><span data-stu-id="96ab8-110">Therefore, you cannot have C:\\ and F:\\ represent the same volume.</span></span>

> [!Caution]
>
> <span data-ttu-id="96ab8-111">Wenn Sie einen vorhandenen Laufwerk Buchstaben löschen und einen neuen zuweisen, können vorhandene Pfade, z. b. die in Desktop Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="96ab8-111">Deleting an existing drive letter and assigning a new one may break existing paths, such as those in desktop shortcuts.</span></span> <span data-ttu-id="96ab8-112">Möglicherweise wird auch der Pfad des Programms unterbrechen, sodass der Laufwerksbuchstabe geändert wird.</span><span class="sxs-lookup"><span data-stu-id="96ab8-112">It may also break the path to the program making the drive letter changes.</span></span> <span data-ttu-id="96ab8-113">Mit der Verwaltung von virtuellen Windows-Arbeitsspeicher kann dies die Anwendung unterbrechen, sodass das System instabil und möglicherweise unbrauchbar ist.</span><span class="sxs-lookup"><span data-stu-id="96ab8-113">With Windows virtual memory management, this may break the application, leaving the system in an unstable and possibly unusable state.</span></span> <span data-ttu-id="96ab8-114">Der Programm-Designer ist dafür verantwortlich, derartige potenzielle Katastrophen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="96ab8-114">It is the program designer's responsibility to avoid such potential catastrophes.</span></span>

 

 

 



