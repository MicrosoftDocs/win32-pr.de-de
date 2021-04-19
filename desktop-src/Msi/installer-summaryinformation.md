---
description: Die SummaryInformation-Eigenschaft des Installer-Objekts gibt ein SummaryInfo-Objekt zurück, das zum Überprüfen, aktualisieren und Hinzufügen von Eigenschaften zum Zusammenfassungs Informationsdaten Strom eines Pakets oder einer Transformation verwendet werden kann.
ms.assetid: 6a1d81b9-d61f-4bff-92c3-35fc436a6a41
title: Installer. SummaryInformation (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.SummaryInformation
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1ee593ca2ffebf3ca5574a8e2a6547b9cd81be40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368307"
---
# <a name="installersummaryinformation-property"></a><span data-ttu-id="3d293-103">Installer. SummaryInformation (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3d293-103">Installer.SummaryInformation property</span></span>

<span data-ttu-id="3d293-104">Die **SummaryInformation** -Eigenschaft des [**Installer**](installer-object.md) -Objekts gibt ein [**SummaryInfo**](summaryinfo-object.md) -Objekt zurück, das zum Überprüfen, aktualisieren und Hinzufügen von Eigenschaften zum Zusammenfassungs Informationsdaten Strom eines Pakets oder einer Transformation verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="3d293-104">The **SummaryInformation** property of the [**Installer**](installer-object.md) object returns a [**SummaryInfo**](summaryinfo-object.md) object that can be used to examine, update, and add properties to the summary information stream of a package or transform.</span></span>

<span data-ttu-id="3d293-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="3d293-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d293-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d293-106">Syntax</span></span>


```JScript
propVal = Installer.SummaryInformation
```



## <a name="property-value"></a><span data-ttu-id="3d293-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="3d293-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="3d293-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d293-108">Remarks</span></span>

<span data-ttu-id="3d293-109">Wenn ein Wert von *maxproperties* größer als 0 verwendet wird, um einen vorhandenen Zusammenfassungs Informationsdaten Strom zu öffnen, muss die persistente [**Methode vor dem Schließen**](summaryinfo-persist.md) des Objekts aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="3d293-109">If a value of *maxProperties* greater than 0 is used to open an existing summary information stream, the [**Persist**](summaryinfo-persist.md) method must be called before closing the object.</span></span> <span data-ttu-id="3d293-110">Wenn dies nicht der Fall ist, verlieren Sie die vorhandenen Datenstrom Informationen.</span><span class="sxs-lookup"><span data-stu-id="3d293-110">Failing to do this loses the existing stream information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d293-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d293-111">Requirements</span></span>



| <span data-ttu-id="3d293-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d293-112">Requirement</span></span> | <span data-ttu-id="3d293-113">Wert</span><span class="sxs-lookup"><span data-stu-id="3d293-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d293-114">Version</span><span class="sxs-lookup"><span data-stu-id="3d293-114">Version</span></span><br/> | <span data-ttu-id="3d293-115">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3d293-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3d293-116">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3d293-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3d293-117">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="3d293-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="3d293-118">DLL</span><span class="sxs-lookup"><span data-stu-id="3d293-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="3d293-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d293-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="3d293-120">IID</span><span class="sxs-lookup"><span data-stu-id="3d293-120">IID</span></span><br/>     | <span data-ttu-id="3d293-121">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="3d293-121">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




