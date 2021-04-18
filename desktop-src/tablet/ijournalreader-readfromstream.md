---
description: Nimmt einen Stream in eine Journal Notiz Datei und gibt einen XML-Stream zurück, der den Inhalt des Dokuments darstellt.
ms.assetid: 5a169dfe-b102-4aef-9efe-5db2cd2fb96f
title: 'Ijournalreader:: lesefromstream-Methode (Journal. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IJournalReader.ReadFromStream
api_type:
- COM
api_location:
- Journal.dll
ms.openlocfilehash: 258ac30b8857fa4ef24bd86a08c7e402229f4bff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344260"
---
# <a name="ijournalreaderreadfromstream-method"></a>Ijournalreader:: lesefromstream-Methode

Nimmt einen Stream in eine Journal Notiz Datei und gibt einen XML-Stream zurück, der den Inhalt des Dokuments darstellt.

> [!Note]  
> Die Journal Leser Komponente kann keine Windows-Journal Dateien lesen, die von Computern mit Windows 7 oder höher erstellt wurden. Die ijournalreader-Schnittstelle sollte als veraltet oder veraltet betrachtet werden und sollte nicht verwendet werden.

 

## <a name="syntax"></a>Syntax


```C++
HRESULT ReadFromStream(
  [in]          IStream *pJournalFileStream,
  [out, retval] IStream **ppXmlStream
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pjournalfilestream* \[ in\]
</dt> <dd>

Ein [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Objekt, das die zu lesende Journal Datei darstellt.

</dd> <dt>

*ppxmlstream* \[ Out, retval\]
</dt> <dd>

Ein Zeiger auf die Adresse eines [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Objekts, das den XML-Stream empfängt, der durchlesen der Journal Datei erstellt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Streams werden verwendet, um den direkten Zugriff auf das Dateisystem zu vermeiden und die Entscheidung zu treffen, welche XML-Methode verwendet werden soll.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel eines Handlers für das [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) -Ereignis einer Schaltfläche wird eine Instanz der [**ijournalreader-Schnittstellen**](ijournalreader.md) Schnittstelle erstellt und verwendet, um eine vorhandene Journal Datei zu lesen.


```C++
void CJntlReaderMFCDlg::OnBnClickedButton1()
{
  IStream* pJntStream;
  IStream* pXmlStream;
  IJournalReader* pJntReader;
  HRESULT hr;
  CString szFileName = "";
  static char BASED_CODE szFilter[] = 
    "Journal files (*.jnt)|*.jnt|All files (*.*)|*.*";
  CFileDialog* fileDialog = new CFileDialog(TRUE, "*.jnt", NULL, 
                                 OFN_FILEMUSTEXIST, szFilter, this);

  // Get the filename from the user by using a File Open dialog
  if (IDOK == fileDialog->DoModal())
  {
    szFileName = fileDialog->GetPathName();

    // Read a JNT file into a memory buffer
    HANDLE hFile = CreateFile(szFileName.GetBuffer(), GENERIC_READ, FILE_SHARE_READ, NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
    
    if (INVALID_HANDLE_VALUE != hFile)
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
          if (ReadFile(hFile, pData, dwFileSize, &dwRead, NULL) && dwRead == dwFileSize)
          {
            // Create an IStream that points to the buffer
            hr = CreateStreamOnHGlobal(hGlobal, FALSE, &pJntStream);

            if (SUCCEEDED(hr))
            {
              // Create a JournalReader object
              hr = CoCreateInstance(CLSID_JournalReader, NULL, CLSCTX_ALL, 
                          IID_IJournalReader, (void**)&pJntReader);

              if (SUCCEEDED(hr))
              {
                // Read in the JNT file by using the JournalReader
                hr = pJntReader->ReadFromStream(pJntStream, &pXmlStream);

                // Display results
                if (SUCCEEDED(hr))
                {
                  DisplayXml(pXmlStream);
                }

                // Clean up
                pXmlStream->Release();
                pJntReader = NULL;
                pJntStream->Release();
              }
            }
          }
          GlobalUnlock(hGlobal);
        }
        GlobalFree(hGlobal);
      }
    }
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

[**Ijournalreader-Schnittstelle**](ijournalreader.md)
</dt> <dt>

[Schema Referenz für Journal Reader](journal-reader-schema-reference.md)
</dt> </dl>

 

