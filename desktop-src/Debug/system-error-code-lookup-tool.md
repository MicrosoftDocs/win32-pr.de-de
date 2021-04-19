---
description: Beschreibt, wie Sie mit dem Microsoft Error Lookup-Tool Texterklärungen von hexadezimalen Fehlercodes in Windows finden.
title: Das Microsoft-Tool zur Fehlersuche
ms.topic: article
ms.date: 12/4/2019
ms.openlocfilehash: e39b5623458fc176f5ecc81eae71212ba279945c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342985"
---
# <a name="the-microsoft-error-lookup-tool"></a><span data-ttu-id="99dff-103">Das Microsoft-Tool zur Fehlersuche</span><span class="sxs-lookup"><span data-stu-id="99dff-103">The Microsoft Error Lookup Tool</span></span>

<span data-ttu-id="99dff-104">Das Microsoft-Tool für die Fehlersuche zeigt den Meldungs Text an, der einem hexadezimalen Statuscode (oder anderem Code) zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="99dff-104">The Microsoft Error Lookup Tool displays the message text that is associated with a hexadecimal status code (or other code).</span></span> <span data-ttu-id="99dff-105">Dieser Text wird in verschiedenen Microsoft-Quell Code Headern definiert, wie z. b. "Winerror. h", "Setupapi. h" usw.</span><span class="sxs-lookup"><span data-stu-id="99dff-105">This text is defined in various Microsoft source-code header files, such as Winerror.h, Setupapi.h, and so on.</span></span>

<span data-ttu-id="99dff-106">Das Tool wird von Microsoft digital signiert.</span><span class="sxs-lookup"><span data-stu-id="99dff-106">The tool is digitally signed by Microsoft.</span></span> <span data-ttu-id="99dff-107">Im folgenden finden Sie die SHA256-Informationen zum Herunterladen von Dateien:</span><span class="sxs-lookup"><span data-stu-id="99dff-107">The following is the SHA256 information for the file download:</span></span>  

|<span data-ttu-id="99dff-108">Algorithmus</span><span class="sxs-lookup"><span data-stu-id="99dff-108">Algorithm</span></span> |<span data-ttu-id="99dff-109">Hash</span><span class="sxs-lookup"><span data-stu-id="99dff-109">Hash</span></span> |
| --- | --- |
|<span data-ttu-id="99dff-110">SHA256</span><span class="sxs-lookup"><span data-stu-id="99dff-110">SHA256</span></span> |<span data-ttu-id="99dff-111">88739ec82ba16a0b4a3c83c1dd2f ca6336ad8e2a1e5b1238c085b1e86ab8834a</span><span class="sxs-lookup"><span data-stu-id="99dff-111">88739EC82BA16A0B4A3C83C1DD2FCA6336AD8E2A1E5F1238C085B1E86AB8834A</span></span> |

> [!NOTE]
> <span data-ttu-id="99dff-112">Geschäftsumgebungen können einschränken, welche Dateien ausgeführt werden können und von wo aus.</span><span class="sxs-lookup"><span data-stu-id="99dff-112">Business environments may restrict which files can run and from where.</span></span> <span data-ttu-id="99dff-113">Bevor Sie dieses Tool herunterladen und ausführen, überprüfen Sie die folgenden Details:</span><span class="sxs-lookup"><span data-stu-id="99dff-113">Before you download and run this tool, check the following details:</span></span>
> - <span data-ttu-id="99dff-114">Müssen Sie über eine Berechtigung oder eine Sicherheits Ausnahme verfügen, damit das Tool heruntergeladen oder ausgeführt werden kann?</span><span class="sxs-lookup"><span data-stu-id="99dff-114">Do you have to have permission or a security exception in order to download or run the tool?</span></span>
> - <span data-ttu-id="99dff-115">Können Sie dieses Tool auf Ihrem Computer speichern und ausführen (z. b. im Ordner "Dokumente")?</span><span class="sxs-lookup"><span data-stu-id="99dff-115">Can you store and run this tool on your computer (for example, in your Documents folder)?</span></span> <span data-ttu-id="99dff-116">Oder müssen Sie das Tool auf einem spezialisierten Computer, z. b. einem zentralen Dateiserver, speichern und ausführen?</span><span class="sxs-lookup"><span data-stu-id="99dff-116">Or do you have to store and run the tool on a specialized computer, such as a central file server?</span></span>

## <a name="usage"></a><span data-ttu-id="99dff-117">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="99dff-117">Usage</span></span>

1. <span data-ttu-id="99dff-118">Wählen Sie [diesen Link](https://download.microsoft.com/download/4/3/2/432140e8-fb6c-4145-8192-25242838c542/Err_6.4.5/Err_6.4.5.exe)aus, um das Tool herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="99dff-118">Download the tool by selecting [this link](https://download.microsoft.com/download/4/3/2/432140e8-fb6c-4145-8192-25242838c542/Err_6.4.5/Err_6.4.5.exe).</span></span>
1. <span data-ttu-id="99dff-119">Wenn Sie in Schritt 1 keinen Speicherort angegeben haben, navigieren Sie zu Ihrem Downloadordner, und kopieren oder verschieben Sie die heruntergeladene Datei (Err_6.4.5.exe) in den Ordner, in dem Sie das Tool speichern.</span><span class="sxs-lookup"><span data-stu-id="99dff-119">If you didn't specify a location in step 1, go to your download folder, and copy or move the downloaded file (Err_6.4.5.exe) to folder in which you will store the tool.</span></span> <span data-ttu-id="99dff-120">Sie müssen die Datei nicht erweitern oder installieren.</span><span class="sxs-lookup"><span data-stu-id="99dff-120">You do not have to expand or install the file.</span></span>
   > [!NOTE]
   > <span data-ttu-id="99dff-121">Wenn Sie die Datei in einen Ordner kopieren oder verschieben, der in der **path** -Umgebungsvariable Ihres Betriebssystems aufgeführt ist, funktioniert Sie an jeder Eingabeaufforderung.</span><span class="sxs-lookup"><span data-stu-id="99dff-121">If you copy or move the file to a folder that is listed in your operating system's **Path** environment variable, it will work at any command prompt.</span></span>

1. <span data-ttu-id="99dff-122">Öffnen Sie ein Eingabeaufforderungsfenster.</span><span class="sxs-lookup"><span data-stu-id="99dff-122">Open a Command Prompt window.</span></span> <span data-ttu-id="99dff-123">Ändern Sie ggf. das Verzeichnis in den Speicherort des Tools für die Fehlersuche.</span><span class="sxs-lookup"><span data-stu-id="99dff-123">If necessary, change the directory to the location of the Error Lookup Tool.</span></span>
1. <span data-ttu-id="99dff-124">Führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="99dff-124">Run the following command:</span></span>
   ```cmd
   Err_6.4.5.exe <error code>
   ```
   > [!NOTE]  
   > <span data-ttu-id="99dff-125">In diesem Befehl \<*error code*> stellt den Hexadezimal Code dar, den Sie suchen möchten.</span><span class="sxs-lookup"><span data-stu-id="99dff-125">In this command, \<*error code*> represents the hexadecimal code that you want to look up.</span></span>

## <a name="examples"></a><span data-ttu-id="99dff-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="99dff-126">Examples</span></span>

```cmd
C:\Tools>Err_6.4.5.exe c000021a
# for hex 0xc000021a / decimal -1073741286
 STATUS_SYSTEM_PROCESS_TERMINATED                ntstatus.h
# {Fatal System Error}
# The %hs system process terminated unexpectedly with a
# status of 0x%08x (0x%08x 0x%08x).
# The system has been shut down.
# as an HRESULT: Severity: FAILURE (1), FACILITY_NULL (0x0), Code 0x21a
# for hex 0x21a / decimal 538
 ERROR_ABIOS_ERROR                               winerror.h
# An error occurred in the ABIOS subsystem.
# 2 matches found for "c000021a"
```

```cmd
C:\Tools>Err_6.4.5.exe 7b
# for hex 0x7b / decimal 123
 INACCESSIBLE_BOOT_DEVICE                       bugcodes.h
 NMERR_SECURITY_BREACH_CAPTURE_DELETED              netmon.h
 ERROR_INVALID_NAME                       winerror.h
# The filename, directory name, or volume label syntax is
# incorrect.
# as an HRESULT: Severity: SUCCESS (0), FACILITY_NULL (0x0), Code 0x7b
# for hex 0x7b / decimal 123
 ERROR_INVALID_NAME                       winerror.h
# The filename, directory name, or volume label syntax is
# incorrect.
# 4 matches found for "7b"
```

## <a name="more-information"></a><span data-ttu-id="99dff-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="99dff-127">More information</span></span>

<span data-ttu-id="99dff-128">Beachten Sie, dass es sich hierbei um ein "Point-in-Time"-Tool handelt.</span><span class="sxs-lookup"><span data-stu-id="99dff-128">Keep in mind that this is a "point-in-time" tool.</span></span> <span data-ttu-id="99dff-129">Das Microsoft Error Lookup-Tool decodiert die meisten Microsoft-Fehlercodes ab dem Zeitpunkt, an dem das Tool kompiliert wurde.</span><span class="sxs-lookup"><span data-stu-id="99dff-129">The Microsoft Error Lookup Tool decodes most Microsoft error codes as of the date on which the tool was compiled.</span></span> <span data-ttu-id="99dff-130">Wenn neue Versionen von Windows neue Ereignis-und Fehlercodes hinzufügen, müssen Sie möglicherweise eine neue Version des Tools für die Fehlersuche herunterladen.</span><span class="sxs-lookup"><span data-stu-id="99dff-130">As new releases of Windows add new event and error codes, you may have to download a new version of the Error Lookup Tool.</span></span> <span data-ttu-id="99dff-131">Überprüfen Sie das Microsoft Download Center auf eine neue Version, oder sehen Sie sich die [Fehler Codes](system-error-codes.md)an.</span><span class="sxs-lookup"><span data-stu-id="99dff-131">Check the Microsoft Download Center for a new version, or see [Error Codes](system-error-codes.md).</span></span>
