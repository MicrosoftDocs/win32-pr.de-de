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
# <a name="ijournalreader-interface"></a><span data-ttu-id="81d12-103">Ijournalreader-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="81d12-103">IJournalReader interface</span></span>

<span data-ttu-id="81d12-104">Bietet Lesezugriff auf eine Windows-Journal Datei und gibt einen Stream zurück, der eine XML-Version des Datei Inhalts enthält.</span><span class="sxs-lookup"><span data-stu-id="81d12-104">Provides read access to a Windows Journal file, returning a stream containing an XML version of the file's contents.</span></span>

> [!Note]  
> <span data-ttu-id="81d12-105">Die Journal Leser Komponente kann keine Windows-Journal Dateien lesen, die von Computern mit Windows 7 oder höher erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="81d12-105">The Journal Reader component cannot read Windows Journal files created by machines running Windows 7 or later.</span></span> <span data-ttu-id="81d12-106">Die ijournalreader-Schnittstelle sollte als veraltet oder veraltet betrachtet werden und sollte nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="81d12-106">The IJournalReader interface should be considered deprecated or obsolete and should not be used.</span></span>

 

## <a name="members"></a><span data-ttu-id="81d12-107">Member</span><span class="sxs-lookup"><span data-stu-id="81d12-107">Members</span></span>

<span data-ttu-id="81d12-108">Die **ijournalreader** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="81d12-108">The **IJournalReader** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="81d12-109">**Ijournalreader** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="81d12-109">**IJournalReader** also has these types of members:</span></span>

-   [<span data-ttu-id="81d12-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="81d12-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="81d12-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="81d12-111">Methods</span></span>

<span data-ttu-id="81d12-112">Die **ijournalreader** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="81d12-112">The **IJournalReader** interface has these methods.</span></span>



| <span data-ttu-id="81d12-113">Methode</span><span class="sxs-lookup"><span data-stu-id="81d12-113">Method</span></span>                                                  | <span data-ttu-id="81d12-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="81d12-114">Description</span></span>                                                                                                           |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81d12-115">**"Read FromStream"**</span><span class="sxs-lookup"><span data-stu-id="81d12-115">**ReadFromStream**</span></span>](ijournalreader-readfromstream.md) | <span data-ttu-id="81d12-116">Nimmt einen Stream in eine Journal Notiz Datei und gibt einen XML-Stream zurück, der den Inhalt des Dokuments darstellt.</span><span class="sxs-lookup"><span data-stu-id="81d12-116">Takes a stream to a Journal Note file and returns an XML stream representing the contents of the document.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="81d12-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="81d12-117">Remarks</span></span>

<span data-ttu-id="81d12-118">Die **JournalReader** -Klasse ermöglicht das Laden eines Journal Dokument Datenstroms und das Empfangen eines XML-Streams, der den Inhalt darstellt.</span><span class="sxs-lookup"><span data-stu-id="81d12-118">The **JournalReader** class enables you to load a Journal document stream and to receive an XML stream representing the contents.</span></span> <span data-ttu-id="81d12-119">Sie können das frei Handzeichen wiederherstellen, anzeigen und bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="81d12-119">You can reconstitute, display, and manipulate the ink.</span></span>

## <a name="examples"></a><span data-ttu-id="81d12-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="81d12-120">Examples</span></span>

<span data-ttu-id="81d12-121">Im folgenden Beispiel eines Handlers für das [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) -Ereignis einer Schaltfläche wird eine Instanz der **JournalReader** -Klasse erstellt und verwendet, um eine vorhandene Journal Datei zu lesen.</span><span class="sxs-lookup"><span data-stu-id="81d12-121">The following example of a handler for a button's [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) event creates an instance of the **JournalReader** class and uses it to read an existing Journal file.</span></span>

> [!Note]  
> <span data-ttu-id="81d12-122">Die von diesem Beispiel aufgerufene **displayxml** -Methode wird nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="81d12-122">The **DisplayXml** method called from this example is not shown.</span></span> <span data-ttu-id="81d12-123">Die spezifische Implementierung einer solchen Methode hängt von den Anforderungen Ihrer Anwendung ab.</span><span class="sxs-lookup"><span data-stu-id="81d12-123">The specific implementation of such a method is dependent on your application's needs.</span></span>

 


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



## <a name="requirements"></a><span data-ttu-id="81d12-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81d12-124">Requirements</span></span>



| <span data-ttu-id="81d12-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="81d12-125">Requirement</span></span> | <span data-ttu-id="81d12-126">Wert</span><span class="sxs-lookup"><span data-stu-id="81d12-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81d12-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="81d12-127">Minimum supported client</span></span><br/> | <span data-ttu-id="81d12-128">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="81d12-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="81d12-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="81d12-129">Minimum supported server</span></span><br/> | <span data-ttu-id="81d12-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="81d12-130">None supported</span></span><br/>                                                                                         |
| <span data-ttu-id="81d12-131">Header</span><span class="sxs-lookup"><span data-stu-id="81d12-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="81d12-132"><dt>Journal. h (erfordert auch Journal \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="81d12-132"><dt>Journal.h (also requires journal\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="81d12-133">DLL</span><span class="sxs-lookup"><span data-stu-id="81d12-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81d12-134"><dt>Journal.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81d12-134"><dt>Journal.dll</dt></span></span> </dl>                            |



## <a name="see-also"></a><span data-ttu-id="81d12-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81d12-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81d12-136">GUIDs der benutzerdefinierten Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="81d12-136">Custom Property GUIDs</span></span>](custom-property-guids.md)
</dt> <dt>

[<span data-ttu-id="81d12-137">**Read FromStream-Methode**</span><span class="sxs-lookup"><span data-stu-id="81d12-137">**ReadFromStream Method**</span></span>](ijournalreader-readfromstream.md)
</dt> </dl>

 

