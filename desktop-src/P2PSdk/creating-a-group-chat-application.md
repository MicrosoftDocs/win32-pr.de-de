---
description: Dieses Thema enthält relevante Codebeispiele für die wichtigsten Schritte zum Entwickeln einer Chatanwendung mit der Peergruppierungs-API, die einen Kontext für jeden API-Aufruf bereitstellt.
ms.assetid: 47bb8606-0b7b-4e71-9d6f-c400d6a82e43
title: Erstellen einer Gruppenchatanwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcb8f9458f8e01bea86e42f0cd976395e951bda52f13af46952479d5810e46c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011658"
---
# <a name="creating-a-group-chat-application"></a>Erstellen einer Gruppenchatanwendung

Dieses Thema enthält relevante Codebeispiele für die wichtigsten Schritte zum Entwickeln einer Chatanwendung mit der Peergruppierungs-API, die einen Kontext für jeden API-Aufruf bereitstellt. Benutzeroberflächenverhalten und allgemeine Anwendungsstruktur sind nicht enthalten.

> [!Note]  
> Die vollständige Peergruppenchat-Beispielanwendung wird im Peer SDK bereitgestellt. Dieses Thema verweist auf Funktionen, die im Beispiel bereitgestellt werden.

 

## <a name="initializing-a-group"></a>Initialisieren einer Gruppe

Der erste Schritt beim Erstellen einer Chatanwendung besteht darin, die Peergruppierungsinfrastruktur durch Aufrufen von [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) mit der höchsten unterstützten Version zu initialisieren. In diesem Fall wird **PEER \_ GROUP \_ VERSION** in der Anwendungsheaderdatei definiert. Die tatsächlich von der Infrastruktur unterstützte Version wird in **peerVersion** zurückgegeben.


```C++
    PEER_VERSION_DATA peerVersion;

    hr = PeerGroupStartup(PEER_GROUP_VERSION, &peerVersion);
    if (FAILED(hr))
    {
        return hr;
    }
```



## <a name="creating-a-group"></a>Erstellen einer Gruppe

Eine Chatanwendung muss in der Lage sein, eine Peergruppe zu erstellen, wenn keine Gruppe für den Beitritt verfügbar ist oder wenn der Anwendungsbenutzer eine neue erstellen möchte. Hierzu müssen Sie eine [**PEER \_ GROUP \_ PROPERTIES-Struktur**](/windows/desktop/api/P2P/ns-p2p-peer_group_properties) erstellen und mit den Anfangseinstellungen für die Gruppe auffüllen, einschließlich der Klassifizierung für die Peergruppe, des Anzeigenamens, des Peernamens des Erstellers und der Lebensdauer der Anwesenheit. Nachdem diese Struktur aufgefüllt wurde, übergeben Sie sie an [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate).


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



## <a name="issuing-invitations"></a>Ausstellen von Einladungen

Beim Ausstellen einer Einladung müssen die GMCs der Eingeladenen abgerufen werden. Diese können abgerufen werden, indem [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml) für die eingeladene Person mit ihrem Identitätsnamen aufgerufen wird. Bei Erfolg werden die Identitätsinformationen (der XML-Code, der das Base64-codierte Zertifikat mit dem öffentlichen RSA-Schlüssel enthält) an einen externen Speicherort (in diesem Beispiel eine Datei) geschrieben, wo der einladende Benutzer es abrufen und zum Erstellen einer Einladung verwenden kann.

An diesem Punkt muss ein Mechanismus für die Übermittlung der Einladung an den eingeladenen Teilnehmer eingerichtet werden. Dies kann eine E-Mail oder eine andere sichere Methode für den Dateiaustausch sein. Im folgenden Beispiel wird die Einladung in eine Datei geschrieben, die dann auf den Computer des eingeladenen Benutzers übertragen werden kann.


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



Einladungen wie Identitäten werden auch extern ausgegeben. In diesem Beispiel wird die Einladung in eine Datei mit **Fputws** geschrieben, in der der eingeladene Benutzer sie abrufen und verwenden kann, wenn er [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)aufruft.


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



## <a name="joining-a-peer-group"></a>Beitreten zu einer Peergruppe

Wenn der Peer versucht, einer Peergruppe beizutreten, die von einem anderen Peer erstellt wurde, benötigt er eine Einladung von diesem Peer. Einladungen werden von einem externen Prozess oder einer externen Anwendung an den Eingeladenen übermittelt und in einer lokalen Datei gespeichert, die im folgenden Beispiel als *pwzFileName* angegeben ist. Das EINLADUNGS-XML-Blob wird aus der Datei in **wzInvitation** gelesen und an [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)übergeben.


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



## <a name="register-for-peer-events"></a>Registrieren für Peerereignisse

Bevor Sie eine Verbindung herstellen, sollten Sie sich für jedes Peerereignis registrieren, das für die Anwendung relevant ist. Im folgenden Beispiel registrieren Sie sich für die folgenden Ereignisse:

-   DER \_ \_ PEERGRUPPENEREIGNISDATENSATZ \_ \_ WURDE GEÄNDERT. Da Datensätze verwendet werden, um öffentliche Chatnachrichten zu enthalten, muss die Anwendung jedes Mal benachrichtigt werden, wenn eine neue hinzugefügt wird. Wenn dieses Peerereignis empfangen wird, machen die Ereignisdaten den Datensatz mit der Chatnachricht verfügbar. Anwendungen sollten sich nur für die Datensatztypen registrieren, die sie direkt behandeln möchten.
-   DAS \_ \_ PEERGRUPPENEREIGNISMITGLIED \_ \_ WURDE GEÄNDERT. Die Anwendung muss benachrichtigt werden, wenn Mitglieder der Peergruppe beitreten oder diese verlassen, damit die Liste der Teilnehmer entsprechend aktualisiert werden kann.
-   STATUS DES \_ \_ PEERGRUPPENEREIGNISSES \_ \_ GEÄNDERT. Änderungen am Peergruppenstatus müssen der Anwendung übermittelt werden. Ein Peergruppenmitglied gilt nur als innerhalb der Peergruppe verfügbar, wenn sein Status angibt, dass es mit der Gruppe verbunden, mit der Peergruppen-Datensatzdatenbank synchronisiert und aktiv auf Datensatzaktualisierungen lauscht.
-   DIREKTE VERBINDUNG MIT \_ \_ PEERGRUPPENEREIGNISSEN. \_ \_ Private Nachrichten zwischen zwei Membern und der Datenaustausch müssen über eine direkte Verbindung erfolgen, sodass die Anwendung anforderungen für direkte Verbindungen verarbeiten kann.
-   \_EINGEHENDE DATEN DES PEERGRUPPENEREIGNISSES. \_ \_ \_ Nachdem eine direkte Verbindung initiiert wurde, warnt dieses Peerereignis die Anwendung, dass eine private Nachricht empfangen wurde.


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



## <a name="connecting-to-a-peer-group"></a>Herstellen einer Verbindung mit einer Peergruppe

Nachdem Sie die Gruppe erstellt oder der Gruppe beigetreten und sich für die entsprechenden Ereignisse registriert haben, ist es an der Zeit, online zu gehen und eine aktive Chatsitzung zu starten. Hierzu rufen Sie [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) auf und übergeben das Gruppenhandle, das von [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate) oder [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)abgerufen wurde. Nach dem Aufruf werden Chatnachrichten als PEER \_ GROUP \_ EVENT RECORD \_ \_ CHANGED-Ereignisse empfangen.

## <a name="obtaining-a-list-of-peer-group-members"></a>Abrufen einer Liste von Peergruppenmitgliedern

Das Abrufen einer Liste von Mitgliedern, die mit der Peergruppe verbunden sind, ist einfach: Rufen Sie [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers) auf, um die Liste der Gruppenmitglieder abzurufen, und rufen Sie [**peerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) dann iterativ auf, bis alle Mitglieder abgerufen werden. Sie sollten [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata) aufrufen, nachdem Sie die einzelnen Memberstrukturen verarbeitet haben, und Sie müssen die Enumeration schließen, indem Sie [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) aufrufen, wenn die Verarbeitung abgeschlossen ist.


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



## <a name="sending-a-chat-message"></a>Senden einer Chatnachricht

In diesem Beispiel wird eine Chatnachricht gesendet, indem sie im **Datenfeld** einer [**PEER \_ RECORD-Struktur**](/windows/desktop/api/P2P/ns-p2p-peer_record) platziert wird. Der Datensatz wird den Peergruppendatensätzen durch Aufrufen von [**PeerGroupAddRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord)hinzugefügt. Dadurch wird er veröffentlicht und das \_ PEER GROUP EVENT RECORD \_ \_ \_ CHANGED-Ereignis auf allen Peers, die an der Peergruppe teilnehmen, ausgegeben.


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



## <a name="receiving-a-chat-message"></a>Empfangen einer Chatnachricht

Um die Chatnachricht zu empfangen, erstellen Sie eine Rückruffunktion für das PEER \_ GROUP \_ EVENT RECORD \_ \_ CHANGED-Ereignis, das eine Funktion ähnlich der folgenden aufruft. Der Datensatz wird durch Aufrufen von [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) für die Ereignisdaten abgerufen, die durch einen vorherigen Aufruf von [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) in der Rückruffunktion empfangen wurden. Die Chatnachricht wird im **Datenfeld** dieses Datensatzes gespeichert.


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



 

 



