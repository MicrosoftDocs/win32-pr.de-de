---
description: Jeder Named Pipe hat einen eindeutigen Namen, der ihn von anderen benannten Pipes in der System Liste benannter Objekte unterscheidet. Ein pipenserver gibt einen Namen für die Pipe an, wenn die Funktion "" die Funktion "" erstellt, um eine oder mehrere Instanzen einer Named Pipe zu erstellen.
ms.assetid: 8f7e717a-648b-421e-ab79-a4abbae670be
title: Pipenamen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e470a09fa4cfe1b2f259ca3fd5b53f79045787fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352286"
---
# <a name="pipe-names"></a><span data-ttu-id="de3f8-104">Pipenamen</span><span class="sxs-lookup"><span data-stu-id="de3f8-104">Pipe Names</span></span>

<span data-ttu-id="de3f8-105">Jede Named Pipe hat einen eindeutigen Namen, der Sie von anderen benannten Pipes in der Liste benannter Objekte des Systems unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="de3f8-105">Each named pipe has a unique name that distinguishes it from other named pipes in the system's list of named objects.</span></span> <span data-ttu-id="de3f8-106">Ein pipenserver gibt einen Namen für die Pipe an, wenn [**die Funktion "**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) " die Funktion "" erstellt, um eine oder mehrere Instanzen einer Named Pipe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="de3f8-106">A pipe server specifies a name for the pipe when it calls the [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) function to create one or more instances of a named pipe.</span></span> <span data-ttu-id="de3f8-107">Pipe-Clients geben den Pipenamen an, wenn Sie die Funktion "up [**" oder "**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) [**callnamedpipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) " aufrufen, um eine Verbindung mit einer Instanz des Named Pipe herzustellen.</span><span class="sxs-lookup"><span data-stu-id="de3f8-107">Pipe clients specify the pipe name when they call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) or [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) function to connect to an instance of the named pipe.</span></span>

<span data-ttu-id="de3f8-108">Verwenden Sie das folgende Formular, wenn Sie den Namen einer Pipe in der Funktion "up- [**File**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)", " [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea)" oder " [**callnamedpipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) " angeben:</span><span class="sxs-lookup"><span data-stu-id="de3f8-108">Use the following form when specifying the name of a pipe in the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea), or [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) function:</span></span>

<span data-ttu-id="de3f8-109">\\\\*Servername* \\ \\*Pipename* der Pipe</span><span class="sxs-lookup"><span data-stu-id="de3f8-109">\\\\*ServerName*\\pipe\\*PipeName*</span></span>

<span data-ttu-id="de3f8-110">Dabei ist *Server* Name entweder der Name eines Remote Computers oder ein Zeitraum, um den lokalen Computer anzugeben.</span><span class="sxs-lookup"><span data-stu-id="de3f8-110">where *ServerName* is either the name of a remote computer or a period, to specify the local computer.</span></span> <span data-ttu-id="de3f8-111">Die von *Pipename* angegebene Pipe-namens Zeichenfolge kann ein beliebiges Zeichen enthalten, das kein umgekehrter Schrägstrich ist, einschließlich Zahlen und Sonderzeichen.</span><span class="sxs-lookup"><span data-stu-id="de3f8-111">The pipe name string specified by *PipeName* can include any character other than a backslash, including numbers and special characters.</span></span> <span data-ttu-id="de3f8-112">Die Zeichenfolge für den gesamten Pipenamen kann bis zu 256 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="de3f8-112">The entire pipe name string can be up to 256 characters long.</span></span> <span data-ttu-id="de3f8-113">Bei Pipenamen wird die Groß-/Kleinschreibung nicht beachtet</span><span class="sxs-lookup"><span data-stu-id="de3f8-113">Pipe names are not case-sensitive.</span></span>

<span data-ttu-id="de3f8-114">Der Pipeserver kann eine Pipe nicht auf einem anderen Computer erstellen, daher muss " [**anatenamedpipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) " einen Punkt für den Servernamen verwenden, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="de3f8-114">The pipe server cannot create a pipe on another computer, so [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) must use a period for the server name, as shown in the following example.</span></span>

<span data-ttu-id="de3f8-115">\\\\.\\ \\*Pipename* der Pipe</span><span class="sxs-lookup"><span data-stu-id="de3f8-115">\\\\.\\pipe\\*PipeName*</span></span>

<span data-ttu-id="de3f8-116">Ein Pipeserver kann den Pipenamen an die Pipe-Clients bereitstellen, sodass er eine Verbindung mit der Pipe herstellen kann.</span><span class="sxs-lookup"><span data-stu-id="de3f8-116">A pipe server can provide the pipe name to its pipe clients, so they can connect to the pipe.</span></span> <span data-ttu-id="de3f8-117">Der Pipeclient ermittelt den Pipenamen aus einer permanenten Quelle, z. b. einem Registrierungs Eintrag, einer Datei oder einer anderen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="de3f8-117">The pipe client discovers the pipe name from some persistent source, such as a registry entry, a file, or another application.</span></span> <span data-ttu-id="de3f8-118">Andernfalls müssen die Clients den Pipenamen zum Zeitpunkt der Kompilierung kennen.</span><span class="sxs-lookup"><span data-stu-id="de3f8-118">Otherwise, the clients must know the pipe name at compile time.</span></span>

 

 
