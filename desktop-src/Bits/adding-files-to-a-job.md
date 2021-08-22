---
title: Hinzufügen von Dateien zu einem Auftrag
description: Ein Auftrag enthält eine oder mehrere Dateien, die Sie übertragen möchten.
ms.assetid: fb6e7219-b6ca-4f72-b7a3-60d65e8f3892
keywords:
- BITS des Übertragungsauftrags, Hinzufügen von Dateien
- Dateiübertragungsbits , hinzufügen
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: b6c369c0a9ee207790d0370da6543c642ee294b072e0d91f1837cd734a6a625d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529270"
---
# <a name="adding-files-to-a-job"></a>Hinzufügen von Dateien zu einem Auftrag

Ein Auftrag enthält eine oder mehrere Dateien, die Sie übertragen möchten. Verwenden Sie eine der folgenden Methoden, um einem Auftrag Dateien hinzuzufügen:

<dl> <dt>

<span id="IBackgroundCopyJob__AddFile"></span><span id="ibackgroundcopyjob__addfile"></span><span id="IBACKGROUNDCOPYJOB__ADDFILE"></span>[**IBackgroundCopyJob::AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)
</dt> <dd>

Fügt einem Auftrag eine einzelne Datei hinzu.

</dd> <dt>

<span id="IBackgroundCopyJob__AddFileSet"></span><span id="ibackgroundcopyjob__addfileset"></span><span id="IBACKGROUNDCOPYJOB__ADDFILESET"></span>[**IBackgroundCopyJob::AddFileSet**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset)
</dt> <dd>

Fügt einem Auftrag eine oder mehrere Dateien hinzu. Wenn Sie mehrere Dateien hinzufügen, ist es effizienter, diese Methode als die **AddFile-Methode** in einer -Schleife auf aufruft.

</dd> <dt>

<span id="IBackgroundCopyJob3__AddFileWithRanges"></span><span id="ibackgroundcopyjob3__addfilewithranges"></span><span id="IBACKGROUNDCOPYJOB3__ADDFILEWITHRANGES"></span>[**IBackgroundCopyJob3::AddFileWithRanges**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-addfilewithranges)
</dt> <dd>

Fügt einem Auftrag eine einzelne Datei hinzu. Verwenden Sie diese Methode, wenn Sie Datenbereiche aus einer Datei herunterladen möchten. Sie können diese Methode nur für Downloadaufträge verwenden.

</dd> </dl>

Wenn Sie einem Auftrag eine Datei hinzufügen, geben Sie den Remotenamen und den lokalen Namen der Datei an. Weitere Informationen zum Format der lokalen und Remotedateinamen finden Sie in der [**BG \_ FILE \_ INFO-Struktur.**](/windows/desktop/api/Bits/ns-bits-bg_file_info)

Ein Uploadauftrag kann nur eine Datei enthalten. Die [**Methoden IBackgroundCopyJob::AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile) und [**IBackgroundCopyJob::AddFileSet**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset) geben BG E TOO MANY FILES zurück, wenn Sie versuchen, einem Uploadauftrag mehrere Dateien \_ \_ \_ \_ hinzuzufügen. Wenn Sie mehrere Dateien hochladen müssen, sollten Sie eine CAB- oder ZIP-Datei verwenden.

Bei Downloadaufträgen beschränkt BITS die Anzahl der Dateien, die ein Benutzer einem Auftrag hinzufügen kann, auf 200 Dateien und die Anzahl der Bereiche für eine Datei auf 500 Bereiche. Diese Grenzwerte gelten nicht für Administratoren oder Dienste. Informationen zum Ändern dieser Standardgrenzwerte finden Sie unter [Gruppenrichtlinien.](group-policies.md)

Der Besitzer des Auftrags oder ein Benutzer mit Administratorrechten kann dem Auftrag jederzeit Dateien hinzufügen, bevor er die [**IBackgroundCopyJob::Complete-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) oder die [**IBackgroundCopyJob::Cancel-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) aufruft.

Wenn Sie den Remotenamen der Datei ändern müssen, nachdem Sie die Datei dem Auftrag hinzugefügt haben, können Sie die [**IBackgroundCopyJob3::ReplaceRemotePrefix-Methode**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) oder die [**IBackgroundCopyFile2::SetRemoteName-Methode**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) aufrufen. Verwenden Sie **die ReplaceRemotePrefix-Methode,** um den Serverteil des Remotenamens zu ändern, wenn der Server nicht verfügbar ist, oder um Roamingbenutzern die Verbindung mit dem nächstgelegenen Server zu ermöglichen. Verwenden Sie **die SetRemoteName-Methode,** um das Protokoll zu ändern, das zum Übertragen der Datei oder zum Ändern des Dateinamens oder Pfads verwendet wird.

BITS erstellt eine temporäre Datei im Zielverzeichnis und verwendet die temporäre Datei für die Dateiübertragung. Um den temporären Dateinamen zu erhalten, rufen Sie die [**IBackgroundCopyFile3::GetTemporaryName-Methode**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) auf. BITS ändert den temporären Dateinamen in den Zieldateinamen, wenn Sie die [**Complete-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) aufrufen. BITS gibt beim Erstellen der temporären Datei keinen Sicherheitsdeskriptor an (die Datei erbt die ACL-Informationen aus dem Zielverzeichnis). [](/windows/desktop/api/fileapi/nf-fileapi-createfilea) Wenn die übertragenen Daten vertraulich sind, sollte die Anwendung eine geeignete Zugriffssteuerungsliste für das Zielverzeichnis angeben, um nicht autorisierten Zugriff zu verhindern.

Um die Besitzer- und ACL-Informationen mit der übertragenen Datei zu verwalten, rufen Sie die [**IBackgroundCopyJob3::SetFileACLFlags-Methode**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-setfileaclflags) auf.

Der Besitzer des Auftrags (der Benutzer, der [](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership) den Auftrag erstellt hat, oder der Administrator, der den Besitz des Auftrags übertragen hat) muss über Berechtigungen für die Datei auf dem Server und dem Client verfügen. Um beispielsweise eine Datei herunterzuladen, muss der Benutzer über Leseberechtigungen auf dem Server und Schreibberechtigungen für das lokale Verzeichnis auf dem Client verfügen.

Das folgende Beispiel zeigt, wie dem Auftrag eine einzelne Datei hinzugefügt wird. Im Beispiel wird davon ausgegangen, dass [**der IBackgroundCopyJob-Schnittstellenzeiger**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) pJob gültig ist.


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



Das folgende Beispiel zeigt, wie dem Auftrag mehrere Dateien hinzugefügt werden. Im Beispiel wird davon ausgegangen, dass der [**IBackgroundCopyJob-Schnittstellenzeiger**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) pJob gültig ist und die lokalen und Remotenamen aus einer Liste auf der Benutzeroberfläche stammen.


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



 

 