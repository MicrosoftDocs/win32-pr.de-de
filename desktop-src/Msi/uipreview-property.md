---
description: Die Property-Eigenschaft des uipreview-Objekts ist eine Lese-/Schreibeigenschaft, die den Zeichen folgen Wert einer benannten installereigenschaft darstellt, oder, wenn ein Prozentzeichen (%) als Präfix angegeben ist, der Wert einer System Umgebungsvariablen für den aktuellen Prozess.
ms.assetid: 92900426-8fb5-4a94-a982-438267ad756e
title: Uipreview. Property (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 430c6f75b03fe69f8054bb2b0a61bab59dcc4d58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358079"
---
# <a name="uipreviewproperty-property"></a><span data-ttu-id="33238-103">Uipreview. Property (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="33238-103">UIPreview.Property property</span></span>

<span data-ttu-id="33238-104">Die **Property** -Eigenschaft des [**uipreview**](uipreview-object.md) -Objekts ist eine Lese-/Schreibeigenschaft, die den Zeichen folgen Wert einer benannten installereigenschaft darstellt, oder, wenn ein Prozentzeichen (%) als Präfix angegeben ist, der Wert einer System Umgebungsvariablen für den aktuellen Prozess.</span><span class="sxs-lookup"><span data-stu-id="33238-104">The **Property** property of the [**UIPreview**](uipreview-object.md) object is a read-write property that represents the string value of a named installer property, or, if it is prefixed with a percent sign (%), the value of a system environment variable for the current process.</span></span> <span data-ttu-id="33238-105">Dies ist verfügbar, um eine ordnungsgemäße Anzeige von Dialogfeldern zu ermöglichen, die von Eigenschafts Werten abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="33238-105">This is exposed to allow proper display of dialog boxes that are dependent upon property values.</span></span> <span data-ttu-id="33238-106">Es können entweder Zeichen folgen Werte oder ganzzahlige Werte angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="33238-106">Either string or integer values may be supplied.</span></span> <span data-ttu-id="33238-107">Eine nicht vorhandene Eigenschaft oder Umgebungsvariable entspricht dem Wert NULL.</span><span class="sxs-lookup"><span data-stu-id="33238-107">A nonexistent property or environment variable is equivalent to its value being null.</span></span>

<span data-ttu-id="33238-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="33238-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="33238-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="33238-109">Syntax</span></span>


```JScript
propVal = UIPreview.Property
UIPreview.Property = propVal 
```



## <a name="property-value"></a><span data-ttu-id="33238-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="33238-110">Property value</span></span>

<span data-ttu-id="33238-111">Der Unterscheidung nach Groß-/Kleinschreibung oder der Name einer Umgebungsvariablen mit dem Präfix "Prozentzeichen (%)" ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="33238-111">Required case-sensitive name of a property, or a case-insensitive name of an environment variable prefixed by a percent sign (%).</span></span>

## <a name="requirements"></a><span data-ttu-id="33238-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33238-112">Requirements</span></span>



| <span data-ttu-id="33238-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33238-113">Requirement</span></span> | <span data-ttu-id="33238-114">Wert</span><span class="sxs-lookup"><span data-stu-id="33238-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33238-115">Version</span><span class="sxs-lookup"><span data-stu-id="33238-115">Version</span></span><br/> | <span data-ttu-id="33238-116">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="33238-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="33238-117">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="33238-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="33238-118">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="33238-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="33238-119">DLL</span><span class="sxs-lookup"><span data-stu-id="33238-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="33238-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33238-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="33238-121">IID</span><span class="sxs-lookup"><span data-stu-id="33238-121">IID</span></span><br/>     | <span data-ttu-id="33238-122">IID \_ iuipreview ist definiert als 000c109a-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="33238-122">IID\_IUIPreview is defined as 000C109A-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




