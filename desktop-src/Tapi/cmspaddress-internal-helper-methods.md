---
description: In der folgenden Liste sind die internen CMSP-Adress Methoden enthalten.
ms.assetid: 2016a776-1464-46b5-96b9-b045834f9e38
title: Interne cmspaddress-Hilfsmethoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17064d161e2a073addb2e8eef6d9d290b41278b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363850"
---
# <a name="cmspaddress-internal-helper-methods"></a><span data-ttu-id="a350c-103">Interne cmspaddress-Hilfsmethoden</span><span class="sxs-lookup"><span data-stu-id="a350c-103">CMSPAddress Internal Helper Methods</span></span>



| <span data-ttu-id="a350c-104">Interne cmspaddress-Hilfsmethoden</span><span class="sxs-lookup"><span data-stu-id="a350c-104">CMSPAddress internal helper methods</span></span>                                        | <span data-ttu-id="a350c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a350c-105">Description</span></span>                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a350c-106">**Getstaticterminals**</span><span class="sxs-lookup"><span data-stu-id="a350c-106">**GetStaticTerminals**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getstaticterminals)               | <span data-ttu-id="a350c-107">Wird von [**get \_ staticterminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_staticterminals) und [**enumeratestaticterminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratestaticterminals) aufgerufen, um ein Array von statischen Terminals zu erhalten, das für diese Adresse verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a350c-107">Called by [**get\_StaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_staticterminals) and [**EnumerateStaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratestaticterminals) to get an array of static terminals that can be used on this address.</span></span>                                     |
| [<span data-ttu-id="a350c-108">**Getdynamicterminalclasses**</span><span class="sxs-lookup"><span data-stu-id="a350c-108">**GetDynamicTerminalClasses**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getdynamicterminalclasses) | <span data-ttu-id="a350c-109">Wird von [**get \_ dynamicterminalclasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_dynamicterminalclasses) und [**enumeratedynamicterminalclasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses) aufgerufen, um ein Array dynamischer Terminal Klassen zu erhalten, das für diese Adresse verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a350c-109">Called by [**get\_DynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_dynamicterminalclasses) and [**EnumerateDynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses) to get an array of dynamic terminal classes that can be used on this address.</span></span> |
| [<span data-ttu-id="a350c-110">**Updateterminallist**</span><span class="sxs-lookup"><span data-stu-id="a350c-110">**UpdateTerminalList**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-updateterminallist)               | <span data-ttu-id="a350c-111">Füllt die Liste der statischen Terminals des MSP auf.</span><span class="sxs-lookup"><span data-stu-id="a350c-111">Populates the MSP's list of static terminals.</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="a350c-112">**Receivetspaddressdata**</span><span class="sxs-lookup"><span data-stu-id="a350c-112">**ReceiveTSPAddressData**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-receivetspaddressdata)         | <span data-ttu-id="a350c-113">Wird aufgerufen, wenn eine TSP-Daten Nachricht von der Adresse anstelle eines bestimmten Aufrufs verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a350c-113">Called when a TSP data message is intended to be processed by the address rather than by a specific call.</span></span>                                                                                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="a350c-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a350c-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a350c-115">**Cmspaddress**</span><span class="sxs-lookup"><span data-stu-id="a350c-115">**CMSPAddress**</span></span>](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)
</dt> </dl>

 

 
