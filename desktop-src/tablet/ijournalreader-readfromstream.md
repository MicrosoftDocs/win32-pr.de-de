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
# <a name="ijournalreaderreadfromstream-method"></a><span data-ttu-id="0fd33-103">Ijournalreader:: lesefromstream-Methode</span><span class="sxs-lookup"><span data-stu-id="0fd33-103">IJournalReader::ReadFromStream method</span></span>

<span data-ttu-id="0fd33-104">Nimmt einen Stream in eine Journal Notiz Datei und gibt einen XML-Stream zurück, der den Inhalt des Dokuments darstellt.</span><span class="sxs-lookup"><span data-stu-id="0fd33-104">Takes a stream to a Journal Note file and returns an XML stream representing the contents of the document.</span></span>

> [!Note]  
> <span data-ttu-id="0fd33-105">Die Journal Leser Komponente kann keine Windows-Journal Dateien lesen, die von Computern mit Windows 7 oder höher erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="0fd33-105">The Journal Reader component cannot read Windows Journal files created by machines running Windows 7 or later.</span></span> <span data-ttu-id="0fd33-106">Die ijournalreader-Schnittstelle sollte als veraltet oder veraltet betrachtet werden und sollte nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0fd33-106">The IJournalReader interface should be considered deprecated or obsolete and should not be used.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="0fd33-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fd33-107">Syntax</span></span>


```C++
HRESULT ReadFromStream(
  [in]          IStream *pJournalFileStream,
  [out, retval] IStream **ppXmlStream
);
```



## <a name="parameters"></a><span data-ttu-id="0fd33-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0fd33-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fd33-109">*pjournalfilestream* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0fd33-109">*pJournalFileStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fd33-110">Ein [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Objekt, das die zu lesende Journal Datei darstellt.</span><span class="sxs-lookup"><span data-stu-id="0fd33-110">An [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) object representing the Journal file to read.</span></span>

</dd> <dt>

<span data-ttu-id="0fd33-111">*ppxmlstream* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="0fd33-111">*ppXmlStream* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="0fd33-112">Ein Zeiger auf die Adresse eines [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Objekts, das den XML-Stream empfängt, der durchlesen der Journal Datei erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="0fd33-112">A pointer to the address of an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) object that will receive the XML stream created by reading the Journal file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fd33-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0fd33-113">Return value</span></span>

<span data-ttu-id="0fd33-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="0fd33-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0fd33-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0fd33-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fd33-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0fd33-116">Remarks</span></span>

<span data-ttu-id="0fd33-117">Streams werden verwendet, um den direkten Zugriff auf das Dateisystem zu vermeiden und die Entscheidung zu treffen, welche XML-Methode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0fd33-117">Streams are used to avoid direct access to the file system and to allow choice in which XML parsing method to use.</span></span>

## <a name="examples"></a><span data-ttu-id="0fd33-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0fd33-118">Examples</span></span>

<span data-ttu-id="0fd33-119">Im folgenden Beispiel eines Handlers für das [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) -Ereignis einer Schaltfläche wird eine Instanz der [**ijournalreader-Schnittstellen**](ijournalreader.md) Schnittstelle erstellt und verwendet, um eine vorhandene Journal Datei zu lesen.</span><span class="sxs-lookup"><span data-stu-id="0fd33-119">The following example of a handler for a button's [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) event creates an instance of the [**IJournalReader Interface**](ijournalreader.md) interface and uses it to read an existing Journal file.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="0fd33-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0fd33-120">Requirements</span></span>



| <span data-ttu-id="0fd33-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0fd33-121">Requirement</span></span> | <span data-ttu-id="0fd33-122">Wert</span><span class="sxs-lookup"><span data-stu-id="0fd33-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fd33-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0fd33-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0fd33-124">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0fd33-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0fd33-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0fd33-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0fd33-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0fd33-126">None supported</span></span><br/>                                                                                         |
| <span data-ttu-id="0fd33-127">Header</span><span class="sxs-lookup"><span data-stu-id="0fd33-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fd33-128"><dt>Journal. h (erfordert auch Journal \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0fd33-128"><dt>Journal.h (also requires journal\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0fd33-129">DLL</span><span class="sxs-lookup"><span data-stu-id="0fd33-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fd33-130"><dt>Journal.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fd33-130"><dt>Journal.dll</dt></span></span> </dl>                            |



## <a name="see-also"></a><span data-ttu-id="0fd33-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0fd33-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fd33-132">**Ijournalreader-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="0fd33-132">**IJournalReader Interface**</span></span>](ijournalreader.md)
</dt> <dt>

[<span data-ttu-id="0fd33-133">Schema Referenz für Journal Reader</span><span class="sxs-lookup"><span data-stu-id="0fd33-133">Journal Reader Schema Reference</span></span>](journal-reader-schema-reference.md)
</dt> </dl>

 

