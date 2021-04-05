---
description: Evalcom2.dll können zur Implementierung von Validierungs Vorgängen für Installationspakete und Mergemodule mithilfe interner Konsistenz Auswertungen-ICES verwendet werden.
ms.assetid: df38e75e-554c-4a6d-b9ad-8eee5123a16f
title: Verwenden von Evalcom2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c49a165115b505d5c78ebe5b5e714b8a3c359d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751696"
---
# <a name="using-evalcom2"></a><span data-ttu-id="79889-103">Verwenden von Evalcom2</span><span class="sxs-lookup"><span data-stu-id="79889-103">Using Evalcom2</span></span>

<span data-ttu-id="79889-104">Evalcom2.dll können zur Implementierung von Validierungs Vorgängen für Installationspakete und Mergemodule mithilfe [interner Konsistenz Auswertungen-ICES](internal-consistency-evaluators-ices.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="79889-104">Evalcom2.dll can be used to implement validation operations for installation packages and merge modules using [Internal Consistency Evaluators - ICEs](internal-consistency-evaluators-ices.md).</span></span> <span data-ttu-id="79889-105">Das Hauptobjekt implementiert Schnittstellen für C/C++-Programme.</span><span class="sxs-lookup"><span data-stu-id="79889-105">The main object implements interfaces for C/C++ programs.</span></span>

<span data-ttu-id="79889-106">Das Hauptobjekt implementiert auch [Evalcom2-Schnittstellen](evalcom2-interfaces.md) für C/C++-Programme.</span><span class="sxs-lookup"><span data-stu-id="79889-106">The main object also implements [Evalcom2 interfaces](evalcom2-interfaces.md) for C/C++ programs.</span></span> <span data-ttu-id="79889-107">Die zum Abrufen der Schnittstelle von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) erforderliche CLSID ist {6e5e1910-8053-4660-B795-6b612e29bc58}.</span><span class="sxs-lookup"><span data-stu-id="79889-107">The CLSID required to obtain the interface from [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) is {6E5E1910-8053-4660-B795-6B612E29BC58}.</span></span> <span data-ttu-id="79889-108">Die refid ist {E482E5C6-E31E-4143-A2E6-DBC3D8E4B8D3}.</span><span class="sxs-lookup"><span data-stu-id="79889-108">The REFIID is {E482E5C6-E31E-4143-A2E6-DBC3D8E4B8D3}.</span></span>

<span data-ttu-id="79889-109">Mit dem folgenden Verfahren können Sie Validierungs Vorgänge implementieren.</span><span class="sxs-lookup"><span data-stu-id="79889-109">You can use the following procedure to implement validation operations.</span></span>

<span data-ttu-id="79889-110">**So implementieren Sie Validierungs Vorgänge**</span><span class="sxs-lookup"><span data-stu-id="79889-110">**To implement validation operations**</span></span>

1.  <span data-ttu-id="79889-111">Initialisieren Sie com auf dem aufrufenden Thread mithilfe von [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize).</span><span class="sxs-lookup"><span data-stu-id="79889-111">Initialize COM on the calling thread using [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize).</span></span>
2.  <span data-ttu-id="79889-112">Rufen Sie mithilfe von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)den Zeiger auf die [**IValidate**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="79889-112">Obtain the pointer to the [**IValidate**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate) interface using [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>
3.  <span data-ttu-id="79889-113">Öffnen Sie das Installationspaket oder Mergemodul mithilfe der [**OpenDatabase**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opendatabase) -Methode.</span><span class="sxs-lookup"><span data-stu-id="79889-113">Open the installation package or merge module using the [**OpenDatabase**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opendatabase) method.</span></span>
4.  <span data-ttu-id="79889-114">Öffnen Sie die Auswertungs Datei mithilfe der [**opencub**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opencub) -Methode.</span><span class="sxs-lookup"><span data-stu-id="79889-114">Open the evaluation file using the [**OpenCUB**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opencub) method.</span></span>
5.  <span data-ttu-id="79889-115">Legen Sie die Anzeige Rückruffunktion mithilfe der [**setdisplay**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setdisplay) -Methode fest.</span><span class="sxs-lookup"><span data-stu-id="79889-115">Set the display callback function using the [**SetDisplay**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setdisplay) method.</span></span>
6.  <span data-ttu-id="79889-116">Legen Sie die Status Rückruffunktion mithilfe der [**SetStatus**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setstatus) -Methode fest.</span><span class="sxs-lookup"><span data-stu-id="79889-116">Set the status callback function using the [**SetStatus**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setstatus) method.</span></span>
7.  <span data-ttu-id="79889-117">Führen Sie die Validierung mithilfe der [**Validate**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-validate) -Methode aus.</span><span class="sxs-lookup"><span data-stu-id="79889-117">Perform the validation using the [**Validate**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-validate) method.</span></span>
8.  <span data-ttu-id="79889-118">Schließen Sie die CUB-Datei mithilfe der [**closecub**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closecub) -Methode.</span><span class="sxs-lookup"><span data-stu-id="79889-118">Close the .cub file using the [**CloseCUB**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closecub) method.</span></span>
9.  <span data-ttu-id="79889-119">Schließen Sie die Datenbank mit der [**CloseDatabase**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closedatabase) -Methode.</span><span class="sxs-lookup"><span data-stu-id="79889-119">Close the database using the [**CloseDatabase**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closedatabase) method.</span></span>
10. <span data-ttu-id="79889-120">Geben Sie die [**IValidate**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate) -Schnittstelle frei.</span><span class="sxs-lookup"><span data-stu-id="79889-120">Release the [**IValidate**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate) interface.</span></span>
11. <span data-ttu-id="79889-121">Initialisieren Sie com mithilfe von " [**zählinitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize)".</span><span class="sxs-lookup"><span data-stu-id="79889-121">Uninitialize COM using [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span></span>

## <a name="related-topics"></a><span data-ttu-id="79889-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="79889-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79889-123">Evalcom2-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="79889-123">Evalcom2 Interfaces</span></span>](evalcom2-interfaces.md)
</dt> <dt>

[<span data-ttu-id="79889-124">Validierungs Automatisierung</span><span class="sxs-lookup"><span data-stu-id="79889-124">Validation Automation</span></span>](validation-automation.md)
</dt> <dt>

[<span data-ttu-id="79889-125">Validierungs Rückruf Funktionen</span><span class="sxs-lookup"><span data-stu-id="79889-125">Validation Callback Functions</span></span>](validation-callback-functions.md)
</dt> </dl>

 

 
