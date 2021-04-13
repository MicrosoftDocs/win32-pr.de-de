---
description: Jede Datei und jedes Verzeichnis auf einem Volume, das die Komprimierung für einzelne Dateien und Verzeichnisse unterstützt, hat einen Komprimierungs Status.
ms.assetid: 9db1b2e2-864e-45b5-8227-400cad75222e
title: Komprimierungs Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e182921a6c5e1b79c08fbafb6a8104c4bd8ca1cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216251"
---
# <a name="compression-state"></a><span data-ttu-id="684c0-103">Komprimierungs Status</span><span class="sxs-lookup"><span data-stu-id="684c0-103">Compression State</span></span>

<span data-ttu-id="684c0-104">Jede Datei und jedes Verzeichnis auf einem Volume, das die Komprimierung für einzelne Dateien und Verzeichnisse unterstützt, hat einen *Komprimierungs Status*.</span><span class="sxs-lookup"><span data-stu-id="684c0-104">Each file and directory on a volume that supports compression for individual files and directories has a *compression state*.</span></span>

<span data-ttu-id="684c0-105">Während das Komprimierungs Attribut einer Datei oder eines Verzeichnisses lediglich angibt, ob die Datei oder das Verzeichnis komprimiert oder nicht komprimiert ist, wird im Komprimierungs Status auch das Format aller komprimierten Daten angegeben.</span><span class="sxs-lookup"><span data-stu-id="684c0-105">Whereas the compression attribute of a file or directory indicates simply whether the file or directory is compressed or not compressed, the compression state also specifies the format of any compressed data.</span></span>

<span data-ttu-id="684c0-106">Verwenden Sie den Code für die [**FSCTL- \_ \_ Komprimierung**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) , um den Komprimierungs Status einer Datei oder eines Verzeichnisses zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="684c0-106">Use the [**FSCTL\_GET\_COMPRESSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) control code to determine the compression state of a file or directory.</span></span>

<span data-ttu-id="684c0-107">Der Komprimierungs Status wird als 16-Bit-Wert codiert.</span><span class="sxs-lookup"><span data-stu-id="684c0-107">Compression state is encoded as a 16-bit value.</span></span> <span data-ttu-id="684c0-108">Der Komprimierungs Statuswert " \_ \_ None" gibt an, dass eine Datei nicht komprimiert ist.</span><span class="sxs-lookup"><span data-stu-id="684c0-108">A compression state value of COMPRESSION\_FORMAT\_NONE indicates that a file is not compressed.</span></span> <span data-ttu-id="684c0-109">Der Standardwert für das Komprimierungs \_ Format \_ gibt an, dass eine Datei mit dem Standard Komprimierungs Format komprimiert wird.</span><span class="sxs-lookup"><span data-stu-id="684c0-109">A value of COMPRESSION\_FORMAT\_DEFAULT indicates that a file is compressed, using the default compression format.</span></span> <span data-ttu-id="684c0-110">Jeder andere Wert gibt an, dass eine Datei komprimiert wird. dabei wird das vom Komprimierungs Zustandswert angegebene Komprimierungs Format verwendet.</span><span class="sxs-lookup"><span data-stu-id="684c0-110">Any other value indicates that a file is compressed, using the compression format specified by the compression state value.</span></span>

<span data-ttu-id="684c0-111">Verwenden Sie den Code für die [**\_ \_ Komprimierung des FSCTL-Satzes**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) , um den Komprimierungs Status einer Datei oder eines Verzeichnisses festzulegen.</span><span class="sxs-lookup"><span data-stu-id="684c0-111">Use the [**FSCTL\_SET\_COMPRESSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) control code to set the compression state of a file or directory.</span></span> <span data-ttu-id="684c0-112">Mit diesem Vorgang wird auch das Komprimierungs Attribut der Datei oder des Verzeichnisses festgelegt.</span><span class="sxs-lookup"><span data-stu-id="684c0-112">This operation also sets the compression attribute of the file or directory.</span></span>

<span data-ttu-id="684c0-113">Wenn Sie den Komprimierungs Status einer Datei auf einen Wert ungleich 0 (null) festlegen, wird die Datei mit dem Komprimierungs Format komprimiert, das durch den Komprimierungs Zustandswert codiert ist</span><span class="sxs-lookup"><span data-stu-id="684c0-113">Setting the compression state of a file to a nonzero value compresses the file, using the compression format encoded by the compression state value.</span></span> <span data-ttu-id="684c0-114">Wenn Sie den Komprimierungs Status einer Datei auf NULL festlegen, wird die Datei von dekomprimiert.</span><span class="sxs-lookup"><span data-stu-id="684c0-114">Setting a file's compression state to zero decompresses the file.</span></span> <span data-ttu-id="684c0-115">Dies sind synchrone Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="684c0-115">These are synchronous operations.</span></span> <span data-ttu-id="684c0-116">Wenn Sie den Komprimierungs Status festlegen, wird die Datei sofort komprimiert oder dekomprimiert.</span><span class="sxs-lookup"><span data-stu-id="684c0-116">The file is compressed or decompressed immediately when you set its compression state.</span></span>

<span data-ttu-id="684c0-117">Das Festlegen des Komprimierungs Zustands eines Verzeichnisses führt nicht zu einer sofortigen Komprimierung oder Komprimierung.</span><span class="sxs-lookup"><span data-stu-id="684c0-117">Setting a directory's compression state does not cause any immediate compression or decompression.</span></span> <span data-ttu-id="684c0-118">Stattdessen wird beim Festlegen des Komprimierungs Zustands eines Verzeichnisses ein Standard Komprimierungs Status festgelegt, der allen neu erstellten Dateien und Unterverzeichnissen zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="684c0-118">Instead, setting a directory's compression state sets a default compression state that will be given to all newly created files and subdirectories.</span></span>

 

 
