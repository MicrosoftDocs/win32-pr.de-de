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
# <a name="creating-a-group-chat-application"></a><span data-ttu-id="05049-103">Erstellen einer Gruppen Chat-Anwendung</span><span class="sxs-lookup"><span data-stu-id="05049-103">Creating a Group Chat Application</span></span>

<span data-ttu-id="05049-104">Dieses Thema enthält relevante Codebeispiele für die wichtigsten Schritte bei der Entwicklung einer Chatanwendung mit der Peer Gruppierungs-API, die einen Kontext für jeden API-Befehl bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="05049-104">This topic provides relevant code samples for the major steps of developing a chat application with the Peer Grouping API, providing a context for each API call.</span></span> <span data-ttu-id="05049-105">UI-Verhalten und allgemeine Anwendungs Struktur sind nicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="05049-105">UI behaviors and overall application structure are not included.</span></span>

> [!Note]  
> <span data-ttu-id="05049-106">Die Beispielanwendung für die komplette Peer Gruppen Chat-Anwendung wird im Peer SDK bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="05049-106">The complete Peer Group Chat sample application is provided in the Peer SDK.</span></span> <span data-ttu-id="05049-107">Dieses Thema verweist auf Funktionen, die im Beispiel bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="05049-107">This topic references functions provided within the sample.</span></span>

 

## <a name="initializing-a-group"></a><span data-ttu-id="05049-108">Initialisieren einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="05049-108">Initializing a Group</span></span>

<span data-ttu-id="05049-109">Der erste Schritt beim Erstellen einer Chatanwendung besteht darin, die Peer Gruppierungs Infrastruktur zu initialisieren, indem [**peergroupstartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) mit der höchsten unterstützten Version aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="05049-109">The first step when constructing a chat application is to initialize the Peer Grouping Infrastructure by calling [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) with the highest supported version.</span></span> <span data-ttu-id="05049-110">In diesem Fall wird die **Peer \_ Gruppen \_ Version** in der Anwendungs Header Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="05049-110">In this case, **PEER\_GROUP\_VERSION** will be defined in the application header file.</span></span> <span data-ttu-id="05049-111">Die von der Infrastruktur tatsächlich unterstützte Version wird in " **Peer Version**" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="05049-111">The version actually supported by the infrastructure is returned in **peerVersion**.</span></span>


```C++
    PEER_VERSION_DATA peerVersion;

    hr = PeerGroupStartup(PEER_GROUP_VERSION, &peerVersion);
    if (FAILED(hr))
    {
        return hr;
    }
```



## <a name="creating-a-group"></a><span data-ttu-id="05049-112">Erstellen einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="05049-112">Creating a Group</span></span>

<span data-ttu-id="05049-113">Eine Chatanwendung muss in der Lage sein, eine Peer Gruppe zu erstellen, wenn keine Gruppe zum beitreten verfügbar ist, oder wenn der Anwendungs Benutzer eine neue erstellen möchte.</span><span class="sxs-lookup"><span data-stu-id="05049-113">A chat application must be able to create a peer group if no group is available to join, or if the application user wants to create a new one.</span></span> <span data-ttu-id="05049-114">Zu diesem Zweck müssen Sie eine Struktur der [**Peer \_ Gruppen \_ Eigenschaften**](/windows/desktop/api/P2P/ns-p2p-peer_group_properties) erstellen und Sie mit den anfänglichen Einstellungen für die Gruppe auffüllen, einschließlich des Klassifizierers für die Peer Gruppe, des anzeigen Amens, des anzeigen Amens und der Anwesenheits Lebensdauer.</span><span class="sxs-lookup"><span data-stu-id="05049-114">To do this, you must create a [**PEER\_GROUP\_PROPERTIES**](/windows/desktop/api/P2P/ns-p2p-peer_group_properties) structure and populate it with the initial settings for the group, including the classifier for the peer group, the friendly name, the creator's peer name, and the presence lifetime.</span></span> <span data-ttu-id="05049-115">Nachdem diese Struktur aufgefüllt wurde, übergeben Sie Sie an " [**Peer groupcreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)".</span><span class="sxs-lookup"><span data-stu-id="05049-115">Once this structure has been populated, you pass it to [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate).</span></span>


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



## <a name="issuing-invitations"></a><span data-ttu-id="05049-116">Ausstellende Einladungen</span><span class="sxs-lookup"><span data-stu-id="05049-116">Issuing Invitations</span></span>

<span data-ttu-id="05049-117">Beim Ausgeben einer Einladung müssen die gmcs der eingeladenen Personen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="05049-117">When issuing an invitation, the GMCs of the invitees must be obtained.</span></span> <span data-ttu-id="05049-118">Diese können durch Aufrufen von " [**Peer Identity tygetxml**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml) " für den einladenden Empfänger mit Ihrem Identitäts Namen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="05049-118">These can obtained by calling [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml) on the invitee with their identity name.</span></span> <span data-ttu-id="05049-119">Bei erfolgreicher Ausführung werden die Identitätsinformationen (der XML-Code, der das Base-64-codierte Zertifikat mit dem öffentlichen RSA-Schlüssel enthält) an einen externen Speicherort (in diesem Beispiel eine Datei) geschrieben, wo der einlader Sie abrufen und zum Erstellen einer Einladung verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="05049-119">If successful, the identity information (the XML that contains the base-64 encoded certificate with the RSA public key) is written to an external location (a file, in this sample) where the inviter can obtain it and use it to create an invitation.</span></span>

<span data-ttu-id="05049-120">An diesem Punkt muss ein Mechanismus für die Übermittlung der Einladung an den einladenden Empfänger eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="05049-120">At this point, a mechanism for the delivery of the invitation to the invitee must be established.</span></span> <span data-ttu-id="05049-121">Dabei kann es sich um eine e-Mail oder eine andere sichere Methode des Datei Austauschs handeln.</span><span class="sxs-lookup"><span data-stu-id="05049-121">This can be email or another secure method of file exchange.</span></span> <span data-ttu-id="05049-122">Im folgenden Beispiel wird die Einladung in eine Datei geschrieben, die dann auf den Computer des einladenden Benutzers übertragen werden kann.</span><span class="sxs-lookup"><span data-stu-id="05049-122">In the sample below, the invitation is written to a file which can then be transferred to the invitee's computer.</span></span>


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



<span data-ttu-id="05049-123">Einladungen, wie Identitäten, werden auch extern ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="05049-123">Invitations, like identities, are also issued externally.</span></span> <span data-ttu-id="05049-124">In diesem Beispiel wird die Einladung in eine Datei mit **fputws** geschrieben, wo Sie vom einladenden Benutzer abgerufen und beim Aufrufen von " [**Peer GroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)" verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="05049-124">In this example, the invitation is written to a file with **fputws** where the invitee can obtain it and use it when it calls [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).</span></span>


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



## <a name="joining-a-peer-group"></a><span data-ttu-id="05049-125">Beitreten zu einer Peer Gruppe</span><span class="sxs-lookup"><span data-stu-id="05049-125">Joining a Peer Group</span></span>

<span data-ttu-id="05049-126">Wenn der Peer versucht, einer Peer Gruppe beizutreten, die von einem anderen Peer erstellt wurde, wird eine Einladung dieses Peers benötigt.</span><span class="sxs-lookup"><span data-stu-id="05049-126">If the peer is attempting to join a peer group created by another peer, it will need an invitation from that peer.</span></span> <span data-ttu-id="05049-127">Einladungen werden von einem externen Prozess oder einer externen Anwendung an den einladenden gesendet und in einer lokalen Datei gespeichert, die im folgenden Beispiel als *pwzfilename* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="05049-127">Invitations are delivered by an external process or application to the invitee and saved to a local file, specified in the sample below as *pwzFileName*.</span></span> <span data-ttu-id="05049-128">Der Einladungs-XML-BLOB wird aus der Datei in **wzeinladungs** gelesen und an " [**Peer GroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)" weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="05049-128">The invitation XML blob is read from the file into **wzInvitation** and passed to [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).</span></span>


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



## <a name="register-for-peer-events"></a><span data-ttu-id="05049-129">Für Peer Ereignisse registrieren</span><span class="sxs-lookup"><span data-stu-id="05049-129">Register for Peer Events</span></span>

<span data-ttu-id="05049-130">Bevor Sie eine Verbindung herstellen, sollten Sie sich für jedes Peer Ereignis registrieren, das für die Anwendung relevant ist.</span><span class="sxs-lookup"><span data-stu-id="05049-130">Before connecting, you should register for every peer event pertinent to the application.</span></span> <span data-ttu-id="05049-131">Im folgenden Beispiel registrieren Sie sich für die folgenden Ereignisse:</span><span class="sxs-lookup"><span data-stu-id="05049-131">In the example below, you register for the following events:</span></span>

-   <span data-ttu-id="05049-132">\_Ereignisdaten Satz der Peer Gruppe wurde \_ \_ \_ geändert.</span><span class="sxs-lookup"><span data-stu-id="05049-132">PEER\_GROUP\_EVENT\_RECORD\_CHANGED.</span></span> <span data-ttu-id="05049-133">Da Datensätze verwendet werden, um öffentliche Chat Nachrichten zu enthalten, muss die Anwendung jedes Mal benachrichtigt werden, wenn eine neue hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="05049-133">Since records will be used to contain public chat messages, the application must be notified every time a new one is added.</span></span> <span data-ttu-id="05049-134">Wenn dieses Peer Ereignis empfangen wird, machen die Ereignisdaten den Datensatz mit der Chat Nachricht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="05049-134">When this peer event is received, the event data exposes the record with the chat message.</span></span> <span data-ttu-id="05049-135">Anwendungen sollten nur für die Daten Satz Typen registriert werden, die direkt verarbeitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="05049-135">Applications should only register for those record types they intend to handle directly.</span></span>
-   <span data-ttu-id="05049-136">Das Peer \_ Gruppen- \_ \_ Ereignismember wurde \_ geändert.</span><span class="sxs-lookup"><span data-stu-id="05049-136">PEER\_GROUP\_EVENT\_MEMBER\_CHANGED.</span></span> <span data-ttu-id="05049-137">Die Anwendung muss benachrichtigt werden, wenn Mitglieder der Peer Gruppe beitreten oder diese verlassen, sodass die Liste der Teilnehmer entsprechend aktualisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="05049-137">The application must be notified when members join or leave the peer group so the list of participants can be updated accordingly.</span></span>
-   <span data-ttu-id="05049-138">der Peer \_ Gruppen- \_ Ereignis Status wurde \_ \_ geändert.</span><span class="sxs-lookup"><span data-stu-id="05049-138">PEER\_GROUP\_EVENT\_STATUS\_CHANGED.</span></span> <span data-ttu-id="05049-139">Änderungen am Peer Gruppenstatus müssen an die Anwendung übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="05049-139">Changes to the peer group status must be conveyed to the application.</span></span> <span data-ttu-id="05049-140">Ein Peer Gruppenmitglied wird nur in der Peer Gruppe als verfügbar betrachtet, wenn sein Status angibt, dass es mit der Gruppe verbunden ist, mit der datensatzdatenbank der Peer Gruppe synchronisiert wird und aktiv auf Daten Satz Aktualisierungen lauscht.</span><span class="sxs-lookup"><span data-stu-id="05049-140">A peer group member is only considered to be available within the peer group when its status indicates that it is connected to the group, synchronized with the peer group record database, and actively listening to record updates.</span></span>
-   <span data-ttu-id="05049-141">\_direkte Peer Gruppen- \_ Ereignis \_ \_ Verbindung.</span><span class="sxs-lookup"><span data-stu-id="05049-141">PEER\_GROUP\_EVENT\_DIRECT\_CONNECTION.</span></span> <span data-ttu-id="05049-142">Private Nachrichten zwischen zwei Mitgliedern und Austauschen von Daten müssen über eine direkte Verbindung durchgeführt werden, sodass die Anwendung direkte Verbindungsanforderungen verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="05049-142">Private messages between two members and exchanges of data must be conducted over a direct connection, so the application must be able to handle direct connection requests.</span></span>
-   <span data-ttu-id="05049-143">\_ \_ eingehende Daten der Peer Gruppen Ereignisse \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="05049-143">PEER\_GROUP\_EVENT\_INCOMING\_DATA.</span></span> <span data-ttu-id="05049-144">Nachdem eine direkte Verbindung initiiert wurde, warnt dieses Peer Ereignis die Anwendung, dass eine private Nachricht empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="05049-144">After a direct connection is initiated, this peer event alerts the application that a private message has been received.</span></span>


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



## <a name="connecting-to-a-peer-group"></a><span data-ttu-id="05049-145">Herstellen einer Verbindung mit einer Peer Gruppe</span><span class="sxs-lookup"><span data-stu-id="05049-145">Connecting to a Peer Group</span></span>

<span data-ttu-id="05049-146">Nachdem Sie die Gruppe erstellt oder verknüpft und für die entsprechenden Ereignisse registriert haben, ist es an der Zeit, Online zu gehen und eine aktive Chatsitzung zu starten.</span><span class="sxs-lookup"><span data-stu-id="05049-146">Having either created or joined the group and registered for the appropriate events, it's time to go online and begin an active chat session.</span></span> <span data-ttu-id="05049-147">Dazu rufen Sie " [**Peer groupconnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) " auf und übergeben das Gruppen handle, das von " [**Peer groupcreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate) " oder " [**Peer-GroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)" abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="05049-147">To do this, you call [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) and pass in the group handle obtained from [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate) or [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).</span></span> <span data-ttu-id="05049-148">Nach dem Aufruf dieser Methode werden Chat Nachrichten als \_ geänderte Ereignisse für Peer Gruppen \_ Ereignis \_ Datensätze empfangen \_ .</span><span class="sxs-lookup"><span data-stu-id="05049-148">After calling this, chat messages will be received as PEER\_GROUP\_EVENT\_RECORD\_CHANGED events.</span></span>

## <a name="obtaining-a-list-of-peer-group-members"></a><span data-ttu-id="05049-149">Abrufen einer Liste von Peer Gruppenmitgliedern</span><span class="sxs-lookup"><span data-stu-id="05049-149">Obtaining a List of Peer Group Members</span></span>

<span data-ttu-id="05049-150">Das Abrufen einer Liste von Membern, die mit der Peer Gruppe verbunden sind, ist einfach: Rufen Sie [**peergroutzenummembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers) auf, um die Liste der Gruppenmitglieder abzurufen, und rufen Sie [**peergetnextitem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) dann iterativ auf, bis alle Elemente abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="05049-150">Obtaining a list of members connected to the peer group is simple: call [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers) to retrieve the list of group members, and then iteratively call [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) until all members are retrieved.</span></span> <span data-ttu-id="05049-151">Sie sollten " [**Peer Service**](/windows/desktop/api/P2P/nf-p2p-peerfreedata) " aufrufen, nachdem Sie die einzelnen Element Strukturen verarbeitet haben, und Sie müssen die Enumeration schließen, indem Sie " [**Peer Enumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) " aufrufen, wenn die Verarbeitung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="05049-151">You should call [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata) after you process each member structure, and you must close the enumeration by calling [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) when processing is complete.</span></span>


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



## <a name="sending-a-chat-message"></a><span data-ttu-id="05049-152">Senden einer Chat Nachricht</span><span class="sxs-lookup"><span data-stu-id="05049-152">Sending a Chat Message</span></span>

<span data-ttu-id="05049-153">In diesem Beispiel wird eine Chat Nachricht gesendet, indem Sie im **Datenfeld** einer [**Peer \_ Daten Satz**](/windows/desktop/api/P2P/ns-p2p-peer_record) Struktur abgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="05049-153">In this example, a chat message is sent by placing it in the **data** field of a [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) structure.</span></span> <span data-ttu-id="05049-154">Der Datensatz wird den Peer Gruppendaten Sätzen hinzugefügt, indem [**peergroupaddrecord**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord)aufgerufen wird, der ihn veröffentlicht und das Änderungs Ereignis des Peer \_ Gruppen \_ Ereignis \_ Datensatzes \_ auf allen Peers, die an der Peer Gruppe teilnehmen, aufhebt.</span><span class="sxs-lookup"><span data-stu-id="05049-154">The record is added to the peer group records by calling [**PeerGroupAddRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord), which will publish it and raise the PEER\_GROUP\_EVENT\_RECORD\_CHANGED event on all peers participating in the peer group.</span></span>


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



## <a name="receiving-a-chat-message"></a><span data-ttu-id="05049-155">Empfangen einer Chat Nachricht</span><span class="sxs-lookup"><span data-stu-id="05049-155">Receiving a Chat Message</span></span>

<span data-ttu-id="05049-156">Um die Chat Nachricht zu empfangen, erstellen Sie eine Rückruffunktion für das Ereignisdaten Satz-Änderungs Ereignis des Peer \_ Gruppen \_ Ereignisses \_ \_ , das eine Funktion ähnlich der folgenden aufruft.</span><span class="sxs-lookup"><span data-stu-id="05049-156">To receive the chat message, create a callback function for the PEER\_GROUP\_EVENT\_RECORD\_CHANGED event that calls a function similar to one below.</span></span> <span data-ttu-id="05049-157">Der Datensatz wird abgerufen, indem für die Ereignisdaten, die von einem vorherigen Aufruf von " [**Peer groupgeteventdata**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) " in der Rückruffunktion empfangen wurden, " [**Peer groupgetrecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) " aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="05049-157">The record is obtained by calling [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) on the event data received by a previous call to [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) in the callback function.</span></span> <span data-ttu-id="05049-158">Die Chat Nachricht wird im **Datenfeld dieses Daten** Satzes gespeichert.</span><span class="sxs-lookup"><span data-stu-id="05049-158">The chat message is stored in the **data** field of this record.</span></span>


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



 

 



