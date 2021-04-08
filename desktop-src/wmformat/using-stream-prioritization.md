---
title: Verwenden der streampriorisierung
description: Verwenden der streampriorisierung
ms.assetid: 5fff212e-b47b-49a6-817f-f0e09c895b3a
keywords:
- Windows Media-Format-SDK, streampriorisierung
- Profile, streampriorisierung
- Streams, Priorisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99a6b0bd3d49db9523ef9ea5585803b4c703c279
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103948413"
---
# <a name="using-stream-prioritization"></a>Verwenden der streampriorisierung

Die streampriorisierung ermöglicht Ihnen mehr Kontrolle über die Wiedergabe von Inhalten, indem Sie die Prioritäts Reihenfolge für die Datenströme in einem Profil festlegen können. Wenn der Reader und der Streamingserver während der Wiedergabe auf Bandbreite stoßen, müssen möglicherweise Beispiele gelöscht werden, um eine ununterbrochene Wiedergabe zu ermöglichen. Wenn Sie im Profil eine Prioritäts Reihenfolge mit einem streampriorisierungsobjekt angeben, werden die Beispiele zuerst aus den Datenströmen der niedrigsten Priorität gelöscht.

Anders als bei Bandbreiten Freigabe und Objekten mit gegenseitigem Ausschluss verwendet ein streampriorisierungsobjekt die [**iwmstreamlist**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist) -Schnittstelle nicht, um die Liste der Streams nachzuverfolgen. Stattdessen müssen Sie ein Array von [**\_ \_ \_ Daten Satz**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_priority_record) Strukturen mit WM-Stream-Priorität verwenden. Die Strukturen müssen im Array in absteigender Reihenfolge der Priorität angeordnet werden. Zusätzlich zum Speichern einer streamnummer können Sie mit der Stream-Prioritäts Struktur auch angeben, ob ein Stream obligatorisch ist. Obligatorische Streams werden nicht gelöscht, unabhängig von ihrer Position in der Liste.

Der folgende Beispielcode zeigt, wie Sie eine streampriorisierung in ein Profil einschließen. Dieses Profil ist für eine Classroom-Präsentation mit einem Audiostream des Dozenten, einem Videostream des Dozenten und einem Videostream, der die Präsentationsfolien erfasst. Der Audiodatenstrom ist die wichtigste und ist obligatorisch. Die Präsentationsfolien haben die niedrigste Priorität, da das Bild ziemlich konstant ist, sodass einige Bilder hier verloren gehen und es keinen großen Unterschied gibt.


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

 

 




