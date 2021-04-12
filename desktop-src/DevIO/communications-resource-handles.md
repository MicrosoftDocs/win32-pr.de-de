---
description: Ein Prozess verwendet die Funktion "Funktion", um ein Handle für eine Kommunikations Ressource zu öffnen.
ms.assetid: eaef6067-97a6-40c4-84ec-c0d86af6bb4a
title: Kommunikationsressourcenhandles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f709fc041f6125d93a1c52f3e17b77c96f35825c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393086"
---
# <a name="communications-resource-handles"></a><span data-ttu-id="a7f8d-103">Kommunikationsressourcenhandles</span><span class="sxs-lookup"><span data-stu-id="a7f8d-103">Communications Resource Handles</span></span>

<span data-ttu-id="a7f8d-104">Ein Prozess [**verwendet die Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) "Funktion", um ein Handle für eine Kommunikations Ressource zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a7f8d-104">A process uses the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to open a handle to a communications resource.</span></span> <span data-ttu-id="a7f8d-105">Wenn Sie z. b. COM1 angeben, wird ein Handle für einen seriellen Anschluss geöffnet, und LPT1 öffnet ein Handle für einen parallelen Port.</span><span class="sxs-lookup"><span data-stu-id="a7f8d-105">For example, specifying COM1 opens a handle to a serial port, and LPT1 opens a handle to a parallel port.</span></span> <span data-ttu-id="a7f8d-106">Wenn die angegebene Ressource zurzeit von einem anderen Prozess verwendet wird, schlägt " **deatefile** " fehl.</span><span class="sxs-lookup"><span data-stu-id="a7f8d-106">If the specified resource is currently being used by another process, **CreateFile** fails.</span></span> <span data-ttu-id="a7f8d-107">Jeder Thread des Prozesses kann das von " **kreatefile** " zurückgegebene Handle verwenden, um die Ressource in einer der Funktionen zu identifizieren, die auf die Ressource zugreifen.</span><span class="sxs-lookup"><span data-stu-id="a7f8d-107">Any thread of the process can use the handle returned by **CreateFile** to identify the resource in any of the functions that access the resource.</span></span>

<span data-ttu-id="a7f8d-108">Wenn der Prozess " [**kreatefile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) " aufruft, um eine Kommunikations Ressource zu öffnen, gibt er die folgenden Attribute an:</span><span class="sxs-lookup"><span data-stu-id="a7f8d-108">When the process calls [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) to open a communications resource, it specifies the following attributes:</span></span>

-   <span data-ttu-id="a7f8d-109">Der Typ des Lese-/Schreibzugriffs, der für die angegebene Ressource vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a7f8d-109">What type of read/write access exists for the specified resource.</span></span>
-   <span data-ttu-id="a7f8d-110">Gibt an, ob das Handle von untergeordneten Prozessen geerbt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a7f8d-110">Whether the handle can be inherited by child processes.</span></span>
-   <span data-ttu-id="a7f8d-111">Gibt an, ob das Handle in überlappenden (asynchronen) e/a-Vorgängen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a7f8d-111">Whether the handle can be used in overlapped (asynchronous) I/O operations.</span></span> <span data-ttu-id="a7f8d-112">(Eine Beschreibung der überlappenden Vorgänge finden Sie unter [Synchronisierung](/windows/desktop/Sync/synchronization).)</span><span class="sxs-lookup"><span data-stu-id="a7f8d-112">(For a description of overlapped operations, see [Synchronization](/windows/desktop/Sync/synchronization).)</span></span>

<span data-ttu-id="a7f8d-113">Wenn der Prozess zum Öffnen einer Kommunikations Ressource " [**kreatefile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) " verwendet, müssen bestimmte Werte für die folgenden Parameter angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="a7f8d-113">When the process uses [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) to open a communications resource, it must specify certain values for the following parameters:</span></span>

-   <span data-ttu-id="a7f8d-114">Der Parameter " *fidwsharemode* " muss NULL sein, um die Ressource für exklusiven Zugriff zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a7f8d-114">The *fdwShareMode* parameter must be zero, opening the resource for exclusive access.</span></span>
-   <span data-ttu-id="a7f8d-115">Der Parameter " *sdwcreate* " muss das Open \_ vorhandene-Flag angeben.</span><span class="sxs-lookup"><span data-stu-id="a7f8d-115">The *fdwCreate* parameter must specify the OPEN\_EXISTING flag.</span></span>
-   <span data-ttu-id="a7f8d-116">Der *htemplatefile* -Parameter muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="a7f8d-116">The *hTemplateFile* parameter must be **NULL**.</span></span>

<span data-ttu-id="a7f8d-117">Wenn Sie mit " [**anatefile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) " ein Handle direkt auf einem Gerät öffnen, muss eine Anwendung die Sonderzeichen " \\ \\ ." verwenden, \\ um das Gerät zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a7f8d-117">When using [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) to open a handle directly to a device, an application must use the special characters " \\\\ .\\" to identify the device.</span></span> <span data-ttu-id="a7f8d-118">Um z. b. ein Handle zum Steuern eines zu öffnen, geben Sie an \\ \\ . \\ a: für den *lpszname* -Parameter von " **kreatefile**".</span><span class="sxs-lookup"><span data-stu-id="a7f8d-118">For example, to open a handle to drive A, specify \\\\ .\\a: for the *lpszName* parameter of **CreateFile**.</span></span> <span data-ttu-id="a7f8d-119">Der aufrufenden Prozess kann das Handle in der [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) -Funktion verwenden, um Steuerungs Codes an das Gerät zu senden.</span><span class="sxs-lookup"><span data-stu-id="a7f8d-119">The calling process can use the handle in the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function to send control codes to the device.</span></span>

 

 
