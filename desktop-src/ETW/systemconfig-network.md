---
description: Diese Klasse ist die Ereignistyp Klasse für Netzwerkereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: afa994ef-dd1c-4909-a6cd-7021be4fff40
title: SystemConfig_Network-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Network
- SystemConfig_Network.TcbTablePartitions
- SystemConfig_Network.MaxHashTableSize
- SystemConfig_Network.MaxUserPort
- SystemConfig_Network.TcpTimedWaitDelay
api_type:
- NA
api_location: ''
ms.openlocfilehash: 23b469c31645c6a5b04319f91b758ee19beb935c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977584"
---
# <a name="systemconfig_network-class"></a><span data-ttu-id="c47b9-104">SystemConfig- \_ Netzwerk Klasse</span><span class="sxs-lookup"><span data-stu-id="c47b9-104">SystemConfig\_Network class</span></span>

<span data-ttu-id="c47b9-105">Diese Klasse ist die Ereignistyp Klasse für Netzwerkereignisse.</span><span class="sxs-lookup"><span data-stu-id="c47b9-105">This class is the event type class for network events.</span></span>

<span data-ttu-id="c47b9-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="c47b9-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c47b9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c47b9-107">Syntax</span></span>

``` syntax
[EventType(17), EventTypeName("Network")]
class SystemConfig_Network : SystemConfig
{
  uint32 TcbTablePartitions;
  uint32 MaxHashTableSize;
  uint32 MaxUserPort;
  uint32 TcpTimedWaitDelay;
};
```

## <a name="members"></a><span data-ttu-id="c47b9-108">Member</span><span class="sxs-lookup"><span data-stu-id="c47b9-108">Members</span></span>

<span data-ttu-id="c47b9-109">Die **\_ Netzwerk Klasse "SystemConfig** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c47b9-109">The **SystemConfig\_Network** class has these types of members:</span></span>

-   [<span data-ttu-id="c47b9-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c47b9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c47b9-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c47b9-111">Properties</span></span>

<span data-ttu-id="c47b9-112">Die **SystemConfig- \_ Netzwerk** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c47b9-112">The **SystemConfig\_Network** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c47b9-113">**MaxHashTableSize**</span><span class="sxs-lookup"><span data-stu-id="c47b9-113">**MaxHashTableSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c47b9-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c47b9-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c47b9-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c47b9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c47b9-116">Qualifizierer: wmidataid (2)</span><span class="sxs-lookup"><span data-stu-id="c47b9-116">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="c47b9-117">Die Größe der Hash Tabelle, in der die TCP-Steuerungsblöcke (TCBS) gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="c47b9-117">The size of the hash table in which TCP control blocks (TCBs) are stored.</span></span> <span data-ttu-id="c47b9-118">TCP speichert Kontroll Blöcke in einer Hash Tabelle, sodass Sie Sie schnell finden können.</span><span class="sxs-lookup"><span data-stu-id="c47b9-118">TCP stores control blocks in a hash table so it can find them very quickly.</span></span>

</dd> <dt>

<span data-ttu-id="c47b9-119">**MaxUserPort**</span><span class="sxs-lookup"><span data-stu-id="c47b9-119">**MaxUserPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c47b9-120">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c47b9-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c47b9-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c47b9-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c47b9-122">Qualifizierer: wmidataid (3)</span><span class="sxs-lookup"><span data-stu-id="c47b9-122">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="c47b9-123">Die höchste Portnummer, die TCP zuweisen kann, wenn eine Anwendung einen verfügbaren Benutzerport vom System anfordert.</span><span class="sxs-lookup"><span data-stu-id="c47b9-123">The highest port number TCP can assign when an application requests an available user port from the system.</span></span> <span data-ttu-id="c47b9-124">Normalerweise werden kurzlebige Ports (die kurz verwendet) den Portnummern 1024 bis 5000 zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c47b9-124">Typically, ephemeral ports (those used briefly) are allocated to port numbers 1024 through 5000.</span></span>

<span data-ttu-id="c47b9-125">Der Wert für die höchste Benutzer Portnummer, die TCP zugewiesen werden kann, wird von einer Registrierungs Einstellung gesteuert.</span><span class="sxs-lookup"><span data-stu-id="c47b9-125">The value for the highest user port number TCP can assign is controlled by a registry setting.</span></span> <span data-ttu-id="c47b9-126">Weitere Informationen finden Sie unter [MaxUserPort](/previous-versions/windows/it-pro/windows-2000-server/cc938196(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="c47b9-126">For more information, see [MaxUserPort](/previous-versions/windows/it-pro/windows-2000-server/cc938196(v=technet.10)).</span></span>

</dd> <dt>

<span data-ttu-id="c47b9-127">**Tcbtablepartitions**</span><span class="sxs-lookup"><span data-stu-id="c47b9-127">**TcbTablePartitions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c47b9-128">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c47b9-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c47b9-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c47b9-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c47b9-130">Qualifizierer: wmidataid (1)</span><span class="sxs-lookup"><span data-stu-id="c47b9-130">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="c47b9-131">Die Anzahl der Partitionen in der Transport Steuerungs Block-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c47b9-131">The number of partitions in the Transport Control Block table.</span></span> <span data-ttu-id="c47b9-132">Durch die Partitionierung der Transport Steuerungs Block Tabelle werden Konflikte für den Tabellen Zugriff minimiert.</span><span class="sxs-lookup"><span data-stu-id="c47b9-132">Partitioning the Transport Control Block table minimizes contention for table access.</span></span> <span data-ttu-id="c47b9-133">Dies ist besonders bei Multiprozessorsystemen von nutzen.</span><span class="sxs-lookup"><span data-stu-id="c47b9-133">This is especially useful on multiprocessor systems.</span></span>

</dd> <dt>

<span data-ttu-id="c47b9-134">**TcpTimedWaitDelay**</span><span class="sxs-lookup"><span data-stu-id="c47b9-134">**TcpTimedWaitDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c47b9-135">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c47b9-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c47b9-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c47b9-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c47b9-137">Qualifizierer: wmidataid (4)</span><span class="sxs-lookup"><span data-stu-id="c47b9-137">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="c47b9-138">Die Zeitspanne, die ververgehen muss, bevor TCP eine geschlossene Verbindung freigeben und deren Ressourcen wieder verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="c47b9-138">The time that must elapse before TCP can release a closed connection and reuse its resources.</span></span> <span data-ttu-id="c47b9-139">Dieses Intervall zwischen Closure und Release wird als Zeit \_ Wartezeit oder 2MSL-Status bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c47b9-139">This interval between closure and release is known as the TIME\_WAIT state or 2MSL state.</span></span> <span data-ttu-id="c47b9-140">Während dieser Zeit kann die Verbindung auf dem Client und dem Server um kostengünstiger wieder geöffnet werden, als eine neue Verbindung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="c47b9-140">During this time, the connection can be reopened at much less cost to the client and server than establishing a new connection.</span></span>

<span data-ttu-id="c47b9-141">Die vom IETF veröffentlichte RFC 793 erfordert, dass TCP eine geschlossene Verbindung für ein Intervall beibehält, das mindestens der doppelten Segment Lebensdauer (2MSL) des Netzwerks entspricht.</span><span class="sxs-lookup"><span data-stu-id="c47b9-141">RFC 793 published by the IETF requires that TCP maintains a closed connection for an interval at least equal to twice the maximum segment lifetime (2MSL) of the network.</span></span> <span data-ttu-id="c47b9-142">Wenn eine Verbindung freigegeben wird, können das Socketpaar und der TCP-Kontroll Block (TCB) zur Unterstützung einer anderen Verbindung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c47b9-142">When a connection is released, its socket pair and TCP control block (TCB) can be used to support another connection.</span></span> <span data-ttu-id="c47b9-143">Standardmäßig ist MSL auf 120 Sekunden festgelegt, und der Wert dieses Eintrags ist gleich 2 MSLs oder 4 Minuten.</span><span class="sxs-lookup"><span data-stu-id="c47b9-143">By default, the MSL is defined to be 120 seconds, and the value of this entry is equal to two MSLs, or 4 minutes.</span></span> <span data-ttu-id="c47b9-144">Weitere Informationen finden Sie unter [RFC 793](https://tools.ietf.org/html/rfc973).</span><span class="sxs-lookup"><span data-stu-id="c47b9-144">For more information, see [RFC 793](https://tools.ietf.org/html/rfc973).</span></span>

<span data-ttu-id="c47b9-145">Wenn Sie den Wert dieses Eintrags mithilfe einer Registrierungs Einstellung verringern, kann TCP geschlossene Verbindungen schneller freigeben und damit mehr Ressourcen für neue Verbindungen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c47b9-145">Reducing the value of this entry using a registry setting allows TCP to release closed connections faster, providing more resources for new connections.</span></span> <span data-ttu-id="c47b9-146">Wenn der Wert jedoch zu niedrig ist, gibt TCP möglicherweise Verbindungs Ressourcen frei, bevor die Verbindung hergestellt wird, sodass der Server zusätzliche Ressourcen zum erneuten Herstellen der Verbindung verwenden muss.</span><span class="sxs-lookup"><span data-stu-id="c47b9-146">However, if the value is too low, TCP might release connection resources before the connection is complete, requiring the server to use additional resources to reestablish the connection.</span></span>

<span data-ttu-id="c47b9-147">Normalerweise gibt TCP keine geschlossenen Verbindungen frei, bis der Wert dieses Eintrags abläuft.</span><span class="sxs-lookup"><span data-stu-id="c47b9-147">Normally, TCP does not release closed connections until the value of this entry expires.</span></span> <span data-ttu-id="c47b9-148">TCP kann jedoch Verbindungen freigeben, bevor dieser Wert abläuft, wenn die TCP-Steuerungsblöcke (TCBS) nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c47b9-148">However, TCP can release connections before this value expires if it is running out of TCP control blocks (TCBs).</span></span> <span data-ttu-id="c47b9-149">Die Anzahl der vom System erstellten TCBS wird von einer Registrierungs Einstellung gesteuert.</span><span class="sxs-lookup"><span data-stu-id="c47b9-149">The number of TCBs the system creates is controlled by a registry setting.</span></span> <span data-ttu-id="c47b9-150">Weitere Informationen finden Sie unter [maxfreetcbs](/previous-versions/windows/it-pro/windows-2000-server/cc938178(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="c47b9-150">For more information, see [MaxFreeTCBs](/previous-versions/windows/it-pro/windows-2000-server/cc938178(v=technet.10)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c47b9-151">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c47b9-151">Requirements</span></span>



| <span data-ttu-id="c47b9-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c47b9-152">Requirement</span></span> | <span data-ttu-id="c47b9-153">Wert</span><span class="sxs-lookup"><span data-stu-id="c47b9-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c47b9-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c47b9-154">Minimum supported client</span></span><br/> | <span data-ttu-id="c47b9-155">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c47b9-155">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c47b9-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c47b9-156">Minimum supported server</span></span><br/> | <span data-ttu-id="c47b9-157">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c47b9-157">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c47b9-158">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c47b9-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c47b9-159">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="c47b9-159">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 
