---
title: Nachverfolgen von geänderten Bereichen einer Datei
description: Nachverfolgen von geänderten Bereichen einer Datei
ms.assetid: 756881E9-EFD0-42FE-9B1C-4A2EF1998D71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664e7a5c0a9148471d2a1a28f2881e1c375089c1
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "106337878"
---
# <a name="tracking-modified-ranges-of-a-file"></a><span data-ttu-id="76aad-103">Nachverfolgen von geänderten Bereichen einer Datei</span><span class="sxs-lookup"><span data-stu-id="76aad-103">Tracking modified ranges of a file</span></span>

## <a name="platforms"></a><span data-ttu-id="76aad-104">Plattformen</span><span class="sxs-lookup"><span data-stu-id="76aad-104">Platforms</span></span>

<span data-ttu-id="76aad-105">**Clients:** Windows 8.1 (alle SKUs)</span><span class="sxs-lookup"><span data-stu-id="76aad-105">**Clients -** Windows 8.1 (all SKUs)</span></span>  
<span data-ttu-id="76aad-106">**Server:** Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="76aad-106">**Servers -** Windows Server 2012 R2</span></span>  

## <a name="description"></a><span data-ttu-id="76aad-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="76aad-107">Description</span></span>

<span data-ttu-id="76aad-108">Das NTFS-Team (NT File System) hat Windows ein neues Feature hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="76aad-108">The NT File System (NTFS) team has added a new feature to Windows.</span></span> <span data-ttu-id="76aad-109">Das Daten Journal gibt einen Update Sequenznummern-Datensatz (Update Sequence Number, d) mit geänderten Bereichen für eine Datei nach dem Schließen aus.</span><span class="sxs-lookup"><span data-stu-id="76aad-109">USN Journal will output an update sequence number (USN) record containing modified ranges for a file upon close.</span></span> <span data-ttu-id="76aad-110">Ein neuer Daten Recordtyp wurde \_ eingeführt, \_ um die geänderten Bereiche einer Datei aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="76aad-110">A new record type, USN\_RECORD\_V4 has been introduced to record these changed ranges of a file.</span></span>

<span data-ttu-id="76aad-111">Die Funktion ist standardmäßig nicht aktiviert. Benutzer müssen einen Befehl für die Dateisystem Steuerung (FSCTL) aufrufen, um Sie zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="76aad-111">The feature is not enabled by default; users must invoke a file system control (FSCTL) command to enable it.</span></span> <span data-ttu-id="76aad-112">Da jedoch andere Windows-Komponenten die Bereichs Überwachung aktivieren können, können Benutzer und Entwickler erkennen, dass die Funktion immer aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="76aad-112">However, because other Windows components may turn on range tracking, users and developers may perceive that the feature is always enabled.</span></span> <span data-ttu-id="76aad-113">Mit Windows können Entwickler das Anwendungs Journal Abfragen, um herauszufinden, ob die Bereichs Überwachung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="76aad-113">Windows will allow developers to query USN journal to find out if range tracking is enabled.</span></span>

<span data-ttu-id="76aad-114">Die MSDN-Dokumentation wird zu einem späteren Zeitpunkt bereitgestellt, um Entwicklern den Zugriff auf die \_ \_ Datensätze der Datensätze von Datensätzen in der Version Version</span><span class="sxs-lookup"><span data-stu-id="76aad-114">MSDN documentation will be provided at a later date to instruct developers in how to access USN\_RECORD\_V4 records.</span></span>

## <a name="manifestation"></a><span data-ttu-id="76aad-115">Ausstrahlung</span><span class="sxs-lookup"><span data-stu-id="76aad-115">Manifestation</span></span>

<span data-ttu-id="76aad-116">Alle vorhandenen Anwendungen, die das Anwendungs Journal verwenden, funktionieren weiterhin problemlos ohne Kompatibilitätsprobleme.</span><span class="sxs-lookup"><span data-stu-id="76aad-116">All existing applications that use USN Journal will continue to work well without any compatibility issues.</span></span>

 

 




