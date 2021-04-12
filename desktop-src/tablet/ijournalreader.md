---
description: Bietet Lesezugriff auf eine Windows-Journal Datei und gibt einen Stream zurück, der eine XML-Version des Datei Inhalts enthält.
ms.assetid: e4e19f69-6377-4f06-856d-7f9b453e7656
title: Ijournalreader-Schnittstelle (Journal. h)
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
ms.openlocfilehash: 7576996d341f13518879310f08c0a48996e1293f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349909"
---
# <a name="ijournalreader-interface"></a>Ijournalreader-Schnittstelle

Bietet Lesezugriff auf eine Windows-Journal Datei und gibt einen Stream zurück, der eine XML-Version des Datei Inhalts enthält.

> [!Note]  
> Die Journal Leser Komponente kann keine Windows-Journal Dateien lesen, die von Computern mit Windows 7 oder höher erstellt wurden. Die ijournalreader-Schnittstelle sollte als veraltet oder veraltet betrachtet werden und sollte nicht verwendet werden.

 

## <a name="members"></a>Member

Die **ijournalreader** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Ijournalreader** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ijournalreader** -Schnittstelle verfügt über diese Methoden.



| Methode                                                  | BESCHREIBUNG                                                                                                           |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**"Read FromStream"**](ijournalreader-readfromstream.md) | Nimmt einen Stream in eine Journal Notiz Datei und gibt einen XML-Stream zurück, der den Inhalt des Dokuments darstellt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die **JournalReader** -Klasse ermöglicht das Laden eines Journal Dokument Datenstroms und das Empfangen eines XML-Streams, der den Inhalt darstellt. Sie können das frei Handzeichen wiederherstellen, anzeigen und bearbeiten.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel eines Handlers für das [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) -Ereignis einer Schaltfläche wird eine Instanz der **JournalReader** -Klasse erstellt und verwendet, um eine vorhandene Journal Datei zu lesen.

> [!Note]  
> Die von diesem Beispiel aufgerufene **displayxml** -Methode wird nicht angezeigt. Die spezifische Implementierung einer solchen Methode hängt von den Anforderungen Ihrer Anwendung ab.

 


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                     |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                         |
| Header<br/>                   | <dl> <dt>Journal. h (erfordert auch Journal \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Journal.dll</dt> </dl>                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[GUIDs der benutzerdefinierten Eigenschaft](custom-property-guids.md)
</dt> <dt>

[**Read FromStream-Methode**](ijournalreader-readfromstream.md)
</dt> </dl>

 

