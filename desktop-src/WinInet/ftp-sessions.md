---
title: FTP-Sitzungen
description: WinInet ermöglicht es Anwendungen, Verzeichnisse und Dateien auf einem FTP-Server zu navigieren und zu bearbeiten. Da CERN-Proxys FTP nicht unterstützen, müssen Anwendungen, die einen CERN-Proxy verwenden, exklusiv die InternetOpenURL-Funktion verwenden.
ms.assetid: 23763672-765f-4bbc-95c9-c28775e91f3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8310c2b83b81fc18b84d39153ed3dc7afda0df5a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039285"
---
# <a name="ftp-sessions"></a><span data-ttu-id="5669a-104">FTP-Sitzungen</span><span class="sxs-lookup"><span data-stu-id="5669a-104">FTP Sessions</span></span>

<span data-ttu-id="5669a-105">WinInet ermöglicht es Anwendungen, Verzeichnisse und Dateien auf einem FTP-Server zu navigieren und zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="5669a-105">WinINet enables applications to navigate and manipulate directories and files on an ftp server.</span></span> <span data-ttu-id="5669a-106">Da CERN-Proxys FTP nicht unterstützen, müssen Anwendungen, die einen CERN-Proxy verwenden, exklusiv die [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="5669a-106">Because CERN proxies do not support FTP, applications that use a CERN proxy exclusively must use the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function.</span></span> <span data-ttu-id="5669a-107">Weitere Informationen zur Verwendung von [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)finden Sie unter Direktes [Aufrufen von URLs](handling-uniform-resource-locators.md).</span><span class="sxs-lookup"><span data-stu-id="5669a-107">For more information about how to use [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), see [Accessing URLs Directly](handling-uniform-resource-locators.md).</span></span>

<span data-ttu-id="5669a-108">Verwenden Sie zum Starten einer FTP-Sitzung [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) , um das Sitzungs Handle zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5669a-108">To begin an FTP session, use [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) to create the session handle.</span></span>

<span data-ttu-id="5669a-109">Mit WinInet können Sie die folgenden Aktionen auf einem FTP-Server ausführen:</span><span class="sxs-lookup"><span data-stu-id="5669a-109">WinINet enables you to perform the following actions on an FTP server:</span></span>

-   <span data-ttu-id="5669a-110">Navigieren zwischen Verzeichnissen.</span><span class="sxs-lookup"><span data-stu-id="5669a-110">Navigate between directories.</span></span>
-   <span data-ttu-id="5669a-111">Auflisten, erstellen, entfernen und Umbenennen von Verzeichnissen.</span><span class="sxs-lookup"><span data-stu-id="5669a-111">Enumerate, create, remove, and rename directories.</span></span>
-   <span data-ttu-id="5669a-112">Umbenennen, hochladen, herunterladen und Löschen von Dateien.</span><span class="sxs-lookup"><span data-stu-id="5669a-112">Rename, upload, download, and delete files.</span></span>

<span data-ttu-id="5669a-113">Die Navigation wird von den Funktionen [**ftpgetcurrentdirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) und [**ftpsetcurrentdirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="5669a-113">Navigation is provided by the [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) and [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) functions.</span></span> <span data-ttu-id="5669a-114">Diese Funktionen verwenden das Sitzungs handle, das von einem vorherigen [**Internet Verbindungs**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) aufrufungstyp erstellt wurde, um zu bestimmen, in welchem Verzeichnis sich die Anwendung derzeit befindet, oder um in ein anderes Unterverzeichnis zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="5669a-114">These functions utilize the session handle created by a previous call to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) to determine which directory the application is currently in, or to change to a different subdirectory.</span></span>

<span data-ttu-id="5669a-115">Die verzeichnisenumeration wird mithilfe der Funktionen [**ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) und [**internetfindnextfile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5669a-115">Directory enumeration is performed by using the [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) and [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) functions.</span></span> <span data-ttu-id="5669a-116">[**Ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) verwendet das Sitzungs handle, das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) erstellt wurde, um die erste Datei zu suchen, die den angegebenen Suchkriterien entspricht, und gibt ein Handle zurück, um die verzeichnisenumeration fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="5669a-116">[**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) uses the session handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) to find the first file that matches the given search criteria and returns a handle to continue the directory enumeration.</span></span> <span data-ttu-id="5669a-117">[**Internetfindnextfile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) verwendet das von [**ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) zurückgegebene Handle, um die nächste Datei zurückzugeben, die den ursprünglichen Suchkriterien entspricht.</span><span class="sxs-lookup"><span data-stu-id="5669a-117">[**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) uses the handle returned by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) to return the next file that matches the original search criteria.</span></span> <span data-ttu-id="5669a-118">Die Anwendung sollte weiterhin [**internetfindnextfile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) aufruft, bis keine weiteren Dateien mehr im Verzeichnis vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="5669a-118">The application should continue to call [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) until there are no more files left in the directory.</span></span>

<span data-ttu-id="5669a-119">Verwenden Sie die [**ftpkreatedirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) -Funktion, um neue Verzeichnisse zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5669a-119">Use the [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) function to create new directories.</span></span> <span data-ttu-id="5669a-120">Diese Funktion verwendet das Sitzungs handle, das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) erstellt wurde, und erstellt das Verzeichnis, das durch die an die Funktion über gegebene Zeichenfolge angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5669a-120">This function uses the session handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) and creates the directory specified by the string passed to the function.</span></span> <span data-ttu-id="5669a-121">Die Zeichenfolge kann einen Verzeichnisnamen relativ zum aktuellen Verzeichnis oder einen voll qualifizierten Verzeichnispfad enthalten.</span><span class="sxs-lookup"><span data-stu-id="5669a-121">The string can contain a directory name relative to the current directory, or a fully qualified directory path.</span></span>

<span data-ttu-id="5669a-122">Zum Umbenennen von Dateien oder Verzeichnissen kann die Anwendung [**ftprenamefile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)aufruft.</span><span class="sxs-lookup"><span data-stu-id="5669a-122">To rename either files or directories, the application can call [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea).</span></span> <span data-ttu-id="5669a-123">Diese Funktion ersetzt den ursprünglichen Namen durch den neuen Namen, der an die Funktion übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="5669a-123">This function replaces the original name with the new name passed to the function.</span></span> <span data-ttu-id="5669a-124">Der Name der Datei oder des Verzeichnisses kann relativ zum aktuellen Verzeichnis oder ein voll qualifizierter Name sein.</span><span class="sxs-lookup"><span data-stu-id="5669a-124">The name of the file or directory can be relative to the current directory, or a fully qualified name.</span></span>

<span data-ttu-id="5669a-125">Um Dateien auf einem FTP-Server hochzuladen oder zu platzieren, kann die Anwendung entweder [**ftpputfile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) oder [**ftpopenfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (zusammen mit [**internetschreitedatei**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)) verwenden.</span><span class="sxs-lookup"><span data-stu-id="5669a-125">To upload or place files on an FTP server, the application can use either [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) or [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (along with [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)).</span></span> <span data-ttu-id="5669a-126">[**Ftpputfile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) kann verwendet werden, wenn die Datei bereits lokal vorhanden ist, während [**ftpopenfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) und [**internetschreitefile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) verwendet werden können, wenn Daten in eine Datei auf dem FTP-Server geschrieben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5669a-126">[**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) can be used if the file already exists locally, while [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) and [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) can be used if data needs to be written to a file on the FTP server.</span></span>

<span data-ttu-id="5669a-127">Zum Herunterladen oder Herunterladen von Dateien kann die Anwendung entweder [**ftpgetfile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) oder [**ftpopenfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (mit [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)) verwenden.</span><span class="sxs-lookup"><span data-stu-id="5669a-127">To download or get files, the application can use either [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) or [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (with [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)).</span></span> <span data-ttu-id="5669a-128">[**Ftpgetfile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) wird verwendet, um eine Datei von einem FTP-Server abzurufen und lokal zu speichern, während [**ftpopenfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) und [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) verwendet werden können, um zu steuern, wo die heruntergeladenen Informationen erfolgen (z. b. die Anwendung kann die Informationen in einem Bearbeitungsfeld anzeigen).</span><span class="sxs-lookup"><span data-stu-id="5669a-128">[**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) is used to retrieve a file from an FTP server and store it locally, while [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) and [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) can be used to control where the downloaded information is going (for example, the application could display the information in an edit box).</span></span>

<span data-ttu-id="5669a-129">Löschen Sie Dateien auf einem FTP-Server mithilfe der [**ftpdeletefile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="5669a-129">Delete files on an FTP server by using the [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) function.</span></span> <span data-ttu-id="5669a-130">Diese Funktion entfernt einen Dateinamen, der entweder relativ zum aktuellen Verzeichnis oder zu einem voll qualifizierten Dateinamen vom FTP-Server ist.</span><span class="sxs-lookup"><span data-stu-id="5669a-130">This function removes a file name that is relative either to the current directory or to a fully qualified file name from the FTP server.</span></span> <span data-ttu-id="5669a-131">[**Ftpdeletefile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) erfordert ein Sitzungs handle, das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="5669a-131">[**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) requires a session handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>

## <a name="ftp-function-handles"></a><span data-ttu-id="5669a-132">FTP-Funktions Handles</span><span class="sxs-lookup"><span data-stu-id="5669a-132">FTP Function Handles</span></span>

<span data-ttu-id="5669a-133">Um ordnungsgemäß zu funktionieren, benötigen die FTP-Funktionen bestimmte Typen von [**hinternethandles**](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="5669a-133">To work properly, the FTP functions require certain types of [**HINTERNET**](appendix-a-hinternet-handles.md) handles.</span></span> <span data-ttu-id="5669a-134">Diese Handles müssen in einer bestimmten Reihenfolge erstellt werden, beginnend mit dem Stamm handle, das von [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5669a-134">These handles must be created in a specific order, starting with the root handle created by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="5669a-135">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) kann dann ein FTP-Sitzungs Handle erstellen.</span><span class="sxs-lookup"><span data-stu-id="5669a-135">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) can then create an FTP session handle.</span></span>

<span data-ttu-id="5669a-136">Das folgende Diagramm zeigt die Funktionen, die von dem von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)zurückgegebenen FTP-Sitzungs handle abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="5669a-136">The following diagram shows the functions that are dependent on the FTP session handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="5669a-137">Die schattierten Felder stellen Funktionen dar, die [**hinternethandles**](appendix-a-hinternet-handles.md) zurückgeben, während die einfachen Felder Funktionen darstellen, die das hinternethandle verwenden, das von der Funktion erstellt wurde, von der Sie abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="5669a-137">The shaded boxes represent functions that return [**HINTERNET**](appendix-a-hinternet-handles.md) handles, while the plain boxes represent functions that use the HINTERNET handle created by the function on which they depend.</span></span>

![FTP-Funktionen, die vom von InternetConnect zurückgegebenen FTP-Sitzungs handle abhängen](images/ax-wnt06.png)

<span data-ttu-id="5669a-139">Das folgende Diagramm zeigt die beiden Funktionen, die [hinternethandles](appendix-a-hinternet-handles.md) und die von ihnen abhängigen Funktionen zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="5669a-139">The following diagram shows the two functions that return [HINTERNET](appendix-a-hinternet-handles.md) handles and the functions that are dependent on them.</span></span> <span data-ttu-id="5669a-140">Die schattierten Felder stellen Funktionen dar, die **hinternethandles** zurückgeben, während die einfachen Felder Funktionen darstellen, die das **hinternethandle** verwenden, das von der Funktion erstellt wurde, von der Sie abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="5669a-140">The shaded boxes represent functions that return **HINTERNET** handles, while the plain boxes represent functions that use the **HINTERNET** handle created by the function on which they depend.</span></span>

![FTP-Funktionen, die HINTERNET Handles zurückgeben](images/ax-wnt03.png)

<span data-ttu-id="5669a-142">Weitere Informationen finden Sie unter [HINTERNET Handles](appendix-a-hinternet-handles.md).</span><span class="sxs-lookup"><span data-stu-id="5669a-142">For more information, see [HINTERNET Handles](appendix-a-hinternet-handles.md).</span></span>

## <a name="using-the-wininet-functions-for-ftp-sessions"></a><span data-ttu-id="5669a-143">Verwenden der WinInet-Funktionen für FTP-Sitzungen</span><span class="sxs-lookup"><span data-stu-id="5669a-143">Using the WinINet Functions for FTP Sessions</span></span>

<span data-ttu-id="5669a-144">Die folgenden Funktionen werden bei FTP-Sitzungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="5669a-144">The following functions are used during FTP sessions.</span></span> <span data-ttu-id="5669a-145">Diese Funktionen werden von CERN-Proxys nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="5669a-145">These functions are not recognized by CERN proxies.</span></span> <span data-ttu-id="5669a-146">Anwendungen, die über CERN-Proxys funktionieren müssen, sollten [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) verwenden und direkt auf die Ressourcen zugreifen.</span><span class="sxs-lookup"><span data-stu-id="5669a-146">Applications that must function through CERN proxies should use [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) and access the resources directly.</span></span> <span data-ttu-id="5669a-147">Weitere Informationen zum direkten Zugriff auf Ressourcen finden Sie unter Direktes [Aufrufen von URLs](handling-uniform-resource-locators.md).</span><span class="sxs-lookup"><span data-stu-id="5669a-147">For more information on direct resource access, see [Accessing URLs Directly](handling-uniform-resource-locators.md).</span></span>



| <span data-ttu-id="5669a-148">Funktion</span><span class="sxs-lookup"><span data-stu-id="5669a-148">Function</span></span>                                                 | <span data-ttu-id="5669a-149">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5669a-149">Description</span></span>                                                                                                                                                    |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5669a-150">**Ftpkreatedirectory**</span><span class="sxs-lookup"><span data-stu-id="5669a-150">**FtpCreateDirectory**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya)         | <span data-ttu-id="5669a-151">Erstellt ein neues Verzeichnis auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="5669a-151">Creates a new directory on the server.</span></span> <span data-ttu-id="5669a-152">Diese Funktion erfordert ein Handle, das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5669a-152">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                  |
| [<span data-ttu-id="5669a-153">**Ftpdeletefile**</span><span class="sxs-lookup"><span data-stu-id="5669a-153">**FtpDeleteFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)                   | <span data-ttu-id="5669a-154">Löscht eine Datei vom Server.</span><span class="sxs-lookup"><span data-stu-id="5669a-154">Deletes a file from the server.</span></span> <span data-ttu-id="5669a-155">Diese Funktion erfordert ein Handle, das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5669a-155">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                         |
| [<span data-ttu-id="5669a-156">**Ftpfindfirstfile**</span><span class="sxs-lookup"><span data-stu-id="5669a-156">**FtpFindFirstFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)             | <span data-ttu-id="5669a-157">Startet die Dateienumeration oder die Dateisuche im aktuellen Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="5669a-157">Starts file enumeration or file search in the current directory.</span></span> <span data-ttu-id="5669a-158">Diese Funktion erfordert ein Handle, das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5669a-158">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>        |
| [<span data-ttu-id="5669a-159">**Ftpgetcurrentdirectory**</span><span class="sxs-lookup"><span data-stu-id="5669a-159">**FtpGetCurrentDirectory**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) | <span data-ttu-id="5669a-160">Gibt das aktuelle Verzeichnis des Clients auf dem Server zurück.</span><span class="sxs-lookup"><span data-stu-id="5669a-160">Returns the client's current directory on the server.</span></span> <span data-ttu-id="5669a-161">Diese Funktion erfordert ein Handle, das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5669a-161">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                   |
| [<span data-ttu-id="5669a-162">**Ftpgetfile**</span><span class="sxs-lookup"><span data-stu-id="5669a-162">**FtpGetFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)                         | <span data-ttu-id="5669a-163">Ruft eine Datei vom Server ab.</span><span class="sxs-lookup"><span data-stu-id="5669a-163">Retrieves a file from the server.</span></span> <span data-ttu-id="5669a-164">Diese Funktion erfordert ein Handle, das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5669a-164">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                       |
| [<span data-ttu-id="5669a-165">**Ftpopumfile**</span><span class="sxs-lookup"><span data-stu-id="5669a-165">**FtpOpenFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)                       | <span data-ttu-id="5669a-166">Initiiert den Zugriff auf eine Datei auf dem Server zum Lesen oder schreiben.</span><span class="sxs-lookup"><span data-stu-id="5669a-166">Initiates access to a file on the server for either reading or writing.</span></span> <span data-ttu-id="5669a-167">Diese Funktion erfordert ein Handle, das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5669a-167">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> |
| [<span data-ttu-id="5669a-168">**Ftpputfile**</span><span class="sxs-lookup"><span data-stu-id="5669a-168">**FtpPutFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)                         | <span data-ttu-id="5669a-169">Schreibt eine Datei auf den Server.</span><span class="sxs-lookup"><span data-stu-id="5669a-169">Writes a file to the server.</span></span> <span data-ttu-id="5669a-170">Diese Funktion erfordert ein Handle, das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5669a-170">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                            |
| [<span data-ttu-id="5669a-171">**Ftpremuvedirectory**</span><span class="sxs-lookup"><span data-stu-id="5669a-171">**FtpRemoveDirectory**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya)         | <span data-ttu-id="5669a-172">Löscht ein Verzeichnis auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="5669a-172">Deletes a directory on the server.</span></span> <span data-ttu-id="5669a-173">Diese Funktion erfordert ein Handle, das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5669a-173">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                      |
| [<span data-ttu-id="5669a-174">**Ftprenamefile**</span><span class="sxs-lookup"><span data-stu-id="5669a-174">**FtpRenameFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)                   | <span data-ttu-id="5669a-175">Benennt eine Datei auf dem Server um.</span><span class="sxs-lookup"><span data-stu-id="5669a-175">Renames a file on the server.</span></span> <span data-ttu-id="5669a-176">Diese Funktion erfordert ein Handle, das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5669a-176">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                           |
| [<span data-ttu-id="5669a-177">**Ftpsetcurrentdirectory**</span><span class="sxs-lookup"><span data-stu-id="5669a-177">**FtpSetCurrentDirectory**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) | <span data-ttu-id="5669a-178">Ändert das aktuelle Verzeichnis des Clients auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="5669a-178">Changes the client's current directory on the server.</span></span> <span data-ttu-id="5669a-179">Diese Funktion erfordert ein Handle, das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5669a-179">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                   |
| [<span data-ttu-id="5669a-180">**Internetschreibdatei**</span><span class="sxs-lookup"><span data-stu-id="5669a-180">**InternetWriteFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)           | <span data-ttu-id="5669a-181">Schreibt Daten in eine geöffnete Datei auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="5669a-181">Writes data to an open file on the server.</span></span> <span data-ttu-id="5669a-182">Diese Funktion erfordert ein Handle, das von [**ftpopenfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5669a-182">This function requires a handle created by [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea).</span></span>                                      |



 

### <a name="starting-an-ftp-session"></a><span data-ttu-id="5669a-183">Starten einer FTP-Sitzung</span><span class="sxs-lookup"><span data-stu-id="5669a-183">Starting an FTP Session</span></span>

<span data-ttu-id="5669a-184">Die Anwendung richtet eine FTP-Sitzung ein, indem Sie [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) für ein Handle aufrufen, das von [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5669a-184">The application establishes an FTP session by calling [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) on a handle created by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="5669a-185">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) benötigt den Servernamen, die Portnummer, den Benutzernamen, das Kennwort und den Diensttyp (der auf Internet Dienst-FTP festgelegt sein muss \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="5669a-185">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) needs the server name, port number, user name, password, and service type (which must be set to INTERNET\_SERVICE\_FTP).</span></span> <span data-ttu-id="5669a-186">Bei der passiven FTP-Semantik muss die Anwendung auch das [Internet \_ Flag \_ passiv](api-flags.md) -Flag festlegen.</span><span class="sxs-lookup"><span data-stu-id="5669a-186">For passive FTP semantics, the application must also set the [INTERNET\_FLAG\_PASSIVE](api-flags.md) flag.</span></span>

<span data-ttu-id="5669a-187">Der Internet \_ \_ Standardftp \_ -Port und Internet- \_ ungültige \_ Port \_ Nummern Werte können für die Portnummer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5669a-187">The INTERNET\_DEFAULT\_FTP\_PORT and INTERNET\_INVALID\_PORT\_NUMBER values can be used for the port number.</span></span> <span data-ttu-id="5669a-188">Der Standardftp- \_ \_ \_ Port des Internets verwendet den Standardftp-Port, aber der Diensttyp muss noch festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5669a-188">INTERNET\_DEFAULT\_FTP\_PORT uses the default FTP port, but the service type still must be set.</span></span> <span data-ttu-id="5669a-189">Internet \_ ungültige \_ Port \_ Nummer verwendet den Standardwert für den bestimmten Diensttyp.</span><span class="sxs-lookup"><span data-stu-id="5669a-189">INTERNET\_INVALID\_PORT\_NUMBER uses the default value for the indicated service type.</span></span>

<span data-ttu-id="5669a-190">Die Werte für Benutzername und Kennwort können auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5669a-190">The values for the user name and password can be set to **NULL**.</span></span> <span data-ttu-id="5669a-191">Wenn beide Werte auf **null** festgelegt sind, verwendet [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) "Anonymous" als Benutzernamen und die e-Mail-Adresse des Benutzers für das Kennwort.</span><span class="sxs-lookup"><span data-stu-id="5669a-191">If both values are set to **NULL**, [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) uses "anonymous" for the user name, and the user's email address for the password.</span></span> <span data-ttu-id="5669a-192">Wenn nur das Kennwort auf **null** festgelegt ist, wird der an [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) über gegebene Benutzername als Benutzername verwendet, und für das Kennwort wird eine leere Zeichenfolge verwendet.</span><span class="sxs-lookup"><span data-stu-id="5669a-192">If only the password is set to **NULL**, the user name passed to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) is used for the user name, and an empty string is used for the password.</span></span> <span data-ttu-id="5669a-193">Wenn kein Wert **null** ist, werden der Benutzername und das Kennwort für [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) verwendet.</span><span class="sxs-lookup"><span data-stu-id="5669a-193">If neither value is **NULL**, the user name and password given to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) are used.</span></span>

### <a name="enumerating-directories"></a><span data-ttu-id="5669a-194">Auflisten von Verzeichnissen</span><span class="sxs-lookup"><span data-stu-id="5669a-194">Enumerating Directories</span></span>

<span data-ttu-id="5669a-195">Die Enumeration eines Verzeichnisses auf einem FTP-Server erfordert die Erstellung eines Handles durch [**ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea).</span><span class="sxs-lookup"><span data-stu-id="5669a-195">Enumeration of a directory on an FTP server requires the creation of a handle by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea).</span></span> <span data-ttu-id="5669a-196">Dieses Handle ist eine Verzweigung des Sitzungs Handles, das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5669a-196">This handle is a branch of the session handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="5669a-197">[**Ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) sucht die erste Datei oder das erste Verzeichnis auf dem Server und gibt Sie in einer Win32-Such [**\_ \_ Daten**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="5669a-197">[**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) locates the first file or directory on the server and returns it in a [**WIN32\_FIND\_DATA**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) structure.</span></span> <span data-ttu-id="5669a-198">Verwenden Sie [**internetfindnextfile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) , bis der [**Fehler \_ keine \_ weiteren \_ Dateien**](wininet-errors.md)zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="5669a-198">Use [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) until it returns [**ERROR\_NO\_MORE\_FILES**](wininet-errors.md).</span></span> <span data-ttu-id="5669a-199">Diese Methode sucht alle nachfolgenden Dateien und Verzeichnisse auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="5669a-199">This method finds all subsequent files and directories on the server.</span></span> <span data-ttu-id="5669a-200">Weitere Informationen zu [**internetfindnextfile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)finden Sie untersuchen [der nächsten Datei](common-functions.md).</span><span class="sxs-lookup"><span data-stu-id="5669a-200">For more information on [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), see [Finding the Next File](common-functions.md).</span></span>

<span data-ttu-id="5669a-201">Um festzustellen, ob es sich bei der von [**ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) oder [**internetfindnextfile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) abgerufenen Datei um ein Verzeichnis handelt, überprüfen Sie das Element **dwfileattribute** der [**Win32- \_ \_ Datenstruktur suchen**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) , um festzustellen, ob es gleich dem Datei \_ Attribut Verzeichnis ist \_ .</span><span class="sxs-lookup"><span data-stu-id="5669a-201">To determine if the file retrieved by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) or [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) is a directory, check the **dwFileAttributes** member of the [**WIN32\_FIND\_DATA**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) structure to see if it is equal to FILE\_ATTRIBUTE\_DIRECTORY.</span></span>

<span data-ttu-id="5669a-202">Wenn die Anwendung Änderungen am FTP-Server vornimmt oder sich der FTP-Server häufig ändert, sollten die Flags " [Internet \_ Flag \_ No \_ Cache \_ Write](api-flags.md) " und " [Internet \_ Flag neu \_ Laden](api-flags.md) " in [**ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5669a-202">If the application makes changes on the FTP server or if the FTP server changes frequently, the [INTERNET\_FLAG\_NO\_CACHE\_WRITE](api-flags.md) and [INTERNET\_FLAG\_RELOAD](api-flags.md) flags should be set in [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea).</span></span> <span data-ttu-id="5669a-203">Diese Flags stellen sicher, dass die Verzeichnisinformationen, die vom FTP-Server abgerufen werden, aktuell sind.</span><span class="sxs-lookup"><span data-stu-id="5669a-203">These flags ensure that the directory information being retrieved from the FTP server is current.</span></span>

<span data-ttu-id="5669a-204">Nachdem die Anwendung die verzeichnisenumeration abgeschlossen hat, muss die Anwendung den [**internetclosehandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) -Vorgang für das Handle ausführen, das von [**ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5669a-204">After the application completes the directory enumeration, the application must make a call to [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) on the handle created by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea).</span></span> <span data-ttu-id="5669a-205">Bis das Handle geschlossen ist, kann die Anwendung [**ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) nicht mehr für das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)erstellte Sitzungs handle abrufen.</span><span class="sxs-lookup"><span data-stu-id="5669a-205">Until that handle is closed, the application cannot call [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) again on the session handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="5669a-206">Wenn ein [**ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) -Befehl für das gleiche Sitzungs handle ausgeführt wird, bevor der vorherige-Befehl der gleichen Funktion geschlossen wird, schlägt die Funktion fehl, und es wird die [Fehler-FTP- \_ \_ Übertragung \_ in \_](wininet-errors.md)Bearbeitung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5669a-206">If a call to [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) is made on the same session handle before the previous call to the same function is closed, the function fails, returning [ERROR\_FTP\_TRANSFER\_IN\_PROGRESS](wininet-errors.md).</span></span>

<span data-ttu-id="5669a-207">Im folgenden Beispiel wird der Inhalt eines FTP-Verzeichnisses in einem Listenfeld-Steuerelement aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="5669a-207">The following example enumerates the contents of an FTP directory into a list box control.</span></span> <span data-ttu-id="5669a-208">Der *hconnection* -Parameter ist ein Handle, das von der [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) -Funktion zurückgegeben wird, nachdem eine FTP-Sitzung eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="5669a-208">The *hConnection* parameter is a handle returned by the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function after it establishes an FTP session.</span></span> <span data-ttu-id="5669a-209">Beispiel Quell Code für die internetterrorout-Funktion, auf die in diesem Beispiel verwiesen wird, finden Sie im Thema [Behandlung von Fehlern](appendix-c-handling-errors.md).</span><span class="sxs-lookup"><span data-stu-id="5669a-209">Sample source code for the InternetErrorOut function referenced in this example can be found in the [Handling Errors](appendix-c-handling-errors.md)topic.</span></span>


```C++
#include <windows.h>
#include <strsafe.h>
#include <wininet.h>

#pragma comment(lib, "wininet.lib")
#pragma comment(lib, "user32.lib")

#define  FTP_FUNCTIONS_BUFFER_SIZE          MAX_PATH+8

BOOL WINAPI DisplayFtpDir(
                           HWND hDlg,
                           HINTERNET hConnection,
                           DWORD dwFindFlags,
                           int nListBoxId )
{
  WIN32_FIND_DATA dirInfo;
  HINTERNET       hFind;
  DWORD           dwError;
  BOOL            retVal = FALSE;
  TCHAR           szMsgBuffer[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR           szFName[FTP_FUNCTIONS_BUFFER_SIZE];
  
  SendDlgItemMessage( hDlg, nListBoxId, LB_RESETCONTENT, 0, 0 );
  hFind = FtpFindFirstFile( hConnection, TEXT( "*.*" ), 
                            &dirInfo, dwFindFlags, 0 );
  if ( hFind == NULL )
  {
    dwError = GetLastError( );
    if( dwError == ERROR_NO_MORE_FILES )
    {
      StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
        TEXT( "No files found at FTP location specified." ) );
      retVal = TRUE;
      goto DisplayDirError_1;
    }
    StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
      TEXT( "FtpFindFirstFile failed." ) );
    goto DisplayDirError_1;
  }

  do
  {
    if( FAILED( StringCchCopy( szFName, FTP_FUNCTIONS_BUFFER_SIZE,
                  dirInfo.cFileName ) ) ||
        ( ( dirInfo.dwFileAttributes & FILE_ATTRIBUTE_DIRECTORY ) &&
        ( FAILED( StringCchCat( szFName, FTP_FUNCTIONS_BUFFER_SIZE,
         TEXT( " <DIR> " ) ) ) ) ) )
    {
      StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
        TEXT( "Failed to copy a file or directory name." ) );
      retVal = FALSE;
      goto DisplayDirError_2;
    }
    SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 
                        0, (LPARAM) szFName );
  } while( InternetFindNextFile( hFind, (LPVOID) &dirInfo ) );

  if( ( dwError = GetLastError( ) ) == ERROR_NO_MORE_FILES )
  {
    InternetCloseHandle(hFind);
    return( TRUE );
  }
  StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
    TEXT( "FtpFindNextFile failed." ) );

DisplayDirError_2:
  InternetCloseHandle( hFind );
DisplayDirError_1:
  MessageBox( hDlg,
    (LPCTSTR) szMsgBuffer,
    TEXT( "DisplayFtpDir( ) Problem" ),
    MB_OK | MB_ICONERROR );
  return( retVal );
}
```



### <a name="navigating-directories"></a><span data-ttu-id="5669a-210">Navigieren in Verzeichnissen</span><span class="sxs-lookup"><span data-stu-id="5669a-210">Navigating Directories</span></span>

<span data-ttu-id="5669a-211">Die Funktionen " [**ftpgetcurrentdirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) " und " [**ftpsetcurrentdirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) " behandeln die Verzeichnis Navigation.</span><span class="sxs-lookup"><span data-stu-id="5669a-211">The [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) and [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) functions handle directory navigation.</span></span>

<span data-ttu-id="5669a-212">[**Ftpgetcurrentdirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) gibt das aktuelle Verzeichnis der Anwendung auf dem FTP-Server zurück.</span><span class="sxs-lookup"><span data-stu-id="5669a-212">[**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) returns the application's current directory on the FTP server.</span></span> <span data-ttu-id="5669a-213">Der Verzeichnispfad aus dem Stammverzeichnis auf dem FTP-Server ist enthalten.</span><span class="sxs-lookup"><span data-stu-id="5669a-213">The directory path from the root directory on the FTP server is included.</span></span>

<span data-ttu-id="5669a-214">[**Ftpsetcurrentdirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) ändert das Arbeitsverzeichnis auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="5669a-214">[**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) changes the working directory on the server.</span></span> <span data-ttu-id="5669a-215">Bei den an [**ftpsetcurrentdirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) weiter gegebenen Verzeichnisinformationen kann es sich entweder um einen teilweise oder voll qualifizierten Pfadnamen handeln, der relativ zum aktuellen Verzeichnis ist.</span><span class="sxs-lookup"><span data-stu-id="5669a-215">The directory information passed to [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) can be either a partially or fully qualified path name relative to the current directory.</span></span> <span data-ttu-id="5669a-216">Wenn sich die Anwendung z. b. zurzeit im Verzeichnis "Public/Info" befindet und der Pfad "FTP/example" lautet, ändert [**ftpsetcurrentdirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) das aktuelle Verzeichnis in "Public/Info/FTP/example".</span><span class="sxs-lookup"><span data-stu-id="5669a-216">For example, if the application is currently in the directory "public/info" and the path is "ftp/example", [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) changes the current directory to "public/info/ftp/example".</span></span>

<span data-ttu-id="5669a-217">Im folgenden Beispiel wird das FTP-Sitzungs handle hconnection verwendet, das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5669a-217">The following example uses the FTP session handle hConnection, which is returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="5669a-218">Der neue Verzeichnisname wird aus dem Bearbeitungsfeld des übergeordneten Dialog Felds übernommen, dessen IDC im *ndirnameid* -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="5669a-218">The new directory name is taken from the edit box of the parent dialog whose IDC is passed in the *nDirNameId* parameter.</span></span> <span data-ttu-id="5669a-219">Bevor die Verzeichnis Änderung vorgenommen wird, ruft die Funktion das aktuelle Verzeichnis ab und speichert es in demselben Bearbeitungsfeld.</span><span class="sxs-lookup"><span data-stu-id="5669a-219">Before the directory change is made, the function retrieves the current directory and stores it in the same edit box.</span></span> <span data-ttu-id="5669a-220">Der Quelle-Code für die displayftpdir-Funktion, die am Ende aufgerufen wird, ist oben aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="5669a-220">The souce code for the DisplayFtpDir function called at the end is listed above.</span></span>


```C++
BOOL WINAPI ChangeFtpDir( HWND hDlg, 
                          HINTERNET hConnection,
                          int nDirNameId, 
                          int nListBoxId )
{
  DWORD dwSize;
  TCHAR szNewDirName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szOldDirName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR* szFailedFunctionName;

  dwSize = FTP_FUNCTIONS_BUFFER_SIZE;

  if( !GetDlgItemText( hDlg, nDirNameId, szNewDirName, dwSize ) )
  {
    szFailedFunctionName = TEXT( "GetDlgItemText" );
    goto ChangeFtpDirError;
  }

  if ( !FtpGetCurrentDirectory( hConnection, szOldDirName, &dwSize ))
  {
    szFailedFunctionName = TEXT( "FtpGetCurrentDirectory" );
    goto ChangeFtpDirError;
  }

  if( !SetDlgItemText( hDlg, nDirNameId, szOldDirName ) )
  {
    szFailedFunctionName = TEXT( "SetDlgItemText" );
    goto ChangeFtpDirError;
  }

  if( !FtpSetCurrentDirectory( hConnection, szNewDirName ) )
  {
    szFailedFunctionName = TEXT( "FtpSetCurrentDirectory" );
    goto ChangeFtpDirError;
  }
  return( DisplayFtpDir( hDlg, hConnection, 0, nListBoxId ) );

ChangeFtpDirError:
  InternetErrorOut( hDlg, GetLastError( ), szFailedFunctionName );
  DisplayFtpDir( hDlg, hConnection, INTERNET_FLAG_RELOAD, nListBoxId);
  return( FALSE );
}
```



### <a name="manipulating-directories-on-an-ftp-server"></a><span data-ttu-id="5669a-221">Manipulieren von Verzeichnissen auf einem FTP-Server</span><span class="sxs-lookup"><span data-stu-id="5669a-221">Manipulating Directories on an FTP Server</span></span>

<span data-ttu-id="5669a-222">WinInet bietet die Möglichkeit, Verzeichnisse auf einem FTP-Server zu erstellen und zu entfernen, auf dem die Anwendung über die erforderlichen Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="5669a-222">WinINet provides the capability to create and remove directories on an FTP server to which the application has the necessary privileges.</span></span> <span data-ttu-id="5669a-223">Wenn sich die Anwendung bei einem Server mit einem bestimmten Benutzernamen und einem Kennwort anmelden muss, können die Werte beim Erstellen des FTP-Sitzungs Handles in [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5669a-223">If the application must log on to a server with a specific user name and password, the values can be used in [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) when creating the FTP session handle.</span></span>

<span data-ttu-id="5669a-224">Die [**ftpkreatedirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) -Funktion nimmt ein gültiges FTP-Sitzungs Handle und eine auf **null** endenden Zeichenfolge, die entweder einen voll qualifizierten Pfad oder einen Namen relativ zum aktuellen Verzeichnis enthält, und erstellt ein Verzeichnis auf dem FTP-Server.</span><span class="sxs-lookup"><span data-stu-id="5669a-224">The [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) function takes a valid FTP session handle and a **null**-terminated string that contains either a fully qualified path or a name relative to the current directory and creates a directory on the FTP server.</span></span>

<span data-ttu-id="5669a-225">Das folgende Beispiel zeigt zwei separate Aufrufe von [**ftpkreatedirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya).</span><span class="sxs-lookup"><span data-stu-id="5669a-225">The following example shows two separate calls to [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya).</span></span> <span data-ttu-id="5669a-226">In beiden Beispielen ist hftpsession das Sitzungs handle, das von der [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) -Funktion erstellt wird, und das Stammverzeichnis ist das aktuelle Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="5669a-226">In both examples, hFtpSession is the session handle created by the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function, and the root directory is the current directory.</span></span>

``` syntax
/* Creates the directory "test" in the current (root) directory. */
FtpCreateDirectory( hFtpSession, "test" );

/* Creates the directory "example" in the test directory. */
FtpCreateDirectory( hFtpSession, "\\test\\example" );
```

<span data-ttu-id="5669a-227">Die Funktion [**ftpremuvedirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya) nimmt ein Sitzungs Handle und eine auf **null** endenden Zeichenfolge, die entweder einen voll qualifizierten Pfad oder einen Namen relativ zum aktuellen Verzeichnis enthält, und entfernt dieses Verzeichnis vom FTP-Server.</span><span class="sxs-lookup"><span data-stu-id="5669a-227">The [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya) function takes a session handle and a **null**-terminated string that contains either a fully qualified path or a name relative to the current directory and removes that directory from the FTP server.</span></span>

<span data-ttu-id="5669a-228">Das folgende Beispiel zeigt zwei Beispiel Aufrufe von [**ftpremumuvedirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya).</span><span class="sxs-lookup"><span data-stu-id="5669a-228">The following example shows two sample calls to [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya).</span></span> <span data-ttu-id="5669a-229">In beiden Aufrufen ist hftpsession das Sitzungs handle, das von der [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) -Funktion erstellt wird, und das Stammverzeichnis ist das aktuelle Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="5669a-229">In both calls, hFtpSession is the session handle created by the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function, and the root directory is the current directory.</span></span> <span data-ttu-id="5669a-230">Das Stammverzeichnis enthält ein Verzeichnis mit dem Namen "Test" und ein Verzeichnis mit dem Namen "example" im Verzeichnis "Test".</span><span class="sxs-lookup"><span data-stu-id="5669a-230">There is a directory called "test" in the root directory and a directory called "example" in the "test" directory.</span></span>

``` syntax
/* Removes the "example" directory (plus any files/directories it contains) from the "test" directory. */
FtpRemoveDirectory(hFtpSession,"\\test\\example");

/* Removes the "test" directory (plus any files/directories it contains) from the root directory. */
FtpRemoveDirectory(hFtpSession, "test");
```


```C++
FtpRemoveDirectory(hFtpSession,TEXT("\\test\\example"));
/* Removes the "example" directory and any files or 
directories contained in it from the "test" directory. */

FtpRemoveDirectory(hFtpSession, TEXT("test"));
/* Removes the "test" directory and any files or 
directories contained in it from the root directory. */
```



<span data-ttu-id="5669a-231">Im folgenden Beispiel wird ein neues Verzeichnis auf dem FTP-Server erstellt.</span><span class="sxs-lookup"><span data-stu-id="5669a-231">The following example creates a new directory on the FTP server.</span></span> <span data-ttu-id="5669a-232">Der neue Verzeichnisname wird aus dem Bearbeitungsfeld des übergeordneten Dialog Felds übernommen, dessen IDC im *ndirnameid* -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="5669a-232">The new directory name is taken from the edit box of the parent dialog whose IDC is passed in the *nDirNameId* parameter.</span></span> <span data-ttu-id="5669a-233">Das *hconnection* -Handle wurde von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) erstellt, nachdem eine FTP-Sitzung eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="5669a-233">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span> <span data-ttu-id="5669a-234">Der Quellcode für die displayftpdir-Funktion, die am Ende aufgerufen wird, ist oben aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="5669a-234">The source code for the DisplayFtpDir function called at the end is listed above.</span></span>


```C++
BOOL WINAPI CreateFtpDir( HWND hDlg, HINTERNET hConnection,
                          int nDirNameId, int nListBoxId )
{
  TCHAR szNewDirName[FTP_FUNCTIONS_BUFFER_SIZE];

  if( !GetDlgItemText( hDlg, nDirNameId, 
                       szNewDirName, 
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Error: Directory Name Must Be Specified" ),
                TEXT( "Create FTP Directory" ), 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpCreateDirectory( hConnection, szNewDirName ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), 
                      TEXT( "FtpCreateDirectory" ) );
    return( FALSE );
  }

  return( DisplayFtpDir( hDlg, hConnection, 
                         INTERNET_FLAG_RELOAD, 
                         nListBoxId ) );
}
```



<span data-ttu-id="5669a-235">Im folgenden Beispiel wird ein Verzeichnis vom FTP-Server gelöscht.</span><span class="sxs-lookup"><span data-stu-id="5669a-235">The following example deletes a directory from the FTP server.</span></span> <span data-ttu-id="5669a-236">Der Name des zu löschenden Verzeichnisses wird aus dem Bearbeitungsfeld im übergeordneten Dialogfeld übernommen, dessen IDC an den *ndirnameid* -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="5669a-236">The name of the directory to be deleted is taken from the edit box in the parent dialog whose IDC is passed into the *nDirNameId* parameter.</span></span> <span data-ttu-id="5669a-237">Das *hconnection* -Handle wurde von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) erstellt, nachdem eine FTP-Sitzung eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="5669a-237">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span> <span data-ttu-id="5669a-238">Der Quellcode für die displayftpdir-Funktion, die am Ende aufgerufen wird, ist oben aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="5669a-238">The source code for the DisplayFtpDir function called at the end is listed above.</span></span>


```C++
BOOL WINAPI RemoveFtpDir( HWND hDlg, HINTERNET hConnection,
                          int nDirNameId, int nListBoxId )
{
  TCHAR szDelDirName[FTP_FUNCTIONS_BUFFER_SIZE];

  if( !GetDlgItemText( hDlg, nDirNameId, szDelDirName, 
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Error: Directory Name Must Be Specified" ),
                TEXT( "Remove FTP Directory" ), 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpRemoveDirectory( hConnection, szDelDirName ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), 
                      TEXT( "FtpRemoveDirectory" ) );
    return( FALSE );
  }

  return( DisplayFtpDir( hDlg, hConnection, 
                         INTERNET_FLAG_RELOAD, nListBoxId ) );
}
```



### <a name="getting-files-on-an-ftp-server"></a><span data-ttu-id="5669a-239">Dateien werden auf einem FTP-Server erhalten.</span><span class="sxs-lookup"><span data-stu-id="5669a-239">Getting Files on an FTP Server</span></span>

<span data-ttu-id="5669a-240">Es gibt drei Methoden zum Abrufen von Dateien von einem FTP-Server:</span><span class="sxs-lookup"><span data-stu-id="5669a-240">There are three methods for retrieving files from an FTP server:</span></span>

-   <span data-ttu-id="5669a-241">Verwenden Sie [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) und [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span><span class="sxs-lookup"><span data-stu-id="5669a-241">Use [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) and [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span></span>
-   <span data-ttu-id="5669a-242">Verwenden Sie " [**ftpopeinfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) " und " [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)".</span><span class="sxs-lookup"><span data-stu-id="5669a-242">Use [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) and [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span></span>
-   <span data-ttu-id="5669a-243">Verwenden Sie " [**ftpgetfile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)".</span><span class="sxs-lookup"><span data-stu-id="5669a-243">Use [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea).</span></span>

<span data-ttu-id="5669a-244">Weitere Informationen zum Verwenden der [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) -Funktion finden Sie unter [Lesen von Dateien](common-functions.md).</span><span class="sxs-lookup"><span data-stu-id="5669a-244">For more information about using the [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) function, see [Reading Files](common-functions.md).</span></span>

<span data-ttu-id="5669a-245">Wenn die URL der Datei verfügbar ist, kann die Anwendung [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) anrufen, um eine Verbindung mit dieser URL herzustellen, und dann mit [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) den Download der Datei steuern.</span><span class="sxs-lookup"><span data-stu-id="5669a-245">If the URL of the file is available, the application can call [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) to connect to that URL, then use [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) to control the download of the file.</span></span> <span data-ttu-id="5669a-246">Dies ermöglicht der Anwendung eine strengere Kontrolle über den Download und eignet sich ideal für Situationen, in denen keine anderen Vorgänge auf dem FTP-Server durchgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5669a-246">This allows the application tighter control over the download and is ideal for situations where no other operations need to be made on the FTP server.</span></span> <span data-ttu-id="5669a-247">Weitere Informationen zum direkten Zugriff auf Ressourcen finden Sie unter Direktes [Aufrufen von URLs](handling-uniform-resource-locators.md).</span><span class="sxs-lookup"><span data-stu-id="5669a-247">For more information about how to directly access resources, see [Accessing URLs Directly](handling-uniform-resource-locators.md).</span></span>

<span data-ttu-id="5669a-248">Wenn die Anwendung ein FTP-Sitzungs Handle für den Server mit [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)eingerichtet hat, kann die Anwendung [**ftpopenfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) mit dem vorhandenen Dateinamen und mit einem neuen Namen für die lokal gespeicherte Datei abrufen.</span><span class="sxs-lookup"><span data-stu-id="5669a-248">If the application has established an FTP session handle to the server with [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), the application can call [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) with the existing file name and with a new name for the locally stored file.</span></span> <span data-ttu-id="5669a-249">Die Anwendung kann dann die Datei mit " [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) " herunterladen.</span><span class="sxs-lookup"><span data-stu-id="5669a-249">The application can then use [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) to download the file.</span></span> <span data-ttu-id="5669a-250">Dies ermöglicht es der Anwendung, den Download zu verkürzen und die Verbindung mit dem FTP-Server aufrecht zu erhalten, sodass weitere Befehle ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="5669a-250">This allows the application tighter control over the download and keeps the connection to the FTP server, so more commands can be executed.</span></span>

<span data-ttu-id="5669a-251">Wenn die Anwendung keine strenge Kontrolle über den Download benötigt, kann die Anwendung [**ftpgetfile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) mit dem FTP-Sitzungs handle, dem Remote Dateinamen und dem lokalen Dateinamen verwenden, um die Datei abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5669a-251">If the application does not need tight control over the download, the application can use [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) with the FTP session handle, remote file name, and local file name to retrieve the file.</span></span> <span data-ttu-id="5669a-252">[**Ftpgetfile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) führt sämtliche Buchhaltungs-und Verwaltungsaufwand für das Lesen einer Datei von einem FTP-Server durch und speichert Sie lokal.</span><span class="sxs-lookup"><span data-stu-id="5669a-252">[**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) performs all the bookkeeping and overhead associated with reading a file from an FTP server and storing it locally.</span></span>

<span data-ttu-id="5669a-253">Das folgende Beispiel ruft eine Datei von einem FTP-Server ab und speichert Sie lokal.</span><span class="sxs-lookup"><span data-stu-id="5669a-253">The following example retrieves a file from an FTP server and saves it locally.</span></span> <span data-ttu-id="5669a-254">Der Name der Datei auf dem FTP-Server wird aus dem Bearbeitungsfeld im übergeordneten Dialogfeld übernommen, dessen IDC im *nftpfileameid* -Parameter übergeben wird, und der lokale Name, unter dem die Datei gespeichert wird, wird aus dem Bearbeitungsfeld entnommen, dessen IDC im *nlocalfileameid* -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="5669a-254">The name of the file on the FTP server is taken from the edit box in the parent dialog whose IDC is passed in the *nFtpFileNameId* parameter, and the local name under which the file is saved is taken from the edit box whose IDC is passed in the *nLocalFileNameId* parameter.</span></span> <span data-ttu-id="5669a-255">Das *hconnection* -Handle wurde von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) erstellt, nachdem eine FTP-Sitzung eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="5669a-255">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span>


```C++
BOOL WINAPI GetFtpFile( HWND hDlg, HINTERNET hConnection,
                        int nFtpFileNameId, int nLocalFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szLocalFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  DWORD dwTransferType;
  TCHAR szBoxTitle[] = TEXT( "Download FTP File" );
  TCHAR szAsciiQuery[] =
    TEXT("Do you want to download as ASCII text?(Default is binary)");
  TCHAR szAsciiDone[] = 
    TEXT( "ASCII Transfer completed successfully..." );
  TCHAR szBinaryDone[] = 
    TEXT( "Binary Transfer completed successfully..." );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nLocalFileNameId, szLocalFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Target File or Destination File Missing" ),
                szBoxTitle, 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  dwTransferType = ( MessageBox( hDlg, 
                                 szAsciiQuery, 
                                 szBoxTitle, 
                                 MB_YESNO ) == IDYES ) ?
                   FTP_TRANSFER_TYPE_ASCII : FTP_TRANSFER_TYPE_BINARY;
  dwTransferType |= INTERNET_FLAG_RELOAD;

  if( !FtpGetFile( hConnection, szFtpFileName, szLocalFileName, FALSE,
                   FILE_ATTRIBUTE_NORMAL, dwTransferType, 0 ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), TEXT( "FtpGetFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg,( dwTransferType == 
                      (FTP_TRANSFER_TYPE_ASCII | INTERNET_FLAG_RELOAD)) ?
                      szAsciiDone : szBinaryDone, szBoxTitle, MB_OK );
  return( TRUE );
}
```



### <a name="placing-files-on-an-ftp-server"></a><span data-ttu-id="5669a-256">Platzieren von Dateien auf einem FTP-Server</span><span class="sxs-lookup"><span data-stu-id="5669a-256">Placing Files on an FTP Server</span></span>

<span data-ttu-id="5669a-257">Es gibt zwei Methoden zum Platzieren einer Datei auf einem FTP-Server:</span><span class="sxs-lookup"><span data-stu-id="5669a-257">There are two methods for placing a file on an FTP server:</span></span>

-   <span data-ttu-id="5669a-258">Verwenden Sie [**ftpopeinfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) mit [**internetschreibdatei**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile).</span><span class="sxs-lookup"><span data-stu-id="5669a-258">Use [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) with [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile).</span></span>
-   <span data-ttu-id="5669a-259">Verwenden Sie [**ftpputfile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).</span><span class="sxs-lookup"><span data-stu-id="5669a-259">Use [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).</span></span>

<span data-ttu-id="5669a-260">Eine Anwendung, die Daten an einen FTP-Server senden muss, aber nicht über eine lokale Datei, die alle Daten enthält, sollte [**ftpopenfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) verwenden, um eine Datei auf dem FTP-Server zu erstellen und zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5669a-260">An application that must send data to an FTP server, but does not have a local file that contains all the data, should use [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) to create and open a file on the ftp server.</span></span> <span data-ttu-id="5669a-261">Die Anwendung kann dann [**internetschreibdatei**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) verwenden, um die Informationen in die Datei hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="5669a-261">The application then can use [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) to upload the information to the file.</span></span>

<span data-ttu-id="5669a-262">Wenn die Datei bereits lokal vorhanden ist, kann die Anwendung [**ftpputfile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) verwenden, um die Datei auf den FTP-Server hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="5669a-262">If the file already exists locally, the application can use [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) to upload the file to the FTP server.</span></span> <span data-ttu-id="5669a-263">[**Ftpputfile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) führt den gesamten mehr Aufwand für das Hochladen einer lokalen Datei auf einen Remote-FTP-Server aus.</span><span class="sxs-lookup"><span data-stu-id="5669a-263">[**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) performs all the overhead that goes with uploading a local file to a remote FTP server.</span></span>

<span data-ttu-id="5669a-264">Im folgenden Beispiel wird eine lokale Datei auf den FTP-Server kopiert.</span><span class="sxs-lookup"><span data-stu-id="5669a-264">The following example copies a local file onto the FTP server.</span></span> <span data-ttu-id="5669a-265">Der lokale Name der Datei wird aus dem Bearbeitungsfeld im übergeordneten Dialogfeld übernommen, dessen IDC im *nlocalfileameid* -Parameter übergeben wird, und der Name, unter dem die Datei auf dem FTP-Server gespeichert wird, wird aus dem Bearbeitungsfeld entnommen, dessen IDC im *nftpfileameid* -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="5669a-265">The local name of the file is taken from the edit box in the parent dialog whose IDC is passed in the *nLocalFileNameId* parameter, and the name under which the file is saved on the FTP server is taken from the edit box whose IDC is passed in the *nFtpFileNameId* parameter.</span></span> <span data-ttu-id="5669a-266">Das *hconnection* -Handle wurde von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) erstellt, nachdem eine FTP-Sitzung eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="5669a-266">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span>


```C++
BOOL WINAPI PutFtpFile( HWND hDlg, HINTERNET hConnection,
                        int nFtpFileNameId, int nLocalFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szLocalFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  DWORD dwTransferType;
  TCHAR szBoxTitle[] = TEXT( "Upload FTP File" );
  TCHAR szASCIIQuery[] =
    TEXT("Do you want to upload as ASCII text? (Default is binary)");
  TCHAR szAsciiDone[] = 
    TEXT( "ASCII Transfer completed successfully..." );
  TCHAR szBinaryDone[] = 
    TEXT( "Binary Transfer completed successfully..." );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nLocalFileNameId, szLocalFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT("Target File or Destination File Missing"),
                szBoxTitle, 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  dwTransferType =
    ( MessageBox( hDlg, 
                  szASCIIQuery, 
                  szBoxTitle, 
                  MB_YESNO ) == IDYES ) ?
    FTP_TRANSFER_TYPE_ASCII : FTP_TRANSFER_TYPE_BINARY;

  if( !FtpPutFile( hConnection, 
                   szLocalFileName, 
                   szFtpFileName, 
                   dwTransferType, 
                   0 ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), TEXT( "FtpGetFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg,
              ( dwTransferType == FTP_TRANSFER_TYPE_ASCII ) ?
                szAsciiDone : szBinaryDone, szBoxTitle, MB_OK );
  return( TRUE );  // Remember to refresh directory listing
}
```



### <a name="deleting-files-from-an-ftp-server"></a><span data-ttu-id="5669a-267">Löschen von Dateien von einem FTP-Server</span><span class="sxs-lookup"><span data-stu-id="5669a-267">Deleting Files from an FTP Server</span></span>

<span data-ttu-id="5669a-268">Um eine Datei von einem FTP-Server zu löschen, verwenden Sie die [**ftpdeletefile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="5669a-268">To delete a file from an FTP server, use the [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) function.</span></span> <span data-ttu-id="5669a-269">Die aufrufende Anwendung muss über die erforderlichen Berechtigungen zum Löschen einer Datei vom FTP-Server verfügen.</span><span class="sxs-lookup"><span data-stu-id="5669a-269">The calling application must have the necessary privileges to delete a file from the FTP server.</span></span>

<span data-ttu-id="5669a-270">Im folgenden Beispiel wird eine Datei vom FTP-Server gelöscht.</span><span class="sxs-lookup"><span data-stu-id="5669a-270">The following example deletes a file from the FTP server.</span></span> <span data-ttu-id="5669a-271">Der Name der zu löschenden Datei wird aus dem Bearbeitungsfeld im übergeordneten Dialogfeld übernommen, dessen IDC int dem *nftpfileameid* -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="5669a-271">The name of the file to be deleted is taken from the edit box in the parent dialog whose IDC is passed int the *nFtpFileNameId* parameter.</span></span> <span data-ttu-id="5669a-272">Das *hconnection* -Handle wurde von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) erstellt, nachdem eine FTP-Sitzung eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="5669a-272">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span> <span data-ttu-id="5669a-273">Da diese Funktion keine Datei Auflistungen oder Verzeichnis Anzeige aktualisiert, sollte der aufrufenden Prozess nach erfolgreichem löschen Vorgehen.</span><span class="sxs-lookup"><span data-stu-id="5669a-273">Since this function does not refresh file listings or directory display, the calling process should do so upon successful deletion.</span></span>


```C++
BOOL WINAPI DeleteFtpFile( HWND hDlg, HINTERNET hConnection,
                           int nFtpFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szBoxTitle[] = TEXT( "Delete FTP File" );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, TEXT( "File Name Must Be Specified!" ),
                szBoxTitle, MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpDeleteFile( hConnection, szFtpFileName ) )
  {
    InternetErrorOut( hDlg, 
                      GetLastError( ), 
                      TEXT( "FtpDeleteFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg, 
              TEXT( "File has been deleted" ), 
              szBoxTitle, 
              MB_OK );
  return( TRUE );  // Remember to refresh directory listing
}
```



### <a name="renaming-files-and-directories-on-an-ftp-server"></a><span data-ttu-id="5669a-274">Umbenennen von Dateien und Verzeichnissen auf einem FTP-Server</span><span class="sxs-lookup"><span data-stu-id="5669a-274">Renaming Files and Directories on an FTP Server</span></span>

<span data-ttu-id="5669a-275">Dateien und Verzeichnisse auf einem FTP-Server können mithilfe der [**ftprenamefile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) -Funktion umbenannt werden.</span><span class="sxs-lookup"><span data-stu-id="5669a-275">Files and directories on an FTP server can be renamed using the [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) function.</span></span> <span data-ttu-id="5669a-276">[**Ftprenamefile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) akzeptiert zwei **null**-terminierte Zeichen folgen, die relativ zum aktuellen Verzeichnis entweder teilweise oder voll qualifizierte Namen enthalten.</span><span class="sxs-lookup"><span data-stu-id="5669a-276">[**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) accepts two **null**-terminated strings that contain either partially or fully qualified names relative to the current directory.</span></span> <span data-ttu-id="5669a-277">Die-Funktion ändert den Namen der von der ersten Zeichenfolge bezeichneten Datei in den von der zweiten Zeichenfolge bezeichneten Namen.</span><span class="sxs-lookup"><span data-stu-id="5669a-277">The function changes the name of the file designated by the first string to the name designated by the second string.</span></span>

<span data-ttu-id="5669a-278">Im folgenden Beispiel wird eine Datei oder ein Verzeichnis auf dem FTP-Server umbenannt.</span><span class="sxs-lookup"><span data-stu-id="5669a-278">The following example renames a file or directory on the FTP server.</span></span> <span data-ttu-id="5669a-279">Der aktuelle Name der Datei oder des Verzeichnisses wird aus dem Bearbeitungsfeld im übergeordneten Dialogfeld übernommen, dessen IDC im *noldfileameid* -Parameter übergeben wird, und der neue Name wird aus dem Bearbeitungsfeld übernommen, dessen IDC im *nnewfilename ameid* -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="5669a-279">The current name of the file or directory is taken from the edit box in the parent dialog whose IDC is passed in the *nOldFileNameId* parameter, and the new name is taken from the edit box whose IDC is passed in the *nNewFileNameId* parameter.</span></span> <span data-ttu-id="5669a-280">Das *hconnection* -Handle wurde von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) erstellt, nachdem eine FTP-Sitzung eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="5669a-280">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span> <span data-ttu-id="5669a-281">Da diese Funktion keine Datei Auflistungen oder Verzeichnis Anzeige aktualisiert, sollte der aufrufenden Prozess bei erfolgreicher Umbenennung Vorgehen.</span><span class="sxs-lookup"><span data-stu-id="5669a-281">Since this function does not refresh file listings or directory display, the calling process should do so upon successful renaming.</span></span>


```C++
BOOL WINAPI RenameFtpFile( HWND hDlg, HINTERNET hConnection,
                           int nOldFileNameId, int nNewFileNameId )
{
  TCHAR szOldFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szNewFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szBoxTitle[] = TEXT( "Rename FTP File" );

  if( !GetDlgItemText( hDlg, nOldFileNameId, szOldFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nNewFileNameId, szNewFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg,
        TEXT( "Both the current and new file names must be supplied" ),
        szBoxTitle, 
        MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpRenameFile( hConnection, szOldFileName, szNewFileName ) )
  {
    MessageBox( hDlg,
        TEXT( "FtpRenameFile failed" ),
        szBoxTitle, 
        MB_OK | MB_ICONERROR );
    return( FALSE );
  }
  return( TRUE );  // Remember to refresh directory listing
}
```



> [!Note]  
> <span data-ttu-id="5669a-282">WinInet unterstützt keine Server Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="5669a-282">WinINet does not support server implementations.</span></span> <span data-ttu-id="5669a-283">Außerdem sollte Sie nicht von einem Dienst verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5669a-283">In addition, it should not be used from a service.</span></span> <span data-ttu-id="5669a-284">Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="5669a-284">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 