---
title: RAS_PORT_STATISTICS Struktur (rassapi. h)
description: Die Struktur der RAS- \_ Port \_ Statistik meldet die Statistiken, die ein RAS-Server für einen verbundenen Port sammelt.
ms.assetid: c42c7059-ff92-4f49-a86e-2f47a083aa8e
keywords:
- RAS_PORT_STATISTICS Struktur-RAS
- PRAS_PORT_STATISTICS-Struktur Zeiger RAS
topic_type:
- apiref
api_name:
- RAS_PORT_STATISTICS
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85e60fb001da3f8401e47c366eecc86aced22b77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345299"
---
# <a name="ras_port_statistics-structure"></a><span data-ttu-id="c233e-105">Struktur der RAS- \_ Port \_ Statistik</span><span class="sxs-lookup"><span data-stu-id="c233e-105">RAS\_PORT\_STATISTICS structure</span></span>

<span data-ttu-id="c233e-106">\[Die Struktur der **RAS- \_ Port \_ Statistik** wird ab Windows Vista nicht unterstützt.\]</span><span class="sxs-lookup"><span data-stu-id="c233e-106">\[The **RAS\_PORT\_STATISTICS** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="c233e-107">Die Struktur der **RAS- \_ Port \_ Statistik** meldet die Statistiken, die ein RAS-Server für einen verbundenen Port sammelt.</span><span class="sxs-lookup"><span data-stu-id="c233e-107">The **RAS\_PORT\_STATISTICS** structure reports the statistics that a RAS server collects for a connected port.</span></span> <span data-ttu-id="c233e-108">Der RAS-Server setzt die einzelnen Statistik Indikatoren zurück, wenn der Port verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="c233e-108">The RAS server resets the various statistic counters each time the port is connected.</span></span> <span data-ttu-id="c233e-109">Aufrufen der [**rasadminportclearstatistics**](rasadminportclearstatistics.md) -Funktion, um das Zurücksetzen der Statistik Zähler durch den RAS-Server zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="c233e-109">Call the [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md) function to force the RAS server to reset the statistic counters.</span></span>

<span data-ttu-id="c233e-110">Bei einem Port, der Teil einer Verbindung mit mehreren Links ist, stellt diese Struktur zwei Sätze von Statistiken bereit.</span><span class="sxs-lookup"><span data-stu-id="c233e-110">For a port that is part of a multilink connection, this structure provides two sets of statistics.</span></span> <span data-ttu-id="c233e-111">Der erste Satz enthält die kumulativen Statistiken für alle Ports in der Verbindung.</span><span class="sxs-lookup"><span data-stu-id="c233e-111">The first set contains the cumulative statistics for all ports in the connection.</span></span> <span data-ttu-id="c233e-112">Diese Statistiken sind für alle Ports in der Verbindung identisch.</span><span class="sxs-lookup"><span data-stu-id="c233e-112">These statistics are the same for all ports in the connection.</span></span> <span data-ttu-id="c233e-113">Die zweite Gruppe enthält die Statistiken für nur diesen Port.</span><span class="sxs-lookup"><span data-stu-id="c233e-113">The second set contains the statistics for just this port.</span></span> <span data-ttu-id="c233e-114">Wenn der Port nicht Teil einer Verbindung mit mehreren Links ist, haben beide Statistik Sätze die gleichen Informationen.</span><span class="sxs-lookup"><span data-stu-id="c233e-114">If the port is not part of a multilink connection, both sets of statistics have the same information.</span></span> <span data-ttu-id="c233e-115">Um zu ermitteln, ob ein Port Teil einer Multilinkverbindung ist, überprüfen Sie das \_ multilinked-multilinked-Bit im **Flags** -Member der Struktur des Ports " [**RAS- \_ Port \_ 0**](ras-port-0-str.md) " des Ports.</span><span class="sxs-lookup"><span data-stu-id="c233e-115">To determine whether a port is part of a multilink connection, check the PORT\_MULTILINKED bit in the **Flags** member of the port's [**RAS\_PORT\_0**](ras-port-0-str.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="c233e-116">Syntax</span><span class="sxs-lookup"><span data-stu-id="c233e-116">Syntax</span></span>


```C++
typedef struct _RAS_PORT_STATISTICS {
  DWORD dwBytesXmited;
  DWORD dwBytesRcved;
  DWORD dwFramesXmited;
  DWORD dwFramesRcved;
  DWORD dwCrcErr;
  DWORD dwTimeoutErr;
  DWORD dwAlignmentErr;
  DWORD dwHardwareOverrunErr;
  DWORD dwFramingErr;
  DWORD dwBufferOverrunErr;
  DWORD dwBytesXmitedUncompressed;
  DWORD dwBytesRcvedUncompressed;
  DWORD dwBytesXmitedCompressed;
  DWORD dwBytesRcvedCompressed;
  DWORD dwPortBytesXmited;
  DWORD dwPortBytesRcved;
  DWORD dwPortFramesXmited;
  DWORD dwPortFramesRcved;
  DWORD dwPortCrcErr;
  DWORD dwPortTimeoutErr;
  DWORD dwPortAlignmentErr;
  DWORD dwPortHardwareOverrunErr;
  DWORD dwPortFramingErr;
  DWORD dwPortBufferOverrunErr;
  DWORD dwPortBytesXmitedUncompressed;
  DWORD dwPortBytesRcvedUncompressed;
  DWORD dwPortBytesXmitedCompressed;
  DWORD dwPortBytesRcvedCompressed;
} RAS_PORT_STATISTICS, *PRAS_PORT_STATISTICS;
```



## <a name="members"></a><span data-ttu-id="c233e-117">Member</span><span class="sxs-lookup"><span data-stu-id="c233e-117">Members</span></span>

<dl> <dt>

<span data-ttu-id="c233e-118">**dwbytesxgetrennte**</span><span class="sxs-lookup"><span data-stu-id="c233e-118">**dwBytesXmited**</span></span>
</dt> <dd>

<span data-ttu-id="c233e-119">Gibt die Gesamtanzahl der Bytes an, die von der Verbindung übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="c233e-119">Specifies the total number of bytes transmitted by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="c233e-120">**dwbytesrcved**</span><span class="sxs-lookup"><span data-stu-id="c233e-120">**dwBytesRcved**</span></span>
</dt> <dd>

<span data-ttu-id="c233e-121">Gibt die Gesamtanzahl von Bytes an, die von der Verbindung empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="c233e-121">Specifies the total number of bytes received by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="c233e-122">**dwframesxgetrennte**</span><span class="sxs-lookup"><span data-stu-id="c233e-122">**dwFramesXmited**</span></span>
</dt> <dd>

<span data-ttu-id="c233e-123">Gibt die Gesamtanzahl der von der Verbindung übertragenen Frames an.</span><span class="sxs-lookup"><span data-stu-id="c233e-123">Specifies the total number of frames transmitted by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="c233e-124">**dwframesrcved**</span><span class="sxs-lookup"><span data-stu-id="c233e-124">**dwFramesRcved**</span></span>
</dt> <dd>

<span data-ttu-id="c233e-125">Gibt die Gesamtanzahl der von der Verbindung empfangenen Rahmen an.</span><span class="sxs-lookup"><span data-stu-id="c233e-125">Specifies the total number of frames received by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="c233e-126">**dwcrcerr**</span><span class="sxs-lookup"><span data-stu-id="c233e-126">**dwCrcErr**</span></span>
</dt> <dd>

<span data-ttu-id="c233e-127">Gibt die Gesamtanzahl von CRC-Fehlern für die Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="c233e-127">Specifies the total number of CRC errors on the connection.</span></span> <span data-ttu-id="c233e-128">CRC-Fehler werden dadurch verursacht, dass eine zyklische Redundanz Prüfung fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="c233e-128">CRC errors are caused by the failure of a cyclic redundancy check.</span></span> <span data-ttu-id="c233e-129">Ein CRC-Fehler gibt an, dass ein oder mehrere Zeichen im empfangenen Datenpaket beim Eintreffen gegartet wurden.</span><span class="sxs-lookup"><span data-stu-id="c233e-129">A CRC error indicates that one or more characters in the data packet received were found garbled on arrival.</span></span>

</dd> <dt>

<span data-ttu-id="c233e-130">**dwtimeouterr**</span><span class="sxs-lookup"><span data-stu-id="c233e-130">**dwTimeoutErr**</span></span>
</dt> <dd>

<span data-ttu-id="c233e-131">Gibt die Gesamtzahl der Timeout Fehler für die Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="c233e-131">Specifies the total number of time-out errors on the connection.</span></span> <span data-ttu-id="c233e-132">Timeout Fehler treten auf, wenn ein erwartetes Zeichen nicht rechtzeitig empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="c233e-132">Time-out errors occur when an expected character is not received in time.</span></span> <span data-ttu-id="c233e-133">Wenn dies der Fall ist, geht die Software davon aus, dass die Daten verloren gegangen sind und fordert, dass Sie erneut gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="c233e-133">When this occurs, the software assumes that the data has been lost and requests that it be resent.</span></span>

</dd> <dt>

<span data-ttu-id="c233e-134">**dwalignmenterr**</span><span class="sxs-lookup"><span data-stu-id="c233e-134">**dwAlignmentErr**</span></span>
</dt> <dd>

<span data-ttu-id="c233e-135">Gibt die Gesamtanzahl der Ausrichtungsfehler für die Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="c233e-135">Specifies the total number of alignment errors on the connection.</span></span> <span data-ttu-id="c233e-136">Ausrichtungsfehler treten auf, wenn ein empfangenes Zeichen nicht das erwartete Zeichen ist.</span><span class="sxs-lookup"><span data-stu-id="c233e-136">Alignment errors occur when a character received is not the one expected.</span></span> <span data-ttu-id="c233e-137">Dies geschieht normalerweise, wenn ein Zeichen verloren geht oder ein Timeout Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="c233e-137">This usually happens when a character is lost or when a time-out error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="c233e-138">**dwhardwareoverrunerr**</span><span class="sxs-lookup"><span data-stu-id="c233e-138">**dwHardwareOverrunErr**</span></span>
</dt> <dd>

<span data-ttu-id="c233e-139">Gibt die Gesamtanzahl der Hardware Überlauf Fehler bei der Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="c233e-139">Specifies the total number of hardware overrun errors on the connection.</span></span> <span data-ttu-id="c233e-140">Diese Fehler geben an, wie oft der Sende Computer Zeichen schneller übertragen hat, als die Hardware des empfangenden Computers verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="c233e-140">These errors indicate the number of times the sending computer has transmitted characters faster than the receiving computer hardware can process them.</span></span> <span data-ttu-id="c233e-141">Wenn dieses Problem weiterhin besteht, verringern Sie die Verbindungs Rate für Bit/s auf dem Client.</span><span class="sxs-lookup"><span data-stu-id="c233e-141">If this problem persists, reduce the BPS connection rate on the client.</span></span>

</dd> <dt>

<span data-ttu-id="c233e-142">**dwframingerr**</span><span class="sxs-lookup"><span data-stu-id="c233e-142">**dwFramingErr**</span></span>
</dt> <dd>

<span data-ttu-id="c233e-143">Gibt die Gesamtzahl der Rahmen Fehler für die Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="c233e-143">Specifies the total number of framing errors on the connection.</span></span> <span data-ttu-id="c233e-144">Ein Rahmen Fehler tritt auf, wenn ein asynchrones Zeichen mit einem ungültigen Start-oder Stoppbit empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="c233e-144">A framing error occurs when an asynchronous character is received with an invalid start or stop bit.</span></span>

</dd> <dt>

<span data-ttu-id="c233e-145">**dwbufferoverrunerr**</span><span class="sxs-lookup"><span data-stu-id="c233e-145">**dwBufferOverrunErr**</span></span>
</dt> <dd>

<span data-ttu-id="c233e-146">Gibt die Gesamtanzahl der Pufferüberlauf Fehler für die Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="c233e-146">Specifies the total number of buffer overrun errors on the connection.</span></span> <span data-ttu-id="c233e-147">Ein Pufferüberlauf Fehler tritt auf, wenn der sendende Computer Zeichen schneller überträgt, als er von dem empfangenden Computer aufgenommen werden kann.</span><span class="sxs-lookup"><span data-stu-id="c233e-147">A buffer overrun error occurs when the sending computer is transmitting characters faster than the receiving computer can accommodate them.</span></span> <span data-ttu-id="c233e-148">Wenn dieses Problem weiterhin besteht, verringern Sie die Verbindungs Rate für Bit/s auf dem Client.</span><span class="sxs-lookup"><span data-stu-id="c233e-148">If this problem persists, reduce the BPS connection rate on the client.</span></span>

</dd> <dt>

<span data-ttu-id="c233e-149">**dwbytesxmiteduncompressed**</span><span class="sxs-lookup"><span data-stu-id="c233e-149">**dwBytesXmitedUncompressed**</span></span>
</dt> <dd>

<span data-ttu-id="c233e-150">Gibt die Gesamtanzahl der Bytes an, die von der Verbindung nicht komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="c233e-150">Specifies the total number of bytes transmitted uncompressed by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="c233e-151">**dwbytesrcveduncompressed**</span><span class="sxs-lookup"><span data-stu-id="c233e-151">**dwBytesRcvedUncompressed**</span></span>
</dt> <dd>

<span data-ttu-id="c233e-152">Gibt die Gesamtanzahl der Bytes an, die von der Verbindung nicht komprimiert empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="c233e-152">Specifies the total number of bytes received uncompressed by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="c233e-153">**dwbytesxmitedcompressed**</span><span class="sxs-lookup"><span data-stu-id="c233e-153">**dwBytesXmitedCompressed**</span></span>
</dt> <dd>

<span data-ttu-id="c233e-154">Gibt die Gesamtanzahl von Bytes an, die von der Verbindung komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="c233e-154">Specifies the total number of bytes transmitted compressed by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="c233e-155">**dwbytesrcvedcompressed**</span><span class="sxs-lookup"><span data-stu-id="c233e-155">**dwBytesRcvedCompressed**</span></span>
</dt> <dd>

<span data-ttu-id="c233e-156">Gibt die Gesamtanzahl der Bytes an, die von der Verbindung komprimiert wurden.</span><span class="sxs-lookup"><span data-stu-id="c233e-156">Specifies the total number of bytes received compressed by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="c233e-157">**dwportbytesxgetrennte**</span><span class="sxs-lookup"><span data-stu-id="c233e-157">**dwPortBytesXmited**</span></span>
</dt> <dd>

<span data-ttu-id="c233e-158">Gibt die Gesamtanzahl von Bytes an, die vom Port übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="c233e-158">Specifies the total number of bytes transmitted by the port.</span></span>

</dd> <dt>

<span data-ttu-id="c233e-159">**dwportbytesrcved**</span><span class="sxs-lookup"><span data-stu-id="c233e-159">**dwPortBytesRcved**</span></span>
</dt> <dd>

<span data-ttu-id="c233e-160">Gibt die Gesamtanzahl von Bytes an, die vom Port empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="c233e-160">Specifies the total number of bytes received by the port.</span></span>

</dd> <dt>

<span data-ttu-id="c233e-161">**dwportframesxgetrennte**</span><span class="sxs-lookup"><span data-stu-id="c233e-161">**dwPortFramesXmited**</span></span>
</dt> <dd>

<span data-ttu-id="c233e-162">Gibt die Gesamtanzahl der vom Port übertragenen Frames an.</span><span class="sxs-lookup"><span data-stu-id="c233e-162">Specifies the total number of frames transmitted by the port.</span></span>

</dd> <dt>

<span data-ttu-id="c233e-163">**dwportframesrcved**</span><span class="sxs-lookup"><span data-stu-id="c233e-163">**dwPortFramesRcved**</span></span>
</dt> <dd>

<span data-ttu-id="c233e-164">Gibt die Gesamtanzahl von Frames an, die vom Port empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="c233e-164">Specifies the total number of frames received by the port.</span></span>

</dd> <dt>

<span data-ttu-id="c233e-165">**dwportcrcerr**</span><span class="sxs-lookup"><span data-stu-id="c233e-165">**dwPortCrcErr**</span></span>
</dt> <dd>

<span data-ttu-id="c233e-166">Gibt die Gesamtanzahl von CRC-Fehlern auf dem Port an.</span><span class="sxs-lookup"><span data-stu-id="c233e-166">Specifies the total number of CRC errors on the port.</span></span> <span data-ttu-id="c233e-167">CRC-Fehler werden dadurch verursacht, dass eine zyklische Redundanz Prüfung fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="c233e-167">CRC errors are caused by the failure of a cyclic redundancy check.</span></span> <span data-ttu-id="c233e-168">Ein CRC-Fehler gibt an, dass ein oder mehrere Zeichen im empfangenen Datenpaket beim Eintreffen gegartet wurden.</span><span class="sxs-lookup"><span data-stu-id="c233e-168">A CRC error indicates that one or more characters in the data packet received were found garbled on arrival.</span></span>

</dd> <dt>

<span data-ttu-id="c233e-169">**dwporttimeouterr**</span><span class="sxs-lookup"><span data-stu-id="c233e-169">**dwPortTimeoutErr**</span></span>
</dt> <dd>

<span data-ttu-id="c233e-170">Gibt die Gesamtzahl der Timeout Fehler für den Port an.</span><span class="sxs-lookup"><span data-stu-id="c233e-170">Specifies the total number of time-out errors on the port.</span></span> <span data-ttu-id="c233e-171">Timeout Fehler treten auf, wenn ein erwartetes Zeichen nicht rechtzeitig empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="c233e-171">Time-out errors occur when an expected character is not received in time.</span></span> <span data-ttu-id="c233e-172">Wenn dies der Fall ist, geht die Software davon aus, dass die Daten verloren gegangen sind und fordert, dass Sie erneut gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="c233e-172">When this occurs, the software assumes that the data has been lost and requests that it be resent.</span></span>

</dd> <dt>

<span data-ttu-id="c233e-173">**dwportalignmenterr**</span><span class="sxs-lookup"><span data-stu-id="c233e-173">**dwPortAlignmentErr**</span></span>
</dt> <dd>

<span data-ttu-id="c233e-174">Gibt die Gesamtanzahl der Ausrichtungsfehler für den Port an.</span><span class="sxs-lookup"><span data-stu-id="c233e-174">Specifies the total number of alignment errors on the port.</span></span> <span data-ttu-id="c233e-175">Ausrichtungsfehler treten auf, wenn ein empfangenes Zeichen nicht das erwartete Zeichen ist.</span><span class="sxs-lookup"><span data-stu-id="c233e-175">Alignment errors occur when a character received is not the one expected.</span></span> <span data-ttu-id="c233e-176">Dies geschieht normalerweise, wenn ein Zeichen verloren geht oder ein Timeout Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="c233e-176">This usually happens when a character is lost or when a time-out error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="c233e-177">**dwporthardwareoverrunerr**</span><span class="sxs-lookup"><span data-stu-id="c233e-177">**dwPortHardwareOverrunErr**</span></span>
</dt> <dd>

<span data-ttu-id="c233e-178">Gibt die Gesamtanzahl der Hardware Überlauf Fehler auf dem Port an.</span><span class="sxs-lookup"><span data-stu-id="c233e-178">Specifies the total number of hardware overrun errors on the port.</span></span> <span data-ttu-id="c233e-179">Diese Fehler geben an, wie oft der Sende Computer Zeichen schneller übertragen hat, als die Hardware des empfangenden Computers verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="c233e-179">These errors indicate the number of times the sending computer has transmitted characters faster than the receiving computer hardware can process them.</span></span> <span data-ttu-id="c233e-180">Wenn dieses Problem weiterhin besteht, verringern Sie die Verbindungs Rate für Bit/s auf dem Client.</span><span class="sxs-lookup"><span data-stu-id="c233e-180">If this problem persists, reduce the BPS connection rate on the client.</span></span>

</dd> <dt>

<span data-ttu-id="c233e-181">**dwportframingerr**</span><span class="sxs-lookup"><span data-stu-id="c233e-181">**dwPortFramingErr**</span></span>
</dt> <dd>

<span data-ttu-id="c233e-182">Gibt die Gesamtzahl der Rahmen Fehler an dem Port an.</span><span class="sxs-lookup"><span data-stu-id="c233e-182">Specifies the total number of framing errors on the port.</span></span> <span data-ttu-id="c233e-183">Ein Rahmen Fehler tritt auf, wenn ein asynchrones Zeichen mit einem ungültigen Start-oder Stoppbit empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="c233e-183">A framing error occurs when an asynchronous character is received with an invalid start or stop bit.</span></span>

</dd> <dt>

<span data-ttu-id="c233e-184">**dwportbufferoverrunerr**</span><span class="sxs-lookup"><span data-stu-id="c233e-184">**dwPortBufferOverrunErr**</span></span>
</dt> <dd>

<span data-ttu-id="c233e-185">Gibt die Gesamtanzahl der Pufferüberlauf Fehler auf dem Port an.</span><span class="sxs-lookup"><span data-stu-id="c233e-185">Specifies the total number of buffer overrun errors on the port.</span></span> <span data-ttu-id="c233e-186">Ein Pufferüberlauf Fehler tritt auf, wenn der sendende Computer Zeichen schneller überträgt, als er von dem empfangenden Computer aufgenommen werden kann.</span><span class="sxs-lookup"><span data-stu-id="c233e-186">A buffer overrun error occurs when the sending computer is transmitting characters faster than the receiving computer can accommodate them.</span></span> <span data-ttu-id="c233e-187">Wenn dieses Problem weiterhin besteht, verringern Sie die Verbindungs Rate für Bit/s auf dem Client.</span><span class="sxs-lookup"><span data-stu-id="c233e-187">If this problem persists, reduce the BPS connection rate on the client.</span></span>

</dd> <dt>

<span data-ttu-id="c233e-188">**dwportbytesxmiteduncompressed**</span><span class="sxs-lookup"><span data-stu-id="c233e-188">**dwPortBytesXmitedUncompressed**</span></span>
</dt> <dd>

<span data-ttu-id="c233e-189">Gibt die Gesamtanzahl der Bytes an, die vom Port nicht komprimiert gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="c233e-189">Specifies the total number of bytes transmitted uncompressed by the port.</span></span> <span data-ttu-id="c233e-190">Wenn der Port Teil einer Verbindung mit mehreren Links ist, ist dieser Member ungültig.</span><span class="sxs-lookup"><span data-stu-id="c233e-190">If the port is part of a multilink connection, this member is not valid.</span></span> <span data-ttu-id="c233e-191">Verwenden Sie stattdessen die Komprimierungs Statistik für die Verbindung.</span><span class="sxs-lookup"><span data-stu-id="c233e-191">Use the compression statistics for the connection instead.</span></span>

</dd> <dt>

<span data-ttu-id="c233e-192">**dwportbytesrcveduncompressed**</span><span class="sxs-lookup"><span data-stu-id="c233e-192">**dwPortBytesRcvedUncompressed**</span></span>
</dt> <dd>

<span data-ttu-id="c233e-193">Gibt die Gesamtanzahl der Bytes an, die vom Port nicht komprimiert empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="c233e-193">Specifies the total number of bytes received uncompressed by the port.</span></span> <span data-ttu-id="c233e-194">Wenn der Port Teil einer Verbindung mit mehreren Links ist, ist dieser Member ungültig.</span><span class="sxs-lookup"><span data-stu-id="c233e-194">If the port is part of a multilink connection, this member is not valid.</span></span> <span data-ttu-id="c233e-195">Verwenden Sie stattdessen die Komprimierungs Statistik für die Verbindung.</span><span class="sxs-lookup"><span data-stu-id="c233e-195">Use the compression statistics for the connection instead.</span></span>

</dd> <dt>

<span data-ttu-id="c233e-196">**dwportbytesxmitedcompressed**</span><span class="sxs-lookup"><span data-stu-id="c233e-196">**dwPortBytesXmitedCompressed**</span></span>
</dt> <dd>

<span data-ttu-id="c233e-197">Gibt die Gesamtanzahl von Bytes an, die vom Port komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="c233e-197">Specifies the total number of bytes transmitted compressed by the port.</span></span> <span data-ttu-id="c233e-198">Wenn der Port Teil einer Verbindung mit mehreren Links ist, ist dieser Member ungültig.</span><span class="sxs-lookup"><span data-stu-id="c233e-198">If the port is part of a multilink connection, this member is not valid.</span></span> <span data-ttu-id="c233e-199">Verwenden Sie stattdessen die Komprimierungs Statistik für die Verbindung.</span><span class="sxs-lookup"><span data-stu-id="c233e-199">Use the compression statistics for the connection instead.</span></span>

</dd> <dt>

<span data-ttu-id="c233e-200">**dwportbytesrcvedcompressed**</span><span class="sxs-lookup"><span data-stu-id="c233e-200">**dwPortBytesRcvedCompressed**</span></span>
</dt> <dd>

<span data-ttu-id="c233e-201">Gibt die Gesamtanzahl der Bytes an, die vom Port komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="c233e-201">Specifies the total number of bytes received compressed by the port.</span></span> <span data-ttu-id="c233e-202">Wenn der Port Teil einer Verbindung mit mehreren Links ist, ist dieser Member ungültig.</span><span class="sxs-lookup"><span data-stu-id="c233e-202">If the port is part of a multilink connection, this member is not valid.</span></span> <span data-ttu-id="c233e-203">Verwenden Sie stattdessen die Komprimierungs Statistik für die Verbindung.</span><span class="sxs-lookup"><span data-stu-id="c233e-203">Use the compression statistics for the connection instead.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c233e-204">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c233e-204">Requirements</span></span>



| <span data-ttu-id="c233e-205">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c233e-205">Requirement</span></span> | <span data-ttu-id="c233e-206">Wert</span><span class="sxs-lookup"><span data-stu-id="c233e-206">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c233e-207">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c233e-207">Minimum supported client</span></span><br/> | <span data-ttu-id="c233e-208">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c233e-208">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c233e-209">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c233e-209">Minimum supported server</span></span><br/> | <span data-ttu-id="c233e-210">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c233e-210">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c233e-211">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="c233e-211">End of client support</span></span><br/>    | <span data-ttu-id="c233e-212">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c233e-212">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="c233e-213">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="c233e-213">End of server support</span></span><br/>    | <span data-ttu-id="c233e-214">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c233e-214">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="c233e-215">Header</span><span class="sxs-lookup"><span data-stu-id="c233e-215">Header</span></span><br/>                   | <dl> <span data-ttu-id="c233e-216"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c233e-216"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c233e-217">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c233e-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c233e-218">Remote Zugriffs Dienst (RAS) (Übersicht)</span><span class="sxs-lookup"><span data-stu-id="c233e-218">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="c233e-219">RAS-Server-Verwaltungsstrukturen</span><span class="sxs-lookup"><span data-stu-id="c233e-219">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="c233e-220">**RAS- \_ Port \_ 0**</span><span class="sxs-lookup"><span data-stu-id="c233e-220">**RAS\_PORT\_0**</span></span>](ras-port-0-str.md)
</dt> <dt>

[<span data-ttu-id="c233e-221">**Rasadminakzeptnewconnection**</span><span class="sxs-lookup"><span data-stu-id="c233e-221">**RasAdminAcceptNewConnection**</span></span>](rasadminacceptnewconnection.md)
</dt> <dt>

[<span data-ttu-id="c233e-222">**Rasadminconnectionhangupnotification**</span><span class="sxs-lookup"><span data-stu-id="c233e-222">**RasAdminConnectionHangupNotification**</span></span>](rasadminconnectionhangupnotification.md)
</dt> <dt>

[<span data-ttu-id="c233e-223">**Rasadminportclearstatistics**</span><span class="sxs-lookup"><span data-stu-id="c233e-223">**RasAdminPortClearStatistics**</span></span>](rasadminportclearstatistics.md)
</dt> <dt>

[<span data-ttu-id="c233e-224">**Rasadminportgetinfo**</span><span class="sxs-lookup"><span data-stu-id="c233e-224">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





