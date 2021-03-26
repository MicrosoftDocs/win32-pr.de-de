---
title: Prozessinformationen
description: Das System verwaltet eine Liste der laufenden Prozesse. Sie können die Bezeichner für diese Prozesse abrufen, indem Sie die EnumProcesses-Funktion aufrufen. Diese Funktion füllt ein Array von DWORD-Werten mit den bezeichgern aller Prozesse im System.
ms.assetid: 229c661e-9c33-47a3-9441-558cfe2a800d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 147debe36dd2647cd46d19a62b0374f47b73bc58
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315554"
---
# <a name="process-information"></a><span data-ttu-id="8f6cd-105">Prozessinformationen</span><span class="sxs-lookup"><span data-stu-id="8f6cd-105">Process Information</span></span>

<span data-ttu-id="8f6cd-106">Das System verwaltet eine Liste der laufenden Prozesse.</span><span class="sxs-lookup"><span data-stu-id="8f6cd-106">The system maintains a list of running processes.</span></span> <span data-ttu-id="8f6cd-107">Sie können die Bezeichner für diese Prozesse abrufen, indem Sie die [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8f6cd-107">You can retrieve the identifiers for these processes by calling the [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) function.</span></span> <span data-ttu-id="8f6cd-108">Diese Funktion füllt ein Array von **DWORD** -Werten mit den bezeichgern aller Prozesse im System.</span><span class="sxs-lookup"><span data-stu-id="8f6cd-108">This function fills an array of **DWORD** values with the identifiers of all processes in the system.</span></span>

<span data-ttu-id="8f6cd-109">Viele Funktionen in PSAPI erfordern ein Prozess handle.</span><span class="sxs-lookup"><span data-stu-id="8f6cd-109">Many functions in PSAPI require a process handle.</span></span> <span data-ttu-id="8f6cd-110">Wenn Sie ein Prozess Handle für einen laufenden Prozess abrufen möchten, übergeben Sie die Prozess-ID (abgerufen von [**enumprozessen**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses)) an die [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="8f6cd-110">To obtain a process handle for a running process, pass its process identifier (obtained from [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses)) to the [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) function.</span></span> <span data-ttu-id="8f6cd-111">Denken Sie daran, die [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) -Funktion aufzurufen, wenn Sie mit dem Prozess handle fertig sind.</span><span class="sxs-lookup"><span data-stu-id="8f6cd-111">Remember to call the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function when you are finished with the process handle.</span></span>

 

 