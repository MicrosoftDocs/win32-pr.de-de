---
description: Bevor Sie Ereignisse in eine Ablauf Verfolgungs Sitzung schreiben können, müssen Sie den Anbieter registrieren.
ms.assetid: 76e7202e-74ce-40a3-a04b-9af5117fe20e
title: Schreiben von Manifest-basierten Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a1817defe85e68860d8a628a2d3275034ce285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130080"
---
# <a name="writing-manifest-based-events"></a>Schreiben von Manifest-basierten Ereignissen

Bevor Sie Ereignisse in eine Ablauf Verfolgungs Sitzung schreiben können, müssen Sie den Anbieter registrieren. Wenn Sie einen Anbieter registrieren, wird etw mitgeteilt, dass der Anbieter zum Schreiben von Ereignissen in eine Ablauf Verfolgungs Sitzung bereit ist. Ein Prozess kann bis zu 1.024 Anbieter-GUIDs registrieren. Sie sollten jedoch die Anzahl der Anbieter, die Ihr Prozess registriert, auf einen oder zwei beschränken.

**Vor Windows Vista:** Es gibt keine Beschränkung für die Anzahl der Anbieter, die ein Prozess registrieren kann.

Um einen Manifest-basierten Anbieter zu registrieren, nennen Sie die [**EventRegister**](/windows/desktop/api/Evntprov/nf-evntprov-eventregister) -Funktion. Die Funktion registriert die GUID des Anbieters und identifiziert einen optionalen Rückruf, der von etw aufgerufen wird, wenn ein Controller den Anbieter aktiviert oder deaktiviert.

Bevor der Anbieter beendet wird, wenden Sie die [**EventUnregister**](/windows/desktop/api/Evntprov/nf-evntprov-eventunregister) -Funktion an, um die Registrierung des Anbieters von etw zu entfernen. Die [**EventRegister**](/windows/desktop/api/Evntprov/nf-evntprov-eventregister) -Funktion gibt das Registrierungs Handle zurück, das Sie an die **EventUnregister** -Funktion übergeben.

Manifestressourcen müssen keine [**enablecallback**](/windows/desktop/api/Evntprov/nc-evntprov-penablecallback) [-](about-event-tracing.md) Funktion implementieren, um Benachrichtigungen zu empfangen, wenn der Anbieter durch eine Sitzung aktiviert oder deaktiviert wird. Der Rückruf ist optional und wird zu Informationszwecken verwendet. beim Registrieren des Anbieters muss der Rückruf nicht angegeben oder implementiert werden. Ein Manifest-basierter Anbieter kann einfach Ereignisse schreiben, und etw entscheidet, ob das Ereignis in einer Ablauf Verfolgungs Sitzung protokolliert wird. Wenn ein Ereignis erfordert, dass Sie umfangreiche Arbeiten ausführen müssen, um die Daten des Ereignisses zu generieren, können Sie zuerst die [**eventaktivierte**](/windows/desktop/api/Evntprov/nf-evntprov-eventenabled) Funktion oder die [**eventprovideraktivierte**](/windows/desktop/api/Evntprov/nf-evntprov-eventproviderenabled) Funktion aufzurufen, um zu überprüfen, ob das Ereignis in eine Sitzung geschrieben wird, bevor Sie die Arbeit ausführen.

In der Regel implementieren Sie den Rückruf, wenn der Anbieter erfordert, dass der Controller Anbieter definierte Filterdaten (siehe den *FilterData* -Parameter von [**enablecallback**](/windows/desktop/api/Evntprov/nc-evntprov-penablecallback)) an den Anbieter übergibt, oder der Anbieter verwendet die Kontextinformationen, die er bei der Registrierung angegeben hat (siehe *callbackcontext* -Parameter von [**EventRegister**](/windows/desktop/api/Evntprov/nf-evntprov-eventregister)).

Manifestressourcenbasierte Anbieter nennen die [**EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) -oder [**EventWrite-String**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritestring) [-](about-event-tracing.md) Funktion, um Ereignisse in eine Sitzung zu schreiben. Wenn es sich bei den Ereignisdaten um eine Zeichenfolge handelt, oder wenn Sie kein Manifest für Ihren Anbieter definieren und die Ereignisdaten eine einzelne Zeichenfolge sind, müssen Sie die [**EventWrite-String**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritestring) -Funktion verwenden, um das Ereignis zu schreiben. Bei Ereignisdaten, die numerische oder komplexe Datentypen enthalten, wird die [**EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) -Funktion aufgerufen, um das Ereignis zu protokollieren.

Im folgenden Beispiel wird gezeigt, wie die Ereignisdaten vorbereitet werden, die mit der [**EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) -Funktion geschrieben werden sollen. Das Beispiel verweist auf die Ereignisse, die in [Veröffentlichen des Ereignis Schemas für einen Manifest-basierten Anbieter](publishing-your-event-schema-for-a-manifest-base-provider.md)definiert sind.


```C++
#include <windows.h>
#include <stdio.h>
#include <evntprov.h>
#include "provider.h"  // Generated from manifest

#define SUNDAY     0X1
#define MONDAY     0X2
#define TUESDAY    0X4
#define WEDNESDAY  0X8
#define THURSDAY   0X10
#define FRIDAY     0X20
#define SATURDAY   0X40

enum TRANSFER_TYPE {
  Download = 1,
  Upload,
  UploadReply
};

#define MAX_NAMEDVALUES          5  // Maximum array size
#define MAX_PAYLOAD_DESCRIPTORS  9 + (2 * MAX_NAMEDVALUES)

typedef struct _namedvalue {
  LPWSTR name;
  USHORT value;
} NAMEDVALUE, *PNAMEDVALUE;

void wmain(void)
{
    DWORD status = ERROR_SUCCESS;
    REGHANDLE RegistrationHandle = NULL; 
    EVENT_DATA_DESCRIPTOR Descriptors[MAX_PAYLOAD_DESCRIPTORS]; 
    DWORD i = 0;

    // Data to load into event descriptors

    USHORT Scores[3] = {45, 63, 21};
    ULONG pImage = (ULONG)&Scores;
    DWORD TransferType = Upload;
    DWORD Day = MONDAY | TUESDAY;
    LPWSTR Path = L"c:\\path\\folder\\file.ext";
    BYTE Cert[11] = {0x2, 0x4, 0x8, 0x10, 0x20, 0x30, 0x40, 0x50, 0x60, 0x0, 0x1};
    PBYTE Guid = (PBYTE) &ProviderGuid;
    USHORT ArraySize = MAX_NAMEDVALUES;
    BOOL IsLocal = TRUE;
    NAMEDVALUE NamedValues[MAX_NAMEDVALUES] = { 
        {L"Bill", 1},
        {L"Bob", 2},
        {L"William", 3},
        {L"Robert", 4},
        {L"", 5}
        };

    status = EventRegister(
        &ProviderGuid,      // GUID that identifies the provider
        NULL,               // Callback not used
        NULL,               // Context noot used
        &RegistrationHandle // Used when calling EventWrite and EventUnregister
        );

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"EventRegister failed with %lu\n", status);
        goto cleanup;
    }
  
    // Load the array of data descriptors for the TransferEvent event. 
    // Add the data to the array in the order of the <data> elements
    // defined in the event's template. 
   
    EventDataDescCreate(&Descriptors[i++], &pImage, sizeof(ULONG));
    EventDataDescCreate(&Descriptors[i++], Scores, sizeof(Scores));
    EventDataDescCreate(&Descriptors[i++], Guid, sizeof(GUID));
    EventDataDescCreate(&Descriptors[i++], Cert, sizeof(Cert));
    EventDataDescCreate(&Descriptors[i++], &IsLocal, sizeof(BOOL));
    EventDataDescCreate(&Descriptors[i++], Path, (ULONG)(wcslen(Path) + 1) * sizeof(WCHAR));
    EventDataDescCreate(&Descriptors[i++], &ArraySize, sizeof(USHORT));

    // If your event contains a structure, you should write each member
    // of the structure separately. If the structure contained integral data types
    // such as DWORDs and the data types were aligned on an 8-byte boundary, you 
    // could use the following call to write the structure, however, you are 
    // encouraged to write the members separately.
    //
    // EventDataDescCreate(&EvtData, struct, sizeof(struct));
    //
    // Because the array of structures in this example contains both strings 
    // and numbers, you must write each member of the structure separately.

    for (int j = 0; j < MAX_NAMEDVALUES; j++)
    {
        EventDataDescCreate(&Descriptors[i++], NamedValues[j].name, (ULONG)(wcslen(NamedValues[j].name)+1) * sizeof(WCHAR) );
        EventDataDescCreate(&Descriptors[i++], &(NamedValues[j].value), sizeof(USHORT) );
    }

    EventDataDescCreate(&Descriptors[i++], &Day, sizeof(DWORD));
    EventDataDescCreate(&Descriptors[i++], &TransferType, sizeof(DWORD));

    // Write the event. You do not have to verify if your provider is enabled before
    // writing the event. ETW will write the event to any session that enabled
    // the provider. If no session enabled the provider, the event is not 
    // written. If you need to perform extra work to write an event that you
    // would not otherwise do, you may want to call the EventEnabled function
    // before performing the extra work. The EventEnabled function tells you if a
    // session has enabled your provider, so you know if you need to perform the 
    // extra work or not.

    status = EventWrite(
        RegistrationHandle,              // From EventRegister
        &TransferEvent,                  // EVENT_DESCRIPTOR generated from the manifest
        (ULONG)MAX_PAYLOAD_DESCRIPTORS,  // Size of the array of EVENT_DATA_DESCRIPTORs
        &Descriptors[0]                  // Array of descriptors that contain the event data
        );

    if (status != ERROR_SUCCESS) 
    {
        wprintf(L"EventWrite failed with 0x%x", status);
    }

cleanup:

    EventUnregister(RegistrationHandle);
}
```



Wenn Sie das Manifest kompilieren (siehe [Kompilieren eines Instrumentierungs Manifests](../wes/compiling-an-instrumentation-manifest.md)), das im obigen Beispiel verwendet wird, wird die folgende Header Datei erstellt (im obigen Beispiel wird darauf verwiesen).


```C++
//**********************************************************************`
//* This is an include file generated by Message Compiler.             *`
//*                                                                    *`
//* Copyright (c) Microsoft Corporation. All Rights Reserved.          *`
//**********************************************************************`
#pragma once
//+
// Provider Microsoft-Windows-ETWProvider Event Count 1
//+
EXTERN_C __declspec(selectany) const GUID ProviderGuid = {0xd8909c24, 0x5be9, 0x4502, {0x98, 0xca, 0xab, 0x7b, 0xdc, 0x24, 0x89, 0x9d}};
//
// Keyword
//
#define READ_KEYWORD 0x1
#define WRITE_KEYWORD 0x2
#define LOCAL_KEYWORD 0x4
#define REMOTE_KEYWORD 0x8

//
// Event Descriptors
//
EXTERN_C __declspec(selectany) const EVENT_DESCRIPTOR TransferEvent = {0x1, 0x0, 0x0, 0x4, 0x0, 0x0, 0x5};
#define TransferEvent_value 0x1
#define MSG_Provider_Name                    0x90000001L
#define MSG_Event_WhenToTransfer             0xB0000001L
#define MSG_Map_Download                     0xD0000001L
#define MSG_Map_Upload                       0xD0000002L
#define MSG_Map_UploadReply                  0xD0000003L
#define MSG_Map_Sunday                       0xF0000001L
#define MSG_Map_Monday                       0xF0000002L
#define MSG_Map_Tuesday                      0xF0000003L
#define MSG_Map_Wednesday                    0xF0000004L
#define MSG_Map_Thursday                     0xF0000005L
#define MSG_Map_Friday                       0xF0000006L
#define MSG_Map_Saturday                     0xF0000007L
```



 

 
