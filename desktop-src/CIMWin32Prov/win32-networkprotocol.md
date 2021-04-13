---
description: Das Win32- \_ networkprotocol-&\# 8194; Die WMI-Klasse stellt ein Protokoll und seine Netzwerk Eigenschaften auf einem Win32-Computersystem dar.
ms.assetid: c864a694-d507-4629-91c5-bd26ccf397f7
ms.tgt_platform: multiple
title: Win32_NetworkProtocol-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkProtocol
- Win32_NetworkProtocol.Caption
- Win32_NetworkProtocol.Description
- Win32_NetworkProtocol.InstallDate
- Win32_NetworkProtocol.Status
- Win32_NetworkProtocol.ConnectionlessService
- Win32_NetworkProtocol.GuaranteesDelivery
- Win32_NetworkProtocol.GuaranteesSequencing
- Win32_NetworkProtocol.MaximumAddressSize
- Win32_NetworkProtocol.MaximumMessageSize
- Win32_NetworkProtocol.MessageOriented
- Win32_NetworkProtocol.MinimumAddressSize
- Win32_NetworkProtocol.Name
- Win32_NetworkProtocol.PseudoStreamOriented
- Win32_NetworkProtocol.SupportsBroadcasting
- Win32_NetworkProtocol.SupportsConnectData
- Win32_NetworkProtocol.SupportsDisconnectData
- Win32_NetworkProtocol.SupportsEncryption
- Win32_NetworkProtocol.SupportsExpeditedData
- Win32_NetworkProtocol.SupportsFragmentation
- Win32_NetworkProtocol.SupportsGracefulClosing
- Win32_NetworkProtocol.SupportsGuaranteedBandwidth
- Win32_NetworkProtocol.SupportsMulticasting
- Win32_NetworkProtocol.SupportsQualityofService
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 33817fa4aa55747ecf9d4e89f5dcf406160c0c67
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483790"
---
# <a name="win32_networkprotocol-class"></a><span data-ttu-id="8e5e4-103">Win32- \_ networkprotocol-Klasse</span><span class="sxs-lookup"><span data-stu-id="8e5e4-103">Win32\_NetworkProtocol class</span></span>

<span data-ttu-id="8e5e4-104">Die **Win32 \_ Network Protocol** [WMI-Klasse](../wmisdk/retrieving-a-class.md) stellt ein Protokoll und seine Netzwerk Eigenschaften auf einem Win32-Computersystem dar.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-104">The **Win32\_NetworkProtocol** [WMI class](../wmisdk/retrieving-a-class.md) represents a protocol and its network characteristics on a Win32 computer system.</span></span>

<span data-ttu-id="8e5e4-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="8e5e4-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e5e4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e5e4-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkProtocol : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  boolean  ConnectionlessService;
  boolean  GuaranteesDelivery;
  boolean  GuaranteesSequencing;
  uint32   MaximumAddressSize;
  uint32   MaximumMessageSize;
  boolean  MessageOriented;
  uint32   MinimumAddressSize;
  string   Name;
  boolean  PseudoStreamOriented;
  boolean  SupportsBroadcasting;
  boolean  SupportsConnectData;
  boolean  SupportsDisconnectData;
  boolean  SupportsEncryption;
  boolean  SupportsExpeditedData;
  boolean  SupportsFragmentation;
  boolean  SupportsGracefulClosing;
  boolean  SupportsGuaranteedBandwidth;
  boolean  SupportsMulticasting;
  boolean  SupportsQualityofService;
};
```

## <a name="members"></a><span data-ttu-id="8e5e4-108">Member</span><span class="sxs-lookup"><span data-stu-id="8e5e4-108">Members</span></span>

<span data-ttu-id="8e5e4-109">Die **Win32- \_ networkprotocol** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8e5e4-109">The **Win32\_NetworkProtocol** class has these types of members:</span></span>

-   [<span data-ttu-id="8e5e4-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8e5e4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8e5e4-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8e5e4-111">Properties</span></span>

<span data-ttu-id="8e5e4-112">Die **Win32- \_ networkprotocol** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-112">The **Win32\_NetworkProtocol** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8e5e4-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5e4-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e5e4-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-116">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="8e5e4-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="8e5e4-117">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-117">A short textual description of the object.</span></span>

<span data-ttu-id="8e5e4-118">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e5e4-119">**ConnectionlessService**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-119">**ConnectionlessService**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5e4-120">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8e5e4-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e5e4-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-122">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets Structures \| Protokoll \_ Info \| dwserviceflags \| XP1 \_ Connectionless")</span><span class="sxs-lookup"><span data-stu-id="8e5e4-122">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP1\_CONNECTIONLESS")</span></span>
</dt> </dl>

<span data-ttu-id="8e5e4-123">Das Protokoll unterstützt den Verbindungs losen Dienst.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-123">Protocol supports connectionless service.</span></span> <span data-ttu-id="8e5e4-124">Ein verbindungsloses-Dienst (Datagramm) beschreibt ein Kommunikationsprotokoll oder einen Transport, in dem Datenpakete unabhängig voneinander weitergeleitet werden und den verschiedenen Routen folgen können und in einer anderen Reihenfolge als der Sendevorgang eintreffen.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-124">A connectionless (datagram) service describes a communications protocol or transport in which data packets are routed independently of each other and may follow different routes and arrive in a different order from that in which they were sent.</span></span> <span data-ttu-id="8e5e4-125">Umgekehrt bietet ein Verbindungs orientierter Dienst eine virtuelle Verbindung, über die Datenpakete in derselben Reihenfolge empfangen werden, in der Sie übertragen wurden.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-125">Conversely, a connection-oriented service provides a virtual circuit through which data packets are received in the same order they were transmitted.</span></span> <span data-ttu-id="8e5e4-126">Wenn die Verbindung zwischen Computern fehlschlägt, wird die Anwendung benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-126">If the connection between computers fails, the application is notified.</span></span>

</dd> <dt>

<span data-ttu-id="8e5e4-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5e4-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e5e4-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-130">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="8e5e4-130">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="8e5e4-131">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-131">A textual description of the object.</span></span>

<span data-ttu-id="8e5e4-132">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e5e4-133">**Zustellungs Bereitstellung**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-133">**GuaranteesDelivery**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5e4-134">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8e5e4-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e5e4-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-136">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets Structures \| Protokoll \_ Info \| dwserviceflags \| XP \_ garantierte \_ Übermittlung")</span><span class="sxs-lookup"><span data-stu-id="8e5e4-136">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_GUARANTEED\_DELIVERY")</span></span>
</dt> </dl>

<span data-ttu-id="8e5e4-137">Das Protokoll unterstützt die Übermittlung von Datenpaketen.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-137">Protocol supports delivery of data packets.</span></span> <span data-ttu-id="8e5e4-138">Wenn dieses Flag **false** ist, ist es unsicher, dass alle gesendeten Daten das beabsichtigte Ziel erreichen.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-138">If this flag is **FALSE**, it is uncertain that all of the data sent will reach the intended destination.</span></span>

</dd> <dt>

<span data-ttu-id="8e5e4-139">**Die Sequenzierung**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-139">**GuaranteesSequencing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5e4-140">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8e5e4-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e5e4-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-142">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets Structures \| Protokoll \_ Info \| dwserviceflags \| XP \_ garantierte \_ Reihenfolge")</span><span class="sxs-lookup"><span data-stu-id="8e5e4-142">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_GUARANTEED\_ORDER")</span></span>
</dt> </dl>

<span data-ttu-id="8e5e4-143">Mit dem Protokoll wird sichergestellt, dass die Daten in der Reihenfolge eintreffen, in der Sie gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-143">Protocol ensures that data will arrive in the order in which it was sent.</span></span> <span data-ttu-id="8e5e4-144">Beachten Sie, dass dieses Merkmal nicht sicherstellt, dass die Daten nur in seiner Reihenfolge bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-144">Be aware that this characteristic does not ensure delivery of the data, only its order.</span></span>

</dd> <dt>

<span data-ttu-id="8e5e4-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5e4-146">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e5e4-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-148">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="8e5e4-148">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="8e5e4-149">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-149">Indicates when the object was installed.</span></span> <span data-ttu-id="8e5e4-150">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-150">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="8e5e4-151">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e5e4-152">**MaximumAddressSize**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-152">**MaximumAddressSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5e4-153">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e5e4-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-155">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets Structures \| Protokoll \_ Info \| imaxsockaddr"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Zeichen")</span><span class="sxs-lookup"><span data-stu-id="8e5e4-155">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|iMaxSockAddr"), [**units**](../wmisdk/standard-qualifiers.md) ("characters")</span></span>
</dt> </dl>

<span data-ttu-id="8e5e4-156">Maximale Länge einer vom Protokoll unterstützten Socketadresse.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-156">Maximum length of a socket address supported by the protocol.</span></span> <span data-ttu-id="8e5e4-157">Socketadressen können Elemente sein, z. b. eine URL ( `www.microsoft.com` ) oder eine IP-Adresse ( `130.215.24.1` ).</span><span class="sxs-lookup"><span data-stu-id="8e5e4-157">Socket addresses may be items such as a URL (`www.microsoft.com`) or an IP address (`130.215.24.1`).</span></span>

</dd> <dt>

<span data-ttu-id="8e5e4-158">**Maximummessagesize**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-158">**MaximumMessageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5e4-159">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e5e4-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-161">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets Structures \| Protokoll \_ Info \| dwmessagesize"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Zeichen")</span><span class="sxs-lookup"><span data-stu-id="8e5e4-161">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwMessageSize"), [**units**](../wmisdk/standard-qualifiers.md) ("characters")</span></span>
</dt> </dl>

<span data-ttu-id="8e5e4-162">Maximale Nachrichtengröße, die vom Protokoll unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-162">Maximum message size supported by the protocol.</span></span> <span data-ttu-id="8e5e4-163">Dies ist die maximale Größe einer Nachricht, die vom Host gesendet oder empfangen werden kann.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-163">This is the maximum size of a message that can be sent from or received by the host.</span></span> <span data-ttu-id="8e5e4-164">Bei Protokollen, die Nachrichtenrahmen nicht unterstützen, kann die tatsächliche maximale Größe einer Nachricht, die an eine bestimmte Adresse gesendet werden kann, kleiner als dieser Wert sein.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-164">For protocols that do not support message framing, the actual maximum size of a message that can be sent to a given address may be less than this value.</span></span>

</dd> <dt>

<span data-ttu-id="8e5e4-165">**Messageoriented**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-165">**MessageOriented**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5e4-166">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8e5e4-166">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e5e4-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-168">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets Structures \| Protokoll \_ Info \| dwserviceflags \| XP \_ Nachrichten \_ orientiert")</span><span class="sxs-lookup"><span data-stu-id="8e5e4-168">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_MESSAGE\_ORIENTED")</span></span>
</dt> </dl>

<span data-ttu-id="8e5e4-169">Protokoll ist Nachrichten orientiert.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-169">Protocol is message-oriented.</span></span> <span data-ttu-id="8e5e4-170">Ein Nachrichten orientiertes Protokoll verwendet Datenpakete zum Übertragen von Informationen.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-170">A message-oriented protocol uses packets of data to transfer information.</span></span> <span data-ttu-id="8e5e4-171">Im Gegensatz dazu übertragen Streamorientierte Protokolle Daten als kontinuierlichen Stream von Bytes.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-171">Conversely, stream-oriented protocols transfer data as a continuous stream of bytes.</span></span>

</dd> <dt>

<span data-ttu-id="8e5e4-172">**MinimumAddressSize**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-172">**MinimumAddressSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5e4-173">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-174">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e5e4-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-175">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets Structures \| Protokoll \_ Info \| iminsockaddr"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Zeichen")</span><span class="sxs-lookup"><span data-stu-id="8e5e4-175">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|iMinSockAddr "), [**units**](../wmisdk/standard-qualifiers.md) ("characters")</span></span>
</dt> </dl>

<span data-ttu-id="8e5e4-176">Die minimale Länge einer Socketadresse, die vom Protokoll unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-176">Minimum length of a socket address supported by the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="8e5e4-177">**Name**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-177">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5e4-178">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e5e4-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-180">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Name"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets Structures \| Protokoll \_ Info \| lpprotocol")</span><span class="sxs-lookup"><span data-stu-id="8e5e4-180">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|lpProtocol")</span></span>
</dt> </dl>

<span data-ttu-id="8e5e4-181">Der Name des Protokolls.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-181">Name for the protocol.</span></span>

<span data-ttu-id="8e5e4-182">Beispiel: "TCP/IP"</span><span class="sxs-lookup"><span data-stu-id="8e5e4-182">Example: "TCP/IP"</span></span>

</dd> <dt>

<span data-ttu-id="8e5e4-183">**PseudoStreamOriented**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-183">**PseudoStreamOriented**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5e4-184">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8e5e4-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e5e4-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-186">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets Structures \| Protokoll \_ Info \| dwserviceflags \| XP \_ Pseudo Daten \_ Strom")</span><span class="sxs-lookup"><span data-stu-id="8e5e4-186">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_PSEUDO\_STREAM")</span></span>
</dt> </dl>

<span data-ttu-id="8e5e4-187">Das Protokoll ist ein Nachrichten orientiertes Protokoll, das Datenpakete variabler Länge oder Stream-Daten für alle Empfangs Vorgänge empfangen kann.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-187">Protocol is a message-oriented protocol that can receive variable-length data packets or streamed data for all receive operations.</span></span> <span data-ttu-id="8e5e4-188">Diese optionale Funktion ist hilfreich, wenn eine Anwendung nicht in der Lage sein soll, Nachrichten in das Protokoll zu unterteilen, und Streamorientierte Merkmale erfordert.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-188">This optional ability is useful when an application does not want the protocol to frame messages, and requires stream-oriented characteristics.</span></span> <span data-ttu-id="8e5e4-189">**True** gibt an, dass das Protokoll Pseudo Datenstrom orientiert ist.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-189">If **TRUE**, the protocol is pseudo stream-oriented.</span></span>

</dd> <dt>

<span data-ttu-id="8e5e4-190">**Status**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-190">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5e4-191">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-192">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e5e4-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-193">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="8e5e4-193">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="8e5e4-194">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-194">String that indicates the current status of the object.</span></span> <span data-ttu-id="8e5e4-195">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-195">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="8e5e4-196">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-196">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="8e5e4-197">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="8e5e4-197">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="8e5e4-198">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-198">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8e5e4-199">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-199">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8e5e4-200">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-200">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8e5e4-201">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="8e5e4-202">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="8e5e4-202">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8e5e4-203">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="8e5e4-203">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8e5e4-204">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="8e5e4-204">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8e5e4-205">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="8e5e4-205">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8e5e4-206">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="8e5e4-206">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="8e5e4-207">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="8e5e4-207">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="8e5e4-208">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="8e5e4-208">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="8e5e4-209">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="8e5e4-209">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="8e5e4-210">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="8e5e4-210">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="8e5e4-211">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="8e5e4-211">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="8e5e4-212">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="8e5e4-212">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="8e5e4-213">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="8e5e4-213">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="8e5e4-214">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="8e5e4-214">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8e5e4-215">**SupportsBroadcasting**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-215">**SupportsBroadcasting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5e4-216">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8e5e4-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-217">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e5e4-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-218">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets Structures \| Protokoll \_ Info \| dwserviceflags \| XP \_ unterstützt \_ Broadcast")</span><span class="sxs-lookup"><span data-stu-id="8e5e4-218">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_SUPPORTS\_BROADCAST")</span></span>
</dt> </dl>

<span data-ttu-id="8e5e4-219">Das Protokoll unterstützt einen Mechanismus zum Senden von Nachrichten über das Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-219">Protocol supports a mechanism for broadcasting messages across the network.</span></span>

</dd> <dt>

<span data-ttu-id="8e5e4-220">**SupportsConnectData**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-220">**SupportsConnectData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5e4-221">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8e5e4-221">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-222">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e5e4-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-223">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets Structures \| Protokoll \_ Info \| dwserviceflags \| XP \_ Connect \_ Data")</span><span class="sxs-lookup"><span data-stu-id="8e5e4-223">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_CONNECT\_DATA")</span></span>
</dt> </dl>

<span data-ttu-id="8e5e4-224">Mit dem Protokoll können Daten über das Netzwerk verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-224">Protocol allows data to be connected across the network.</span></span>

</dd> <dt>

<span data-ttu-id="8e5e4-225">**SupportsDisconnectData**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-225">**SupportsDisconnectData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5e4-226">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8e5e4-226">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-227">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e5e4-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-228">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets Structures \| Protokoll \_ Info \| dwserviceflags \| XP \_ Disconnect \_ Data")</span><span class="sxs-lookup"><span data-stu-id="8e5e4-228">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_DISCONNECT\_DATA")</span></span>
</dt> </dl>

<span data-ttu-id="8e5e4-229">Mit dem Protokoll können Daten über das Netzwerk getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-229">Protocol allows data to be disconnected across the network.</span></span>

</dd> <dt>

<span data-ttu-id="8e5e4-230">**SupportsEncryption**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-230">**SupportsEncryption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5e4-231">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8e5e4-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-232">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e5e4-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-233">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets Structures \| Protokoll \_ Info \| dwserviceflags \| XP \_ verschlüsselt")</span><span class="sxs-lookup"><span data-stu-id="8e5e4-233">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_ENCRYPTS")</span></span>
</dt> </dl>

<span data-ttu-id="8e5e4-234">Das Protokoll unterstützt die Datenverschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-234">Protocol supports data encryption.</span></span>

</dd> <dt>

<span data-ttu-id="8e5e4-235">**Supportsexpediteddata**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-235">**SupportsExpeditedData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5e4-236">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8e5e4-236">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-237">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e5e4-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-238">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets Structures \| Protokoll \_ Info \| dwserviceflags \| XP \_ beschleunigte \_ Daten")</span><span class="sxs-lookup"><span data-stu-id="8e5e4-238">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_EXPEDITED\_DATA")</span></span>
</dt> </dl>

<span data-ttu-id="8e5e4-239">Das Protokoll unterstützt beschleunigte Daten (auch als dringende Daten bezeichnet) im gesamten Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-239">Protocol supports expedited data (also known as urgent data) across the network.</span></span> <span data-ttu-id="8e5e4-240">Beschleunigte Daten können die Fluss Steuerung umgehen und Vorrang vor normalen Datenpaketen erhalten.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-240">Expedited data can bypass flow control and receive priority over normal data packets.</span></span>

</dd> <dt>

<span data-ttu-id="8e5e4-241">**Supportsfragmentierung**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-241">**SupportsFragmentation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5e4-242">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8e5e4-242">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-243">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e5e4-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-244">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets Structures \| Protokoll \_ Info \| dwserviceflags \| XP \_ Fragmentierung")</span><span class="sxs-lookup"><span data-stu-id="8e5e4-244">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_FRAGMENTATION")</span></span>
</dt> </dl>

<span data-ttu-id="8e5e4-245">Das Protokoll unterstützt das Übertragen von Daten in Fragmenten.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-245">Protocol supports transmitting the data in fragments.</span></span> <span data-ttu-id="8e5e4-246">Das physische Netzwerk für die maximale Übertragungseinheit (MTU) ist in den Anwendungen ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-246">Physical network maximum transfer unit (MTU) is hidden from applications.</span></span> <span data-ttu-id="8e5e4-247">Jeder Medientyp hat eine maximale Frame Größe, die nicht überschritten werden kann.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-247">Each media type has a maximum frame size that cannot be exceeded.</span></span> <span data-ttu-id="8e5e4-248">Die Verbindungs Ebene ermittelt die MTU und meldet Sie den verwendeten Protokollen.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-248">The link layer discovers the MTU and reports it to the protocols used.</span></span>

</dd> <dt>

<span data-ttu-id="8e5e4-249">**SupportsGracefulClosing**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-249">**SupportsGracefulClosing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5e4-250">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8e5e4-250">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-251">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e5e4-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-252">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets Structures \| Protokoll \_ Info \| dwserviceflags XP ordnungsgemäß \| \_ \_ Schließen")</span><span class="sxs-lookup"><span data-stu-id="8e5e4-252">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_GRACEFUL\_CLOSE")</span></span>
</dt> </dl>

<span data-ttu-id="8e5e4-253">Das Protokoll unterstützt zweiphasenclose-Vorgänge, auch bekannt als "ordnungsgemäße Schließ Vorgänge".</span><span class="sxs-lookup"><span data-stu-id="8e5e4-253">Protocol supports two-phase close operations, also known as "graceful close operations".</span></span> <span data-ttu-id="8e5e4-254">Andernfalls unterstützt das Protokoll nur Abbruch Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-254">If not, the protocol supports only abortive close operations.</span></span>

</dd> <dt>

<span data-ttu-id="8e5e4-255">**Supportszuder Bandbreite**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-255">**SupportsGuaranteedBandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5e4-256">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8e5e4-256">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-257">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e5e4-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-258">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets Structures \| Protokoll \_ Info \| dwserviceflags \| XP \_ Bandbreiten \_ Zuordnung")</span><span class="sxs-lookup"><span data-stu-id="8e5e4-258">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_BANDWIDTH\_ALLOCATION")</span></span>
</dt> </dl>

<span data-ttu-id="8e5e4-259">Das Protokoll verfügt über einen Mechanismus zum Einrichten und Verwalten einer Bandbreite.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-259">Protocol has a mechanism to establish and maintain a bandwidth.</span></span>

</dd> <dt>

<span data-ttu-id="8e5e4-260">**SupportsMulticasting**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-260">**SupportsMulticasting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5e4-261">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8e5e4-261">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-262">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e5e4-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-263">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets Structures \| Protokoll \_ Info \| dwserviceflags \| XP \_ unterstützt \_ Multicast")</span><span class="sxs-lookup"><span data-stu-id="8e5e4-263">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_SUPPORTS\_MULTICAST")</span></span>
</dt> </dl>

<span data-ttu-id="8e5e4-264">Das Protokoll unterstützt Multicasting.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-264">Protocol supports multicasting.</span></span>

</dd> <dt>

<span data-ttu-id="8e5e4-265">**SupportsQualityofService**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-265">**SupportsQualityofService**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5e4-266">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8e5e4-266">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-267">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e5e4-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e5e4-268">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets-Strukturen \| wsaprotocol \_ Info \| dwServiceFlags1 \| XP1 \_ QoS \_ unterstützt")</span><span class="sxs-lookup"><span data-stu-id="8e5e4-268">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|WSAPROTOCOL\_INFO\|dwServiceFlags1\|XP1\_QOS\_SUPPORTED")</span></span>
</dt> </dl>

<span data-ttu-id="8e5e4-269">Das Protokoll unterstützt Quality of Service (QoS)-Unterstützung durch den zugrunde liegenden, geschichteten Dienstanbieter oder Transportunternehmen.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-269">Protocol is capable of Quality of Service (QoS) support by the underlying layered service provider or transport carrier.</span></span> <span data-ttu-id="8e5e4-270">QoS ist eine Sammlung von-Komponenten, die eine Differenzierung und bevorzugte Behandlung für Teilmengen von Daten ermöglichen, die über das Netzwerk übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-270">QoS is a collection of components that enable differentiation and preferential treatment for subsets of data transmitted over the network.</span></span> <span data-ttu-id="8e5e4-271">QoS bedeutet, dass Teilmengen von Daten bei der Durchquerung eines Netzwerks eine höhere Priorität oder einen garantierten Dienst erhalten.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-271">QoS means subsets of data get higher priority or guaranteed service when traversing a network.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8e5e4-272">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8e5e4-272">Remarks</span></span>

<span data-ttu-id="8e5e4-273">Die **Win32- \_ networkprotocol** -Klasse wird von [**CIM \_ LogicalElement**](cim-logicalelement.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-273">The **Win32\_NetworkProtocol** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="examples"></a><span data-ttu-id="8e5e4-274">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8e5e4-274">Examples</span></span>

<span data-ttu-id="8e5e4-275">Im folgenden VBScript-Codebeispiel wird veranschaulicht, wie eine Liste der laufenden Dienste aus Instanzen von **Win32 \_ Network Protocol** abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-275">The following VBScript code sample demonstrates how to retrieve a list of running services from instances of **Win32\_NetworkProtocol**.</span></span>


```VB
Set ProtocolSet = GetObject("winmgmts:").ExecQuery("select * from Win32_NetworkProtocol")

for each Protocol in ProtocolSet
 WScript.Echo Protocol.Name
next
```



<span data-ttu-id="8e5e4-276">Im folgenden perl-Codebeispiel wird veranschaulicht, wie eine Liste der laufenden Dienste aus Instanzen von **Win32 \_ Network Protocol** abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-276">The following Perl code sample demonstrates how to retrieve a list of running services from instances of **Win32\_NetworkProtocol**.</span></span>


```
use strict;
use Win32::OLE;

my ( $ProtocolSet, $Protocol );

eval { $ProtocolSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_NetworkProtocol"); };
unless($@)
{
 print "\n";
 foreach $Protocol (in $ProtocolSet) 
 {
  print $Protocol->{Name}, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="8e5e4-277">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e5e4-277">Requirements</span></span>



| <span data-ttu-id="8e5e4-278">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8e5e4-278">Requirement</span></span> | <span data-ttu-id="8e5e4-279">Wert</span><span class="sxs-lookup"><span data-stu-id="8e5e4-279">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e5e4-280">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8e5e4-280">Minimum supported client</span></span><br/> | <span data-ttu-id="8e5e4-281">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8e5e4-281">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8e5e4-282">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8e5e4-282">Minimum supported server</span></span><br/> | <span data-ttu-id="8e5e4-283">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e5e4-283">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8e5e4-284">Namespace</span><span class="sxs-lookup"><span data-stu-id="8e5e4-284">Namespace</span></span><br/>                | <span data-ttu-id="8e5e4-285">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8e5e4-285">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8e5e4-286">MOF</span><span class="sxs-lookup"><span data-stu-id="8e5e4-286">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e5e4-287"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8e5e4-287"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e5e4-288">DLL</span><span class="sxs-lookup"><span data-stu-id="8e5e4-288">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e5e4-289"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e5e4-289"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e5e4-290">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e5e4-290">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e5e4-291">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-291">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="8e5e4-292">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="8e5e4-292">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
