---
title: So deaktivieren Sie die automatische Indizierung
description: So deaktivieren Sie die automatische Indizierung
ms.assetid: 41fe18de-3a94-4001-83ce-0bb5dd086995
keywords:
- Windows Medienformat-SDK,Deaktivieren der automatischen Indizierung
- Windows Medienformat-SDK, automatische Indizierung
- Advanced Systems Format (ASF), Deaktivieren der automatischen Indizierung
- ASF (Advanced Systems Format), Deaktivieren der automatischen Indizierung
- Advanced Systems Format (ASF), automatische Indizierung
- ASF (Advanced Systems Format), automatische Indizierung
- Indizes,Deaktivieren der automatischen Indizierung
- Indizes,automatische Indizierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f3b63d58b8f9a0fbbdff88369832b67abca7d9f11a39c56613c6e5d867d6a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699910"
---
# <a name="to-disable-automatic-indexing"></a>So deaktivieren Sie die automatische Indizierung

Möglicherweise möchten Sie nicht immer, dass beim Schreiben einer ASF-Datei standardmäßig ein Index generiert wird. Sie können die automatische Indizierung mithilfe der [**IWMWriterFileSink3::SetAutoIndexing-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-setautoindexing) deaktivieren.

Der folgende Beispielcode veranschaulicht, wie die automatische Indizierung durch den Writer deaktiviert wird.


```C++
IWMWriterFileSink*  pBaseFileSink = NULL;
IWMWriterFileSink3* pMySink       = NULL;

BOOL    fAutoIndex;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a writer file sink.
hr = WMCreateWriterFileSink(&pBaseFileSink);

// Retrieve an IWMWriterFileSink3 interface pointer for the new sink.
hr = pBaseFileSink->QueryInterface(IID_IWMWriterFileSink3,
                                    (void**)&pMySink);

// Release the base file sink.
pBaseFileSink->Release();
pBaseFileSink = NULL;

// Check the state of automatic indexing.
hr = pMySink->GetAutoIndexing(&fAutoIndex);

// If auto indexing is enabled, turn it off.
if(fAutoIndex)
   pMySink->SetAutoIndexing(FALSE);

// You can now write to this sink and the file will not have an index.

// Release the remaining interface.
pMySink->Release();
pMySink = NULL;

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMWriterFileSink3::GetAutoIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-getautoindexing)
</dt> <dt>

[**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink)
</dt> <dt>

[**Arbeiten mit Indizes**](working-with-indexes.md)
</dt> </dl>

 

 




