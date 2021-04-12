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
# <a name="adding-files-to-a-job"></a>Hinzufügen von Dateien zu einem Auftrag

Ein Auftrag enthält eine oder mehrere Dateien, die Sie übertragen möchten. Verwenden Sie eine der folgenden Methoden, um einem Auftrag Dateien hinzuzufügen:

<dl> <dt>

<span id="IBackgroundCopyJob__AddFile"></span><span id="ibackgroundcopyjob__addfile"></span><span id="IBACKGROUNDCOPYJOB__ADDFILE"></span>[**Ibackgroundcopyjob:: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)
</dt> <dd>

Fügt einem Auftrag eine einzelne Datei hinzu.

</dd> <dt>

<span id="IBackgroundCopyJob__AddFileSet"></span><span id="ibackgroundcopyjob__addfileset"></span><span id="IBACKGROUNDCOPYJOB__ADDFILESET"></span>[**Ibackgroundcopyjob:: ADDFILESET**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset)
</dt> <dd>

Fügt einem Auftrag eine oder mehrere Dateien hinzu. Wenn Sie mehrere Dateien hinzufügen, ist es effizienter, diese Methode aufzurufen, als die **AddFile** -Methode in einer-Schleife aufzurufen.

</dd> <dt>

<span id="IBackgroundCopyJob3__AddFileWithRanges"></span><span id="ibackgroundcopyjob3__addfilewithranges"></span><span id="IBACKGROUNDCOPYJOB3__ADDFILEWITHRANGES"></span>[**IBackgroundCopyJob3:: ADDFILEWITHRANGES**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-addfilewithranges)
</dt> <dd>

Fügt einem Auftrag eine einzelne Datei hinzu. Verwenden Sie diese Methode, wenn Sie Datenbereiche aus einer Datei herunterladen möchten. Diese Methode kann nur für Download Aufträge verwendet werden.

</dd> </dl>

Wenn Sie einem Auftrag eine Datei hinzufügen, geben Sie den Remote Namen und den lokalen Namen der Datei an. Ausführliche Informationen zum Format der lokalen und Remote Dateinamen finden Sie in der [**BG- \_ Datei \_ Info**](/windows/desktop/api/Bits/ns-bits-bg_file_info) -Struktur.

Ein Uploadauftrag kann nur eine Datei enthalten. Die [**ibackgroundcopyjob:: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile) -Methode und die [**ibackgroundcopyjob:: ADDFILESET**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset) -Methode geben BG \_ E \_ zu \_ viele \_ Dateien zurück, wenn Sie versuchen, einem Uploadauftrag mehr als eine Datei hinzuzufügen. Wenn Sie mehr als eine Datei hochladen müssen, empfiehlt es sich, eine CAB-oder ZIP-Datei zu verwenden.

Für Download Aufträge beschränkt Bits die Anzahl der Dateien, die ein Benutzer einem Auftrag hinzufügen kann, auf 200-Dateien und die Anzahl der Bereiche für eine Datei in 500-Bereiche. Diese Grenzwerte gelten nicht für Administratoren oder Dienste. Informationen zum Ändern dieser Standard Limits finden Sie unter [Gruppenrichtlinien](group-policies.md).

Der Besitzer des Auftrags oder ein Benutzer mit Administratorrechten kann dem Auftrag jederzeit vor dem Aufrufen der [**ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) -Methode oder der [**ibackgroundcopyjob:: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) -Methode Dateien hinzufügen.

Wenn Sie den Remote Namen der Datei ändern müssen, nachdem Sie die Datei dem Auftrag hinzugefügt haben, können Sie die [**IBackgroundCopyJob3:: REPLACEREMOTEPREFIX**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) -Methode oder die [**IBackgroundCopyFile2:: Setup Report Name**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) -Methode abrufen. Verwenden Sie die **REPLACEREMOTEPREFIX** -Methode, um den Serverteil des Remote namens zu ändern, wenn der Server nicht verfügbar ist, oder damit Roamingbenutzer eine Verbindung mit dem nächstgelegenen Server herstellen können. Verwenden Sie die Methode "Setup **Name** ", um das Protokoll zu ändern, das zum Übertragen der Datei verwendet wird, oder um den Dateinamen oder den Pfad zu ändern.

Bits erstellt eine temporäre Datei im Zielverzeichnis und verwendet die temporäre Datei für die Dateiübertragung. Um den temporären Dateinamen abzurufen, nennen Sie die [**IBackgroundCopyFile3:: gettemporaryname**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) -Methode. Bits ändert den temporären Dateinamen in den Ziel Dateinamen, wenn Sie die [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) -Methode aufzurufen. Bits gibt keine Sicherheits Beschreibung an, wenn die temporäre Datei [**erstellt**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) wird (die Datei erbt die ACL-Informationen aus dem Zielverzeichnis). Wenn die übertragenen Daten sensibel sind, sollte die Anwendung eine geeignete ACL für das Zielverzeichnis angeben, um nicht autorisierten Zugriff zu verhindern.

Um den Besitzer und die ACL-Informationen mit der übertragenen Datei beizubehalten, müssen Sie die [**IBackgroundCopyJob3:: setfileaclflags**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-setfileaclflags) -Methode aufrufen.

Der Besitzer des Auftrags (der Benutzer, der den Auftrag erstellt hat, oder der Administrator, der den Besitz des Auftrags über [genommen](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership) hat) muss über Berechtigungen für die Datei auf dem Server und den Client verfügen. Um z. b. eine Datei herunterzuladen, muss der Benutzer über Leseberechtigungen für den Server und über Schreibberechtigungen für das lokale Verzeichnis auf dem Client verfügen.

Im folgenden Beispiel wird gezeigt, wie eine einzelne Datei zum Auftrag hinzugefügt wird. Im Beispiel wird davon ausgegangen, dass der [**ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) -Schnittstellen Zeiger, pjob, gültig ist.


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



Im folgenden Beispiel wird gezeigt, wie dem Auftrag mehrere Dateien hinzugefügt werden. Im Beispiel wird davon ausgegangen, dass der [**ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) -Schnittstellen Zeiger, pjob, gültig ist und der lokale und der Remote Name aus einer Liste in der Benutzeroberfläche stammen.


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



 

 