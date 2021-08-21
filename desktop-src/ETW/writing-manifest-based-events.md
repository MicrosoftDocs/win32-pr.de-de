---
description: Erfahren Sie mehr über das Schreiben manifestbasierter Ereignisse in eine Ablaufverfolgungssitzung. Beginnen Sie mit der Registrierung Ihres Anbieters, damit er ereignisse in eine Ablaufverfolgungssitzung schreiben kann.
ms.assetid: 76e7202e-74ce-40a3-a04b-9af5117fe20e
title: Schreiben manifestbasierter Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6963051f65beb652eda04e3d0be6db99925e4eed81032c5687850915a0f1c173
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151079"
---
# <a name="writing-manifest-based-events"></a>Schreiben manifestbasierter Ereignisse

Bevor Sie Ereignisse in eine Ablaufverfolgungssitzung schreiben können, müssen Sie Ihren Anbieter registrieren. Das Registrieren eines Anbieters teilt ETW mit, dass Ihr Anbieter bereit ist, Ereignisse in eine Ablaufverfolgungssitzung zu schreiben. Ein Prozess kann bis zu 1.024 Anbieter-GUIDs registrieren. Sie sollten jedoch die Anzahl der Anbieter, die Ihr Prozess registriert, auf ein oder zwei beschränken.

**Vor der Windows Vista:** Es gibt keine Beschränkung für die Anzahl der Anbieter, die ein Prozess registrieren kann.

Um einen manifestbasierten Anbieter zu registrieren, rufen Sie die [**EventRegister-Funktion**](/windows/desktop/api/Evntprov/nf-evntprov-eventregister) auf. Die Funktion registriert die GUID des Anbieters und identifiziert einen optionalen Rückruf, den ETW aufruft, wenn ein Controller den Anbieter aktiviert oder deaktiviert.

Rufen Sie vor dem Beenden des Anbieters die [**EventUnregister-Funktion**](/windows/desktop/api/Evntprov/nf-evntprov-eventunregister) auf, um die Registrierung des Anbieters aus ETW zu entfernen. Die [**EventRegister-Funktion**](/windows/desktop/api/Evntprov/nf-evntprov-eventregister) gibt das Registrierungshand handle zurück, das Sie an die **EventUnregister-Funktion** übergeben.

[Manifestbasierte Anbieter](about-event-tracing.md) müssen keine [**EnableCallback-Funktion**](/windows/desktop/api/Evntprov/nc-evntprov-penablecallback) implementieren, um Benachrichtigungen zu empfangen, wenn eine Sitzung den Anbieter aktiviert oder deaktiviert. Der Rückruf ist optional und wird zu Informationszwecken verwendet. Sie müssen den Rückruf nicht angeben oder implementieren, wenn Sie den Anbieter registrieren. Ein manifestbasierter Anbieter kann einfach Ereignisse schreiben, und ETW entscheidet, ob das Ereignis in einer Ablaufverfolgungssitzung protokolliert wird. Wenn für ein Ereignis umfangreiche Aufgaben zum Generieren der Ereignisdaten erforderlich sind, sollten Sie zuerst die [**Funktion EventEnabled**](/windows/desktop/api/Evntprov/nf-evntprov-eventenabled) oder [**EventProviderEnabled**](/windows/desktop/api/Evntprov/nf-evntprov-eventproviderenabled) aufrufen, um zu überprüfen, ob das Ereignis in eine Sitzung geschrieben wird, bevor Sie die Arbeit ausführen.

In der Regel implementieren Sie den Rückruf, wenn Ihr Anbieter erfordert, dass der Controller anbieterdefinierte Filterdaten (siehe *FilterData-Parameter* von [**EnableCallback**](/windows/desktop/api/Evntprov/nc-evntprov-penablecallback)) an den Anbieter übergibt, oder der Anbieter die Kontextinformationen verwendet, die er bei der Registrierung selbst angegeben hat (siehe *Den CallbackContext-Parameter* von [**EventRegister**](/windows/desktop/api/Evntprov/nf-evntprov-eventregister)).

[Manifestbasierte Anbieter rufen](about-event-tracing.md) die [**Funktion EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) oder [**EventWriteString**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritestring) auf, um Ereignisse in eine Sitzung zu schreiben. Wenn ihre Ereignisdaten eine Zeichenfolge sind oder Wenn Sie kein Manifest für Ihren Anbieter definieren und ihre Ereignisdaten eine einzelne Zeichenfolge sind, rufen Sie die [**EventWriteString-Funktion**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritestring) auf, um das Ereignis zu schreiben. Rufen Sie für Ereignisdaten, die numerische oder komplexe Datentypen enthalten, die [**EventWrite-Funktion**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) auf, um das Ereignis zu protokollieren.

Das folgende Beispiel zeigt, wie sie die Ereignisdaten vorbereiten, die mit der [**EventWrite-Funktion geschrieben werden**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) sollen. Im Beispiel wird auf die Ereignisse verwiesen, die unter [Veröffentlichen des Ereignisschemas für einen manifestbasierten Anbieter definiert sind.](publishing-your-event-schema-for-a-manifest-base-provider.md)


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



Wenn Sie das Manifest kompilieren (siehe [Kompilieren](../wes/compiling-an-instrumentation-manifest.md)eines Instrumentierungsmanifests), das im obigen Beispiel verwendet wird, wird die folgende Headerdatei erstellt (auf die im obigen Beispiel verwiesen wird).


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



 

 
