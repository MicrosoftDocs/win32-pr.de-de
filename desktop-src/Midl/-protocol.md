---
title: /Protocol-Schalter
description: Der/Protocol-Schalter gibt an, welches Wire-Protokoll vom generierten Stub unterstützt wird.
ms.assetid: b565b30c-72e5-442b-9588-324b9041524b
keywords:
- /Protocol-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /protocol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9770fa94d010e21dcbd2a5574a0cffe29273a23
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104313025"
---
# <a name="protocol-switch"></a><span data-ttu-id="1aa28-104">/Protocol-Schalter</span><span class="sxs-lookup"><span data-stu-id="1aa28-104">/protocol switch</span></span>

<span data-ttu-id="1aa28-105">Der **/Protocol** -Schalter gibt an, welches Wire-Protokoll vom generierten Stub unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="1aa28-105">The **/protocol** switch specifies which wire protocol is supported by the generated stub.</span></span>

``` syntax
midl /protocol (dce | ndr64 | all)
```

## <a name="switch-options"></a><span data-ttu-id="1aa28-106">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="1aa28-106">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="dce"></span><span id="DCE"></span>

<span data-ttu-id="1aa28-107"><span id="dce"></span><span id="DCE"></span>DCE \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="1aa28-107"><span id="dce"></span><span id="DCE"></span>\*\*\*\*dce\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="1aa28-108">Der generierte Stub unterstützt nur das DCE-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="1aa28-108">The generated stub supports DCE protocol only.</span></span>

</dd> <dt>

<span id="ndr64"></span><span id="NDR64"></span>

<span data-ttu-id="1aa28-109"><span id="ndr64"></span><span id="NDR64"></span>ndr64\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="1aa28-109"><span id="ndr64"></span><span id="NDR64"></span>\*\*\*\*ndr64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="1aa28-110">Der generierte Stub unterstützt nur das Microsoft NDR64-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="1aa28-110">The generated stub supports Microsoft NDR64 protocol only.</span></span>

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span data-ttu-id="1aa28-111"><span id="all"></span><span id="ALL"></span>Alle \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="1aa28-111"><span id="all"></span><span id="ALL"></span>\*\*\*\*all\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="1aa28-112">Der generierte Stub unterstützt alle verfügbaren Protokolle für eine bestimmte Umgebung.</span><span class="sxs-lookup"><span data-stu-id="1aa28-112">The generated stub supports all available protocols for a given environment.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1aa28-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1aa28-113">Remarks</span></span>

<span data-ttu-id="1aa28-114">RPC marshallt und entmarshallt Daten gemäß einem Strict-Übertragungsprotokoll (auch Übertragungs Syntax genannt), das die Daten Übertragungs Darstellung definiert, wie z. b. die Reihenfolge, in der Datenmember gemarshallt werden, die Ausrichtung der Daten im Netzwerk, zusätzliche Informationen, die in den Daten enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="1aa28-114">RPC marshals and unmarshals data according to a strict wire protocol, also called transfer syntax, that defines data wire representation such as the order in which data members are marshaled, the alignment of data on the wire, additional information included with the data, among others.</span></span> <span data-ttu-id="1aa28-115">Microsoft RPC ist mit dem Protokoll von OSF-DCE (Netzwerkdaten Darstellung) kompatibel.</span><span class="sxs-lookup"><span data-stu-id="1aa28-115">Microsoft RPC is compatible with OSF DCE's NDR (network data representation) protocol.</span></span> <span data-ttu-id="1aa28-116">In der 64-Bit-Version von Windows XP führt Microsoft ein experimentelles Protokoll NDR64 ein, das für die Übertragung von 64-Bit-Daten optimiert ist.</span><span class="sxs-lookup"><span data-stu-id="1aa28-116">In the 64-bit release of Windows XP, Microsoft introduces an experimental protocol NDR64 that is optimized for transferring 64-bit data.</span></span> <span data-ttu-id="1aa28-117">NDR64 ist nicht abwärts kompatibel mit dem DCE-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="1aa28-117">NDR64 is not backward compatible with the DCE protocol.</span></span>

<span data-ttu-id="1aa28-118">Das **DCE** -Protokoll ist mit der NDR-Übertragungs Syntax von OSF DCE kompatibel.</span><span class="sxs-lookup"><span data-stu-id="1aa28-118">The **dce** protocol is compatible with OSF DCE's NDR transfer syntax.</span></span> <span data-ttu-id="1aa28-119">Dieses Protokoll ist für die Übertragung von 32-Bit-Daten optimiert.</span><span class="sxs-lookup"><span data-stu-id="1aa28-119">This protocol is optimized for transferring 32-bit data.</span></span>

<span data-ttu-id="1aa28-120">Das **ndr64** -Protokoll wird zurzeit nur unterstützt, wenn es in Verbindung mit dem [**/Win64**](-win64.md) -Switch verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1aa28-120">The **ndr64** protocol is currently supported only when used in conjunction with the [**/win64**](-win64.md) switch.</span></span> <span data-ttu-id="1aa28-121">Wenn ein ndr64 only-Client versucht, eine Verbindung mit einem nur DCE-Server herzustellen (oder umgekehrt), wird der Aufruf mit der \_ \_ nicht unterstützten Transaktionsdatei RPC S abgelehnt \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1aa28-121">If a ndr64 only client tries to connect to a dce-only server, or vice versa, the call is rejected with RPC\_S\_UNSUPPORTED\_TRANS\_SYN.</span></span>

<span data-ttu-id="1aa28-122">Mit der Option **all** wird ein Stub erstellt, von dem jedes verfügbare Protokoll verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="1aa28-122">The **all** option creates a stub that may use any available protocol.</span></span> <span data-ttu-id="1aa28-123">Bei 32-Bit-stubwerten ist das einzige derzeit verfügbare Protokoll DCE.</span><span class="sxs-lookup"><span data-stu-id="1aa28-123">For 32-bit stubs, the only protocol currently available is DCE.</span></span> <span data-ttu-id="1aa28-124">Bei 64-Bit-stubwerten, die mit dem Schalter [**/Win64**](-win64.md) erstellt wurden, sind sowohl DCE als auch NDR64 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1aa28-124">For 64-bit stubs, created using the [**/win64**](-win64.md) switch, both DCE and NDR64 are available.</span></span>

## <a name="examples"></a><span data-ttu-id="1aa28-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1aa28-125">Examples</span></span>

<span data-ttu-id="1aa28-126">**Mittel l/Protocol alle/Win64 filename. idl**</span><span class="sxs-lookup"><span data-stu-id="1aa28-126">**midl /protocol all /win64 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="1aa28-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1aa28-127">See also</span></span>

<dl> <dt>

[**/<system>**](-system-.md)
</dt> </dl>

 

 




