---
title: TPM-Basisdienste
description: Die TPM-Software stellt Dienste als API bereit, die durch Remote Prozedur Aufrufe verfügbar gemacht wird. Verwenden Sie TPM, um ein TPM-Modul zu erstellen.
ms.assetid: ae6e7fe9-585d-467a-8456-e008b8ea89a0
keywords:
- TDie Basisdienste-TSB von TPM
- Basisdienste für TPM, Startseite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d2cbdfc1f85d6917f2e9a7a5b8e7a0fc25ebdc8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390682"
---
# <a name="tpm-base-services"></a><span data-ttu-id="83140-106">TPM-Basisdienste</span><span class="sxs-lookup"><span data-stu-id="83140-106">TPM Base Services</span></span>

## <a name="purpose"></a><span data-ttu-id="83140-107">Zweck</span><span class="sxs-lookup"><span data-stu-id="83140-107">Purpose</span></span>

<span data-ttu-id="83140-108">Die TPM-Funktion (Trusted Platform Module) zentralisiert den TPM-Zugriff auf Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="83140-108">The Trusted Platform Module (TPM) Base Services (TBS) feature centralizes TPM access across applications.</span></span>

<span data-ttu-id="83140-109">Das TSB-Feature wird als Systemdienst in Windows Server 2008, Windows Vista oder neueren Betriebssystemen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="83140-109">The TBS feature runs as a system service in Windows Server 2008, Windows Vista, or newer operating systems.</span></span> <span data-ttu-id="83140-110">Dienste werden als API bereitgestellt, die über Remote Prozedur Aufrufe (RPC) verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="83140-110">It provides services as an API exposed through remote procedure calls (RPC).</span></span> <span data-ttu-id="83140-111">Das TSB-Feature verwendet Prioritäten, die durch den Aufruf von Anwendungen festgelegt werden, um den TPM-Zugriff zusammen</span><span class="sxs-lookup"><span data-stu-id="83140-111">The TBS feature uses priorities specified by calling applications to cooperatively schedule TPM access.</span></span>

> [!Note]
>
> <span data-ttu-id="83140-112">Das TPM kann für Schlüsselspeicher Vorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="83140-112">The TPM can be used for key storage operations.</span></span> <span data-ttu-id="83140-113">Entwicklern wird jedoch empfohlen, stattdessen die [Schlüsselspeicher-APIs](/windows/desktop/SecCNG/key-storage-and-retrieval) für diese Szenarien zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="83140-113">However, developers are encouraged to use the [Key Storage APIs](/windows/desktop/SecCNG/key-storage-and-retrieval) for these scenarios instead.</span></span> <span data-ttu-id="83140-114">Die Schlüsselspeicher-APIs bieten die Funktionalität zum Erstellen, signieren oder verschlüsseln mit Kryptografieschlüsseln und sind auf höherer Ebene und leichter zu verwenden als die TSB für diese Ziel Szenarien.</span><span class="sxs-lookup"><span data-stu-id="83140-114">The Key Storage APIs provide the functionality to create, sign or encrypt with, and persist cryptographic keys, and they are higher-level and easier to use than the TBS for these targeted scenarios.</span></span>

 

## <a name="developer-audience"></a><span data-ttu-id="83140-115">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="83140-115">Developer audience</span></span>

<span data-ttu-id="83140-116">TSB ist für die Verwendung durch Entwickler von Anwendungen basierend auf den Windows-Betriebssystemen vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="83140-116">TBS is intended for use by developers of applications based on the Windows operating systems.</span></span> <span data-ttu-id="83140-117">Entwickler sollten mit den Programmiersprachen C und C++ und der Microsoft Windows-Programmierumgebung vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="83140-117">Developers should be familiar with the C and C++ programming languages and the Microsoft Windows programming environment.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="83140-118">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="83140-118">Run-time requirements</span></span>

<span data-ttu-id="83140-119">Das TSB-Feature erfordert mindestens das Betriebssystem Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="83140-119">The TBS feature requires at least Windows Server 2008 or Windows Vista operating system.</span></span> <span data-ttu-id="83140-120">Informationen zu den Lauf Zeitanforderungen für ein bestimmtes Programmier Element finden Sie im Abschnitt "Anforderungen" der Referenzseite für dieses Element.</span><span class="sxs-lookup"><span data-stu-id="83140-120">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="83140-121">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="83140-121">In this section</span></span>



| <span data-ttu-id="83140-122">Thema</span><span class="sxs-lookup"><span data-stu-id="83140-122">Topic</span></span>                                         | <span data-ttu-id="83140-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="83140-123">Description</span></span>                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="83140-124">Informationen zu TSB</span><span class="sxs-lookup"><span data-stu-id="83140-124">About TBS</span></span>](about-tbs.md)<br/>         | <span data-ttu-id="83140-125">Wichtige Konzepte und eine allgemeine Übersicht über das TSB-Feature.</span><span class="sxs-lookup"><span data-stu-id="83140-125">Key concepts and a high-level view of the TBS feature.</span></span><br/>               |
| [<span data-ttu-id="83140-126">Verwenden von TSB</span><span class="sxs-lookup"><span data-stu-id="83140-126">Using TBS</span></span>](using-tbs.md)<br/>         | <span data-ttu-id="83140-127">TSB-Prozesse und-Prozeduren für die Verwendung der TSB-API.</span><span class="sxs-lookup"><span data-stu-id="83140-127">TBS processes and procedures for using the TBS API.</span></span><br/>                  |
| [<span data-ttu-id="83140-128">TSB-Referenz</span><span class="sxs-lookup"><span data-stu-id="83140-128">TBS Reference</span></span>](tbs-reference.md)<br/> | <span data-ttu-id="83140-129">Dokumentation zu den TSB-Funktionen,-Strukturen und-Rückgabecodes.</span><span class="sxs-lookup"><span data-stu-id="83140-129">Documentation about the TBS functions, structures, and return codes.</span></span><br/> |



 

 

