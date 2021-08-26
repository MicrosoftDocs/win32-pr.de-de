---
description: Führt einen Stream in eine Journalnotizdatei aus und gibt einen XML-Stream zurück, der den Inhalt des Dokuments darstellt.
ms.assetid: 5a169dfe-b102-4aef-9efe-5db2cd2fb96f
title: IJournalReader::ReadFromStream-Methode (Journal.h)
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
ms.openlocfilehash: 7dbe9d7929f616914d06cad237f486677cd8e5616cb04bf28a5836751ca0a3c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057850"
---
# <a name="ijournalreaderreadfromstream-method"></a>IJournalReader::ReadFromStream-Methode

Führt einen Stream in eine Journalnotizdatei aus und gibt einen XML-Stream zurück, der den Inhalt des Dokuments darstellt.

> [!Note]  
> Die Journalreaderkomponente kann Windows Journaldateien nicht lesen, die von Computern erstellt wurden, auf denen Windows 7 oder höher ausgeführt wird. Die IJournalReader-Schnittstelle sollte als veraltet oder veraltet betrachtet und nicht verwendet werden.

 

## <a name="syntax"></a>Syntax


```C++
HRESULT ReadFromStream(
  [in]          IStream *pJournalFileStream,
  [out, retval] IStream **ppXmlStream
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pJournalFileStream* \[ In\]
</dt> <dd>

Ein [**IStream-Objekt,**](/windows/desktop/api/objidl/nn-objidl-istream) das die zu lesende Journaldatei darstellt.

</dd> <dt>

*ppXmlStream* \[ out, retval\]
</dt> <dd>

Ein Zeiger auf die Adresse eines [**IStream-Objekts,**](/windows/desktop/api/objidl/nn-objidl-istream) das den xml-Stream empfängt, der durch Lesen der Journaldatei erstellt wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Streams werden verwendet, um direkten Zugriff auf das Dateisystem zu vermeiden und die Wahl zu ermöglichen, in welcher XML-Analysemethode verwendet werden soll.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel eines Handlers für das [**Click-Ereignis**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) einer Schaltfläche wird eine Instanz der [**Schnittstelle IJournalReader Interface**](ijournalreader.md) erstellt und zum Lesen einer vorhandenen Journaldatei verwendet.


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
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                     |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                         |
| Header<br/>                   | <dl> <dt>Journal.h (erfordert auch Journal \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Journal.dll</dt> </dl>                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IJournalReader-Schnittstelle**](ijournalreader.md)
</dt> <dt>

[Schemareferenz für Journalleser](journal-reader-schema-reference.md)
</dt> </dl>

 

