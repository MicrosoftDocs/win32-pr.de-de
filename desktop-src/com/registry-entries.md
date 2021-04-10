---
title: Registrierungseinträge (com)
ms.assetid: f4f8875c-6416-4919-b49b-bcd675efcbd2
description: Weitere Informationen finden Sie in den Registrierungs Einträgen (com).
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368e9eb5e4c2174c5b4b90df6586b58135085c5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127569"
---
# <a name="registry-entries-com"></a><span data-ttu-id="6ed41-103">Registrierungseinträge (com)</span><span class="sxs-lookup"><span data-stu-id="6ed41-103">Registry Entries (COM)</span></span>

<span data-ttu-id="6ed41-104">Registrierungs Werte in den folgenden Registrierungs Schlüsseln steuern Aspekte der com-Funktionalität:</span><span class="sxs-lookup"><span data-stu-id="6ed41-104">Registry values in the following registry keys control aspects of the functionality of COM:</span></span>

-   [<span data-ttu-id="6ed41-105">**HKEY \_ - \_ \\ Software \\ Klassen für lokale Computer**</span><span class="sxs-lookup"><span data-stu-id="6ed41-105">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes**</span></span>](hkey-local-machine-software-classes.md)
-   [<span data-ttu-id="6ed41-106">**HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ OLE**</span><span class="sxs-lookup"><span data-stu-id="6ed41-106">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Ole**</span></span>](hkey-local-machine-software-microsoft-ole.md)
-   [<span data-ttu-id="6ed41-107">**HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion**</span><span class="sxs-lookup"><span data-stu-id="6ed41-107">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion**</span></span>](hkey-local-machine-software-microsoft-windows-nt-currentversion.md)

<span data-ttu-id="6ed41-108">Ab Windows Server 2003 verwendet com nur das aktuelle Prozess Token, um zu entscheiden, auf welche Registrierungs Struktur zugegriffen werden soll, und nicht auf das Thread Token.</span><span class="sxs-lookup"><span data-stu-id="6ed41-108">As of Windows Server 2003, COM uses only the current process token to decide which registry hive to access, not the thread token.</span></span> <span data-ttu-id="6ed41-109">Wenn com nicht auf die Benutzerprofil-Registrierungs Struktur zugreifen kann, wird auf die **System Struktur des \_ lokalen \_ \\ HKEY** -Computers zugegriffen.</span><span class="sxs-lookup"><span data-stu-id="6ed41-109">If COM is not able to access the user profile registry hive, it will access the **HKEY\_LOCAL\_MACHINE\\System** hive.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ed41-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6ed41-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ed41-111">Registrierung</span><span class="sxs-lookup"><span data-stu-id="6ed41-111">Registry</span></span>](/windows/desktop/SysInfo/registry)
</dt> </dl>

 

 
