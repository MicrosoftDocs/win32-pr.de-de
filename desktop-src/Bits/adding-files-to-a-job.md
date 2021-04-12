---
title: Hinzufügen von Dateien zu einem Auftrag
description: Ein Auftrag enthält eine oder mehrere Dateien, die Sie übertragen möchten.
ms.assetid: fb6e7219-b6ca-4f72-b7a3-60d65e8f3892
keywords:
- Übertragen von Auftrags Bits, Hinzufügen von Dateien
- Datei Übertragungs Bits, hinzufügen
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: ecb46a535fee117750b8b46066d798a4525aa44c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948884"
---
# <a name="adding-files-to-a-job"></a><span data-ttu-id="c81cc-105">Hinzufügen von Dateien zu einem Auftrag</span><span class="sxs-lookup"><span data-stu-id="c81cc-105">Adding Files to a Job</span></span>

<span data-ttu-id="c81cc-106">Ein Auftrag enthält eine oder mehrere Dateien, die Sie übertragen möchten.</span><span class="sxs-lookup"><span data-stu-id="c81cc-106">A job contains one or more files that you want to transfer.</span></span> <span data-ttu-id="c81cc-107">Verwenden Sie eine der folgenden Methoden, um einem Auftrag Dateien hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="c81cc-107">Use one of the following methods to add files to a job:</span></span>

<dl> <dt>

<span data-ttu-id="c81cc-108"><span id="IBackgroundCopyJob__AddFile"></span><span id="ibackgroundcopyjob__addfile"></span><span id="IBACKGROUNDCOPYJOB__ADDFILE"></span>[**Ibackgroundcopyjob:: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)</span><span class="sxs-lookup"><span data-stu-id="c81cc-108"><span id="IBackgroundCopyJob__AddFile"></span><span id="ibackgroundcopyjob__addfile"></span><span id="IBACKGROUNDCOPYJOB__ADDFILE"></span>[**IBackgroundCopyJob::AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)</span></span>
</dt> <dd>

<span data-ttu-id="c81cc-109">Fügt einem Auftrag eine einzelne Datei hinzu.</span><span class="sxs-lookup"><span data-stu-id="c81cc-109">Adds a single file to a job.</span></span>

</dd> <dt>

<span data-ttu-id="c81cc-110"><span id="IBackgroundCopyJob__AddFileSet"></span><span id="ibackgroundcopyjob__addfileset"></span><span id="IBACKGROUNDCOPYJOB__ADDFILESET"></span>[**Ibackgroundcopyjob:: ADDFILESET**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset)</span><span class="sxs-lookup"><span data-stu-id="c81cc-110"><span id="IBackgroundCopyJob__AddFileSet"></span><span id="ibackgroundcopyjob__addfileset"></span><span id="IBACKGROUNDCOPYJOB__ADDFILESET"></span>[**IBackgroundCopyJob::AddFileSet**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset)</span></span>
</dt> <dd>

<span data-ttu-id="c81cc-111">Fügt einem Auftrag eine oder mehrere Dateien hinzu.</span><span class="sxs-lookup"><span data-stu-id="c81cc-111">Adds one or more files to a job.</span></span> <span data-ttu-id="c81cc-112">Wenn Sie mehrere Dateien hinzufügen, ist es effizienter, diese Methode aufzurufen, als die **AddFile** -Methode in einer-Schleife aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c81cc-112">If you are adding multiple files, it is more efficient to call this method than to call the **AddFile** method in a loop.</span></span>

</dd> <dt>

<span data-ttu-id="c81cc-113"><span id="IBackgroundCopyJob3__AddFileWithRanges"></span><span id="ibackgroundcopyjob3__addfilewithranges"></span><span id="IBACKGROUNDCOPYJOB3__ADDFILEWITHRANGES"></span>[**IBackgroundCopyJob3:: ADDFILEWITHRANGES**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-addfilewithranges)</span><span class="sxs-lookup"><span data-stu-id="c81cc-113"><span id="IBackgroundCopyJob3__AddFileWithRanges"></span><span id="ibackgroundcopyjob3__addfilewithranges"></span><span id="IBACKGROUNDCOPYJOB3__ADDFILEWITHRANGES"></span>[**IBackgroundCopyJob3::AddFileWithRanges**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-addfilewithranges)</span></span>
</dt> <dd>

<span data-ttu-id="c81cc-114">Fügt einem Auftrag eine einzelne Datei hinzu.</span><span class="sxs-lookup"><span data-stu-id="c81cc-114">Adds a single file to a job.</span></span> <span data-ttu-id="c81cc-115">Verwenden Sie diese Methode, wenn Sie Datenbereiche aus einer Datei herunterladen möchten.</span><span class="sxs-lookup"><span data-stu-id="c81cc-115">Use this method if you want to download ranges of data from a file.</span></span> <span data-ttu-id="c81cc-116">Diese Methode kann nur für Download Aufträge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c81cc-116">You can use this method only for download jobs.</span></span>

</dd> </dl>

<span data-ttu-id="c81cc-117">Wenn Sie einem Auftrag eine Datei hinzufügen, geben Sie den Remote Namen und den lokalen Namen der Datei an.</span><span class="sxs-lookup"><span data-stu-id="c81cc-117">When you add a file to a job, you specify the remote name and the local name of the file.</span></span> <span data-ttu-id="c81cc-118">Ausführliche Informationen zum Format der lokalen und Remote Dateinamen finden Sie in der [**BG- \_ Datei \_ Info**](/windows/desktop/api/Bits/ns-bits-bg_file_info) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="c81cc-118">For details on the format of the local and remote file names, see the [**BG\_FILE\_INFO**](/windows/desktop/api/Bits/ns-bits-bg_file_info) structure.</span></span>

<span data-ttu-id="c81cc-119">Ein Uploadauftrag kann nur eine Datei enthalten.</span><span class="sxs-lookup"><span data-stu-id="c81cc-119">An upload job can contain only one file.</span></span> <span data-ttu-id="c81cc-120">Die [**ibackgroundcopyjob:: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile) -Methode und die [**ibackgroundcopyjob:: ADDFILESET**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset) -Methode geben BG \_ E \_ zu \_ viele \_ Dateien zurück, wenn Sie versuchen, einem Uploadauftrag mehr als eine Datei hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="c81cc-120">The [**IBackgroundCopyJob::AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile) and [**IBackgroundCopyJob::AddFileSet**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset) methods return BG\_E\_TOO\_MANY\_FILES if you try to add more than one file to an upload job.</span></span> <span data-ttu-id="c81cc-121">Wenn Sie mehr als eine Datei hochladen müssen, empfiehlt es sich, eine CAB-oder ZIP-Datei zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c81cc-121">If you need to upload more than one file, consider using a CAB or ZIP file.</span></span>

<span data-ttu-id="c81cc-122">Für Download Aufträge beschränkt Bits die Anzahl der Dateien, die ein Benutzer einem Auftrag hinzufügen kann, auf 200-Dateien und die Anzahl der Bereiche für eine Datei in 500-Bereiche.</span><span class="sxs-lookup"><span data-stu-id="c81cc-122">For download jobs, BITS limits the number of files that a user can add to a job to 200 files and the number of ranges for a file to 500 ranges.</span></span> <span data-ttu-id="c81cc-123">Diese Grenzwerte gelten nicht für Administratoren oder Dienste.</span><span class="sxs-lookup"><span data-stu-id="c81cc-123">These limits do not apply to administrators or services.</span></span> <span data-ttu-id="c81cc-124">Informationen zum Ändern dieser Standard Limits finden Sie unter [Gruppenrichtlinien](group-policies.md).</span><span class="sxs-lookup"><span data-stu-id="c81cc-124">To change these default limits, see [Group Policies](group-policies.md).</span></span>

<span data-ttu-id="c81cc-125">Der Besitzer des Auftrags oder ein Benutzer mit Administratorrechten kann dem Auftrag jederzeit vor dem Aufrufen der [**ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) -Methode oder der [**ibackgroundcopyjob:: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) -Methode Dateien hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c81cc-125">The owner of the job or a user with administrator privileges can add files to the job anytime prior to calling the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method or the [**IBackgroundCopyJob::Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) method.</span></span>

<span data-ttu-id="c81cc-126">Wenn Sie den Remote Namen der Datei ändern müssen, nachdem Sie die Datei dem Auftrag hinzugefügt haben, können Sie die [**IBackgroundCopyJob3:: REPLACEREMOTEPREFIX**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) -Methode oder die [**IBackgroundCopyFile2:: Setup Report Name**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="c81cc-126">If you need to change the remote name of the file after you add the file to the job, you can call the [**IBackgroundCopyJob3::ReplaceRemotePrefix**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) method or the [**IBackgroundCopyFile2::SetRemoteName**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) method.</span></span> <span data-ttu-id="c81cc-127">Verwenden Sie die **REPLACEREMOTEPREFIX** -Methode, um den Serverteil des Remote namens zu ändern, wenn der Server nicht verfügbar ist, oder damit Roamingbenutzer eine Verbindung mit dem nächstgelegenen Server herstellen können.</span><span class="sxs-lookup"><span data-stu-id="c81cc-127">Use the **ReplaceRemotePrefix** method to change the server portion of the remote name when the server is unavailable or to let roaming users connect to the closest server.</span></span> <span data-ttu-id="c81cc-128">Verwenden Sie die Methode "Setup **Name** ", um das Protokoll zu ändern, das zum Übertragen der Datei verwendet wird, oder um den Dateinamen oder den Pfad zu ändern.</span><span class="sxs-lookup"><span data-stu-id="c81cc-128">Use the **SetRemoteName** method to change the protocol used to transfer the file or to change the file name or path.</span></span>

<span data-ttu-id="c81cc-129">Bits erstellt eine temporäre Datei im Zielverzeichnis und verwendet die temporäre Datei für die Dateiübertragung.</span><span class="sxs-lookup"><span data-stu-id="c81cc-129">BITS creates a temporary file in the destination directory and uses the temporary file for the file transfer.</span></span> <span data-ttu-id="c81cc-130">Um den temporären Dateinamen abzurufen, nennen Sie die [**IBackgroundCopyFile3:: gettemporaryname**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) -Methode.</span><span class="sxs-lookup"><span data-stu-id="c81cc-130">To get the temporary file name, call the [**IBackgroundCopyFile3::GetTemporaryName**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) method.</span></span> <span data-ttu-id="c81cc-131">Bits ändert den temporären Dateinamen in den Ziel Dateinamen, wenn Sie die [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) -Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c81cc-131">BITS changes the temporary file name to the destination file name when you call the [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method.</span></span> <span data-ttu-id="c81cc-132">Bits gibt keine Sicherheits Beschreibung an, wenn die temporäre Datei [**erstellt**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) wird (die Datei erbt die ACL-Informationen aus dem Zielverzeichnis).</span><span class="sxs-lookup"><span data-stu-id="c81cc-132">BITS does not specify a security descriptor when it [**creates**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) the temporary file (the file inherits the ACL information from the destination directory).</span></span> <span data-ttu-id="c81cc-133">Wenn die übertragenen Daten sensibel sind, sollte die Anwendung eine geeignete ACL für das Zielverzeichnis angeben, um nicht autorisierten Zugriff zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="c81cc-133">If the transferred data is sensitive, the application should specify an appropriate ACL on the destination directory to prevent unauthorized access.</span></span>

<span data-ttu-id="c81cc-134">Um den Besitzer und die ACL-Informationen mit der übertragenen Datei beizubehalten, müssen Sie die [**IBackgroundCopyJob3:: setfileaclflags**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-setfileaclflags) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c81cc-134">To maintain the owner and ACL information with the transferred file, call the [**IBackgroundCopyJob3::SetFileACLFlags**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-setfileaclflags) method.</span></span>

<span data-ttu-id="c81cc-135">Der Besitzer des Auftrags (der Benutzer, der den Auftrag erstellt hat, oder der Administrator, der den Besitz des Auftrags über [genommen](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership) hat) muss über Berechtigungen für die Datei auf dem Server und den Client verfügen.</span><span class="sxs-lookup"><span data-stu-id="c81cc-135">The owner of the job (the user who created the job or the administrator who [took ownership](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership) of the job) must have permissions to the file on the server as well as the client.</span></span> <span data-ttu-id="c81cc-136">Um z. b. eine Datei herunterzuladen, muss der Benutzer über Leseberechtigungen für den Server und über Schreibberechtigungen für das lokale Verzeichnis auf dem Client verfügen.</span><span class="sxs-lookup"><span data-stu-id="c81cc-136">For example, to download a file the user must have read permissions on the server and write permissions to the local directory on the client.</span></span>

<span data-ttu-id="c81cc-137">Im folgenden Beispiel wird gezeigt, wie eine einzelne Datei zum Auftrag hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="c81cc-137">The following example shows how to add a single file to the job.</span></span> <span data-ttu-id="c81cc-138">Im Beispiel wird davon ausgegangen, dass der [**ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) -Schnittstellen Zeiger, pjob, gültig ist.</span><span class="sxs-lookup"><span data-stu-id="c81cc-138">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer, pJob, is valid.</span></span>


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;

//Replace parameters with variables that contain valid paths.
hr = pJob->AddFile(L"https://ServerName/Path/File.Ext", L"d:\\Path\\File.Ext");
if (SUCCEEDED(hr))
{
  //Do something.
}
```



<span data-ttu-id="c81cc-139">Im folgenden Beispiel wird gezeigt, wie dem Auftrag mehrere Dateien hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="c81cc-139">The following example shows how to add multiple files to the job.</span></span> <span data-ttu-id="c81cc-140">Im Beispiel wird davon ausgegangen, dass der [**ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) -Schnittstellen Zeiger, pjob, gültig ist und der lokale und der Remote Name aus einer Liste in der Benutzeroberfläche stammen.</span><span class="sxs-lookup"><span data-stu-id="c81cc-140">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer, pJob, is valid and the local and remote names come from a list in the user interface.</span></span>


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
BG_FILE_INFO* paFiles = NULL;
ULONG idx = 0;
ULONG nCount = 0;            //Set to the number of files to add to the job.
LPWSTR pszLocalName = NULL;  //Comes from the list in the user interface.
LPWSTR pszRemoteName = NULL; //Comes from the list in the user interface.

//Set nCount to the number of files to transfer.

//Allocate a block of memory to contain the array of BG_FILE_INFO structures.
//The BG_FILE_INFO structure contains the local and remote names of the 
//file being transferred.
paFiles = (BG_FILE_INFO*) malloc(sizeof(BG_FILE_INFO) * nCount);
if (NULL == paFiles)
{
  //Handle error
}
else
{
  //Add local and remote file name pairs to the memory block. 
  for (idx=0; idx<nCount; idx++)
  {
    //Set pszLocalName to point to an LPWSTR that contains the local name or
    //allocate memory for pszLocalName and copy the local name to pszLocalName.
    (paFiles+idx)->LocalName = pszLocalName;

    //Set pszRemoteName to point to an LPWSTR that contains the remote name or
    //allocate memory for pszRemoteName and copy the remote name to pszRemoteName.
    (paFiles+idx)->RemoteName = pszRemoteName;
  }

  //Add the files to the job.
  hr = pJob->AddFileSet(nCount, paFiles);
  if (SUCCEEDED(hr))
  {
     //Do Something.
  }

  //Free the memory block for the array of BG_FILE_INFO structures. If you allocated
  //memory for the local and remote file names, loop through the array and free the
  //memory for the file names before you free paFiles.
  free(paFiles);
}
```



 

 