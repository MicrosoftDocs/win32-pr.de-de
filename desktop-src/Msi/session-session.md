---
description: Die Property-Eigenschaft des Session-Objekts ist eine Lese-/Schreibeigenschaft, die den Zeichen folgen Wert einer benannten installereigenschaft darstellt, die vom Sitzungs Objekt verwaltet wird.
ms.assetid: 15ce8264-2573-428c-98d9-690cfaae5144
title: Session. Property (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9635d5b9ee093f270e4ee7993f78609d60caa13a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367116"
---
# <a name="sessionproperty-property"></a><span data-ttu-id="2d708-103">Session. Property (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2d708-103">Session.Property property</span></span>

<span data-ttu-id="2d708-104">Die **Property** -Eigenschaft des [**Session**](session-object.md) -Objekts ist eine Lese-/Schreibeigenschaft, die den Zeichen folgen Wert einer benannten installereigenschaft darstellt, die vom **Sitzungs** Objekt in der in-Memory-Eigenschaften Tabelle verwaltet wird, oder, wenn ein Prozentzeichen (%) als Präfix angegeben wird, der Wert einer System Umgebungsvariablen für den aktuellen Prozess.</span><span class="sxs-lookup"><span data-stu-id="2d708-104">The **Property** property of the [**Session**](session-object.md) object is a read-write property that represents the string value of a named installer property, as maintained by the **Session** object in the in-memory Property table, or, if it is prefixed with a percent sign (%), the value of a system environment variable for the current process.</span></span> <span data-ttu-id="2d708-105">Es können entweder Zeichen folgen Werte oder ganzzahlige Werte angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2d708-105">Either string or integer values may be supplied.</span></span> <span data-ttu-id="2d708-106">Eine nicht vorhandene Eigenschaft oder Umgebungsvariable entspricht dem Wert NULL.</span><span class="sxs-lookup"><span data-stu-id="2d708-106">A non-existent property or environment variable is equivalent to its value being Null.</span></span>

<span data-ttu-id="2d708-107">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="2d708-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d708-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d708-108">Syntax</span></span>


```JScript
propVal = Session.Property
Session.Property = propVal 
```



## <a name="property-value"></a><span data-ttu-id="2d708-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="2d708-109">Property value</span></span>

<span data-ttu-id="2d708-110">Der Unterscheidung nach Groß-/Kleinschreibung oder der Name einer Umgebungsvariablen mit dem Präfix "Prozentzeichen (%)" ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2d708-110">Required case-sensitive name of a property, or a case-insensitive name of an environment variable prefixed by a percent sign (%).</span></span>

## <a name="requirements"></a><span data-ttu-id="2d708-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d708-111">Requirements</span></span>



| <span data-ttu-id="2d708-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2d708-112">Requirement</span></span> | <span data-ttu-id="2d708-113">Wert</span><span class="sxs-lookup"><span data-stu-id="2d708-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d708-114">Version</span><span class="sxs-lookup"><span data-stu-id="2d708-114">Version</span></span><br/> | <span data-ttu-id="2d708-115">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2d708-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2d708-116">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2d708-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2d708-117">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="2d708-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="2d708-118">DLL</span><span class="sxs-lookup"><span data-stu-id="2d708-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="2d708-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d708-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="2d708-120">IID</span><span class="sxs-lookup"><span data-stu-id="2d708-120">IID</span></span><br/>     | <span data-ttu-id="2d708-121">IID \_ ISession ist definiert als 000c109e-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="2d708-121">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




