---
description: 'Die Gruppierungs-API verwendet die folgenden Funktionen:'
ms.assetid: 56ea2880-b468-4816-b6c9-5780c807b3f1
title: Gruppieren von API-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17d2970ca68d69b16a32cf7a6d546a5852b07dd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350232"
---
# <a name="grouping-api-functions"></a><span data-ttu-id="065cf-103">Gruppieren von API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="065cf-103">Grouping API Functions</span></span>

<span data-ttu-id="065cf-104">Die Gruppierungs-API verwendet die folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="065cf-104">The Grouping API uses the following functions:</span></span>

## <a name="group-initialization-and-cleanup-functions"></a><span data-ttu-id="065cf-105">Initialisierungs-und Bereinigungs Funktionen für Gruppen</span><span class="sxs-lookup"><span data-stu-id="065cf-105">Group Initialization and Cleanup Functions</span></span>



| <span data-ttu-id="065cf-106">Funktion</span><span class="sxs-lookup"><span data-stu-id="065cf-106">Function</span></span>                                       | <span data-ttu-id="065cf-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="065cf-107">Description</span></span>                                                                                                            |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="065cf-108">**"Peer groupshutdown"**</span><span class="sxs-lookup"><span data-stu-id="065cf-108">**PeerGroupShutdown**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupshutdown) | <span data-ttu-id="065cf-109">Schließt eine Peer Gruppe, die mit [**peergroupstartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) erstellt wurde, und gibt alle zugeordneten Ressourcen frei.</span><span class="sxs-lookup"><span data-stu-id="065cf-109">Closes a peer group created with [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) and disposes of any allocated resources.</span></span> |
| [<span data-ttu-id="065cf-110">**Peer groupstartup**</span><span class="sxs-lookup"><span data-stu-id="065cf-110">**PeerGroupStartup**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupstartup)   | <span data-ttu-id="065cf-111">Initiiert eine Peer Gruppe mithilfe einer angeforderten Version der Peer Infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="065cf-111">Initiates a peer group by using a requested version of the Peer infrastructure.</span></span>                                        |



 

## <a name="group-creation-and-access-functions"></a><span data-ttu-id="065cf-112">Gruppen Erstellungs-und Zugriffs Funktionen</span><span class="sxs-lookup"><span data-stu-id="065cf-112">Group Creation and Access Functions</span></span>



| <span data-ttu-id="065cf-113">Funktion</span><span class="sxs-lookup"><span data-stu-id="065cf-113">Function</span></span>                                                                       | <span data-ttu-id="065cf-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="065cf-114">Description</span></span>                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="065cf-115">**"Peer groupclose"**</span><span class="sxs-lookup"><span data-stu-id="065cf-115">**PeerGroupClose**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupclose)                                       | <span data-ttu-id="065cf-116">Erklärt das Peer Gruppen Handle für ungültig, das durch einen vorherigen Aufrufen der [**peergroupcreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)-, [**peergroupjoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)-oder [**peergroupopen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) -Funktion abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="065cf-116">Invalidates the peer group handle obtained by a previous call to the [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate), [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin), or [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) function.</span></span> |
| [<span data-ttu-id="065cf-117">**Peer groupconnect**</span><span class="sxs-lookup"><span data-stu-id="065cf-117">**PeerGroupConnect**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)                                   | <span data-ttu-id="065cf-118">Initiiert eine PNRP-Suche für eine Peer Gruppe und versucht, eine Verbindung damit herzustellen.</span><span class="sxs-lookup"><span data-stu-id="065cf-118">Initiates a PNRP search for a peer group and attempts to connect to it.</span></span> <span data-ttu-id="065cf-119">Nachdem diese Funktion erfolgreich aufgerufen wurde, kann ein Peer mit anderen Mitgliedern der Peer Gruppe kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="065cf-119">After this function is called successfully, a peer can communicate with other members of the peer group.</span></span>                             |
| [<span data-ttu-id="065cf-120">**"Peer groupconnectbyaddress"**</span><span class="sxs-lookup"><span data-stu-id="065cf-120">**PeerGroupConnectByAddress**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupconnectbyaddress)                 | <span data-ttu-id="065cf-121">Versucht, eine Verbindung mit der Peer Gruppe herzustellen, an der andere Peers mit bekannten IPv6-Adressen teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="065cf-121">Attempts to connect to the peer group that other peers with known IPv6 addresses are participating in.</span></span>                                                                                                       |
| [<span data-ttu-id="065cf-122">**Peer groupcreate**</span><span class="sxs-lookup"><span data-stu-id="065cf-122">**PeerGroupCreate**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)                                     | <span data-ttu-id="065cf-123">Erstellt eine neue Peer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="065cf-123">Creates a new peer group.</span></span>                                                                                                                                                                                    |
| [<span data-ttu-id="065cf-124">**"Peer groupkreateinvitation"**</span><span class="sxs-lookup"><span data-stu-id="065cf-124">**PeerGroupCreateInvitation**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation)                 | <span data-ttu-id="065cf-125">Gibt eine XML-Zeichenfolge zurück, die vom angegebenen Peer zum beitreten zu einer Gruppe verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="065cf-125">Returns an XML string that can be used by the specified peer to join a group.</span></span>                                                                                                                                |
| [<span data-ttu-id="065cf-126">**Peer groupkreatepasswordinvitation**</span><span class="sxs-lookup"><span data-stu-id="065cf-126">**PeerGroupCreatePasswordInvitation**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupcreatepasswordinvitation) | <span data-ttu-id="065cf-127">Gibt eine XML-Zeichenfolge zurück, die vom angegebenen Peer verwendet werden kann, um eine Gruppe mit einem übereinstimmenden Kennwort zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="065cf-127">Returns an XML string that can be used by the specified peer to join a group with a matching password.</span></span>                                                                                                       |
| [<span data-ttu-id="065cf-128">**"Peer groupdelete"**</span><span class="sxs-lookup"><span data-stu-id="065cf-128">**PeerGroupDelete**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupdelete)                                     | <span data-ttu-id="065cf-129">Löscht die lokalen Daten und das Zertifikat, die einer Peer Gruppe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="065cf-129">Deletes the local data and certificate associated with a peer group.</span></span>                                                                                                                                         |
| [<span data-ttu-id="065cf-130">**Peergroupgetstatus**</span><span class="sxs-lookup"><span data-stu-id="065cf-130">**PeerGroupGetStatus**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupgetstatus)                               | <span data-ttu-id="065cf-131">Ruft den aktuellen Status einer Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="065cf-131">Retrieves the current status of a group.</span></span>                                                                                                                                                                     |
| [<span data-ttu-id="065cf-132">**Peer groupissuecredenseins**</span><span class="sxs-lookup"><span data-stu-id="065cf-132">**PeerGroupIssueCredentials**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)                 | <span data-ttu-id="065cf-133">Gibt Anmelde Informationen, einschließlich einer GMC, für eine bestimmte Identität aus und gibt optional eine Einladungs-XML-Zeichenfolge zurück, mit der der eingeladene Peer einer Peer Gruppe beitreten kann.</span><span class="sxs-lookup"><span data-stu-id="065cf-133">Issues credentials, including a GMC, to a specific identity, and optionally returns an invitation XML string the invited peer can use to join a peer group.</span></span>                                                  |
| [<span data-ttu-id="065cf-134">**Peer GroupJoin**</span><span class="sxs-lookup"><span data-stu-id="065cf-134">**PeerGroupJoin**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)                                         | <span data-ttu-id="065cf-135">Ermöglicht einem Peer mit einer Einladung, einer vorhandenen Peer Gruppe beizutreten.</span><span class="sxs-lookup"><span data-stu-id="065cf-135">Allows a peer with an invitation to join an existing peer group.</span></span>                                                                                                                                             |
| [<span data-ttu-id="065cf-136">**Peer groupopen**</span><span class="sxs-lookup"><span data-stu-id="065cf-136">**PeerGroupOpen**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupopen)                                         | <span data-ttu-id="065cf-137">Öffnet eine Peer Gruppe, die ein Peer erstellt oder verknüpft hat.</span><span class="sxs-lookup"><span data-stu-id="065cf-137">Opens a peer group that a peer has created or joined.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="065cf-138">**"Peer groupparamevitation"**</span><span class="sxs-lookup"><span data-stu-id="065cf-138">**PeerGroupParseInvitation**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupparseinvitation)                   | <span data-ttu-id="065cf-139">Gibt eine [**Peer \_ Einladungs \_ Informations**](/windows/desktop/api/P2P/ns-p2p-peer_invitation_info) Struktur mit den Details einer bestimmten Einladung zurück.</span><span class="sxs-lookup"><span data-stu-id="065cf-139">Returns a [**PEER\_INVITATION\_INFO**](/windows/desktop/api/P2P/ns-p2p-peer_invitation_info) structure with the details of a specific invitation.</span></span>                                                                                        |
| [<span data-ttu-id="065cf-140">**Peer-grouppasswordjoin**</span><span class="sxs-lookup"><span data-stu-id="065cf-140">**PeerGroupPasswordJoin**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergrouppasswordjoin)                         | <span data-ttu-id="065cf-141">Ermöglicht einem Peer mit einer Einladung und dem richtigen Kennwort, um einer Kenn Wort geschützten Peer Gruppe beizutreten.</span><span class="sxs-lookup"><span data-stu-id="065cf-141">Allows a peer with an invitation and the correct password to join a password-protected peer group.</span></span>                                                                                                           |



 

## <a name="group-and-member-information-functions"></a><span data-ttu-id="065cf-142">Gruppen-und Element Informationsfunktionen</span><span class="sxs-lookup"><span data-stu-id="065cf-142">Group and Member Information Functions</span></span>



| <span data-ttu-id="065cf-143">Funktion</span><span class="sxs-lookup"><span data-stu-id="065cf-143">Function</span></span>                                                 | <span data-ttu-id="065cf-144">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="065cf-144">Description</span></span>                                                                                                                        |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="065cf-145">**"Peer groupenummembers"**</span><span class="sxs-lookup"><span data-stu-id="065cf-145">**PeerGroupEnumMembers**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers)     | <span data-ttu-id="065cf-146">Erstellt eine Enumeration der verfügbaren Peer Gruppenmitglieder und der zugehörigen Mitgliedschafts Informationen.</span><span class="sxs-lookup"><span data-stu-id="065cf-146">Creates an enumeration of available peer group members and the associated membership information.</span></span>                                  |
| [<span data-ttu-id="065cf-147">**"Peer groupgetproperties"**</span><span class="sxs-lookup"><span data-stu-id="065cf-147">**PeerGroupGetProperties**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupgetproperties) | <span data-ttu-id="065cf-148">Ruft Informationen zu den Eigenschaften einer angegebenen Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="065cf-148">Retrieves information on the properties of a specified group.</span></span>                                                                      |
| [<span data-ttu-id="065cf-149">**"Peer groupsetproperties"**</span><span class="sxs-lookup"><span data-stu-id="065cf-149">**PeerGroupSetProperties**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupsetproperties) | <span data-ttu-id="065cf-150">Legt die aktuellen Peer Gruppen Eigenschaften fest.</span><span class="sxs-lookup"><span data-stu-id="065cf-150">Sets the current peer group properties.</span></span> <span data-ttu-id="065cf-151">In Version 1,0 dieser API kann dieser Vorgang nur vom Ersteller der Peer Gruppe durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="065cf-151">In version 1.0 of this API, only the creator of the peer group can perform this operation.</span></span> |



 

## <a name="records-and-record-management-functions"></a><span data-ttu-id="065cf-152">Datensätze und Daten Satz Verwaltungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="065cf-152">Records and Record Management Functions</span></span>



| <span data-ttu-id="065cf-153">Funktion</span><span class="sxs-lookup"><span data-stu-id="065cf-153">Function</span></span>                                                 | <span data-ttu-id="065cf-154">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="065cf-154">Description</span></span>                                                                          |
|----------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="065cf-155">**"Peer groupaddrecord"**</span><span class="sxs-lookup"><span data-stu-id="065cf-155">**PeerGroupAddRecord**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord)         | <span data-ttu-id="065cf-156">Fügt der Peer Gruppe einen neuen Datensatz hinzu, der an alle teilnehmenden Peers weitergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="065cf-156">Adds a new record to the peer group, which is propagated to all participating peers.</span></span> |
| [<span data-ttu-id="065cf-157">**Peer groupdeleterecord**</span><span class="sxs-lookup"><span data-stu-id="065cf-157">**PeerGroupDeleteRecord**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupdeleterecord)   | <span data-ttu-id="065cf-158">Löscht einen Datensatz aus einer Peer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="065cf-158">Deletes a record from a peer group.</span></span> <span data-ttu-id="065cf-159">Nur der Ersteller eines Datensatzes kann ihn löschen.</span><span class="sxs-lookup"><span data-stu-id="065cf-159">Only the creator of a record can delete it.</span></span>      |
| [<span data-ttu-id="065cf-160">**Peer groupumschlag**</span><span class="sxs-lookup"><span data-stu-id="065cf-160">**PeerGroupEnumRecords**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupenumrecords)     | <span data-ttu-id="065cf-161">Erstellt eine Enumeration von Peer Gruppen-Datensätzen.</span><span class="sxs-lookup"><span data-stu-id="065cf-161">Creates an enumeration of peer group records.</span></span>                                        |
| [<span data-ttu-id="065cf-162">**"Peer groupgetrecord"**</span><span class="sxs-lookup"><span data-stu-id="065cf-162">**PeerGroupGetRecord**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord)         | <span data-ttu-id="065cf-163">Ruft einen bestimmten Gruppendaten Satz ab.</span><span class="sxs-lookup"><span data-stu-id="065cf-163">Retrieves a specific group record.</span></span>                                                   |
| [<span data-ttu-id="065cf-164">**"Peer groupsearchrecords"**</span><span class="sxs-lookup"><span data-stu-id="065cf-164">**PeerGroupSearchRecords**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) | <span data-ttu-id="065cf-165">Durchsucht die lokale Peer Gruppen Datenbank nach Datensätzen, die den angegebenen Kriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="065cf-165">Searches the local peer group database for records that match the supplied criteria.</span></span> |
| [<span data-ttu-id="065cf-166">**Peer-groupupdaterecord**</span><span class="sxs-lookup"><span data-stu-id="065cf-166">**PeerGroupUpdateRecord**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupupdaterecord)   | <span data-ttu-id="065cf-167">Aktualisiert einen Datensatz innerhalb einer bestimmten Peer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="065cf-167">Updates a record within a specific peer group.</span></span>                                       |



 

## <a name="group-database-importexport-functions"></a><span data-ttu-id="065cf-168">Importieren/Exportieren von Datenbankfunktionen</span><span class="sxs-lookup"><span data-stu-id="065cf-168">Group Database Import/Export Functions</span></span>



| <span data-ttu-id="065cf-169">Funktion</span><span class="sxs-lookup"><span data-stu-id="065cf-169">Function</span></span>                                                   | <span data-ttu-id="065cf-170">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="065cf-170">Description</span></span>                                                                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="065cf-171">**"Peer groupexportdatabase"**</span><span class="sxs-lookup"><span data-stu-id="065cf-171">**PeerGroupExportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase) | <span data-ttu-id="065cf-172">Exportiert eine Peer Gruppen Datenbank in eine bestimmte Datei, die auf einen anderen Computer übertragen und mit der [**peergroupimportdatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase) -Funktion importiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="065cf-172">Exports a peer group database to a specific file, which can be transported to another computer and imported with the [**PeerGroupImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase) function.</span></span> |
| [<span data-ttu-id="065cf-173">**"Peer groupimportdatabase"**</span><span class="sxs-lookup"><span data-stu-id="065cf-173">**PeerGroupImportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase) | <span data-ttu-id="065cf-174">Importiert eine Peer Gruppen Datenbank aus einer lokalen Datei.</span><span class="sxs-lookup"><span data-stu-id="065cf-174">Imports a peer group database from a local file.</span></span>                                                                                                                                          |



 

## <a name="direct-connection-functions"></a><span data-ttu-id="065cf-175">Direkte Verbindungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="065cf-175">Direct Connection Functions</span></span>



| <span data-ttu-id="065cf-176">Funktion</span><span class="sxs-lookup"><span data-stu-id="065cf-176">Function</span></span>                                                                 | <span data-ttu-id="065cf-177">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="065cf-177">Description</span></span>                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="065cf-178">**"Peer groupclosedirectconnection"**</span><span class="sxs-lookup"><span data-stu-id="065cf-178">**PeerGroupCloseDirectConnection**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) | <span data-ttu-id="065cf-179">Schließt eine bestimmte direkte Verbindung zwischen zwei Peers.</span><span class="sxs-lookup"><span data-stu-id="065cf-179">Closes a specific direct connection between two peers.</span></span>              |
| [<span data-ttu-id="065cf-180">**Peergroupumschlag-Verbindungen**</span><span class="sxs-lookup"><span data-stu-id="065cf-180">**PeerGroupEnumConnections**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupenumconnections)             | <span data-ttu-id="065cf-181">Erstellt eine Enumeration der derzeit auf dem Peer aktiven Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="065cf-181">Creates an enumeration of connections currently active on the peer.</span></span> |
| [<span data-ttu-id="065cf-182">**"Peer groupopendirectconnection"**</span><span class="sxs-lookup"><span data-stu-id="065cf-182">**PeerGroupOpenDirectConnection**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection)   | <span data-ttu-id="065cf-183">Stellt eine direkte Verbindung mit einem anderen Peer in einer Peer Gruppe her.</span><span class="sxs-lookup"><span data-stu-id="065cf-183">Establishes a direct connection with another peer in a peer group.</span></span>  |
| [<span data-ttu-id="065cf-184">**"Peer Group"-Daten**</span><span class="sxs-lookup"><span data-stu-id="065cf-184">**PeerGroupSendData**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata)                           | <span data-ttu-id="065cf-185">Sendet Daten über eine Nachbar-oder direkte Verbindung an einen Member.</span><span class="sxs-lookup"><span data-stu-id="065cf-185">Sends data to a member over a neighbor or direct connection.</span></span>        |



 

## <a name="group-events-infrastructure"></a><span data-ttu-id="065cf-186">Infrastruktur für Gruppen Ereignisse</span><span class="sxs-lookup"><span data-stu-id="065cf-186">Group Events Infrastructure</span></span>



| <span data-ttu-id="065cf-187">Funktion</span><span class="sxs-lookup"><span data-stu-id="065cf-187">Function</span></span>                                                     | <span data-ttu-id="065cf-188">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="065cf-188">Description</span></span>                                                                                    |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="065cf-189">**"Peer groupgeteventdata"**</span><span class="sxs-lookup"><span data-stu-id="065cf-189">**PeerGroupGetEventData**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)       | <span data-ttu-id="065cf-190">Ermöglicht einer Anwendung das Abrufen der Daten, die von einem Gruppierungs Ereignis zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="065cf-190">Allows an application to retrieve the data returned by a grouping event.</span></span>                       |
| [<span data-ttu-id="065cf-191">**"Peer-groupregisterevent"**</span><span class="sxs-lookup"><span data-stu-id="065cf-191">**PeerGroupRegisterEvent**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent)     | <span data-ttu-id="065cf-192">Registriert einen Peer für bestimmte Peer Gruppen Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="065cf-192">Registers a peer for specific peer group events.</span></span>                                               |
| [<span data-ttu-id="065cf-193">**"Peer Register Event"**</span><span class="sxs-lookup"><span data-stu-id="065cf-193">**PeerGroupUnregisterEvent**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupunregisterevent) | <span data-ttu-id="065cf-194">Hebt die Registrierung eines Peers von der Benachrichtigung über Peer Ereignisse auf, die dem angegebenen Ereignis Handle zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="065cf-194">Unregisters a peer from notification of peer events associated with the supplied event handle.</span></span> |



 

## <a name="group-time-conversion-functions"></a><span data-ttu-id="065cf-195">Gruppen Zeit Konvertierungs Funktionen</span><span class="sxs-lookup"><span data-stu-id="065cf-195">Group Time Conversion Functions</span></span>



| <span data-ttu-id="065cf-196">Funktion</span><span class="sxs-lookup"><span data-stu-id="065cf-196">Function</span></span>                                                                     | <span data-ttu-id="065cf-197">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="065cf-197">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="065cf-198">**"Peer grouppeer Timeto universaltime"**</span><span class="sxs-lookup"><span data-stu-id="065cf-198">**PeerGroupPeerTimeToUniversalTime**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergrouppeertimetouniversaltime) | <span data-ttu-id="065cf-199">Konvertiert den von der Peer Gruppe verwalteten Verweis Zeitwert in einen lokalisierten Uhrzeitwert, der für die Anzeige auf einem Peer Computer geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="065cf-199">Converts the peer group-maintained reference time value to a localized time value appropriate for display on a peer computer.</span></span> |
| [<span data-ttu-id="065cf-200">**"Peer groupuniversaltimetopeertime"**</span><span class="sxs-lookup"><span data-stu-id="065cf-200">**PeerGroupUniversalTimeToPeerTime**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupuniversaltimetopeertime) | <span data-ttu-id="065cf-201">Konvertiert einen lokalen Uhrzeitwert vom Computer eines Peers in einen gemeinsamen Peer Gruppen-Uhrzeitwert.</span><span class="sxs-lookup"><span data-stu-id="065cf-201">Converts a local time value from a peer's computer to a common peer group time value.</span></span>                                         |



 

## <a name="group-configuration-functions"></a><span data-ttu-id="065cf-202">Gruppen Konfigurationsfunktionen</span><span class="sxs-lookup"><span data-stu-id="065cf-202">Group Configuration Functions</span></span>



| <span data-ttu-id="065cf-203">Funktion</span><span class="sxs-lookup"><span data-stu-id="065cf-203">Function</span></span>                                               | <span data-ttu-id="065cf-204">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="065cf-204">Description</span></span>                                                                                                                       |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="065cf-205">**"Peer groupexportconfig"**</span><span class="sxs-lookup"><span data-stu-id="065cf-205">**PeerGroupExportConfig**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig) | <span data-ttu-id="065cf-206">Exportiert die Gruppenkonfiguration für einen Peer als XML-Zeichenfolge, die die Identität, den Gruppennamen und die GMC für die Identität enthält.</span><span class="sxs-lookup"><span data-stu-id="065cf-206">Exports the group configuration for a peer as an XML string that contains the identity, group name, and the GMC for the identity.</span></span> |
| [<span data-ttu-id="065cf-207">**"Peer groupimportconfig"**</span><span class="sxs-lookup"><span data-stu-id="065cf-207">**PeerGroupImportConfig**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) | <span data-ttu-id="065cf-208">Importiert eine Peer Gruppenkonfiguration für eine Identität basierend auf den spezifischen Einstellungen in einer angegebenen XML-Konfigurations Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="065cf-208">Imports a peer group configuration for an identity based on the specific settings in a supplied XML configuration string.</span></span>         |



 

 

 



