---
description: Beschreibt die Anmelde Sitzung oder Sitzungen, die einem Benutzer zugeordnet sind, der bei einem Computersystem mit Windows angemeldet ist.
ms.assetid: d09a115b-95a3-47c7-a04d-c810d044ccc8
ms.tgt_platform: multiple
title: Win32_LogonSession-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogonSession
- Win32_LogonSession.Caption
- Win32_LogonSession.Description
- Win32_LogonSession.InstallDate
- Win32_LogonSession.Name
- Win32_LogonSession.Status
- Win32_LogonSession.StartTime
- Win32_LogonSession.AuthenticationPackage
- Win32_LogonSession.LogonId
- Win32_LogonSession.LogonType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 78e14bbd41c2fd8bb0c10a7bfeeda0dc9d426b0f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747984"
---
# <a name="win32_logonsession-class"></a><span data-ttu-id="c5197-103">Win32 \_ logonsession-Klasse</span><span class="sxs-lookup"><span data-stu-id="c5197-103">Win32\_LogonSession class</span></span>

<span data-ttu-id="c5197-104">Die WMI-Klasse der **Win32- \_ logonsession** (siehe [Abrufen einer WMI-Klasse](/windows/desktop/wmisdk/retrieving-a-class)) beschreibt die Anmelde Sitzung oder die Sitzungen, die einem Benutzer zugeordnet sind, der bei einem Computersystem mit Windows angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="c5197-104">The **Win32\_LogonSession** WMI class (see [Retrieving a WMI class](/windows/desktop/wmisdk/retrieving-a-class)) describes the logon session or sessions associated with a user logged on to a computer system running Windows.</span></span>

<span data-ttu-id="c5197-105">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c5197-105">The following syntax is simplified from Managed Object Format (MOF) code, and includes all of the inherited properties.</span></span> <span data-ttu-id="c5197-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="c5197-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5197-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5197-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{9083C21E-7D58-4e0e-BC30-0BC8922AFB8B}"), AMENDMENT]
class Win32_LogonSession : Win32_Session
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime StartTime;
  string   AuthenticationPackage;
  string   LogonId;
  uint32   LogonType;
};
```

## <a name="members"></a><span data-ttu-id="c5197-108">Member</span><span class="sxs-lookup"><span data-stu-id="c5197-108">Members</span></span>

<span data-ttu-id="c5197-109">Die **Win32 \_ logonsession** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c5197-109">The **Win32\_LogonSession** class has these types of members:</span></span>

-   [<span data-ttu-id="c5197-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c5197-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c5197-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c5197-111">Properties</span></span>

<span data-ttu-id="c5197-112">Die **Win32 \_ logonsession** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c5197-112">The **Win32\_LogonSession** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c5197-113">**AuthenticationPackage**</span><span class="sxs-lookup"><span data-stu-id="c5197-113">**AuthenticationPackage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5197-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c5197-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5197-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c5197-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5197-116">Der Name des Subsystems, das zum Authentifizieren der Anmelde Sitzung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c5197-116">Name of the subsystem used to authenticate the logon session.</span></span>

</dd> <dt>

<span data-ttu-id="c5197-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c5197-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5197-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c5197-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5197-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c5197-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5197-120">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c5197-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c5197-121">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c5197-121">A short textual description of the object.</span></span>

<span data-ttu-id="c5197-122">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c5197-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5197-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c5197-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5197-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c5197-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5197-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c5197-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5197-126">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="c5197-126">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c5197-127">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c5197-127">A textual description of the object.</span></span>

<span data-ttu-id="c5197-128">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c5197-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5197-129">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c5197-129">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5197-130">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="c5197-130">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c5197-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c5197-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5197-132">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="c5197-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c5197-133">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c5197-133">Indicates when the object was installed.</span></span> <span data-ttu-id="c5197-134">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="c5197-134">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="c5197-135">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c5197-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5197-136">**Anmelde-ID**</span><span class="sxs-lookup"><span data-stu-id="c5197-136">**LogonId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5197-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c5197-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5197-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c5197-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5197-139">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c5197-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c5197-140">Die der Anmelde Sitzung zugewiesene ID.</span><span class="sxs-lookup"><span data-stu-id="c5197-140">ID assigned to the logon session.</span></span>

</dd> <dt>

<span data-ttu-id="c5197-141">**LogonType**</span><span class="sxs-lookup"><span data-stu-id="c5197-141">**LogonType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5197-142">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c5197-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c5197-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c5197-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5197-144">Numerischer Wert, der den Typ der Anmelde Sitzung angibt.</span><span class="sxs-lookup"><span data-stu-id="c5197-144">Numeric value that indicates the type of logon session.</span></span>

<dt>

<span data-ttu-id="c5197-145">0</span><span class="sxs-lookup"><span data-stu-id="c5197-145">0</span></span>
</dt> <dd>

<span data-ttu-id="c5197-146">Wird nur vom System Konto verwendet.</span><span class="sxs-lookup"><span data-stu-id="c5197-146">Used only by the System account.</span></span>

</dd> <dt>

<span id="Interactive"></span><span id="interactive"></span><span id="INTERACTIVE"></span>

<span data-ttu-id="c5197-147"><span id="Interactive"></span><span id="interactive"></span><span id="INTERACTIVE"></span>**Interaktiv** (2)</span><span class="sxs-lookup"><span data-stu-id="c5197-147"><span id="Interactive"></span><span id="interactive"></span><span id="INTERACTIVE"></span>**Interactive** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c5197-148">Gedacht für Benutzer, die den Computer interaktiv verwenden, z. b. ein Benutzer, der von einem Terminal Server, einer Remoteshell oder einem ähnlichen Prozess angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="c5197-148">Intended for users who are interactively using the machine, such as a user being logged on by a terminal server, remote shell, or similar process.</span></span>

</dd> <dt>

<span id="Network"></span><span id="network"></span><span id="NETWORK"></span>

<span data-ttu-id="c5197-149"><span id="Network"></span><span id="network"></span><span id="NETWORK"></span>**Netzwerk** (3)</span><span class="sxs-lookup"><span data-stu-id="c5197-149"><span id="Network"></span><span id="network"></span><span id="NETWORK"></span>**Network** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c5197-150">Ist für Hochleistungsserver zum Authentifizieren von Klartext-Kenn Wörtern vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="c5197-150">Intended for high-performance servers to authenticate clear text passwords.</span></span> <span data-ttu-id="c5197-151">LogonUser speichert die Anmelde Informationen für diesen Anmeldetyp nicht zwischen.</span><span class="sxs-lookup"><span data-stu-id="c5197-151">LogonUser does not cache credentials for this logon type.</span></span>

</dd> <dt>

<span id="Batch"></span><span id="batch"></span><span id="BATCH"></span>

<span data-ttu-id="c5197-152"><span id="Batch"></span><span id="batch"></span><span id="BATCH"></span>**Batch** (4)</span><span class="sxs-lookup"><span data-stu-id="c5197-152"><span id="Batch"></span><span id="batch"></span><span id="BATCH"></span>**Batch** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c5197-153">Gedacht für Batch Server, bei denen Prozesse im Auftrag eines Benutzers ohne direkten Eingriff ausgeführt werden können. oder für Server mit höherer Leistung, die viele Clear-Text-Authentifizierungs Versuche gleichzeitig verarbeiten, z. b. e-Mail-oder Webserver.</span><span class="sxs-lookup"><span data-stu-id="c5197-153">Intended for batch servers, where processes can be executed on behalf of a user without their direct intervention; or for higher performance servers that process many clear-text authentication attempts at a time, such as mail or web servers.</span></span> <span data-ttu-id="c5197-154">LogonUser speichert die Anmelde Informationen für diesen Anmeldetyp nicht zwischen.</span><span class="sxs-lookup"><span data-stu-id="c5197-154">LogonUser does not cache credentials for this logon type.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c5197-155"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Dienst** (5)</span><span class="sxs-lookup"><span data-stu-id="c5197-155"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c5197-156">Gibt die Anmeldung eines Dienst Typs an.</span><span class="sxs-lookup"><span data-stu-id="c5197-156">Indicates a service-type logon.</span></span> <span data-ttu-id="c5197-157">Für das angegebene Konto muss die Dienst Berechtigung aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="c5197-157">The account provided must have the service privilege enabled.</span></span>

</dd> <dt>

<span id="Proxy"></span><span id="proxy"></span><span id="PROXY"></span>

<span data-ttu-id="c5197-158"><span id="Proxy"></span><span id="proxy"></span><span id="PROXY"></span>**Proxy** (6)</span><span class="sxs-lookup"><span data-stu-id="c5197-158"><span id="Proxy"></span><span id="proxy"></span><span id="PROXY"></span>**Proxy** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c5197-159">Gibt eine Proxy-Typ-Anmeldung an.</span><span class="sxs-lookup"><span data-stu-id="c5197-159">Indicates a proxy-type logon.</span></span>

</dd> <dt>

<span id="Unlock"></span><span id="unlock"></span><span id="UNLOCK"></span>

<span data-ttu-id="c5197-160"><span id="Unlock"></span><span id="unlock"></span><span id="UNLOCK"></span>**Entsperren** (7)</span><span class="sxs-lookup"><span data-stu-id="c5197-160"><span id="Unlock"></span><span id="unlock"></span><span id="UNLOCK"></span>**Unlock** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c5197-161">Dieser Anmeldetyp ist für die Gina-DLLs-Protokollierung bei Benutzern vorgesehen, die den Computer interaktiv verwenden.</span><span class="sxs-lookup"><span data-stu-id="c5197-161">This logon type is intended for GINA DLLs logging on users who are interactively using the machine.</span></span> <span data-ttu-id="c5197-162">Dieser Anmeldetyp ermöglicht das Generieren eines eindeutigen Überwachungsdaten Satzes, der anzeigt, wann die Arbeitsstation entsperrt wurde.</span><span class="sxs-lookup"><span data-stu-id="c5197-162">This logon type allows a unique audit record to be generated that shows when the workstation was unlocked.</span></span>

</dd> <dt>

<span id="NetworkCleartext"></span><span id="networkcleartext"></span><span id="NETWORKCLEARTEXT"></span>

<span data-ttu-id="c5197-163"><span id="NetworkCleartext"></span><span id="networkcleartext"></span><span id="NETWORKCLEARTEXT"></span>**Network cleartext** (8)</span><span class="sxs-lookup"><span data-stu-id="c5197-163"><span id="NetworkCleartext"></span><span id="networkcleartext"></span><span id="NETWORKCLEARTEXT"></span>**NetworkCleartext** (8)</span></span>


</dt> <dd>

<span data-ttu-id="c5197-164">Behält den Namen und das Kennwort in den Authentifizierungs Paketen bei und ermöglicht dem Server das Herstellen von Verbindungen mit anderen Netzwerkservern, während die Identität des Clients angenommen wird.</span><span class="sxs-lookup"><span data-stu-id="c5197-164">Preserves the name and password in the authentication packages, allowing the server to make connections to other network servers while impersonating the client.</span></span> <span data-ttu-id="c5197-165">Dadurch kann ein Server Klartext-Anmelde Informationen von einem Client akzeptieren, LogonUser aufrufen, überprüfen, ob der Benutzer über das Netzwerk auf das System zugreifen kann und trotzdem mit anderen Servern kommunizieren kann.</span><span class="sxs-lookup"><span data-stu-id="c5197-165">This allows a server to accept clear text credentials from a client, call LogonUser, verify that the user can access the system across the network, and still communicate with other servers.</span></span>

</dd> <dt>

<span id="NewCredentials"></span><span id="newcredentials"></span><span id="NEWCREDENTIALS"></span>

<span data-ttu-id="c5197-166"><span id="NewCredentials"></span><span id="newcredentials"></span><span id="NEWCREDENTIALS"></span>**Neuanmelde** Informationen (9)</span><span class="sxs-lookup"><span data-stu-id="c5197-166"><span id="NewCredentials"></span><span id="newcredentials"></span><span id="NEWCREDENTIALS"></span>**NewCredentials** (9)</span></span>


</dt> <dd>

<span data-ttu-id="c5197-167">Ermöglicht dem Aufrufer das Klonen seines aktuellen Tokens und das Angeben neuer Anmelde Informationen für ausgehende Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="c5197-167">Allows the caller to clone its current token and specify new credentials for outbound connections.</span></span> <span data-ttu-id="c5197-168">Die neue Anmelde Sitzung hat dieselbe lokale Identifizierung, verwendet jedoch andere Anmelde Informationen für andere Netzwerkverbindungen.</span><span class="sxs-lookup"><span data-stu-id="c5197-168">The new logon session has the same local identify, but uses different credentials for other network connections.</span></span>

</dd> <dt>

<span id="RemoteInteractive"></span><span id="remoteinteractive"></span><span id="REMOTEINTERACTIVE"></span>

<span data-ttu-id="c5197-169"><span id="RemoteInteractive"></span><span id="remoteinteractive"></span><span id="REMOTEINTERACTIVE"></span>**Remoteinteractive** (10)</span><span class="sxs-lookup"><span data-stu-id="c5197-169"><span id="RemoteInteractive"></span><span id="remoteinteractive"></span><span id="REMOTEINTERACTIVE"></span>**RemoteInteractive** (10)</span></span>


</dt> <dd>

<span data-ttu-id="c5197-170">Terminal Dienste-Sitzung, die sowohl Remote als auch interaktiv ist.</span><span class="sxs-lookup"><span data-stu-id="c5197-170">Terminal Services session that is both remote and interactive.</span></span>

</dd> <dt>

<span id="CachedInteractive"></span><span id="cachedinteractive"></span><span id="CACHEDINTERACTIVE"></span>

<span data-ttu-id="c5197-171"><span id="CachedInteractive"></span><span id="cachedinteractive"></span><span id="CACHEDINTERACTIVE"></span>**Cachedinteractive** (11)</span><span class="sxs-lookup"><span data-stu-id="c5197-171"><span id="CachedInteractive"></span><span id="cachedinteractive"></span><span id="CACHEDINTERACTIVE"></span>**CachedInteractive** (11)</span></span>


</dt> <dd>

<span data-ttu-id="c5197-172">Versuchen Sie zwischengespeicherte Anmelde Informationen ohne Zugriff auf das Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="c5197-172">Attempt cached credentials without accessing the network.</span></span>

</dd> <dt>

<span id="CachedRemoteInteractive"></span><span id="cachedremoteinteractive"></span><span id="CACHEDREMOTEINTERACTIVE"></span>

<span data-ttu-id="c5197-173"><span id="CachedRemoteInteractive"></span><span id="cachedremoteinteractive"></span><span id="CACHEDREMOTEINTERACTIVE"></span>**Cachedremuteinteractive** (12)</span><span class="sxs-lookup"><span data-stu-id="c5197-173"><span id="CachedRemoteInteractive"></span><span id="cachedremoteinteractive"></span><span id="CACHEDREMOTEINTERACTIVE"></span>**CachedRemoteInteractive** (12)</span></span>


</dt> <dd>

<span data-ttu-id="c5197-174">Identisch mit remoteinteractive.</span><span class="sxs-lookup"><span data-stu-id="c5197-174">Same as RemoteInteractive.</span></span> <span data-ttu-id="c5197-175">Diese wird für die interne Überwachung verwendet.</span><span class="sxs-lookup"><span data-stu-id="c5197-175">This is used for internal auditing.</span></span>

</dd> <dt>

<span id="CachedUnlock"></span><span id="cachedunlock"></span><span id="CACHEDUNLOCK"></span>

<span data-ttu-id="c5197-176"><span id="CachedUnlock"></span><span id="cachedunlock"></span><span id="CACHEDUNLOCK"></span>**Cachedunlock** (13)</span><span class="sxs-lookup"><span data-stu-id="c5197-176"><span id="CachedUnlock"></span><span id="cachedunlock"></span><span id="CACHEDUNLOCK"></span>**CachedUnlock** (13)</span></span>


</dt> <dd>

<span data-ttu-id="c5197-177">Arbeitsstations Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="c5197-177">Workstation logon.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c5197-178">**Name**</span><span class="sxs-lookup"><span data-stu-id="c5197-178">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5197-179">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c5197-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5197-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c5197-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5197-181">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="c5197-181">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="c5197-182">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="c5197-182">Label by which the object is known.</span></span> <span data-ttu-id="c5197-183">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="c5197-183">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="c5197-184">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c5197-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5197-185">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="c5197-185">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5197-186">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="c5197-186">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c5197-187">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c5197-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5197-188">Der Zeitpunkt, zu dem die Sitzung gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="c5197-188">Time at which the session started.</span></span>

<span data-ttu-id="c5197-189">Diese Eigenschaft wird von der [**Win32- \_ Sitzung**](win32-session.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c5197-189">This property is inherited from [**Win32\_Session**](win32-session.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5197-190">**Status**</span><span class="sxs-lookup"><span data-stu-id="c5197-190">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5197-191">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c5197-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5197-192">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c5197-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5197-193">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="c5197-193">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c5197-194">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="c5197-194">String that indicates the current status of the object.</span></span> <span data-ttu-id="c5197-195">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="c5197-195">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="c5197-196">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="c5197-196">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="c5197-197">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="c5197-197">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="c5197-198">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="c5197-198">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c5197-199">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="c5197-199">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c5197-200">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="c5197-200">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c5197-201">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c5197-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c5197-202">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="c5197-202">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c5197-203">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="c5197-203">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c5197-204">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="c5197-204">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c5197-205">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="c5197-205">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c5197-206">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="c5197-206">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c5197-207">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="c5197-207">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c5197-208">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="c5197-208">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c5197-209">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="c5197-209">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c5197-210">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="c5197-210">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c5197-211">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="c5197-211">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c5197-212">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="c5197-212">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c5197-213">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="c5197-213">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c5197-214">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="c5197-214">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="c5197-215"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c5197-215"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="examples"></a><span data-ttu-id="c5197-216">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c5197-216">Examples</span></span>

<span data-ttu-id="c5197-217">Das PowerShell-Beispiel " [Auflisten von Anmelde Informationen](https://Gallery.TechNet.Microsoft.Com/scriptcenter/64cc7ab5-f1cd-460c-9d37-e6f989444de3) " gibt Informationen zu Anmelde Sitzungen zurück, die dem aktuell auf einem Computer angemeldeten Benutzer zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c5197-217">The [List Logon Session Information](https://Gallery.TechNet.Microsoft.Com/scriptcenter/64cc7ab5-f1cd-460c-9d37-e6f989444de3) PowerShell sample returns information about logon sessions associated with the user currently logged on to a computer.</span></span>

<span data-ttu-id="c5197-218">Das folgende PowerShell-Beispiel prüft, ob eine Remote Sitzung für einen angegebenen Benutzer geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="c5197-218">The following PowerShell example checks for remote session open for a specified user.</span></span>


```PowerShell
$user = "<user name>"
$servers = gci servers.txt 

     foreach ($server in $servers){
     $logons = gwmi win32_loggedonuser -computername $server

          foreach ($logon in $logons){
               if ($logon.antecedent -match $user){
               $logonid = $logon.dependent.split("=")[1] 
               $session =gwmi win32_logonsession |? {$_.logonid -match $logonid}
               if ($session.logontype -eq "10"){
               Write-host "You have an active Terminal Server session on server $($server)"
                }
          }
```



## <a name="requirements"></a><span data-ttu-id="c5197-219">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5197-219">Requirements</span></span>



| <span data-ttu-id="c5197-220">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5197-220">Requirement</span></span> | <span data-ttu-id="c5197-221">Wert</span><span class="sxs-lookup"><span data-stu-id="c5197-221">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5197-222">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c5197-222">Minimum supported client</span></span><br/> | <span data-ttu-id="c5197-223">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c5197-223">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c5197-224">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c5197-224">Minimum supported server</span></span><br/> | <span data-ttu-id="c5197-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c5197-225">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c5197-226">Namespace</span><span class="sxs-lookup"><span data-stu-id="c5197-226">Namespace</span></span><br/>                | <span data-ttu-id="c5197-227">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c5197-227">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c5197-228">MOF</span><span class="sxs-lookup"><span data-stu-id="c5197-228">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c5197-229"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c5197-229"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c5197-230">DLL</span><span class="sxs-lookup"><span data-stu-id="c5197-230">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5197-231"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5197-231"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5197-232">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5197-232">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5197-233">**Win32- \_ Sitzung**</span><span class="sxs-lookup"><span data-stu-id="c5197-233">**Win32\_Session**</span></span>](win32-session.md)
</dt> <dt>

<span data-ttu-id="c5197-234">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c5197-234">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

