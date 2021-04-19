---
description: Die SourcePath-Eigenschaft des Session-Objekts ist eine schreibgeschützte Eigenschaft, die den vollständigen Pfad zum angegebenen Ordner auf dem Quell Medium oder dem Server Image bereitstellt.
ms.assetid: ed8eea4f-e15e-4d56-ac0c-e18f9cb46d07
title: Session. SourcePath (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.SourcePath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a868e68e26f28d4fc2137e735ddc6d4c6ab0066
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372736"
---
# <a name="sessionsourcepath-property"></a><span data-ttu-id="05ec8-103">Session. SourcePath (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="05ec8-103">Session.SourcePath property</span></span>

<span data-ttu-id="05ec8-104">Die **SourcePath** -Eigenschaft des [**Session**](session-object.md) -Objekts ist eine schreibgeschützte Eigenschaft, die den vollständigen Pfad zum angegebenen Ordner auf dem Quell Medium oder dem Server Image bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="05ec8-104">The **SourcePath** property of the [**Session**](session-object.md) object is a read-only property that provides the full path to the designated folder on the source media or server image.</span></span>

<span data-ttu-id="05ec8-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="05ec8-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="05ec8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="05ec8-106">Syntax</span></span>


```JScript
propVal = Session.SourcePath
```



## <a name="property-value"></a><span data-ttu-id="05ec8-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="05ec8-107">Property value</span></span>

<span data-ttu-id="05ec8-108">Unter Berücksichtigung der Groß-/Kleinschreibung für eine Ordner Eigenschaft, die durch einen Primärschlüssel der [Verzeichnis Tabelle](directory-table.md)angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="05ec8-108">Required case-sensitive name of a folder property as specified by a primary key of the [Directory table](directory-table.md).</span></span> <span data-ttu-id="05ec8-109">Wenn der Ordner nicht vorhanden ist, wird ein Fehler generiert.</span><span class="sxs-lookup"><span data-stu-id="05ec8-109">An error is generated if the folder does not exist.</span></span>

## <a name="remarks"></a><span data-ttu-id="05ec8-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="05ec8-110">Remarks</span></span>

<span data-ttu-id="05ec8-111">Wenn die Eigenschaft fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="05ec8-111">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="05ec8-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05ec8-112">Requirements</span></span>



| <span data-ttu-id="05ec8-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="05ec8-113">Requirement</span></span> | <span data-ttu-id="05ec8-114">Wert</span><span class="sxs-lookup"><span data-stu-id="05ec8-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05ec8-115">Version</span><span class="sxs-lookup"><span data-stu-id="05ec8-115">Version</span></span><br/> | <span data-ttu-id="05ec8-116">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="05ec8-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="05ec8-117">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="05ec8-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="05ec8-118">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="05ec8-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="05ec8-119">DLL</span><span class="sxs-lookup"><span data-stu-id="05ec8-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="05ec8-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05ec8-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="05ec8-121">IID</span><span class="sxs-lookup"><span data-stu-id="05ec8-121">IID</span></span><br/>     | <span data-ttu-id="05ec8-122">IID \_ ISession ist definiert als 000c109e-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="05ec8-122">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




