---
description: Da die Image-Datenübertragung Datenstrom basiert in der Windows-Abbild Erfassung (WIA) 2,0 ist, müssen Sie keinen Zieltyp angeben (z. b.
ms.assetid: ebb9fce5-9450-4ffe-b480-b21670b60f90
title: Übertragen von Bilddaten in WIA 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85ded5c6cd8fb94b1beccd86c3cd8aef3018aed0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343658"
---
# <a name="transferring-image-data-in-wia-20"></a>Übertragen von Bilddaten in WIA 2,0

> [!Note]  
> In diesem Tutorial wird veranschaulicht, wie Sie Abbild Daten in Anwendungen übertragen, die unter Windows Vista oder höher ausgeführt werden. Informationen zum Übertragen von Bilddaten in Anwendungen, die unter Windows XP oder früher ausgeführt werden, finden Sie unter über [tragen von Bilddaten in WIA 1,0](-wia-transferring-image-data.md) .

 

Da die Image-Datenübertragung Datenstrom basiert in Windows-Abbild Abruf (WIA) 2,0 ist, müssen Sie keinen Zieltyp angeben (z. b. Arbeitsspeicher oder Datei). Die Anwendung gibt lediglich WIA 2,0 den zu verwendenden Stream aus, und der Treiber liest oder schreibt in den Stream. Der Stream kann ein Dateistream, ein Arbeitsspeicherstream oder ein beliebiger anderer Streamtyp sein und ist für den Treiber transparent. Die Verwendung von Streams bietet auch eine einfache Integration in den Bild Verarbeitungs Filter.

Verwenden Sie die Methoden der [**iwiatransfer**](-wia-iwiatransfer.md) -Schnittstelle zum Übertragen von Daten von einem WIA 2,0-Gerät an eine Anwendung. Diese Schnittstelle ist über die [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstelle verfügbar. Die **iwiatransfer** -Schnittstelle verfügt über Methoden zum Anfordern oder Herunterladen von Daten auf ein und von einem Gerät. Diese Methoden verwenden einen Rückruf, der von der Anwendung bereitgestellt wird, und verwenden einen [IStream](/windows/win32/api/objidl/nn-objidl-istream) , der von der Anwendung für das tatsächliche Ziel der Datenübertragung bereitgestellt wird.

Anwendungen müssen ein Bildelement Abfragen, um einen Zeiger auf seine [**iwiatransfer**](-wia-iwiatransfer.md) -Schnittstelle zu erhalten, wie im folgenden Codebeispiel gezeigt:


```
    // Get the IWiaTransfer interface
    //
    IWiaTransfer *pWiaTransfer = NULL;
    hr = pIWiaItem2->QueryInterface(IID_IWiaTransfer,(void**)&pWiaTransfer);
```



Im vorherigen Code wird angenommen, dass **pWiaItem2** ein gültiger Zeiger auf die [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstelle ist. Der [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Aufrufe füllt **pwiatransfer** mit einem Zeiger auf die [**iwiatransfer**](-wia-iwiatransfer.md) -Schnittstelle des Elements, auf das von **pWiaItem2** verwiesen wird.

Die Anwendung instanziiert dann das Rückruf Objekt, wie hier gezeigt.


```
    //   Instantiate the object which receives the callbacks
    //
    CWiaTransferCallback *pWiaClassCallback = new CWiaTransferCallback;
```



Die Anwendung legt die Eigenschaften dann mithilfe der [**iwiapropertystorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) -Schnittstelle von [**IWiaItem2**](-wia-iwiaitem2.md) Item fest und führt die Übertragung aus.

Downloadvorgang läuft:


```
    // Download   
    hr = pWiaTransfer->Download(0,pWiaClassCallback);
```



Hochladen


```
    //Create child item which eventually will be the uploaded image 
    IWiaItem2* pWiaItemChild = NULL;
    HRESULT hr = pIWiaItem2->CreateChildItem(WiaItemTypeImage|WiaItemTypeFile,0,bzUploadFileName,&pWiaItemChild);
    
    if(SUCCEEDED(hr))
    {
                
        //Set the format for the child item as BMP 
        IWiaPropertyStorage* pWiaChildPropertyStorage = NULL;
        hr = pWiaItemChild->QueryInterface( IID_IWiaPropertyStorage, (void**)&pWiaChildPropertyStorage );
        if(SUCCEEDED(hr))
        {
            WritePropertyGuid(pWiaChildPropertyStorage,WIA_IPA_FORMAT,WiaImgFmt_BMP );

            //release pWiaChildPropertyStorage
            pWiaChildPropertyStorage->Release();
            pWiaChildPropertyStorage = NULL;
        }
        

        //Get the IWiaTransfer interface of the child
        IWiaTransfer* pWiaTransferChild = NULL;
        hr = pWiaItemChild->QueryInterface( IID_IWiaTransfer, (void**)&pWiaTransferChild );
        if(SUCCEEDED(hr)){
            IStream* pUploadStream = NULL;
                                        
            //Create stream on test.BMP file
            hr = SHCreateStreamOnFile(L"test.BMP",STGM_READ, &pUploadStream);
            if(SUCCEEDED(hr)){
                pWiaTransferChild->Upload(0,pUploadStream,pWiaClassCallback);
                
            }
         }
   
      }
```



Hier ist das Beispiel für die komplette Datenübertragung:


```
HRESULT TransferWiaItem( IWiaItem2 *pIWiaItem2)
{
    // Validate arguments
    if (NULL == pIWiaItem2)
    {
        _tprintf(TEXT("\nInvalid parameters passed"));
        return E_INVALIDARG;
    }
    
    // Get the IWiaTransfer interface
    IWiaTransfer *pWiaTransfer = NULL;
    HRESULT hr = pIWiaItem2->QueryInterface( IID_IWiaTransfer, (void**)&pWiaTransfer );
    if (SUCCEEDED(hr))
    {
        // Create our callback class
        CWiaTransferCallback *pWiaClassCallback = new CWiaTransferCallback;
        if (pWiaClassCallback)
        {
            
              LONG lItemType = 0;
              hr = pIWiaItem2->GetItemType( &lItemType );

              //download all items which have WiaItemTypeTransfer flag set
              if(lItemType & WiaItemTypeTransfer)
              {

                  // If it is a folder, do folder download . Hence with one API call, all the leaf nodes of this folder 
                  // will be transferred
                  if ((lItemType & WiaItemTypeFolder))
                  {
                        _tprintf ( L"\nI am a folder item");
                        hr = pWiaTransfer->Download(WIA_TRANSFER_ACQUIRE_CHILDREN, pWiaClassCallback);
                        if(S_OK == hr)
                        {
                            _tprintf(TEXT("\npWiaTransfer->Download() on folder item SUCCEEDED"));
                        }
                        else if(S_FALSE == hr)
                        {
                            ReportError(TEXT("\npWiaTransfer->Download() on folder item returned S_FALSE. Folder may not be having child items"),hr);
                        }
                        else if(FAILED(hr))
                        {
                            ReportError(TEXT("\npWiaTransfer->Download() on folder item failed"),hr);
                        }
                   }

                  
                  // If this is an file type, do file download
                  else if (lItemType & WiaItemTypeFile )
                  {
                      hr = pWiaTransfer->Download(0,pWiaClassCallback);
                      if(S_OK == hr)
                      {
                          _tprintf(TEXT("\npWiaTransfer->Download() on file item SUCCEEDED"));
                      }
                      else if(S_FALSE == hr)
                      {
                          ReportError(TEXT("\npWiaTransfer->Download() on file item returned S_FALSE. File may be empty"),hr);
                      }
                      else if(FAILED(hr))
                      {
                         ReportError(TEXT("\npWiaTransfer->Download() on file item failed"),hr);
                      }
                  }                     
                }
                
                // Release our callback.  It should now delete itself.
                pWiaClassCallback->Release();
                pWiaClassCallback = NULL;
        }
        else
        {
            ReportError( TEXT("\nUnable to create CWiaTransferCallback class instance") );
        }
            
        // Release the IWiaTransfer
        pWiaTransfer->Release();
        pWiaTransfer = NULL;
    }
    else
    {
        ReportError( TEXT("\npIWiaItem2->QueryInterface failed on IID_IWiaTransfer"), hr );
    }
    return hr;
}

// Callback Class should be something like this:

class CWiaTransferCallback : public IWiaTransferCallback
{
public: // Constructors, destructor
    CWiaTransferCallback () : m_cRef(1) {};
    ~ CWiaTransferCallback () {};

public: // IWiaTransferCallback
    HRESULT __stdcall TransferCallback(
        LONG                lFlags,
        WiaTransferParams   *pWiaTransferParams)
    {
        HRESULT hr = S_OK;

        switch (pWiaTransferParams->lMessage)
        {
            case WIA_TRANSFER_MSG_STATUS:
                ...
                break;
            case WIA_TRANSFER_MSG_END_OF_STREAM:
                ...
                break;
            case WIA_TRANSFER_MSG_END_OF_TRANSFER:
                ...
                break;
            default:
                break;
        }

        return hr;
    }

    HRESULT __stdcall GetNextStream(
        LONG    lFlags,
        BSTR    bstrItemName,
        BSTR    bstrFullItemName,
        IStream **ppDestination)
    {

        HRESULT hr = S_OK;

        //  Return a new stream for this item's data.
        //
        hr = CreateDestinationStream(bstrItemName, ppDestination);
        return hr;
    }

public: // IUnknown
        .
        .
        . // Etc.

private:
    /// For ref counting implementation
    LONG                m_cRef;
};

```



 

 
