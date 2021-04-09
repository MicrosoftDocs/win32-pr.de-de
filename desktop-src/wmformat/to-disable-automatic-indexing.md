---
title: So deaktivieren Sie die automatische Indizierung
description: So deaktivieren Sie die automatische Indizierung
ms.assetid: 41fe18de-3a94-4001-83ce-0bb5dd086995
keywords:
- Windows Media-Format-SDK, Deaktivieren der automatischen Indizierung
- Windows Media-Format-SDK, automatische Indizierung
- Advanced Systems Format (ASF), Deaktivieren der automatischen Indizierung
- ASF (Advanced Systems Format), Deaktivieren der automatischen Indizierung
- Advanced Systems Format (ASF), automatische Indizierung
- ASF (Advanced Systems Format), automatische Indizierung
- Indizes, Deaktivieren der automatischen Indizierung
- Indizes, automatische Indizierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0235ddac8093d9b1c6d40fde341ee32d078b84b7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103948441"
---
# <a name="to-disable-automatic-indexing"></a>So deaktivieren Sie die automatische Indizierung

Beim Schreiben einer ASF-Datei soll möglicherweise nicht immer ein Index generiert werden. Sie können die automatische Indizierung mithilfe der Methode [**IWMWriterFileSink3:: abtaugemethode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-setautoindexing) deaktivieren.

Im folgenden Beispielcode wird veranschaulicht, wie die automatische Indizierung durch den Writer deaktiviert wird.


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

[**IWMWriterFileSink3:: getautoindizierung**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-getautoindexing)
</dt> <dt>

[**Wmkreateschreiterfilesink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink)
</dt> <dt>

[**Arbeiten mit Indizes**](working-with-indexes.md)
</dt> </dl>

 

 




