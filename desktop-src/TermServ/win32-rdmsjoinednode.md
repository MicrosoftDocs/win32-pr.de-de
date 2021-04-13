---
title: Win32_RDMSJoinedNode-Klasse
description: Stellt einen Server Knoten dar, der von Remotedesktop Verwaltungsdienste (RDMs) verwaltet wird.
ms.assetid: 8751f3f7-dfb5-45bd-a6b1-758aa22a3569
ms.tgt_platform: multiple
keywords:
- Win32_RDMSJoinedNode-Klasse Remotedesktopdienste
- Win32_RDMSJoinedNode Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode
- Win32_RDMSJoinedNode.FQDN
- Win32_RDMSJoinedNode.SID
- Win32_RDMSJoinedNode.OSVersion
- Win32_RDMSJoinedNode.IsRdcb
- Win32_RDMSJoinedNode.IsRdg
- Win32_RDMSJoinedNode.IsRdls
- Win32_RDMSJoinedNode.IsRdvh
- Win32_RDMSJoinedNode.IsRdwa
- Win32_RDMSJoinedNode.IsRdsh
- Win32_RDMSJoinedNode.IsWebAccessCertificateInstalled
- Win32_RDMSJoinedNode.IsGatewayCertificateInstalled
- Win32_RDMSJoinedNode.IsRedirectorCertificateInstalled
- Win32_RDMSJoinedNode.IsPublishingCertificateInstalled
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cabf1cf7ff98b698624285b2877412c4323259b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391564"
---
# <a name="win32_rdmsjoinednode-class"></a><span data-ttu-id="5c99b-105">Win32 \_ rdmsjoinednode-Klasse</span><span class="sxs-lookup"><span data-stu-id="5c99b-105">Win32\_RDMSJoinedNode class</span></span>

<span data-ttu-id="5c99b-106">Stellt einen Server Knoten dar, der von Remotedesktop Verwaltungsdienste (RDMs) verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="5c99b-106">Represents a server node that is managed by Remote Desktop Management Services (RDMS).</span></span>

<span data-ttu-id="5c99b-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5c99b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c99b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c99b-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSJoinedNode
{
  string  FQDN;
  string  SID;
  String  OSVersion;
  boolean IsRdcb;
  boolean IsRdg;
  boolean IsRdls;
  boolean IsRdvh;
  boolean IsRdwa;
  boolean IsRdsh;
  boolean IsWebAccessCertificateInstalled;
  boolean IsGatewayCertificateInstalled;
  boolean IsRedirectorCertificateInstalled;
  boolean IsPublishingCertificateInstalled;
};
```

## <a name="members"></a><span data-ttu-id="5c99b-109">Member</span><span class="sxs-lookup"><span data-stu-id="5c99b-109">Members</span></span>

<span data-ttu-id="5c99b-110">Die **Win32 \_ rdmsjoinednode** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5c99b-110">The **Win32\_RDMSJoinedNode** class has these types of members:</span></span>

-   [<span data-ttu-id="5c99b-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="5c99b-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="5c99b-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5c99b-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5c99b-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="5c99b-113">Methods</span></span>

<span data-ttu-id="5c99b-114">Die **Win32 \_ rdmsjoinednode** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="5c99b-114">The **Win32\_RDMSJoinedNode** class has these methods.</span></span>



| <span data-ttu-id="5c99b-115">Methode</span><span class="sxs-lookup"><span data-stu-id="5c99b-115">Method</span></span>                                                                | <span data-ttu-id="5c99b-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5c99b-116">Description</span></span>                                                                                                                                                                                           |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c99b-117">**Getjoinednoentcount**</span><span class="sxs-lookup"><span data-stu-id="5c99b-117">**GetJoinedNodeCount**</span></span>](win32-rdmsjoinednode-getjoinednodecount.md) | <span data-ttu-id="5c99b-118">**Windows Server 2012 R2 und Windows Server 2012:** Diese Methode ist vor Windows Server 2016 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5c99b-118">**Windows Server 2012 R2 and Windows Server 2012:** This method is unavailable prior to Windows Server 2016.</span></span><br/> <span data-ttu-id="5c99b-119">Ruft die Anzahl der Server ab, auf denen die angegebene Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="5c99b-119">Gets the number of servers that have the specified role installed.</span></span><br/> |
| [<span data-ttu-id="5c99b-120">**Join**</span><span class="sxs-lookup"><span data-stu-id="5c99b-120">**Join**</span></span>](join-win32-rdmsjoinednode.md)                             | <span data-ttu-id="5c99b-121">Fügt RDMs einen Knoten hinzu.</span><span class="sxs-lookup"><span data-stu-id="5c99b-121">Adds a node to RDMS.</span></span><br/>                                                                                                                                                                       |
| [<span data-ttu-id="5c99b-122">**Entfernen**</span><span class="sxs-lookup"><span data-stu-id="5c99b-122">**Unjoin**</span></span>](unjoin-win32-rdmsjoinednode.md)                         | <span data-ttu-id="5c99b-123">Entfernt einen Knoten aus RDMs.</span><span class="sxs-lookup"><span data-stu-id="5c99b-123">Removes a node from RDMS.</span></span><br/>                                                                                                                                                                  |



 

### <a name="properties"></a><span data-ttu-id="5c99b-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5c99b-124">Properties</span></span>

<span data-ttu-id="5c99b-125">Die **Win32 \_ rdmsjoinednode** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5c99b-125">The **Win32\_RDMSJoinedNode** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5c99b-126">**FQDN**</span><span class="sxs-lookup"><span data-stu-id="5c99b-126">**FQDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c99b-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5c99b-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c99b-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5c99b-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c99b-129">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5c99b-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5c99b-130">Ruft den voll qualifizierten Domänen Namen des Knotens ab.</span><span class="sxs-lookup"><span data-stu-id="5c99b-130">Gets the fully qualified domain name of the node.</span></span>

</dd> <dt>

<span data-ttu-id="5c99b-131">**Isgatewaycertifigateinstemmt**</span><span class="sxs-lookup"><span data-stu-id="5c99b-131">**IsGatewayCertificateInstalled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c99b-132">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="5c99b-132">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c99b-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5c99b-133">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5c99b-134">Dient zum Abrufen und Festlegen eines Werts, der angibt, ob der Server über ein Zertifikat zum Durchführen der Authentifizierung für Remotedesktop Gateway-Verbindungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="5c99b-134">Gets and sets a value that indicates whether the server has a certificate to perform authentication for Remote Desktop gateway connections.</span></span> <span data-ttu-id="5c99b-135">**True** , wenn das Zertifikat installiert ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="5c99b-135">**TRUE** if the certificate is installed; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="5c99b-136">**Ispublishingcertifi.**</span><span class="sxs-lookup"><span data-stu-id="5c99b-136">**IsPublishingCertificateInstalled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c99b-137">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="5c99b-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c99b-138">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5c99b-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5c99b-139">Ruft einen Wert ab, der angibt, ob der Server über ein Zertifikat zum Signieren Remotedesktopprotokoll Veröffentlichungs Dateien verfügt, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="5c99b-139">Gets and sets a value that indicates whether the server has a certificate to sign Remote Desktop Protocol publishing files.</span></span> <span data-ttu-id="5c99b-140">**True** , wenn das Zertifikat installiert ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="5c99b-140">**TRUE** if the certificate is installed; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="5c99b-141">**Isrdcb**</span><span class="sxs-lookup"><span data-stu-id="5c99b-141">**IsRdcb**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c99b-142">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="5c99b-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c99b-143">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5c99b-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5c99b-144">Ruft einen Wert ab, der angibt, ob der Server Remotedesktopverbindung Broker ist, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="5c99b-144">Gets and sets a value that indicates whether the server is Remote Desktop Connection Broker.</span></span> <span data-ttu-id="5c99b-145">**True** , wenn es sich bei dem Server um einen Remotedesktopverbindung Broker handelt. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="5c99b-145">**TRUE** if the server is a Remote Desktop Connection Broker; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="5c99b-146">**Isrdg**</span><span class="sxs-lookup"><span data-stu-id="5c99b-146">**IsRdg**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c99b-147">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="5c99b-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c99b-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5c99b-148">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5c99b-149">Ruft einen Wert ab, der angibt, ob der Server Remotedesktop Gatewayserver ist, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="5c99b-149">Gets and sets a value that indicates whether the server is Remote Desktop gateway server.</span></span> <span data-ttu-id="5c99b-150">**True** , wenn der Server ein Remotedesktop Gatewayserver ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="5c99b-150">**TRUE** if the server is a Remote Desktop gateway server; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="5c99b-151">**Isrdls**</span><span class="sxs-lookup"><span data-stu-id="5c99b-151">**IsRdls**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c99b-152">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="5c99b-152">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c99b-153">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5c99b-153">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5c99b-154">Ruft einen Wert ab, der angibt, ob der Server Remotedesktop Lizenzserver ist, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="5c99b-154">Gets and sets a value that indicates whether the server is Remote Desktop license server.</span></span> <span data-ttu-id="5c99b-155">**True** , wenn es sich bei dem Server um einen Remotedesktop Lizenzserver handelt. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="5c99b-155">**TRUE** if the server is a Remote Desktop license server; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="5c99b-156">**Isrdsh**</span><span class="sxs-lookup"><span data-stu-id="5c99b-156">**IsRdsh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c99b-157">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="5c99b-157">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c99b-158">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5c99b-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5c99b-159">Ruft einen Wert ab, der angibt, ob der Server Remotedesktop-Sitzungs Host Servers ist, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="5c99b-159">Gets and sets a value that indicates whether the server is Remote Desktop session host server.</span></span> <span data-ttu-id="5c99b-160">**True** , wenn der Server ein Remotedesktop-Sitzungs Host Server ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="5c99b-160">**TRUE** if the server is a Remote Desktop session host server; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="5c99b-161">**Isrdvh**</span><span class="sxs-lookup"><span data-stu-id="5c99b-161">**IsRdvh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c99b-162">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="5c99b-162">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c99b-163">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5c99b-163">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5c99b-164">Dient zum Abrufen und Festlegen eines Werts, der angibt, ob der Server Remotedesktop Virtualisierungshost ist.</span><span class="sxs-lookup"><span data-stu-id="5c99b-164">Gets and sets a value that indicates whether the server is Remote Desktop virtualization host.</span></span> <span data-ttu-id="5c99b-165">**True** , wenn der Server ein Remotedesktop Virtualisierungshost ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="5c99b-165">**TRUE** if the server is a Remote Desktop virtualization host; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="5c99b-166">**Isrdwa**</span><span class="sxs-lookup"><span data-stu-id="5c99b-166">**IsRdwa**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c99b-167">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="5c99b-167">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c99b-168">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5c99b-168">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5c99b-169">Ruft einen Wert ab, der angibt, ob der Server Remotedesktop Web Access-Server ist, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="5c99b-169">Gets and sets a value that indicates whether the server is Remote Desktop web access server.</span></span> <span data-ttu-id="5c99b-170">**True** , wenn der Server ein Remotedesktop Webzugriff Server ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="5c99b-170">**TRUE** if the server is a Remote Desktop Web Access server; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="5c99b-171">**Isredirector Certifi.**</span><span class="sxs-lookup"><span data-stu-id="5c99b-171">**IsRedirectorCertificateInstalled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c99b-172">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="5c99b-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c99b-173">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5c99b-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5c99b-174">Dient zum Abrufen und Festlegen eines Werts, der angibt, ob der Server über ein Zertifikat zum Durchführen der Authentifizierung für Remotedesktopdienste Bereitstellung verfügt.</span><span class="sxs-lookup"><span data-stu-id="5c99b-174">Gets and sets a value that indicates whether the server has a certificate to perform authentication for Remote Desktop Services deployment.</span></span> <span data-ttu-id="5c99b-175">**True** , wenn das Zertifikat installiert ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="5c99b-175">**TRUE** if the certificate is installed; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="5c99b-176">**Iswebaccesscertifierstemmt**</span><span class="sxs-lookup"><span data-stu-id="5c99b-176">**IsWebAccessCertificateInstalled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c99b-177">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="5c99b-177">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c99b-178">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5c99b-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5c99b-179">Ruft einen Wert ab, der angibt, ob der Server über ein Zertifikat zum Ausführen der Authentifizierung für Remotedesktop Webzugriff verfügt, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="5c99b-179">Gets and sets a value that indicates whether the server has a certificate to perform authentication for Remote Desktop Web Access.</span></span> <span data-ttu-id="5c99b-180">**True** , wenn das Zertifikat installiert ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="5c99b-180">**TRUE** if the certificate is installed; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="5c99b-181">**OSVersion**</span><span class="sxs-lookup"><span data-stu-id="5c99b-181">**OSVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c99b-182">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5c99b-182">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="5c99b-183">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5c99b-183">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5c99b-184">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5c99b-184">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5c99b-185">Ruft die Version der Betriebssysteme auf dem Knoten ab und legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="5c99b-185">Gets and sets the version of the operating systems on the node.</span></span>

</dd> <dt>

<span data-ttu-id="5c99b-186">**SID**</span><span class="sxs-lookup"><span data-stu-id="5c99b-186">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c99b-187">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5c99b-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c99b-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5c99b-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c99b-189">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5c99b-189">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5c99b-190">Ruft die Sicherheits-ID (SID) des Knotens ab.</span><span class="sxs-lookup"><span data-stu-id="5c99b-190">Gets the security identifier (SID) of the node.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5c99b-191">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c99b-191">Requirements</span></span>



| <span data-ttu-id="5c99b-192">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5c99b-192">Requirement</span></span> | <span data-ttu-id="5c99b-193">Wert</span><span class="sxs-lookup"><span data-stu-id="5c99b-193">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c99b-194">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5c99b-194">Minimum supported client</span></span><br/> | <span data-ttu-id="5c99b-195">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5c99b-195">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="5c99b-196">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5c99b-196">Minimum supported server</span></span><br/> | <span data-ttu-id="5c99b-197">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5c99b-197">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="5c99b-198">Namespace</span><span class="sxs-lookup"><span data-stu-id="5c99b-198">Namespace</span></span><br/>                | <span data-ttu-id="5c99b-199">Root \\ CIMV2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="5c99b-199">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="5c99b-200">MOF</span><span class="sxs-lookup"><span data-stu-id="5c99b-200">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5c99b-201"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5c99b-201"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="5c99b-202">DLL</span><span class="sxs-lookup"><span data-stu-id="5c99b-202">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c99b-203"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c99b-203"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="5c99b-204">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c99b-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c99b-205">Remotedesktop Management Services-Anbieter</span><span class="sxs-lookup"><span data-stu-id="5c99b-205">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

