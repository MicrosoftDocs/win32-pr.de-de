---
title: Allgemeine Funktionen (Windows Internet)
description: Bei den verschiedenen Internet Protokollen (z. b. FTP und http) werden mehrere der gleichen WinInet-Funktionen verwendet, um Informationen im Internet zu verarbeiten.
ms.assetid: c80768cf-c8c0-4bdf-9ea2-f82c92ade05a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1893b085da1b3e77228e4a9abf75acc166d84726
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106338513"
---
# <a name="common-functions-windows-internet"></a><span data-ttu-id="42ec9-103">Allgemeine Funktionen (Windows Internet)</span><span class="sxs-lookup"><span data-stu-id="42ec9-103">Common Functions (Windows Internet)</span></span>

<span data-ttu-id="42ec9-104">Bei den verschiedenen Internet Protokollen (z. b. FTP und http) werden mehrere der gleichen WinInet-Funktionen verwendet, um Informationen im Internet zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="42ec9-104">The different Internet protocols (such as ftp and http) use several of the same WinINet functions to handle information on the Internet.</span></span> <span data-ttu-id="42ec9-105">Diese gängigen Funktionen behandeln Ihre Aufgaben auf konsistente Weise, unabhängig vom jeweiligen Protokoll, auf das Sie angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="42ec9-105">These common functions handle their tasks in a consistent manner, regardless of the particular protocol to which they are being applied.</span></span> <span data-ttu-id="42ec9-106">Anwendungen können diese Funktionen verwenden, um allgemeine Funktionen zu erstellen, die Tasks über die verschiedenen Protokolle hinweg verarbeiten (z. b. das Lesen von Dateien für FTP und http).</span><span class="sxs-lookup"><span data-stu-id="42ec9-106">Applications can use these functions to create general-purpose functions that handle tasks across the different protocols (such as reading files for ftp and http).</span></span>

<span data-ttu-id="42ec9-107">Die allgemeinen Funktionen behandeln die folgenden Aufgaben:</span><span class="sxs-lookup"><span data-stu-id="42ec9-107">The common functions handle the following tasks:</span></span>

-   <span data-ttu-id="42ec9-108">Herunterladen von Ressourcen aus dem Internet ([**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**internetsetfilepointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer), [**internetfindnextfile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)und [**internetquerydataavailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)).</span><span class="sxs-lookup"><span data-stu-id="42ec9-108">Downloading resources from the Internet ([**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), and [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)).</span></span>
-   <span data-ttu-id="42ec9-109">Einrichten von asynchronen Vorgängen ([**internetsetstatus Callback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)).</span><span class="sxs-lookup"><span data-stu-id="42ec9-109">Setting up asynchronous operations ([**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)).</span></span>
-   <span data-ttu-id="42ec9-110">Anzeigen und Ändern von Optionen ([**internettoption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) und [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)).</span><span class="sxs-lookup"><span data-stu-id="42ec9-110">Viewing and changing options ([**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) and [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)).</span></span>
-   <span data-ttu-id="42ec9-111">Alle Typen von [**hinternethandles**](appendix-a-hinternet-handles.md) ([**internetclosehandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle)) werden geschlossen.</span><span class="sxs-lookup"><span data-stu-id="42ec9-111">Closing all types of [**HINTERNET**](appendix-a-hinternet-handles.md) handles ([**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle)).</span></span>
-   <span data-ttu-id="42ec9-112">Platzieren und Entfernen von Sperren für Ressourcen ([**internetlockrequestfile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) und [**internetunlockrequestfile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)).</span><span class="sxs-lookup"><span data-stu-id="42ec9-112">Placing and removing locks on resources ([**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) and [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)).</span></span>

## <a name="using-common-functions"></a><span data-ttu-id="42ec9-113">Verwenden von gängigen Funktionen</span><span class="sxs-lookup"><span data-stu-id="42ec9-113">Using Common Functions</span></span>

<span data-ttu-id="42ec9-114">In der folgenden Tabelle sind die allgemeinen Funktionen aufgeführt, die in den WinInet-Funktionen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="42ec9-114">The following table lists the common functions included in the WinINet functions.</span></span> <span data-ttu-id="42ec9-115">Die allgemeinen Funktionen können für verschiedene Typen von [**hinternethandles**](appendix-a-hinternet-handles.md) verwendet werden oder können bei verschiedenen Sitzungs Typen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="42ec9-115">The common functions can be used on different types of [**HINTERNET**](appendix-a-hinternet-handles.md) handles or can be used during different types of sessions.</span></span>



| <span data-ttu-id="42ec9-116">Funktion</span><span class="sxs-lookup"><span data-stu-id="42ec9-116">Function</span></span>                                                         | <span data-ttu-id="42ec9-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="42ec9-117">Description</span></span>                                                                                                                                                                                                                                             |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="42ec9-118">**Internetfindnextfile**</span><span class="sxs-lookup"><span data-stu-id="42ec9-118">**InternetFindNextFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)             | <span data-ttu-id="42ec9-119">Setzt die Dateienumeration oder-Suche fort.</span><span class="sxs-lookup"><span data-stu-id="42ec9-119">Continues file enumeration or search.</span></span> <span data-ttu-id="42ec9-120">Erfordert ein Handle, das von der [**ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)-Funktion oder der [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) -Funktion erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="42ec9-120">Requires a handle created by the [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function.</span></span>                                                                            |
| [<span data-ttu-id="42ec9-121">**Internetlockrequestfile**</span><span class="sxs-lookup"><span data-stu-id="42ec9-121">**InternetLockRequestFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile)       | <span data-ttu-id="42ec9-122">Ermöglicht es dem Benutzer, eine Sperre für die verwendete Datei zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="42ec9-122">Allows the user to place a lock on the file that is being used.</span></span> <span data-ttu-id="42ec9-123">Diese Funktion erfordert ein Handle, das von der [**ftpopenfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)-, der [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)-oder der [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="42ec9-123">This function requires a handle returned by the [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function.</span></span> |
| [<span data-ttu-id="42ec9-124">**Internetquerydataavailable**</span><span class="sxs-lookup"><span data-stu-id="42ec9-124">**InternetQueryDataAvailable**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) | <span data-ttu-id="42ec9-125">Ruft die Menge der verfügbaren Daten ab.</span><span class="sxs-lookup"><span data-stu-id="42ec9-125">Retrieves the amount of data available.</span></span> <span data-ttu-id="42ec9-126">Erfordert ein Handle, das von der [**ftpopenfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)-Funktion oder der [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) -Funktion erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="42ec9-126">Requires a handle created by the [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function.</span></span>                                                                                    |
| [<span data-ttu-id="42ec9-127">**InternetQueryOption**</span><span class="sxs-lookup"><span data-stu-id="42ec9-127">**InternetQueryOption**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)               | <span data-ttu-id="42ec9-128">Ruft die Einstellung einer Internet Option ab.</span><span class="sxs-lookup"><span data-stu-id="42ec9-128">Retrieves the setting of an Internet option.</span></span>                                                                                                                                                                                                            |
| [<span data-ttu-id="42ec9-129">**Internetreadfile**</span><span class="sxs-lookup"><span data-stu-id="42ec9-129">**InternetReadFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)                     | <span data-ttu-id="42ec9-130">Liest URL-Daten.</span><span class="sxs-lookup"><span data-stu-id="42ec9-130">Reads URL data.</span></span> <span data-ttu-id="42ec9-131">Erfordert ein Handle, das von der [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)-, [**ftpopenfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)-oder [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) -Funktion erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="42ec9-131">Requires a handle created by the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function.</span></span>                                                                |
| [<span data-ttu-id="42ec9-132">**Internetsetfilepointer**</span><span class="sxs-lookup"><span data-stu-id="42ec9-132">**InternetSetFilePointer**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer)         | <span data-ttu-id="42ec9-133">Legt die Position für den nächsten Lesevorgang in einer Datei fest.</span><span class="sxs-lookup"><span data-stu-id="42ec9-133">Sets the position for the next read in a file.</span></span> <span data-ttu-id="42ec9-134">Erfordert ein Handle, das von [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (nur auf einer HTTP-URL) erstellt wird, oder ein Handle, das von [**httpoperrequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) mithilfe des HTTP-Verbs Get erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="42ec9-134">Requires a handle created by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (on an HTTP URL only) or a handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) using the GET HTTP verb.</span></span>                 |
| [<span data-ttu-id="42ec9-135">**Internettoption**</span><span class="sxs-lookup"><span data-stu-id="42ec9-135">**InternetSetOption**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)                   | <span data-ttu-id="42ec9-136">Legt eine Internet Option fest.</span><span class="sxs-lookup"><span data-stu-id="42ec9-136">Sets an Internet option.</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="42ec9-137">**Internetsetstatus Callback**</span><span class="sxs-lookup"><span data-stu-id="42ec9-137">**InternetSetStatusCallback**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)   | <span data-ttu-id="42ec9-138">Legt eine Rückruffunktion fest, die Statusinformationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="42ec9-138">Sets a callback function that receives status information.</span></span> <span data-ttu-id="42ec9-139">Weist dem vorgesehenen [**HINTERNET**](appendix-a-hinternet-handles.md) -Handle und allen davon abgeleiteten Handles eine Rückruffunktion zu.</span><span class="sxs-lookup"><span data-stu-id="42ec9-139">Assigns a callback function to the designated [**HINTERNET**](appendix-a-hinternet-handles.md) handle and all handles derived from it.</span></span>                                                      |
| [<span data-ttu-id="42ec9-140">**Internetunlockrequestfile**</span><span class="sxs-lookup"><span data-stu-id="42ec9-140">**InternetUnlockRequestFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)   | <span data-ttu-id="42ec9-141">Entsperrt eine Datei, die mithilfe der [**internetlockrequestfile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) -Funktion gesperrt wurde.</span><span class="sxs-lookup"><span data-stu-id="42ec9-141">Unlocks a file that was locked using the [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) function.</span></span>                                                                                                                                           |



 

<span data-ttu-id="42ec9-142">Das Lesen von Dateien, das Suchen der nächsten Datei, das Bearbeiten von Optionen und das Einrichten von asynchronen Vorgängen wird häufig von den Funktionen verwendet, die verschiedene Protokolle und [**HINTERNET**](appendix-a-hinternet-handles.md) -handle-Typen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="42ec9-142">Reading files, finding the next file, manipulating options, and setting up asynchronous operations are common to the functions that support various protocols and [**HINTERNET**](appendix-a-hinternet-handles.md) handle types.</span></span>

### <a name="reading-files"></a><span data-ttu-id="42ec9-143">Lesen von Dateien</span><span class="sxs-lookup"><span data-stu-id="42ec9-143">Reading Files</span></span>

<span data-ttu-id="42ec9-144">Die [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) -Funktion wird zum Herunterladen von Ressourcen von einem [**hinternethandle**](appendix-a-hinternet-handles.md) verwendet, das von der [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)-, [**ftpopenfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)-oder [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="42ec9-144">The [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) function is used to download resources from an [**HINTERNET**](appendix-a-hinternet-handles.md) handle returned by the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function.</span></span>

<span data-ttu-id="42ec9-145">[**Internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) akzeptiert eine void-Zeiger Variable, die die Adresse eines Puffers enthält, und einen Zeiger auf eine Variable, die die Länge des Puffers enthält.</span><span class="sxs-lookup"><span data-stu-id="42ec9-145">[**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) accepts a void pointer variable that contains the address of a buffer and a pointer to a variable that contains the length of the buffer.</span></span> <span data-ttu-id="42ec9-146">Die-Funktion gibt die Daten im Puffer und die Menge der Daten zurück, die in den Puffer heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="42ec9-146">The function returns the data in the buffer and the amount of data downloaded into the buffer.</span></span>

<span data-ttu-id="42ec9-147">Die WinInet-Funktionen stellen zwei Verfahren zum Herunterladen einer vollständigen Ressource bereit:</span><span class="sxs-lookup"><span data-stu-id="42ec9-147">The WinINet functions provide two techniques to download an entire resource:</span></span>

-   <span data-ttu-id="42ec9-148">Die [**internetquerydataavailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="42ec9-148">The [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) function.</span></span>
-   <span data-ttu-id="42ec9-149">Die Rückgabewerte von " [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)".</span><span class="sxs-lookup"><span data-stu-id="42ec9-149">The return values of [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span></span>

<span data-ttu-id="42ec9-150">[**Internetquerydataavailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) übernimmt das [**hinternethandle**](appendix-a-hinternet-handles.md) , das von [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**ftpopenfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)oder [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) erstellt wurde (nachdem [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) für das Handle aufgerufen wurde), und gibt die Anzahl der verfügbaren Bytes zurück.</span><span class="sxs-lookup"><span data-stu-id="42ec9-150">[**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) takes the [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) (after [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) has been called on the handle) and returns the number of bytes available.</span></span> <span data-ttu-id="42ec9-151">Die Anwendung muss einen Puffer zuordnen, der der Anzahl der verfügbaren Bytes entspricht, plus 1 für das abschließende **null** -Zeichen, und diesen Puffer mit [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)verwenden.</span><span class="sxs-lookup"><span data-stu-id="42ec9-151">The application should allocate a buffer equal to the number of bytes available, plus 1 for the terminating **null** character, and use that buffer with [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span></span> <span data-ttu-id="42ec9-152">Diese Methode funktioniert nicht immer, weil [**internetquerydataavailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) die Dateigröße überprüft, die im Header und nicht in der eigentlichen Datei aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="42ec9-152">This method does not always work because [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) is checking the file size listed in the header and not the actual file.</span></span> <span data-ttu-id="42ec9-153">Die Informationen in der Header Datei sind möglicherweise veraltet, oder die Header Datei fehlt, da Sie derzeit nicht unter allen Standards erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="42ec9-153">The information in the header file could be outdated, or the header file could be missing, since it is not currently required under all standards.</span></span>

<span data-ttu-id="42ec9-154">Im folgenden Beispiel wird der Inhalt der Ressource gelesen, auf die über das hresource-handle zugegriffen wird, und wird im Bearbeitungsfeld angezeigt, das von intctrlid angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="42ec9-154">The following example reads the contents of the resource accessed by the hResource handle and displayed in the edit box indicated by intCtrlID.</span></span>


```C++
int WINAPI Dumper(HWND hX, int intCtrlID, HINTERNET hResource)
{
    LPTSTR    lpszData;           // buffer for the data
    DWORD     dwSize;             // size of the data available
    DWORD     dwDownloaded;       // size of the downloaded data
    DWORD     dwSizeSum=0;        // size of the data in the text box
    LPTSTR    lpszHolding;        // buffer to merge the text box 
                                  // data and buffer

    // Set the cursor to an hourglass.
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    // This loop handles reading the data.  
    do
    {
        // The call to InternetQueryDataAvailable determines the
        // amount of data available to download.
        if (!InternetQueryDataAvailable(hResource,&dwSize,0,0))
        {
            ErrorOut(hX,GetLastError(),TEXT("InternetReadFile"));
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
        {    
            // Allocate a buffer of the size returned by
            // InternetQueryDataAvailable.
            lpszData = new TCHAR[dwSize+1];

            // Read the data from the HINTERNET handle.
            if(!InternetReadFile(hResource,(LPVOID)lpszData,
                                 dwSize,&dwDownloaded))
            {
                ErrorOut(hX,GetLastError(),TEXT("InternetReadFile"));
                delete[] lpszData;
                break;
            }
            else
            {
                // Add a null terminator to the end of the 
                // data buffer.
                lpszData[dwDownloaded]='\0';

                // Allocate the holding buffer.
                lpszHolding = new TCHAR[dwSizeSum + dwDownloaded + 1];
                    
                // Check if there has been any data written to 
                // the text box.
                if (dwSizeSum != 0)
                {
                    // Retrieve the data stored in the text 
                    // box, if any.
                    GetDlgItemText(hX,intCtrlID,
                                   (LPTSTR)lpszHolding, 
                                   dwSizeSum);
                         
                    // Add a null terminator at the end of 
                    // the text box data.
                    lpszHolding[dwSizeSum]='\0';
                }
                else
                {
                    // Make the holding buffer an empty string. 
                    lpszHolding[0]='\0';
                }

                size_t cchDest = dwSizeSum + dwDownloaded + 
                                 dwDownloaded + 1;
                LPTSTR pszDestEnd;
                size_t cchRemaining;

                // Add the new data to the holding buffer.
                HRESULT hr = StringCchCatEx(lpszHolding, cchDest, 
                                            lpszData, &pszDestEnd, 
                                            &cchRemaining, 
                                            STRSAFE_NO_TRUNCATION);
                if(SUCCEEDED(hr))
                {
                    // Write the holding buffer to the text box.
                    SetDlgItemText(hX,intCtrlID,(LPTSTR)lpszHolding);

                    // Delete the two buffers.
                    delete[] lpszHolding;
                    delete[] lpszData;

                    // Add the size of the downloaded data to 
                    // the text box data size.
                    dwSizeSum = dwSizeSum + dwDownloaded + 1;

                    // Check the size of the remaining data.  
                    // If it is zero, break.
                    if (dwDownloaded == 0)
                    {
                        break;
                    }                    
                    else
                    {
                        //  Insert error handling code here.
                    }
                }
            }
        }
    }
    while(TRUE);

    // Close the HINTERNET handle.
    InternetCloseHandle(hResource);

    // Set the cursor back to an arrow.
    SetCursor(LoadCursor(NULL,IDC_ARROW));

    // Return.
    return TRUE;
}
```



<span data-ttu-id="42ec9-155">" [**Internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) " gibt NULL Bytes zurück und wird erfolgreich abgeschlossen, wenn alle verfügbaren Daten gelesen wurden.</span><span class="sxs-lookup"><span data-stu-id="42ec9-155">[**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) returns zero bytes read and completes successfully when all available data has been read.</span></span> <span data-ttu-id="42ec9-156">Dadurch kann eine Anwendung " [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) " in einer Schleife verwenden, um die Daten herunterzuladen und zu beenden, wenn NULL Bytes gelesen und erfolgreich abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="42ec9-156">This allows an application to use [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) in a loop to download the data and exit when it returns zero bytes read and completes successfully.</span></span>

<span data-ttu-id="42ec9-157">Das folgende Beispiel liest die Ressource aus dem Internet und zeigt die Ressource im Bearbeitungsfeld an, das von intctrlid angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="42ec9-157">The following example reads the resource from the Internet and displays the resource in the edit box indicated by intCtrlID.</span></span> <span data-ttu-id="42ec9-158">Das [**HINTERNET**](appendix-a-hinternet-handles.md) handle, HINTERNET, wurde von [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**ftpopumfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)oder [**httpopanrequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) zurückgegeben (nach dem Senden durch [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)).</span><span class="sxs-lookup"><span data-stu-id="42ec9-158">The [**HINTERNET**](appendix-a-hinternet-handles.md) handle, hInternet, was returned by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) (after being sent by [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)).</span></span>


```C++
int WINAPI Dump(HWND hX, int intCtrlID, HINTERNET hResource)
{
     DWORD dwSize = 0;
     LPTSTR lpszData;
     LPTSTR lpszOutPut;
     LPTSTR lpszHolding = TEXT("");
     int nCounter = 1;
     int nBufferSize = 0;
     DWORD BigSize = 8000;

     // Set the cursor to an hourglass.
     SetCursor(LoadCursor(NULL,IDC_WAIT));

     // Begin the loop that reads the data.
     do
     {
          // Allocate the buffer.
          lpszData =new TCHAR[BigSize+1];

          // Read the data.
          if(!InternetReadFile(hResource,
                              (LPVOID)lpszData,
                              BigSize,&dwSize))
          {
               ErrorOut(hX,GetLastError(),TEXT("InternetReadFile"));
               delete []lpszData;
               break;
          }
          else
          {
               // Add a null terminator to the end of the buffer.
               lpszData[dwSize]='\0';

               // Check if all of the data has been read.  This should
               // never get called on the first time through the loop.
               if (dwSize == 0)
               {
                    // Write the final data to the text box.
                    SetDlgItemText(hX,intCtrlID,lpszHolding);

                    // Delete the existing buffers.
                    delete [] lpszData;
                    delete [] lpszHolding;
                    break;
               }

               // Determine the buffer size to hold the new data and
               // the data already written to the text box (if any).
               nBufferSize = (nCounter*BigSize)+1;

               // Increment the number of buffers read.
               nCounter++;               

               // Allocate the output buffer.
               lpszOutPut = new TCHAR[nBufferSize];

               // Make sure the buffer is not the initial buffer.
               if(nBufferSize != int(BigSize+1))
               {
                    // Copy the data in the holding buffer.
                    StringCchCopy(lpszOutPut,nBufferSize,lpszHolding);
                    // Add error handling code here.

                    // Concatenate the new buffer with the 
                    // output buffer.
                    StringCchCat(lpszOutPut, nBufferSize, lpszData);
                    // Add error handling code here.
     
                    // Delete the holding buffer.
                    delete [] lpszHolding;
               }
               else
               {
                    // Copy the data buffer.
                    StringCchCopy(lpszOutPut, nBufferSize, lpszData);
                    // Add error handling code here.
               }

               // Allocate a holding buffer.
               lpszHolding = new TCHAR[nBufferSize]; 

               // Copy the output buffer into the holding buffer.
               memcpy(lpszHolding,lpszOutPut,nBufferSize);

               // Delete the other buffers.
               delete [] lpszData;
               delete [] lpszOutPut;

          }

     }
     while (TRUE);

     // Close the HINTERNET handle.
     InternetCloseHandle(hResource);

     // Set the cursor back to an arrow.
     SetCursor(LoadCursor(NULL,IDC_ARROW));

     // Return.
     return TRUE;
}
```



### <a name="finding-the-next-file"></a><span data-ttu-id="42ec9-159">Suchen der nächsten Datei</span><span class="sxs-lookup"><span data-stu-id="42ec9-159">Finding the Next File</span></span>

<span data-ttu-id="42ec9-160">Die Funktion " [**internetfindnextfile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) " wird verwendet, um die nächste Datei in einer Dateisuche mithilfe der Suchparameter und des [**hinternethandles**](appendix-a-hinternet-handles.md) aus [**ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)oder [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)zu suchen.</span><span class="sxs-lookup"><span data-stu-id="42ec9-160">The [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) function is used to find the next file in a file search, using the search parameters and [**HINTERNET**](appendix-a-hinternet-handles.md) handle from [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span>

<span data-ttu-id="42ec9-161">Um eine Dateisuche abzuschließen, wenden Sie weiterhin [**internetfindnextfile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) mithilfe des [**hinternethandles**](appendix-a-hinternet-handles.md) , das von [**ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)zurückgegeben wird, oder [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) an, bis die Funktion mit der erweiterten Fehlermeldung [ \_ nicht \_ mehr \_ Dateien](wininet-errors.md)fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="42ec9-161">To complete a file search, continue to call [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) using the [**HINTERNET**](appendix-a-hinternet-handles.md) handle returned by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) until the function fails with the extended error message [ERROR\_NO\_MORE\_FILES](wininet-errors.md).</span></span> <span data-ttu-id="42ec9-162">Um die erweiterten Fehlerinformationen abzurufen, müssen Sie die [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="42ec9-162">To get the extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

<span data-ttu-id="42ec9-163">Im folgenden Beispiel wird der Inhalt eines FTP-Verzeichnisses im Listenfeld angezeigt, das von lstdirectory angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="42ec9-163">The following example displays the contents of an FTP directory in the list box indicated by lstDirectory.</span></span> <span data-ttu-id="42ec9-164">Das [**HINTERNET**](appendix-a-hinternet-handles.md) handle, hconnect, ist ein Handle, das von der [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) -Funktion zurückgegeben wird, nachdem eine FTP-Sitzung eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="42ec9-164">The [**HINTERNET**](appendix-a-hinternet-handles.md) handle, hConnect, is a handle returned by the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function after it establishes an FTP session.</span></span>


```C++
bool WINAPI DisplayDir( HWND hX, 
                        int lstDirectory, 
                        HINTERNET hConnect, 
                        DWORD dwFlag )
{
     WIN32_FIND_DATA pDirInfo;
     HINTERNET hDir;
     TCHAR DirList[MAX_PATH];

     // Set the cursor to an hourglass.
     SetCursor(LoadCursor(NULL,IDC_WAIT));

     // Reset the list box.
     SendDlgItemMessage(hX, lstDirectory,LB_RESETCONTENT,0,0);

     // Find the first file.
     hDir = FtpFindFirstFile (hConnect, TEXT ("*.*"), 
                              &pDirInfo, dwFlag, 0);
     if (!hDir)                                     
     {
          // Check if the error was because there were no files.
          if (GetLastError()  == ERROR_NO_MORE_FILES) 
          {
               // Alert user.
               MessageBox(hX, TEXT("There are no files here!!!"), 
                          TEXT("Display Dir"), MB_OK);

               // Close the HINTERNET handle.
               InternetCloseHandle(hDir);

               // Set the cursor back to an arrow.
               SetCursor(LoadCursor(NULL,IDC_ARROW));

               // Return.
               return TRUE;
          }
          else 
          {
               // Call error handler.
               ErrorOut (hX, GetLastError (), TEXT("FindFirst error: "));

               // Close the HINTERNET handle.
               InternetCloseHandle(hDir);

               // Set the cursor back to an arrow.
               SetCursor(LoadCursor(NULL,IDC_ARROW));

               // Return.
               return FALSE;
          }
     }
     else
     {
          // Write the file name to a string.
          StringCchPrintf(DirList, MAX_PATH, pDirInfo.cFileName);

          // Check the type of file.
          if (pDirInfo.dwFileAttributes == FILE_ATTRIBUTE_DIRECTORY)
          {
               // Add <DIR> to indicate that this is 
               // a directory to the user.
               StringCchCat(DirList, MAX_PATH, TEXT(" <DIR> "));
               // Add error handling code here.
          }
       
          // Add the file name (or directory) to the list box.
          SendDlgItemMessage(hX, lstDirectory, LB_ADDSTRING,
                             0, (LPARAM)DirList);
     }
     do
     {
          // Find the next file.
          if (!InternetFindNextFile (hDir, &pDirInfo))
          {
               // Check if there are no more files left. 
               if ( GetLastError() == ERROR_NO_MORE_FILES ) 
               {
                    // Close the HINTERNET handle.
                    InternetCloseHandle(hDir);

                    // Set the cursor back to an arrow.
                    SetCursor(LoadCursor(NULL,IDC_ARROW));

                    // Return.
                    return TRUE;
               }
               else
               {   
                    // Handle the error.
                    ErrorOut (hX, GetLastError(), 
                              TEXT("InternetFindNextFile"));

                    // Close the HINTERNET handle.
                    InternetCloseHandle(hDir);

                    // Set the cursor back to an arrow.
                    SetCursor(LoadCursor(NULL,IDC_ARROW));

                    // Return.
                    return FALSE;
               }
           }
           else
           {
               // Write the file name to a string.
               StringCchPrintf(DirList, MAX_PATH, pDirInfo.cFileName);

               // Check the type of file.
               if(pDirInfo.dwFileAttributes==FILE_ATTRIBUTE_DIRECTORY)
               {
                    // Add <DIR> to indicate that this is a 
                    // directory to the user.
                    StringCchCat(DirList, MAX_PATH, TEXT(" <DIR> "));
                    // Add error handling code here.
               }
     
               // Add the file name (or directory) to the list box.
               SendDlgItemMessage(hX, lstDirectory, LB_ADDSTRING,
                                  0, (LPARAM)DirList);
           }
     }
     while ( TRUE);
     
}
```



### <a name="manipulating-options"></a><span data-ttu-id="42ec9-165">Bearbeiten von Optionen</span><span class="sxs-lookup"><span data-stu-id="42ec9-165">Manipulating Options</span></span>

<span data-ttu-id="42ec9-166">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) und [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) werden verwendet, um die WinInet-Optionen zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="42ec9-166">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) and [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) are used to manipulate the WinINet options.</span></span>

<span data-ttu-id="42ec9-167">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) akzeptiert eine Variable, die die festzulegende Option angibt, einen Puffer, der die Options Einstellung enthalten soll, und einen Zeiger, der die Adresse der Variablen enthält, die die Länge des Puffers enthält.</span><span class="sxs-lookup"><span data-stu-id="42ec9-167">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) accepts a variable that indicates the option to set, a buffer to hold the option setting, and a pointer that contains the address of the variable that contains the length of the buffer.</span></span>

<span data-ttu-id="42ec9-168">[**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) akzeptiert eine Variable, die die abzurufende Option, einen Puffer zum Speichern der Options Einstellung und einen Zeiger mit der Adresse der Variablen angibt, die die Länge des Puffers enthält.</span><span class="sxs-lookup"><span data-stu-id="42ec9-168">[**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) accepts a variable that indicates the option to retrieve, a buffer to hold the option setting, and a pointer that contains the address of the variable that contains the length of the buffer.</span></span>

### <a name="setting-up-asynchronous-operations"></a><span data-ttu-id="42ec9-169">Einrichten von asynchronen Vorgängen</span><span class="sxs-lookup"><span data-stu-id="42ec9-169">Setting Up Asynchronous Operations</span></span>

<span data-ttu-id="42ec9-170">Die WinInet-Funktionen werden standardmäßig synchron ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="42ec9-170">By default, the WinINet functions operate synchronously.</span></span> <span data-ttu-id="42ec9-171">Eine Anwendung kann einen asynchronen Vorgang anfordern, indem das [Internet \_ Flag \_ Async](api-flags.md) -Flag im Aufrufen der [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) -Funktion festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="42ec9-171">An application can request asynchronous operation by setting the [INTERNET\_FLAG\_ASYNC](api-flags.md) flag in the call to the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function.</span></span> <span data-ttu-id="42ec9-172">Alle zukünftigen Aufrufe von Handles, die von dem von [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) zurückgegebenen handle abgeleitet werden, werden asynchron durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="42ec9-172">All future calls made against handles derived from the handle returned from [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) are made asynchronously.</span></span>

<span data-ttu-id="42ec9-173">Der Grund für den asynchronen und synchronen Betrieb besteht darin, dass eine Single Thread Anwendung die Auslastung der CPU maximieren kann, ohne dass auf den Abschluss der Netzwerk-e/a gewartet werden muss.</span><span class="sxs-lookup"><span data-stu-id="42ec9-173">The rationale for asynchronous versus synchronous operation is to allow a single-threaded application to maximize its utilization of the CPU without having to wait for network I/O to complete.</span></span> <span data-ttu-id="42ec9-174">Daher kann der Vorgang abhängig von der Anforderung synchron oder asynchron ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="42ec9-174">Therefore, depending on the request, the operation might complete synchronously or asynchronously.</span></span> <span data-ttu-id="42ec9-175">Die Anwendung sollte den Rückgabecode überprüfen.</span><span class="sxs-lookup"><span data-stu-id="42ec9-175">The application should check the return code.</span></span> <span data-ttu-id="42ec9-176">Wenn eine Funktion " **false** " oder " **null**" zurückgibt und " [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) " eine ausstehende Fehler-e/a zurückgibt \_ \_ , wird die Anforderung asynchron durchgeführt, und die Anwendung wird mit dem Internet \_ Status \_ Request Complete aufgerufen, \_ Wenn die Funktion abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="42ec9-176">If a function returns **FALSE** or **NULL**, and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_IO\_PENDING, the request has been made asynchronously, and the application is called back with INTERNET\_STATUS\_REQUEST\_COMPLETE when the function has completed.</span></span>

<span data-ttu-id="42ec9-177">Um mit dem asynchronen Vorgang zu beginnen, muss die Anwendung das [Internet \_ Flag \_ Async](api-flags.md) -Flag im Aufrufen von [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)festlegen.</span><span class="sxs-lookup"><span data-stu-id="42ec9-177">To begin asynchronous operation, the application must set the [INTERNET\_FLAG\_ASYNC](api-flags.md) flag in its call to [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="42ec9-178">Die Anwendung muss dann mithilfe von [**internetsetstatus Callback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)eine gültige Rückruffunktion registrieren.</span><span class="sxs-lookup"><span data-stu-id="42ec9-178">The application must then register a valid callback function, using [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback).</span></span>

<span data-ttu-id="42ec9-179">Nachdem eine Rückruffunktion für ein Handle registriert wurde, können alle Vorgänge für dieses Handle Status Hinweise generieren, vorausgesetzt, dass der beim Erstellen des Handles angegebene Kontextwert nicht 0 (null) war.</span><span class="sxs-lookup"><span data-stu-id="42ec9-179">After a callback function is registered for a handle, all operations on that handle can generate status indications, provided that the context value that was supplied when the handle was created was not zero.</span></span> <span data-ttu-id="42ec9-180">Das Bereitstellen eines NULL-Kontext Werts erzwingt, dass ein Vorgang synchron ausgeführt wird, obwohl in [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)das [Internet Kennzeichen \_ \_ Async](api-flags.md) angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="42ec9-180">Providing a zero context value forces an operation to complete synchronously, even though [INTERNET\_FLAG\_ASYNC](api-flags.md) was specified in [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span>

<span data-ttu-id="42ec9-181">Status Hinweise geben der Anwendung Feedback zum Fortschritt von Netzwerk Vorgängen, z. b. zum Auflösen eines Host namens, zum Herstellen einer Verbindung mit einem Server und zum Empfangen von Daten.</span><span class="sxs-lookup"><span data-stu-id="42ec9-181">Status indications give the application feedback about the progress of network operations, such as resolving a host name, connecting to a server, and receiving data.</span></span> <span data-ttu-id="42ec9-182">Für ein Handle können drei Status Hinweise zum besonderen Zweck erstellt werden:</span><span class="sxs-lookup"><span data-stu-id="42ec9-182">Three special-purpose status indications can be made for a handle:</span></span>

-   <span data-ttu-id="42ec9-183">\_ \_ \_ Das Schließen des Internet Status Handles ist die letzte Status Anzeige, die für ein Handle erfolgt.</span><span class="sxs-lookup"><span data-stu-id="42ec9-183">INTERNET\_STATUS\_HANDLE\_CLOSING is the last status indication that is made for a handle.</span></span>
-   <span data-ttu-id="42ec9-184">\_ \_ Das erstellte Internet Status handle zeigt an, \_ wann das Handle erstmalig erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="42ec9-184">INTERNET\_STATUS\_HANDLE\_CREATED indicates when the handle is initially created.</span></span>
-   <span data-ttu-id="42ec9-185">Der Internet \_ Status \_ Request \_ Complete gibt an, dass ein asynchroner Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="42ec9-185">INTERNET\_STATUS\_REQUEST\_COMPLETE indicates an asynchronous operation has completed.</span></span>

<span data-ttu-id="42ec9-186">Die Anwendung muss die asynchrone [**Internet \_ \_ Ergebnis**](/windows/desktop/api/Wininet/ns-wininet-internet_async_result) Struktur überprüfen, um zu bestimmen, ob der Vorgang erfolgreich war oder fehlgeschlagen ist \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="42ec9-186">The application must check the [**INTERNET\_ASYNC\_RESULT**](/windows/desktop/api/Wininet/ns-wininet-internet_async_result) structure to determine whether the operation succeeded or failed after receiving an INTERNET\_STATUS\_REQUEST\_COMPLETE indication.</span></span>

<span data-ttu-id="42ec9-187">Das folgende Beispiel zeigt ein Beispiel für eine Rückruffunktion und einen Aufrufen von [**internetsetstatus Callback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) , um die Funktion als Rückruffunktion zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="42ec9-187">The following sample shows an example of a callback function and a call to [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) to register the function as the callback function.</span></span>


```C++
void CALLBACK InternetCallback(
    HINTERNET hInternet,
    DWORD_PTR dwcontext,
    DWORD dwInternetStatus,
    LPVOID lpvStatusInformation,
    DWORD dwStatusInformationLength
    )
{
    _tprintf(TEXT("%0xd %0xp %0xd %0xp %0xd\n"),
             hInternet,
             dwcontext,
             dwInternetStatus,
             lpvStatusInformation,
             dwStatusInformationLength);
};

INTERNET_STATUS_CALLBACK dwISC =
    InternetSetStatusCallback(hInternet, InternetCallback); 
```



### <a name="closing-hinternet-handles"></a><span data-ttu-id="42ec9-188">Schließen von HINTERNET-Handles</span><span class="sxs-lookup"><span data-stu-id="42ec9-188">Closing HINTERNET Handles</span></span>

<span data-ttu-id="42ec9-189">Alle [**HINTERNET**](appendix-a-hinternet-handles.md) -Handles können mithilfe der [**internetclosehandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) -Funktion geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="42ec9-189">All [**HINTERNET**](appendix-a-hinternet-handles.md) handles can be closed by using the [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) function.</span></span> <span data-ttu-id="42ec9-190">Client Anwendungen müssen alle **hinternethandles** schließen, die vom **HINTERNET** -handle abgeleitet sind, das Sie schließen möchten, bevor Sie [**internetclosehandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) für das Handle aufrufen.</span><span class="sxs-lookup"><span data-stu-id="42ec9-190">Client applications must close all **HINTERNET** handles derived from the **HINTERNET** handle they are trying to close before calling [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) on the handle.</span></span>

<span data-ttu-id="42ec9-191">Im folgenden Beispiel wird die Handle-Hierarchie veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="42ec9-191">The following example illustrates the handle hierarchy.</span></span>


```C++
HINTERNET hRootHandle, hOpenUrlHandle;

hRootHandle = InternetOpen( TEXT("Example"), 
                            INTERNET_OPEN_TYPE_DIRECT, 
                            NULL, 
                            NULL, 0);

hOpenUrlHandle = InternetOpenUrl(hRootHandle, 
    TEXT("https://www.server.com/default.htm"), NULL, 0, 
    INTERNET_FLAG_RAW_DATA,0);

// Close the handle created by InternetOpenUrl so that the
// InternetOpen handle can be closed.
InternetCloseHandle(hOpenUrlHandle); 

// Close the handle created by InternetOpen.
InternetCloseHandle(hRootHandle);
```



### <a name="locking-and-unlocking-resources"></a><span data-ttu-id="42ec9-192">Sperren und Entsperren von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="42ec9-192">Locking and Unlocking Resources</span></span>

<span data-ttu-id="42ec9-193">Mit der [**internetlockrequestfile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) -Funktion kann eine Anwendung sicherstellen, dass die zwischengespeicherte Ressource, die dem an Sie über gebenden [**HINTERNET**](appendix-a-hinternet-handles.md) -Handle zugeordnet ist, nicht aus dem Cache verschwindet.</span><span class="sxs-lookup"><span data-stu-id="42ec9-193">The [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) function allows an application to ensure that the cached resource associated with the [**HINTERNET**](appendix-a-hinternet-handles.md) handle passed to it does not disappear from the cache.</span></span> <span data-ttu-id="42ec9-194">Wenn ein anderer Download versucht, einen Commit für eine Ressource durchzusetzen, die dieselbe URL wie die gesperrte Datei hat, vermeidet der Cache das Entfernen der Datei durch einen sicheren Löschvorgang.</span><span class="sxs-lookup"><span data-stu-id="42ec9-194">If another download tries to commit a resource that has the same URL as the locked file, the cache avoids removing the file by doing a safe delete.</span></span> <span data-ttu-id="42ec9-195">Nachdem die Anwendung die [**internetunlockrequestfile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile) -Funktion aufgerufen hat, erhält der Cache die Berechtigung zum Löschen der Datei.</span><span class="sxs-lookup"><span data-stu-id="42ec9-195">After the application calls the [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile) function, the cache is given permission to delete the file.</span></span>

<span data-ttu-id="42ec9-196">Wenn das Flag " [Internet \_ Flag \_ No \_ Cache \_ Write](api-flags.md) " oder " [Internet \_ Flag \_ Not \_ Cache](api-flags.md) " festgelegt wurde, erstellt [**internetlockrequestfile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) eine temporäre Datei mit der Erweiterung tmp, es sei denn, das Handle ist mit einer HTTPS-Ressource verbunden.</span><span class="sxs-lookup"><span data-stu-id="42ec9-196">If the [INTERNET\_FLAG\_NO\_CACHE\_WRITE](api-flags.md) or [INTERNET\_FLAG\_DONT\_CACHE](api-flags.md) flag has been set, [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) creates a temporary file with the extension TMP, unless the handle is connected to an https resource.</span></span> <span data-ttu-id="42ec9-197">Wenn die Funktion auf eine HTTPS-Ressource zugreift und das Internet \_ Flag \_ kein Cache \_ \_ Schreibvorgang (oder Internet \_ Flag nicht \_ \_ Cache) festgelegt wurde, schlägt [**internetlockrequestfile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) fehl.</span><span class="sxs-lookup"><span data-stu-id="42ec9-197">If the function accesses an https resource and INTERNET\_FLAG\_NO\_CACHE\_WRITE (or INTERNET\_FLAG\_DONT\_CACHE) has been set, [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) fails.</span></span>

> [!Note]  
> <span data-ttu-id="42ec9-198">WinInet unterstützt keine Server Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="42ec9-198">WinINet does not support server implementations.</span></span> <span data-ttu-id="42ec9-199">Außerdem sollte Sie nicht von einem Dienst verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="42ec9-199">In addition, it should not be used from a service.</span></span> <span data-ttu-id="42ec9-200">Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="42ec9-200">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 
