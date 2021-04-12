---
description: Dieses Thema enthält relevante Codebeispiele für die wichtigsten Schritte bei der Entwicklung einer Chatanwendung mit der Peer Gruppierungs-API, die einen Kontext für jeden API-Befehl bereitstellt.
ms.assetid: 47bb8606-0b7b-4e71-9d6f-c400d6a82e43
title: Erstellen einer Gruppen Chat-Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 676d4e9913934024df3131c0f965a5d85477d148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345539"
---
# <a name="creating-a-group-chat-application"></a>Erstellen einer Gruppen Chat-Anwendung

Dieses Thema enthält relevante Codebeispiele für die wichtigsten Schritte bei der Entwicklung einer Chatanwendung mit der Peer Gruppierungs-API, die einen Kontext für jeden API-Befehl bereitstellt. UI-Verhalten und allgemeine Anwendungs Struktur sind nicht enthalten.

> [!Note]  
> Die Beispielanwendung für die komplette Peer Gruppen Chat-Anwendung wird im Peer SDK bereitgestellt. Dieses Thema verweist auf Funktionen, die im Beispiel bereitgestellt werden.

 

## <a name="initializing-a-group"></a>Initialisieren einer Gruppe

Der erste Schritt beim Erstellen einer Chatanwendung besteht darin, die Peer Gruppierungs Infrastruktur zu initialisieren, indem [**peergroupstartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) mit der höchsten unterstützten Version aufgerufen wird. In diesem Fall wird die **Peer \_ Gruppen \_ Version** in der Anwendungs Header Datei definiert. Die von der Infrastruktur tatsächlich unterstützte Version wird in " **Peer Version**" zurückgegeben.


```C++
    PEER_VERSION_DATA peerVersion;

    hr = PeerGroupStartup(PEER_GROUP_VERSION, &peerVersion);
    if (FAILED(hr))
    {
        return hr;
    }
```



## <a name="creating-a-group"></a>Erstellen einer Gruppe

Eine Chatanwendung muss in der Lage sein, eine Peer Gruppe zu erstellen, wenn keine Gruppe zum beitreten verfügbar ist, oder wenn der Anwendungs Benutzer eine neue erstellen möchte. Zu diesem Zweck müssen Sie eine Struktur der [**Peer \_ Gruppen \_ Eigenschaften**](/windows/desktop/api/P2P/ns-p2p-peer_group_properties) erstellen und Sie mit den anfänglichen Einstellungen für die Gruppe auffüllen, einschließlich des Klassifizierers für die Peer Gruppe, des anzeigen Amens, des anzeigen Amens und der Anwesenheits Lebensdauer. Nachdem diese Struktur aufgefüllt wurde, übergeben Sie Sie an " [**Peer groupcreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)".


```C++
//-----------------------------------------------------------------------------
// Function: CreateGroup
//
// Purpose:  Creates a new group with the friendly name.
//
// Returns:  HRESULT
//
HRESULT CreateGroup(PCWSTR pwzName, PCWSTR pwzIdentity)
{
    HRESULT hr = S_OK;
    PEER_GROUP_PROPERTIES props = {0};

    if (SUCCEEDED(hr))
    {
        if ((NULL == pwzName) || (0 == *pwzName))
        {
            hr = E_INVALIDARG;
            DisplayHrError(L"Please enter a group name.", hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        CleanupGroup( );

        props.dwSize = sizeof(props);
        props.pwzClassifier = L"SampleChatGroup";
        props.pwzFriendlyName = (PWSTR) pwzName;
        props.pwzCreatorPeerName = (PWSTR) pwzIdentity;

        hr = PeerGroupCreate(&props, &g_hGroup);
        if (FAILED(hr))
        {
            DisplayHrError(L"Failed to create a new group.", hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        hr = PrepareToChat( );
    }

    return hr;
}
```



## <a name="issuing-invitations"></a>Ausstellende Einladungen

Beim Ausgeben einer Einladung müssen die gmcs der eingeladenen Personen abgerufen werden. Diese können durch Aufrufen von " [**Peer Identity tygetxml**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml) " für den einladenden Empfänger mit Ihrem Identitäts Namen abgerufen werden. Bei erfolgreicher Ausführung werden die Identitätsinformationen (der XML-Code, der das Base-64-codierte Zertifikat mit dem öffentlichen RSA-Schlüssel enthält) an einen externen Speicherort (in diesem Beispiel eine Datei) geschrieben, wo der einlader Sie abrufen und zum Erstellen einer Einladung verwenden kann.

An diesem Punkt muss ein Mechanismus für die Übermittlung der Einladung an den einladenden Empfänger eingerichtet werden. Dabei kann es sich um eine e-Mail oder eine andere sichere Methode des Datei Austauschs handeln. Im folgenden Beispiel wird die Einladung in eine Datei geschrieben, die dann auf den Computer des einladenden Benutzers übertragen werden kann.


```C++
//-----------------------------------------------------------------------------
// Function: SaveIdentityInfo
//
// Purpose:  Saves the information for an identity to a file.
//           Displays a message if there was an error.
//
// Returns:  HRESULT
//
HRESULT SaveIdentityInfo(PCWSTR pwzIdentity, PCWSTR pwzFile)
{
    PWSTR pwzXML = NULL;
    HRESULT hr = PeerIdentityGetXML(pwzIdentity, &pwzXML);

    if (FAILED(hr))
    {
        DisplayHrError(L"Unable to retrieve the XML data for the identity.", hr);
    }
    else
    {
        FILE *fp = NULL;
        errno_t err = 0;

        err = _wfopen_s(&fp, pwzFile, L"wb");
        if (err != 0)
        {
            hr = E_FAIL;
            DisplayHrError(L"Please choose a valid path", hr);
        }
        else
        {
            if (fputws(pwzXML, fp) == WEOF)
            {
                hr = E_FAIL;
                DisplayHrError(L"End of file error.", hr);
            }
            fclose(fp);
        }

        PeerFreeData(pwzXML);
    }

    return hr;
}
```



Einladungen, wie Identitäten, werden auch extern ausgegeben. In diesem Beispiel wird die Einladung in eine Datei mit **fputws** geschrieben, wo Sie vom einladenden Benutzer abgerufen und beim Aufrufen von " [**Peer GroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)" verwendet werden kann.


```C++
//-----------------------------------------------------------------------------
// Function: CreateInvitation
//
// Purpose:  Creates an invitation file for an identity.
//           Displays a message if there was an error.
//
// Returns:  HRESULT
//
HRESULT CreateInvitation(PCWSTR wzIdentityInfoPath, PCWSTR wzInvitationPath)
{
    HRESULT hr = S_OK;
    WCHAR wzIdentityInfo[MAX_INVITATION] = {0};
    PWSTR pwzInvitation = NULL;
    errno_t  err  = 0;
    FILE *file = NULL;
        
    err = _wfopen_s(&file, wzIdentityInfoPath, L"rb");
    if (err != 0)
    {
        hr = E_FAIL;
        DisplayHrError(L"Please choose a valid path to the identity information file.", hr);
    }
    else
    {
        fread(wzIdentityInfo, sizeof(WCHAR), MAX_INVITATION, file);
        if (ferror(file))
        {
            hr = E_FAIL;
            DisplayHrError(L"File read error occurred.", hr);
        }
        fclose(file);
    }

    if (SUCCEEDED(hr))
    {
        ULONGLONG ulExpire; // adjust time using this structure
        GetSystemTimeAsFileTime((FILETIME *)&ulExpire);

        // 15days in 100 nanoseconds resolution
        ulExpire += ((ULONGLONG) (60 * 60 * 24 * 15)) * ((ULONGLONG)1000*1000*10);

        hr = PeerGroupCreateInvitation(g_hGroup, wzIdentityInfo, (FILETIME*)&ulExpire, 1, (PEER_ROLE_ID*) &PEER_GROUP_ROLE_MEMBER, &pwzInvitation);
        if (FAILED(hr))
        {
            DisplayHrError(L"Failed to create the invitation.", hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        err = _wfopen_s(&file, wzInvitationPath, L"wb");
        if (err != 0)
        {
            hr = E_FAIL;
            DisplayHrError(L"Please choose a valid path to the invitation file.", hr);
        }
        else
        {
            if (fputws(pwzInvitation, file) == WEOF)
            {
                hr = E_FAIL;
                DisplayHrError(L"End of file error.", hr);
            }
            fclose(file);
        }
    }

    PeerFreeData(pwzInvitation);
    return hr;
}
```



## <a name="joining-a-peer-group"></a>Beitreten zu einer Peer Gruppe

Wenn der Peer versucht, einer Peer Gruppe beizutreten, die von einem anderen Peer erstellt wurde, wird eine Einladung dieses Peers benötigt. Einladungen werden von einem externen Prozess oder einer externen Anwendung an den einladenden gesendet und in einer lokalen Datei gespeichert, die im folgenden Beispiel als *pwzfilename* angegeben ist. Der Einladungs-XML-BLOB wird aus der Datei in **wzeinladungs** gelesen und an " [**Peer GroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)" weitergegeben.


```C++
//-----------------------------------------------------------------------------
// Function: JoinGroup
//
// Purpose:  Uses the invitation to join a group with a specific identity.
//           Displays a message if there was an error.
//
// Returns:  HRESULT
//
HRESULT JoinGroup(PCWSTR pwzIdentity, PCWSTR pwzFileName)
{
    HRESULT hr = S_OK;
    WCHAR wzInvitation[MAX_INVITATION] = {0};
    FILE        *file = NULL;
    errno_t     err;

    err = _wfopen_s(&file, pwzFileName, L"rb");
    if (err !=  0)
    {
        hr = E_FAIL;
        DisplayHrError(L"Error opening group invitation file", hr);
        return hr;
    }
    else
    {
        fread(wzInvitation, sizeof(WCHAR), MAX_INVITATION, file);
        if (ferror(file))
        {
            hr = E_FAIL;
            DisplayHrError(L"File read error occurred.", hr);
        }
        fclose(file);

        hr = PeerGroupJoin(pwzIdentity, wzInvitation, NULL, &g_hGroup);
        if (FAILED(hr))
        {
            DisplayHrError(L"Failed to join group.", hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        hr = PrepareToChat( );
    }

    return hr;
}
```



## <a name="register-for-peer-events"></a>Für Peer Ereignisse registrieren

Bevor Sie eine Verbindung herstellen, sollten Sie sich für jedes Peer Ereignis registrieren, das für die Anwendung relevant ist. Im folgenden Beispiel registrieren Sie sich für die folgenden Ereignisse:

-   \_Ereignisdaten Satz der Peer Gruppe wurde \_ \_ \_ geändert. Da Datensätze verwendet werden, um öffentliche Chat Nachrichten zu enthalten, muss die Anwendung jedes Mal benachrichtigt werden, wenn eine neue hinzugefügt wird. Wenn dieses Peer Ereignis empfangen wird, machen die Ereignisdaten den Datensatz mit der Chat Nachricht verfügbar. Anwendungen sollten nur für die Daten Satz Typen registriert werden, die direkt verarbeitet werden sollen.
-   Das Peer \_ Gruppen- \_ \_ Ereignismember wurde \_ geändert. Die Anwendung muss benachrichtigt werden, wenn Mitglieder der Peer Gruppe beitreten oder diese verlassen, sodass die Liste der Teilnehmer entsprechend aktualisiert werden kann.
-   der Peer \_ Gruppen- \_ Ereignis Status wurde \_ \_ geändert. Änderungen am Peer Gruppenstatus müssen an die Anwendung übermittelt werden. Ein Peer Gruppenmitglied wird nur in der Peer Gruppe als verfügbar betrachtet, wenn sein Status angibt, dass es mit der Gruppe verbunden ist, mit der datensatzdatenbank der Peer Gruppe synchronisiert wird und aktiv auf Daten Satz Aktualisierungen lauscht.
-   \_direkte Peer Gruppen- \_ Ereignis \_ \_ Verbindung. Private Nachrichten zwischen zwei Mitgliedern und Austauschen von Daten müssen über eine direkte Verbindung durchgeführt werden, sodass die Anwendung direkte Verbindungsanforderungen verarbeiten kann.
-   \_ \_ eingehende Daten der Peer Gruppen Ereignisse \_ \_ . Nachdem eine direkte Verbindung initiiert wurde, warnt dieses Peer Ereignis die Anwendung, dass eine private Nachricht empfangen wurde.


```C++
//-----------------------------------------------------------------------------
// Function: RegisterForEvents
//
// Purpose:  Registers the EventCallback function so it will be called for only
//           those events that are specified.
//
// Returns:  HRESULT
//
HRESULT RegisterForEvents(void)
{
    HRESULT hr = S_OK;
    PEER_GROUP_EVENT_REGISTRATION regs[] = {
        { PEER_GROUP_EVENT_RECORD_CHANGED, &RECORD_TYPE_CHAT_MESSAGE },
        { PEER_GROUP_EVENT_MEMBER_CHANGED, 0 },
        { PEER_GROUP_EVENT_STATUS_CHANGED, 0 },
        { PEER_GROUP_EVENT_DIRECT_CONNECTION, &DATA_TYPE_WHISPER_MESSAGE },
        { PEER_GROUP_EVENT_INCOMING_DATA, 0 },
    };

    g_hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
    if (g_hEvent == NULL)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }
    else
    {
        hr = PeerGroupRegisterEvent(g_hGroup, g_hEvent, celems(regs), regs,  &g_hPeerEvent);
    }

    if (SUCCEEDED(hr))
    {
        if (!RegisterWaitForSingleObject(&g_hWait, g_hEvent, EventCallback, NULL, INFINITE, WT_EXECUTEDEFAULT))
        {
            hr = E_UNEXPECTED;
        }
    }

    return hr;
}
```



## <a name="connecting-to-a-peer-group"></a>Herstellen einer Verbindung mit einer Peer Gruppe

Nachdem Sie die Gruppe erstellt oder verknüpft und für die entsprechenden Ereignisse registriert haben, ist es an der Zeit, Online zu gehen und eine aktive Chatsitzung zu starten. Dazu rufen Sie " [**Peer groupconnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) " auf und übergeben das Gruppen handle, das von " [**Peer groupcreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate) " oder " [**Peer-GroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)" abgerufen wurde. Nach dem Aufruf dieser Methode werden Chat Nachrichten als \_ geänderte Ereignisse für Peer Gruppen \_ Ereignis \_ Datensätze empfangen \_ .

## <a name="obtaining-a-list-of-peer-group-members"></a>Abrufen einer Liste von Peer Gruppenmitgliedern

Das Abrufen einer Liste von Membern, die mit der Peer Gruppe verbunden sind, ist einfach: Rufen Sie [**peergroutzenummembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers) auf, um die Liste der Gruppenmitglieder abzurufen, und rufen Sie [**peergetnextitem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) dann iterativ auf, bis alle Elemente abgerufen wurden. Sie sollten " [**Peer Service**](/windows/desktop/api/P2P/nf-p2p-peerfreedata) " aufrufen, nachdem Sie die einzelnen Element Strukturen verarbeitet haben, und Sie müssen die Enumeration schließen, indem Sie " [**Peer Enumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) " aufrufen, wenn die Verarbeitung abgeschlossen ist.


```C++
//-----------------------------------------------------------------------------
// Function: UpdateParticipantList
//
// Purpose:  Update the list of partipants.
//
// Returns:  nothing
//
void UpdateParticipantList(void)
{
    HRESULT          hr = S_OK;
    HPEERENUM        hPeerEnum = NULL;
    PEER_MEMBER   ** ppMember = NULL;

    ClearParticipantList( );
    if (NULL == g_hGroup)
    {
        return;
    }

    // Retrieve only the members currently present in the group.
    hr = PeerGroupEnumMembers(g_hGroup, PEER_MEMBER_PRESENT, NULL, &hPeerEnum);
    if (SUCCEEDED(hr))
    {
        while (SUCCEEDED(hr))
        {
            ULONG cItem = 1;
            hr = PeerGetNextItem(hPeerEnum, &cItem, (PVOID **) &ppMember);
            if (SUCCEEDED(hr))
            {
                if (0 == cItem)
                {
                    PeerFreeData(ppMember);
                    break;
                }
            }

            if (SUCCEEDED(hr))
            {
                if (0 != ((*ppMember)->dwFlags & PEER_MEMBER_PRESENT))
                {
                    AddParticipantName((*ppMember)->pwzIdentity, (*ppMember)->pCredentialInfo->pwzFriendlyName);
                }
                PeerFreeData(ppMember);
            }
        }

        PeerEndEnumeration(hPeerEnum);
    }
}
```



## <a name="sending-a-chat-message"></a>Senden einer Chat Nachricht

In diesem Beispiel wird eine Chat Nachricht gesendet, indem Sie im **Datenfeld** einer [**Peer \_ Daten Satz**](/windows/desktop/api/P2P/ns-p2p-peer_record) Struktur abgelegt wird. Der Datensatz wird den Peer Gruppendaten Sätzen hinzugefügt, indem [**peergroupaddrecord**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord)aufgerufen wird, der ihn veröffentlicht und das Änderungs Ereignis des Peer \_ Gruppen \_ Ereignis \_ Datensatzes \_ auf allen Peers, die an der Peer Gruppe teilnehmen, aufhebt.


```C++
//-----------------------------------------------------------------------------
// Function: AddChatRecord
//
// Purpose:  This adds a new chat message record to the group.
//
// Returns:  HRESULT
//
HRESULT AddChatRecord(PCWSTR pwzMessage)
{
    HRESULT     hr = S_OK;
    PEER_RECORD record = {0};
    GUID        idRecord;
    ULONGLONG   ulExpire;
    ULONG cch = (ULONG) wcslen(pwzMessage);

    GetSystemTimeAsFileTime((FILETIME *) &ulExpire);

    // Calculate a 2 minute expiration time in 100 nanosecond resolution
    ulExpire += ((ULONGLONG) 60 * 2) * ((ULONGLONG)1000*1000*10);

    // Set up the record
    record.dwSize = sizeof(record);
    record.data.cbData = (cch+1) * sizeof(WCHAR);
    record.data.pbData = (PBYTE) pwzMessage;
    memcpy(&record.ftExpiration, &ulExpire, sizeof(ulExpire));

    PeerGroupUniversalTimeToPeerTime(g_hGroup, &record.ftExpiration, &record.ftExpiration);

    // Set the record type GUID
    record.type = RECORD_TYPE_CHAT_MESSAGE;

    // Add the record to the database
    hr = PeerGroupAddRecord(g_hGroup, &record, &idRecord);
    if (FAILED(hr))
    {
        DisplayHrError(L"Failed to add a chat record to the group.", hr);
    }

    return hr;
}
```



## <a name="receiving-a-chat-message"></a>Empfangen einer Chat Nachricht

Um die Chat Nachricht zu empfangen, erstellen Sie eine Rückruffunktion für das Ereignisdaten Satz-Änderungs Ereignis des Peer \_ Gruppen \_ Ereignisses \_ \_ , das eine Funktion ähnlich der folgenden aufruft. Der Datensatz wird abgerufen, indem für die Ereignisdaten, die von einem vorherigen Aufruf von " [**Peer groupgeteventdata**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) " in der Rückruffunktion empfangen wurden, " [**Peer groupgetrecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) " aufgerufen wird. Die Chat Nachricht wird im **Datenfeld dieses Daten** Satzes gespeichert.


```C++
//-----------------------------------------------------------------------------
// Function: ProcessRecordChanged
//
// Purpose:  Processes the PEER_GROUP_EVENT_RECORD_CHANGED event.
//
// Returns:  nothing
//
void ProcessRecordChanged(PEER_EVENT_RECORD_CHANGE_DATA * pData)
{
    switch (pData->changeType)
    {
        case PEER_RECORD_ADDED:
            if (IsEqualGUID(&pData->recordType, &RECORD_TYPE_CHAT_MESSAGE))
            {
                PEER_RECORD * pRecord = {0};
                HRESULT hr = PeerGroupGetRecord(g_hGroup, &pData->recordId, &pRecord);
                if (SUCCEEDED(hr))
                {
                    DisplayChatMessage(pRecord->pwzCreatorId, (PCWSTR) pRecord->data.pbData);
                    PeerFreeData(pRecord);
                }
            }
            break;

        case PEER_RECORD_UPDATED:
        case PEER_RECORD_DELETED:
        case PEER_RECORD_EXPIRED:
            break;

        default:
            break;
    }
}
```



 

 



