---
description: Intel AVX-Funktionen.
ms.assetid: 237f356a-9ee8-4c52-b08c-a6695c52713a
title: AVX-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0b56c83b6beb674bc284b139bb656441956705
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214023"
---
# <a name="avx-functions"></a><span data-ttu-id="22d30-103">AVX-Funktionen</span><span class="sxs-lookup"><span data-stu-id="22d30-103">AVX Functions</span></span>

<span data-ttu-id="22d30-104">Im folgenden sind die Intel AVX-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="22d30-104">The following are the Intel AVX functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="22d30-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="22d30-105">In this section</span></span>



| <span data-ttu-id="22d30-106">Thema</span><span class="sxs-lookup"><span data-stu-id="22d30-106">Topic</span></span>                                                                   | <span data-ttu-id="22d30-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="22d30-107">Description</span></span>                                                                                                                    |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22d30-108">**Copycontext**</span><span class="sxs-lookup"><span data-stu-id="22d30-108">**CopyContext**</span></span>](/windows/desktop/api/WinBase/nf-winbase-copycontext)<br/>                           | <span data-ttu-id="22d30-109">Kopiert eine Quell Kontext Struktur (einschließlich eines beliebigen xstate) in eine initialisierte Ziel Kontext Struktur.</span><span class="sxs-lookup"><span data-stu-id="22d30-109">Copies a source context structure (including any XState) onto an initialized destination context structure.</span></span><br/>         |
| [<span data-ttu-id="22d30-110">**Getenabledxstatefeatures**</span><span class="sxs-lookup"><span data-stu-id="22d30-110">**GetEnabledXStateFeatures**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getenabledxstatefeatures)<br/> | <span data-ttu-id="22d30-111">Ruft eine Maske von aktivierten xstate-Funktionen auf x86-oder x64-Prozessoren ab.</span><span class="sxs-lookup"><span data-stu-id="22d30-111">Gets a mask of enabled XState features on x86 or x64 processors.</span></span><br/>                                                    |
| [<span data-ttu-id="22d30-112">**Getxstatefeaturesmask**</span><span class="sxs-lookup"><span data-stu-id="22d30-112">**GetXStateFeaturesMask**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getxstatefeaturesmask)<br/>       | <span data-ttu-id="22d30-113">Gibt die Maske von xstate-Funktionen zurück, die innerhalb einer [**Kontext**](/windows/desktop/api/WinNT/ns-winnt-wow64_context) Struktur festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="22d30-113">Returns the mask of XState features set within a [**CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-wow64_context) structure.</span></span><br/>                        |
| [<span data-ttu-id="22d30-114">**Initializecontext**</span><span class="sxs-lookup"><span data-stu-id="22d30-114">**InitializeContext**</span></span>](/windows/desktop/api/WinBase/nf-winbase-initializecontext)<br/>               | <span data-ttu-id="22d30-115">Initialisiert eine [**Kontext**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) Struktur in einem Puffer mit der erforderlichen Größe und Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="22d30-115">Initializes a [**CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) structure inside a buffer with the necessary size and alignment.</span></span><br/>       |
| [<span data-ttu-id="22d30-116">**Loerexstatefeature**</span><span class="sxs-lookup"><span data-stu-id="22d30-116">**LocateXStateFeature**</span></span>](/windows/desktop/api/WinBase/nf-winbase-locatexstatefeature)<br/>           | <span data-ttu-id="22d30-117">Ruft einen Zeiger auf den Prozessor Zustand für eine xstate-Funktion innerhalb einer [**Kontext**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) Struktur ab.</span><span class="sxs-lookup"><span data-stu-id="22d30-117">Retrieves a pointer to the processor state for an XState feature within a [**CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) structure.</span></span><br/> |
| [<span data-ttu-id="22d30-118">**Setxstatefeaturesmask**</span><span class="sxs-lookup"><span data-stu-id="22d30-118">**SetXStateFeaturesMask**</span></span>](/windows/desktop/api/WinBase/nf-winbase-setxstatefeaturesmask)<br/>       | <span data-ttu-id="22d30-119">Legt die Maske der in einer [**Kontext**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) Struktur festgelegten xstate-Funktionen fest.</span><span class="sxs-lookup"><span data-stu-id="22d30-119">Sets the mask of XState features set within a [**CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) structure.</span></span><br/>                             |



 

 

 




