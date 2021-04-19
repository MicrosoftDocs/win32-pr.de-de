---
description: Der Adress Filter benachrichtigt den Netzwerkmonitor Treiber, Frames zu akzeptieren, die über eine Vielzahl von angegebenen Mac-Adresstypen verfügen (Ethernet, TokenRing und FDDI).
ms.assetid: 23a38f49-2d63-4fc8-8113-29143493359c
title: Schreiben des "adresssstable"-Filter Teils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b06b00d046d555dffc39561b817629f4f47ca4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362930"
---
# <a name="writing-addresstable-filter-portion"></a><span data-ttu-id="4b5a8-103">Schreiben des "adresssstable"-Filter Teils</span><span class="sxs-lookup"><span data-stu-id="4b5a8-103">Writing ADDRESSTABLE Filter Portion</span></span>

<span data-ttu-id="4b5a8-104">Der Adress Filter benachrichtigt den Netzwerkmonitor Treiber, Frames zu akzeptieren, die über eine Vielzahl von angegebenen Mac-Adresstypen verfügen (Ethernet, TokenRing und FDDI).</span><span class="sxs-lookup"><span data-stu-id="4b5a8-104">The address filter notifies the Network Monitor driver to accept frames that have one of a variety of specified MAC address types (Ethernet, Token Ring, and FDDI).</span></span> <span data-ttu-id="4b5a8-105">Sie können maximal acht Adress Paare angeben.</span><span class="sxs-lookup"><span data-stu-id="4b5a8-105">You can specify a maximum of eight address pairs.</span></span> <span data-ttu-id="4b5a8-106">Ein Adress Paar kann eine Quelle, ein Ziel, beides oder keines von beiden angeben.</span><span class="sxs-lookup"><span data-stu-id="4b5a8-106">An address pair can specify a source, a destination, both, or neither.</span></span>

<span data-ttu-id="4b5a8-107">Der Adress Teil des Filters besteht aus zwei Strukturen: [**adresssstable**](addresstable.md) und [**adresssspair**](addresspair.md).</span><span class="sxs-lookup"><span data-stu-id="4b5a8-107">The address portion of the filter consists of two structures: [**ADDRESSTABLE**](addresstable.md) and [**ADDRESSPAIR**](addresspair.md).</span></span>

<span data-ttu-id="4b5a8-108">Wenn Sie keine Adressen angeben, werden alle Rahmen an den Adress Filter übergeben.</span><span class="sxs-lookup"><span data-stu-id="4b5a8-108">If you specify NO addresses, then ALL frames will pass the address filter.</span></span> <span data-ttu-id="4b5a8-109">Wenn Sie jedoch Adressen angeben, werden nur die Rahmen übergeben, die den angegebenen Adress Filter übergeben.</span><span class="sxs-lookup"><span data-stu-id="4b5a8-109">However, if you specify any addresses, only those frames that pass the given address filter will pass.</span></span>

<span data-ttu-id="4b5a8-110">Das Entwickeln des Adress Filters umfasst das Zuordnen einer [**adressstabilen**](addresstable.md) Struktur und das Ausfüllen von Membern der [**adresspair**](addresspair.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4b5a8-110">Building the address filter involves allocating an [**ADDRESSTABLE**](addresstable.md) structure and filling in members of the [**ADDRESSPAIR**](addresspair.md) structure.</span></span>

<span data-ttu-id="4b5a8-111">**So erstellen Sie den Adress Teil eines Erfassungs Filters**</span><span class="sxs-lookup"><span data-stu-id="4b5a8-111">**To build the address portion of a capture filter**</span></span>

1.  <span data-ttu-id="4b5a8-112">Verwenden Sie das Flag **capturefilter \_ Flags \_ local \_ only** der [**capturefilter**](capturefilter.md) -Struktur, um die Erfassung auf den Datenverkehr zu und von Ihrem lokalen Computer zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="4b5a8-112">Use the **CAPTUREFILTER\_FLAGS\_LOCAL\_ONLY** flag of the [**CAPTUREFILTER**](capturefilter.md) structure to restrict the capture to traffic to and from your local computer.</span></span>

    <span data-ttu-id="4b5a8-113">Wenn Sie dieses Flag festlegen, wird die NIC nicht auf den gemischten-Modus festgelegt. die Erfassungs Datei erfasst nur den lokalen Datenverkehr.</span><span class="sxs-lookup"><span data-stu-id="4b5a8-113">Setting this flag will not set the NIC to promiscuous mode; the capture file will capture only local traffic.</span></span>

2.  <span data-ttu-id="4b5a8-114">Verwenden Sie den folgenden Beispielcode zum Definieren der " [**adresssstable**](addresstable.md) "-Struktur:</span><span class="sxs-lookup"><span data-stu-id="4b5a8-114">Use the following example code to define the [**ADDRESSTABLE**](addresstable.md) structure:</span></span>

    ``` syntax
    typedef struct _ADDRESSTABLE
    {
        DWORD           nAddressPairs;
        DWORD           nNonMacAddressPairs;
        ADDRESSPAIR     AddressPair[MAX_ADDRESS_PAIRS];
    } ADDRESSTABLE;

    typedef ADDRESSTABLE *LPADDRESSTABLE;
     
    typedef struct _ADDRESSPAIR
    {
        WORD        AddressFlags;
        WORD        NalReserved;
        ADDRESS     DstAddress;
        ADDRESS     SrcAddress;
    } ADDRESSPAIR;

    typedef ADDRESSPAIR *LPADDRESSPAIR;
    ```

3.  <span data-ttu-id="4b5a8-115">Verwenden Sie die in der folgenden Tabelle aufgeführten Informationen, um einen [**adresspair**](addresspair.md) -flagtyp auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="4b5a8-115">Use the information, listed in the following table, to select an [**ADDRESSPAIR**](addresspair.md) flag type.</span></span> 

    | <span data-ttu-id="4b5a8-116">Flag</span><span class="sxs-lookup"><span data-stu-id="4b5a8-116">Flag</span></span>                             | <span data-ttu-id="4b5a8-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4b5a8-117">Meaning</span></span>                                                                               |
    |----------------------------------|---------------------------------------------------------------------------------------|
    | <span data-ttu-id="4b5a8-118">\_adressflags \_ entsprechen " \_ DST"</span><span class="sxs-lookup"><span data-stu-id="4b5a8-118">ADDRESS\_FLAGS\_MATCH\_DST</span></span>       | <span data-ttu-id="4b5a8-119">Entspricht einer Zieladresse.</span><span class="sxs-lookup"><span data-stu-id="4b5a8-119">Matches a destination address.</span></span>                                                        |
    | <span data-ttu-id="4b5a8-120">\_adressflags \_ entsprechen \_ src</span><span class="sxs-lookup"><span data-stu-id="4b5a8-120">ADDRESS\_FLAGS\_MATCH\_SRC</span></span>       | <span data-ttu-id="4b5a8-121">Entspricht einer Quelladresse</span><span class="sxs-lookup"><span data-stu-id="4b5a8-121">Matches a source address</span></span>                                                              |
    | <span data-ttu-id="4b5a8-122">\_Ausschließen von adressflags \_</span><span class="sxs-lookup"><span data-stu-id="4b5a8-122">ADDRESS\_FLAGS\_EXCLUDE</span></span>          | <span data-ttu-id="4b5a8-123">Schließt den Frame aus, wenn diese Adresse gefunden wird (entweder eine definierte Quelle oder ein Ziel).</span><span class="sxs-lookup"><span data-stu-id="4b5a8-123">Excludes the frame if this address is found (either a defined source or destination).</span></span> |
    | <span data-ttu-id="4b5a8-124">\_adressflags \_ DST \_ Group \_ addr</span><span class="sxs-lookup"><span data-stu-id="4b5a8-124">ADDRESS\_FLAGS\_DST\_GROUP\_ADDR</span></span> | <span data-ttu-id="4b5a8-125">Entspricht dem Gruppen Bit (der Zieladresse) nur für Broadcast-/typnachrichten.</span><span class="sxs-lookup"><span data-stu-id="4b5a8-125">Matches group bit (of the destination address) only for broadcast-type messages.</span></span>      |
    | <span data-ttu-id="4b5a8-126">\_adressflags \_ stimmen mit \_ beiden identisch.</span><span class="sxs-lookup"><span data-stu-id="4b5a8-126">ADDRESS\_FLAGS\_MATCH\_BOTH</span></span>      | <span data-ttu-id="4b5a8-127">Entspricht der Ziel-und der Quelladresse.</span><span class="sxs-lookup"><span data-stu-id="4b5a8-127">Matches both the destination and source addresses.</span></span>                                    |

    

     

4.  <span data-ttu-id="4b5a8-128">Geben Sie eine Zieladresse ein, die mit dem von Ihnen ausgewählten [**adresssspair**](addresspair.md) -Flag ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="4b5a8-128">Fill in a destination address, which is evaluated against the [**ADDRESSPAIR**](addresspair.md) flag that you select.</span></span>
5.  <span data-ttu-id="4b5a8-129">Geben Sie eine Quelladresse ein, die mit dem von Ihnen ausgewählten [**adresssspair**](addresspair.md) -Flag ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="4b5a8-129">Fill in a source address, which is evaluated against the [**ADDRESSPAIR**](addresspair.md) flag that you select.</span></span>
6.  <span data-ttu-id="4b5a8-130">Füllen Sie die " [**adresstable**](addresstable.md) "-Struktur mit einem Array von [**adresssspair**](addresspair.md) -Strukturen, das die vom Treiber auswerteten Adress Paare enthält.</span><span class="sxs-lookup"><span data-stu-id="4b5a8-130">Populate the [**ADDRESSTABLE**](addresstable.md) structure with an array of [**ADDRESSPAIR**](addresspair.md) structures, which includes the address pairs that the driver evaluates.</span></span> <span data-ttu-id="4b5a8-131">Alle Adress Paare werden als logische OR-Anweisung ausgewertet (adresspair 1 \| \| adresssspair 2).</span><span class="sxs-lookup"><span data-stu-id="4b5a8-131">All address pairs are evaluated as a logical OR statement (ADDRESSPAIR 1 \|\| ADDRESSPAIR 2).</span></span> <span data-ttu-id="4b5a8-132">Sie können maximal acht Adress Paare in einen Erfassungs Filter einschließen.</span><span class="sxs-lookup"><span data-stu-id="4b5a8-132">You can include a maximum of eight address pairs in a capture filter.</span></span>

 

 



