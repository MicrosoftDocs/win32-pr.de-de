---
description: Die enableuipreview-Methode des Database-Objekts erleichtert das Erstellen von Dialogfeldern und-Plakaten durch Bereitstellen der Unterstützung, die zum Anzeigen der in der Installer-Datenbank gespeicherten Dialogfelder der Benutzeroberfläche erforderlich ist.
ms.assetid: c4687de7-8ab4-4377-ac5c-1fed7c915519
title: Database. enableuipreview-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.EnableUIPreview
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1224bb100e0403e8df9f3bdb0cc0b5dbe017233f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371276"
---
# <a name="databaseenableuipreview-method"></a><span data-ttu-id="ce67b-103">Database. enableuipreview-Methode</span><span class="sxs-lookup"><span data-stu-id="ce67b-103">Database.EnableUIPreview method</span></span>

<span data-ttu-id="ce67b-104">Die **enableuipreview** -Methode des [**Database**](database-object.md) -Objekts erleichtert das Erstellen von Dialogfeldern und-Plakaten durch Bereitstellen der Unterstützung, die zum Anzeigen der in der Installer-Datenbank gespeicherten Dialogfelder der Benutzeroberfläche erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="ce67b-104">The **EnableUIPreview** method of the [**Database**](database-object.md) object facilitates the authoring of dialog boxes and billboards by providing the support needed to view user interface dialog boxes stored in the installer database.</span></span> <span data-ttu-id="ce67b-105">Die-Methode startet den Vorschaumodus, indem ein Vorschau **Daten Bank** Objekt zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ce67b-105">The method starts the preview mode by returning a preview **Database** object.</span></span> <span data-ttu-id="ce67b-106">Der Vorschaumodus endet, wenn das Vorschau Objekt freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ce67b-106">The preview mode ends when the preview object is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce67b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce67b-107">Syntax</span></span>


```JScript
Database.EnableUIPreview()
```



## <a name="parameters"></a><span data-ttu-id="ce67b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce67b-108">Parameters</span></span>

<span data-ttu-id="ce67b-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ce67b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ce67b-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ce67b-110">Return value</span></span>

<span data-ttu-id="ce67b-111">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ce67b-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce67b-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce67b-112">Requirements</span></span>



| <span data-ttu-id="ce67b-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce67b-113">Requirement</span></span> | <span data-ttu-id="ce67b-114">Wert</span><span class="sxs-lookup"><span data-stu-id="ce67b-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce67b-115">Version</span><span class="sxs-lookup"><span data-stu-id="ce67b-115">Version</span></span><br/> | <span data-ttu-id="ce67b-116">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ce67b-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ce67b-117">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ce67b-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ce67b-118">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="ce67b-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="ce67b-119">DLL</span><span class="sxs-lookup"><span data-stu-id="ce67b-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="ce67b-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce67b-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="ce67b-121">IID</span><span class="sxs-lookup"><span data-stu-id="ce67b-121">IID</span></span><br/>     | <span data-ttu-id="ce67b-122">IID \_ idatabase ist definiert als 000c109d-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="ce67b-122">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




