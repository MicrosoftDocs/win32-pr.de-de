---
title: Verwenden der Streampriorisierung
description: Verwenden der Streampriorisierung
ms.assetid: 5fff212e-b47b-49a6-817f-f0e09c895b3a
keywords:
- Windows Medienformat-SDK, Streampriorisierung
- Profile,Streampriorisierung
- Streams,Priorisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3db00466eb27685a33851f7bffa5133e1d94a203985b1a0a56b110a09ad88ab6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963949"
---
# <a name="using-stream-prioritization"></a>Verwenden der Streampriorisierung

Mit der Streampriorisierung können Sie mehr Kontrolle über die Wiedergabe von Inhalten haben, indem Sie die Prioritäts reihenfolge für die Streams in einem Profil angeben können. Wenn der Reader und der Streamingserver während der Wiedergabe auf einen Bandbreitenengpass stoßen, müssen die Beispiele möglicherweise gelöscht werden, um eine unterbrechungsfreie Wiedergabe zu ermöglichen. Wenn Sie eine Prioritäts reihenfolge mit einem Streampriorisierungsobjekt im Profil angeben, werden die Stichproben zuerst aus den Streams mit der niedrigsten Priorität gelöscht.

Im Gegensatz zu Objekten der Bandbreitenfreigabe und des gegenseitigen Ausschlusses verwendet ein Streampriorisierungsobjekt nicht die [**IWMStreamList-Schnittstelle,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist) um die Liste der Streams nachverfolgung zu behalten. Stattdessen müssen Sie ein Array von [**WM \_ STREAM PRIORITY \_ \_ RECORD-Strukturen**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_priority_record) verwenden. Die Strukturen müssen im Array in absteigender Reihenfolge der Priorität organisiert werden. Zusätzlich zum Halten einer Streamnummer können Sie mit der Streamprioritätsstruktur auch angeben, ob ein Stream obligatorisch ist. Obligatorische Streams werden unabhängig von ihrer Position in der Liste nicht gelöscht.

Der folgende Beispielcode zeigt, wie sie eine Streampriorisierung in ein Profil einordnen. Dieses Profil ist für eine Classroom-Präsentation mit einem Audiostream des Sprechens, einem Videostream der Darstellung und einem Videostream mit den Präsentationsfolien. Der Audiostream ist der wichtigste und obligatorisch. Die Präsentationsfolien haben die niedrigste Priorität, da das Bild ziemlich konstant ist, sodass einige Frames hier verloren gehen und es keinen großen Unterschied machen wird.


```C++
IWMProfileManager*       pProfileMgr = NULL;
IWMProfile*              pProfileTmp = NULL;
IWMProfile3*             pProfile    = NULL;
IWMStreamPrioritization* pPriority   = NULL;

WM_STREAM_PRIORITY_RECORD StreamArray[3];
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a profile manager object.
hr = WMCreateProfileManager(&pProfileMgr);

// Create an empty profile.
hr = pProfileMgr->CreateEmptyProfile(WMT_VER_9_0, &pProfileTmp)

// Get the IWMProfile3 for the new profile, then release the old one.
hr = pProfileTmp->QueryInterface(IID_IWMProfile3, (void**)&pProfile);
pProfileTmp->Release();
pProfileTmp = NULL;

// Give the new profile a name and description.
hr = pProfile->SetName(L"Prioritization_Example");
hr = pProfile->SetDescription(L"Only for use with example code.");

// Create the first stream.
hr = pProfile->CreateNewStream(WMMEDIATYPE_Audio, &pStream);

// TODO: configure the stream as needed for the scenario.

// Set the stream number.
hr = pStream->SetStreamNumber(1);

// Give the stream a name for clarity.
hr = pStream->SetStreamName(L"Lecturer_Audio");

// Include the new stream in the profile.
hr = pProfile->AddStream(pStream);

// Release the stream configuration interface.
pStream->Release();
pStream = NULL;

// Repeat for the other two streams.
hr = pProfile->CreateNewStream(WMMEDIATYPE_Video, &pStream);

// TODO: configure the stream as needed for the scenario.
hr = pStream->SetStreamNumber(2);
hr = pStream->SetStreamName(L"Lecturer_Video");
hr = pProfile->AddStream(pStream);
pStream->Release();
pStream = NULL;

hr = pProfile->CreateNewStream(WMMEDIATYPE_Video, &pStream);

// TODO: configure the stream as needed for the scenario.
hr = pStream->SetStreamNumber(3);
hr = pStream->SetStreamName(L"Slide_Video");
hr = pProfile->AddStream(pStream);
pStream->Release();
pStream = NULL;

// Create a stream prioritization object.
hr = pProfile->CreateNewStreamPrioritization(&pPriority);

// Fill the array with data.
StreamArray[0].wStreamNum = 1;
StreamArray[0].fMandatory = TRUE;

StreamArray[1].wStreamNum = 2;
StreamArray[1].fMandatory = FALSE;

StreamArray[2].wStreamNum = 3;
StreamArray[2].fMandatory = FALSE;

// Assign the stream array to the stream prioritization object.
hr = pPriority->SetPriorityRecords(StreamArray, 3);

// Add the stream prioritization to the profile.
hr = pProfile->SetStreamPrioritization(pPriority);

// Release the stream prioritization object.
pPriority->Release();
pPriority = NULL;

// TODO: Save the profile to a string, and save the string to a file.
// For more information, see To Save a Custom Profile.

// Release the remaining interfaces.
pProfile->Release();
pProfile = NULL;

pProfileMgr->Release();
pProfileMgr = NULL;
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Arbeiten mit Profilen**](working-with-profiles.md)
</dt> </dl>

 

 




