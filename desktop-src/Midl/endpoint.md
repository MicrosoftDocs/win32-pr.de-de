---
title: Endpunkt Attribut
description: Das Attribut \ Endpoint \ gibt einen bekannten Port oder Ports (Kommunikations Endpunkte) an, auf denen Server der Schnittstelle auf Aufrufe lauschen.
ms.assetid: b88c5a97-b726-43de-b5b6-649cda60c320
keywords:
- Endpunkt Attribut-Mittel l
topic_type:
- apiref
api_name:
- endpoint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4383df496a791859f7249766f0dbb59266d28e93
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858175"
---
# <a name="endpoint-attribute"></a><span data-ttu-id="d55cf-104">Endpunkt Attribut</span><span class="sxs-lookup"><span data-stu-id="d55cf-104">endpoint attribute</span></span>

<span data-ttu-id="d55cf-105">Das **\[ Endpunkt \]** Attribut gibt einen bekannten Port oder Ports (Kommunikations Endpunkte) an, auf denen Server der Schnittstelle auf Aufrufe lauschen.</span><span class="sxs-lookup"><span data-stu-id="d55cf-105">The **\[endpoint\]** attribute specifies a well-known port or ports (communication endpoints) on which servers of the interface listen for calls.</span></span>

``` syntax
endpoint("protocol-sequence:[endpoint-port]" [ , ...] )
```

## <a name="parameters"></a><span data-ttu-id="d55cf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d55cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d55cf-107">*Protokoll Sequenz*</span><span class="sxs-lookup"><span data-stu-id="d55cf-107">*protocol-sequence*</span></span> 
</dt> <dd>

<span data-ttu-id="d55cf-108">Gibt eine Zeichenfolge an, die eine gültige Kombination eines RPC-Protokolls (z. b. "ncacn"), eines Transport Protokolls (z. b. "TCP") und eines Netzwerk Protokolls (z. b. "IP") darstellt.</span><span class="sxs-lookup"><span data-stu-id="d55cf-108">Specifies a character string that represents a valid combination of an RPC protocol (such as "ncacn"), a transport protocol (such as "tcp"), and a network protocol (such as "ip").</span></span> <span data-ttu-id="d55cf-109">Eine Liste der gültigen Protokoll Sequenzen finden Sie unter [Protokoll Sequenz Konstanten](/windows/desktop/Rpc/protocol-sequence-constants).</span><span class="sxs-lookup"><span data-stu-id="d55cf-109">For a list of valid protocol sequences, see [Protocol Sequence Constants](/windows/desktop/Rpc/protocol-sequence-constants).</span></span>

</dd> <dt>

<span data-ttu-id="d55cf-110">*Endpunkt-Port*</span><span class="sxs-lookup"><span data-stu-id="d55cf-110">*endpoint-port*</span></span> 
</dt> <dd>

<span data-ttu-id="d55cf-111">Gibt eine Zeichenfolge an, die die Endpunkt Bezeichnung für die angegebene Protokollfamilie darstellt.</span><span class="sxs-lookup"><span data-stu-id="d55cf-111">Specifies a string that represents the endpoint designation for the specified protocol family.</span></span> <span data-ttu-id="d55cf-112">Die Syntax der Port Zeichenfolge ist spezifisch für jede Protokoll Sequenz.</span><span class="sxs-lookup"><span data-stu-id="d55cf-112">The syntax of the port string is specific to each protocol sequence.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d55cf-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d55cf-113">Remarks</span></span>

<span data-ttu-id="d55cf-114">Das **\[ Endpunkt \]** Attribut gibt eine Transport Familie an, z. b. das Verbindungs orientierte TCP/IP-Protokoll, ein NetBIOS-Verbindungs orientiertes Protokoll oder das Verbindungs orientierte Named Pipe-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="d55cf-114">The **\[endpoint\]** attribute specifies a transport family such as the TCP/IP connection-oriented protocol, a NetBIOS connection-oriented protocol, or the named-pipe connection-oriented protocol.</span></span> <span data-ttu-id="d55cf-115">Die Verwendung des **\[ Endpunkt \]** Attributs ist mit anderen Methoden zum Hinzufügen eines Endpunkts konsistent und bietet keine zusätzlichen oder speziellen Dienste für den Endpunkt. er bietet lediglich eine Verknüpfung zum Aufrufen der API.</span><span class="sxs-lookup"><span data-stu-id="d55cf-115">Use of the **\[endpoint\]** attribute is consistent with other methods for adding an endpoint, and does not provide additional or special services for the endpoint; it simply provides a shortcut for calling the API.</span></span>

> [!Note]  
> <span data-ttu-id="d55cf-116">Angeben eines Endpunkts in. Die IDL-Schnittstellen Definition schränkt den Zugriff auf die-Schnittstelle nicht auf den angegebenen Endpunkt ein.</span><span class="sxs-lookup"><span data-stu-id="d55cf-116">Specifying an endpoint in the .IDL interface definition does not restrict access to the interface to the specified endpoint.</span></span> <span data-ttu-id="d55cf-117">Hinzufügen eines Endpunkts zu. Mithilfe der IDL-Schnittstellen Definition kann die Schnittstelle über einen beliebigen Endpunkt in diesem Prozess aufgerufen werden, und der Endpunkt kann verwendet werden, um andere Schnittstellen in diesem Prozess aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d55cf-117">Adding an endpoint to the .IDL interface definition allows the interface to be called through any endpoint in that process, and allows the endpoint to be used to call other interfaces in that process.</span></span>

 

<span data-ttu-id="d55cf-118">Der *Protokoll Sequenz* Wert bestimmt die gültigen Werte für den *Endpunkt-Port*.</span><span class="sxs-lookup"><span data-stu-id="d55cf-118">The *protocol-sequence* value determines the valid values for the *endpoint-port*.</span></span> <span data-ttu-id="d55cf-119">Der mittlerer l-Compiler prüft nur die allgemeine Syntax für den *Endpunkt-Port-* Eintrag.</span><span class="sxs-lookup"><span data-stu-id="d55cf-119">The MIDL compiler checks only general syntax for the *endpoint-port* entry.</span></span> <span data-ttu-id="d55cf-120">Port Spezifikations Fehler werden von den Laufzeitbibliotheken gemeldet.</span><span class="sxs-lookup"><span data-stu-id="d55cf-120">Port specification errors are reported by the run-time libraries.</span></span> <span data-ttu-id="d55cf-121">Informationen zu den zulässigen Werten für jede Protokoll Sequenz finden Sie unter den [Protokoll Sequenz Konstanten](/windows/desktop/Rpc/protocol-sequence-constants).</span><span class="sxs-lookup"><span data-stu-id="d55cf-121">For information about the allowed values for each protocol sequence, see the [Protocol Sequence Constants](/windows/desktop/Rpc/protocol-sequence-constants).</span></span>

<span data-ttu-id="d55cf-122">Die folgenden durch DCE angegebenen Protokoll Sequenzen werden von dem mit Microsoft RPC: **ncacn \_ OSI \_ DNA** und **ncadg \_ DDS** bereitgestellten Mittell-Compiler nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d55cf-122">The following protocol sequences specified by DCE are not supported by the MIDL compiler provided with Microsoft RPC: **ncacn\_osi\_dna** and **ncadg\_dds**.</span></span>

<span data-ttu-id="d55cf-123">Stellen Sie sicher, dass Sie umgekehrte Schrägstriche in Endpunkten ordnungsgemäß angeben.</span><span class="sxs-lookup"><span data-stu-id="d55cf-123">Make sure that you correctly quote backslash characters in endpoints.</span></span> <span data-ttu-id="d55cf-124">Dieser Fehler tritt häufig auf, wenn der Endpunkt eine Named Pipe ist.</span><span class="sxs-lookup"><span data-stu-id="d55cf-124">This error commonly occurs when the endpoint is a named pipe.</span></span>

<span data-ttu-id="d55cf-125">Die in der IDL-Datei angegebenen Endpunkt Informationen werden von den RPC-Lauf Zeitfunktionen [**rpcserveruseprotabqif**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif) und [**rpcserveruseallprotsqsif**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif)verwendet.</span><span class="sxs-lookup"><span data-stu-id="d55cf-125">Endpoint information specified in the IDL file is used by the RPC run-time functions [**RpcServerUseProtseqIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif) and [**RpcServerUseAllProtseqsIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif).</span></span>

## <a name="examples"></a><span data-ttu-id="d55cf-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d55cf-126">Examples</span></span>

``` syntax
endpoint("ncacn_np:[\\pipe\\rainier]") 

endpoint("ncacn_ip_tcp:[1044]", "ncacn_np:[\\pipe\\shasta]")
```

## <a name="see-also"></a><span data-ttu-id="d55cf-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d55cf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d55cf-128">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="d55cf-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="d55cf-129">**Rpcserveruseallprotabqsif**</span><span class="sxs-lookup"><span data-stu-id="d55cf-129">**RpcServerUseAllProtseqsIf**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif)
</dt> <dt>

[<span data-ttu-id="d55cf-130">**Rpcserveruseprotabqif**</span><span class="sxs-lookup"><span data-stu-id="d55cf-130">**RpcServerUseProtseqIf**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif)
</dt> </dl>

 

 