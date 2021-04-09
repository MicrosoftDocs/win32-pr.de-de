---
description: Stellt die Konfiguration des Datei Versions Verlaufs des Benutzers dar, unter dem das bhconfigmgr-Objekt erstellt wird. Alle Konfigurations Vorgänge werden durch Aufrufen der-Methoden der ifhconfigmgr-Schnittstelle ausgeführt.
ms.assetid: CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788
title: Fhconfigmgr-Klasse (fhcfg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FhConfigMgr
api_type:
- COM
api_location:
- Fhcfg.idl
ms.openlocfilehash: 083ce344e44035b5872d91ad14465659defc8229
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861076"
---
# <a name="fhconfigmgr-class"></a><span data-ttu-id="0ebbf-104">Klasse "fihconfigmgr"</span><span class="sxs-lookup"><span data-stu-id="0ebbf-104">FhConfigMgr class</span></span>

<span data-ttu-id="0ebbf-105">Stellt die Konfiguration des Datei Versions Verlaufs des Benutzers dar, unter dem das **bhconfigmgr** -Objekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="0ebbf-105">Represents the File History configuration of the user under which the **FhConfigMgr** object is created.</span></span> <span data-ttu-id="0ebbf-106">Alle Konfigurations Vorgänge werden durch Aufrufen der-Methoden der [**ifhconfigmgr**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhconfigmgr) -Schnittstelle ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0ebbf-106">All configuration operations are performed by calling the methods of the [**IFhConfigMgr**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhconfigmgr) interface.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="0ebbf-107">Gründe für die Implementierung</span><span class="sxs-lookup"><span data-stu-id="0ebbf-107">When to implement</span></span>

<span data-ttu-id="0ebbf-108">Die API für den Datei Versionsverlauf implementiert diese Klasse.</span><span class="sxs-lookup"><span data-stu-id="0ebbf-108">The File History API implements this class.</span></span> <span data-ttu-id="0ebbf-109">Verwenden Sie die [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion, um eine Instanz dieser Klasse zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0ebbf-109">To create an instance of this class, use the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ebbf-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ebbf-110">Requirements</span></span>



| <span data-ttu-id="0ebbf-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ebbf-111">Requirement</span></span> | <span data-ttu-id="0ebbf-112">Wert</span><span class="sxs-lookup"><span data-stu-id="0ebbf-112">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0ebbf-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0ebbf-113">Minimum supported client</span></span><br/> | <span data-ttu-id="0ebbf-114">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0ebbf-114">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0ebbf-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0ebbf-115">Minimum supported server</span></span><br/> | <span data-ttu-id="0ebbf-116">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0ebbf-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0ebbf-117">Header</span><span class="sxs-lookup"><span data-stu-id="0ebbf-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ebbf-118"><dt>Fhcfg. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ebbf-118"><dt>Fhcfg.h</dt></span></span> </dl>   |
| <span data-ttu-id="0ebbf-119">IDL</span><span class="sxs-lookup"><span data-stu-id="0ebbf-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0ebbf-120"><dt>Fhcfg. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0ebbf-120"><dt>Fhcfg.idl</dt></span></span> </dl> |



 

 
