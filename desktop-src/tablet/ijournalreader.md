---
description: Bietet Lesezugriff auf eine Windows Journaldatei und gibt einen Stream zurück, der eine XML-Version des Dateiinhalts enthält.
ms.assetid: e4e19f69-6377-4f06-856d-7f9b453e7656
title: I JournalReader-Schnittstelle (Journal.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IJournalReader
api_type:
- COM
api_location:
- Journal.dll
ms.openlocfilehash: ff0151432e38a3e611e09efe2d5192eefb8c1d3e6cb0e79296e992b728c5a16a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590313"
---
# <a name="ijournalreader-interface"></a>IJournalReader-Schnittstelle

Bietet Lesezugriff auf eine Windows Journaldatei und gibt einen Stream zurück, der eine XML-Version des Dateiinhalts enthält.

> [!Note]  
> Die Journallesekomponente kann keine Journaldateien Windows, die von Computern mit Windows 7 oder höher erstellt wurden. Die IJournalReader-Schnittstelle sollte als veraltet oder veraltet betrachtet und nicht verwendet werden.

 

## <a name="members"></a>Member

Die **IJournalReader-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IJournalReader** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IJournalReader-Schnittstelle** verfügt über diese Methoden.



| Methode                                                  | Beschreibung                                                                                                           |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**ReadFromStream**](ijournalreader-readfromstream.md) | Übergibt einen Stream an eine Journal Note-Datei und gibt einen XML-Stream zurück, der den Inhalt des Dokuments darstellt.<br/> |



 

## <a name="remarks"></a>Hinweise

Mit **der JournalReader-Klasse** können Sie einen Journaldokumentstream laden und einen XML-Stream empfangen, der den Inhalt darstellt. Sie können die Ink-Datei rekonsituieren, anzeigen und bearbeiten.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel eines Handlers für das [**Click-Ereignis**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) einer Schaltfläche wird eine Instanz der **JournalReader-Klasse** erstellt und zum Lesen einer vorhandenen Journaldatei verwendet.

> [!Note]  
> Die in diesem Beispiel aufgerufene **DisplayXml-Methode** wird nicht angezeigt. Die spezifische Implementierung einer solchen Methode hängt von den Anforderungen Ihrer Anwendung ab.

 


```C++
void CJntlReaderMFCDlg::OnBnClickedButton1()
{
  static TCHAR BASED_CODE szFilter[] = 
    _T("Journal files (*.jnt)|*.jnt|All files (*.*)|*.*");
  CFileDialog* fileDialog = new CFileDialog(TRUE, _T("*.jnt"), NULL, 
                                 OFN_FILEMUSTEXIST, szFilter, this);

  // Get the filename from the user via a File Open dialog
  if (fileDialog != NULL &&
      fileDialog->DoModal() == IDOK)
  {
    CString strFileName = fileDialog->GetPathName();

    // Read a JNT file into a memory buffer
    HANDLE hFile = CreateFile(strFileName,
                              GENERIC_READ,
                              FILE_SHARE_READ,
                              NULL,
                              OPEN_EXISTING,
                              FILE_ATTRIBUTE_NORMAL,
                              NULL);
    
    if (hFile != INVALID_HANDLE_VALUE)
    {
      // Allocate memory to hold the file contents
      DWORD dwFileSize = GetFileSize(hFile, NULL);
      HGLOBAL hGlobal = GlobalAlloc(GHND, dwFileSize);

      if (hGlobal != NULL)
      {
        LPBYTE pData = (LPBYTE)GlobalLock(hGlobal);

        if (pData != NULL)
        {
          DWORD dwRead;

          // Read the Journal file into the pData buffer
          if (ReadFile(hFile, pData, dwFileSize, &dwRead, NULL) &&
              (dwRead == dwFileSize))
          {
            HRESULT hr;
            IStream* pJntStream;

            // Create an IStream that points to the buffer
            hr = CreateStreamOnHGlobal(hGlobal, FALSE, &pJntStream);

            if (SUCCEEDED(hr))
            {
              IJournalReader* pJntReader;

              // Create a JournalReader object
              hr = CoCreateInstance(CLSID_JournalReader, NULL, CLSCTX_ALL, 
                          IID_IJournalReader, (void**)&pJntReader);

              if (SUCCEEDED(hr))
              {
                IStream* pXmlStream;

                // Read in the JNT file via the JournalReader
                hr = pJntReader->ReadFromStream(pJntStream, &pXmlStream);

                if (SUCCEEDED(hr))
                {
                  // Display results
                  DisplayXml(pXmlStream);

                  // Clean up
                  pXmlStream->Release();
                }
                pJntReader->Release();
              }
              pJntStream->Release();
            }
          }
          GlobalUnlock(hGlobal);
        }
        GlobalFree(hGlobal);
      }
      CloseHandle(hFile);
    }
    delete fileDialog;
  }
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                     |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                         |
| Header<br/>                   | <dl> <dt>Journal.h (erfordert auch Journal \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Journal.dll</dt> </dl>                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Benutzerdefinierte Eigenschaften-GUIDs](custom-property-guids.md)
</dt> <dt>

[**ReadFromStream-Methode**](ijournalreader-readfromstream.md)
</dt> </dl>

 

