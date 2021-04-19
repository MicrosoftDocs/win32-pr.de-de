---
description: Die featurecost-Eigenschaft des Session-Objekts gibt die Gesamtmenge des Speicherplatzes (in Einheiten von 512 Bytes) zurück, die für die angegebene Funktion und ihre übergeordneten Funktionen erforderlich ist (bis zum Stamm der Funktions Tabelle).
ms.assetid: 5df9912a-2722-41c8-991b-256a009e85df
title: Session. featurecost-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureCost
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 25c93ce0b3b4efa91a827217d221546e8bab5744
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370166"
---
# <a name="sessionfeaturecost-property"></a><span data-ttu-id="e4a80-103">Session. featurecost-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e4a80-103">Session.FeatureCost property</span></span>

<span data-ttu-id="e4a80-104">Die **featurecost** -Eigenschaft des [**Session**](session-object.md) -Objekts gibt die Gesamtmenge des Speicherplatzes (in Einheiten von 512 Bytes) zurück, die für die angegebene Funktion und ihre übergeordneten Funktionen erforderlich ist (bis zum Stamm der Funktions Tabelle).</span><span class="sxs-lookup"><span data-stu-id="e4a80-104">The **FeatureCost** property of the [**Session**](session-object.md) object returns the total amount of disk space (in units of 512 bytes) required by the specified feature and its parent features (up to the root of the Feature table).</span></span> <span data-ttu-id="e4a80-105">Für jede Funktion werden die Gesamtkosten aus den Datenträger Kosten der einzelnen mit dem Feature verknüpften Komponenten zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="e4a80-105">For each feature, the total cost is made up of the disk costs attributed to every component linked to the feature.</span></span>

<span data-ttu-id="e4a80-106">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="e4a80-106">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4a80-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4a80-107">Syntax</span></span>


```JScript
propVal = Session.FeatureCost
```



## <a name="property-value"></a><span data-ttu-id="e4a80-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e4a80-108">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="e4a80-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4a80-109">Remarks</span></span>

<span data-ttu-id="e4a80-110">Wenn die Eigenschaft fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="e4a80-110">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4a80-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4a80-111">Requirements</span></span>



| <span data-ttu-id="e4a80-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4a80-112">Requirement</span></span> | <span data-ttu-id="e4a80-113">Wert</span><span class="sxs-lookup"><span data-stu-id="e4a80-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4a80-114">Version</span><span class="sxs-lookup"><span data-stu-id="e4a80-114">Version</span></span><br/> | <span data-ttu-id="e4a80-115">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e4a80-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e4a80-116">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e4a80-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e4a80-117">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="e4a80-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="e4a80-118">DLL</span><span class="sxs-lookup"><span data-stu-id="e4a80-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="e4a80-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4a80-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="e4a80-120">IID</span><span class="sxs-lookup"><span data-stu-id="e4a80-120">IID</span></span><br/>     | <span data-ttu-id="e4a80-121">IID \_ ISession ist definiert als 000c109e-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e4a80-121">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




