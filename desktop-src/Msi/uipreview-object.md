---
description: Das uipreview-Objekt wird verwendet, um Benutzeroberflächen-Dialogfelder und-Plakate während der Erstellung anzuzeigen. Dieses Objekt wird von der enableuipreview-Methode des Database-Objekts erstellt.
ms.assetid: 5df2a4f3-6352-4575-b822-1811150a86be
title: Uipreview-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6650dc9bcc66a24d0e8a9d7f0d971884a2379f60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368421"
---
# <a name="uipreview-object"></a><span data-ttu-id="fa703-104">Uipreview-Objekt</span><span class="sxs-lookup"><span data-stu-id="fa703-104">UIPreview object</span></span>

<span data-ttu-id="fa703-105">Das **uipreview** -Objekt wird verwendet, um Benutzeroberflächen-Dialogfelder und-Plakate während der Erstellung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="fa703-105">The **UIPreview** object is used to view user interface dialog boxes and billboards during authoring.</span></span> <span data-ttu-id="fa703-106">Dieses Objekt wird von der [**enableuipreview**](database-enableuipreview.md) -Methode des [**Database**](database-object.md) -Objekts erstellt.</span><span class="sxs-lookup"><span data-stu-id="fa703-106">This object is created by the [**EnableUIPreview**](database-enableuipreview.md) method of the [**Database**](database-object.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="fa703-107">Member</span><span class="sxs-lookup"><span data-stu-id="fa703-107">Members</span></span>

<span data-ttu-id="fa703-108">Das **uipreview** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="fa703-108">The **UIPreview** object has these types of members:</span></span>

-   [<span data-ttu-id="fa703-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="fa703-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="fa703-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fa703-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fa703-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="fa703-111">Methods</span></span>

<span data-ttu-id="fa703-112">Das **uipreview** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="fa703-112">The **UIPreview** object has these methods.</span></span>



| <span data-ttu-id="fa703-113">Methode</span><span class="sxs-lookup"><span data-stu-id="fa703-113">Method</span></span>                                           | <span data-ttu-id="fa703-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fa703-114">Description</span></span>                                                                                             |
|:-------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa703-115">**Viewbillboard**</span><span class="sxs-lookup"><span data-stu-id="fa703-115">**ViewBillboard**</span></span>](uipreview-viewbillboard.md) | <span data-ttu-id="fa703-116">Zeigt ein erstelltes Billboard mithilfe des Host Steuer Elements im momentan angezeigten Dialogfeld an.</span><span class="sxs-lookup"><span data-stu-id="fa703-116">Displays an authored billboard using the host control in the currently displayed dialog box.</span></span><br/> |
| [<span data-ttu-id="fa703-117">**Viewdialog**</span><span class="sxs-lookup"><span data-stu-id="fa703-117">**ViewDialog**</span></span>](uipreview-viewdialog.md)       | <span data-ttu-id="fa703-118">Zeigt das in der aktuellen Datenbank gespeicherte Dialogfeld "erstellte Benutzeroberfläche" an.</span><span class="sxs-lookup"><span data-stu-id="fa703-118">Displays an authored UI dialog box stored in the current database.</span></span><br/>                           |



 

### <a name="properties"></a><span data-ttu-id="fa703-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fa703-119">Properties</span></span>

<span data-ttu-id="fa703-120">Das **uipreview** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fa703-120">The **UIPreview** object has these properties.</span></span>



| <span data-ttu-id="fa703-121">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fa703-121">Property</span></span>                                          | <span data-ttu-id="fa703-122">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="fa703-122">Access type</span></span>           | <span data-ttu-id="fa703-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fa703-123">Description</span></span>                                                                                                                                                                       |
|:--------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa703-124">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="fa703-124">**Property**</span></span>](uipreview-property.md)<br/> | <span data-ttu-id="fa703-125">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fa703-125">Read/write</span></span><br/> | <span data-ttu-id="fa703-126">Stellt den Zeichen folgen Wert einer benannten installereigenschaft oder, wenn ein Prozentzeichen (%) als Präfix vorangestellt ist, den Wert einer System Umgebungsvariablen für den aktuellen Prozess dar.</span><span class="sxs-lookup"><span data-stu-id="fa703-126">Represents the string value of a named installer property or, if prefixed with a percent sign (%), the value of a system environment variable for the current process.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fa703-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa703-127">Requirements</span></span>



| <span data-ttu-id="fa703-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fa703-128">Requirement</span></span> | <span data-ttu-id="fa703-129">Wert</span><span class="sxs-lookup"><span data-stu-id="fa703-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa703-130">Version</span><span class="sxs-lookup"><span data-stu-id="fa703-130">Version</span></span><br/> | <span data-ttu-id="fa703-131">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fa703-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="fa703-132">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fa703-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="fa703-133">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="fa703-133">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="fa703-134">DLL</span><span class="sxs-lookup"><span data-stu-id="fa703-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="fa703-135"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa703-135"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="fa703-136">IID</span><span class="sxs-lookup"><span data-stu-id="fa703-136">IID</span></span><br/>     | <span data-ttu-id="fa703-137">IID \_ iuipreview ist definiert als 000c109a-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="fa703-137">IID\_IUIPreview is defined as 000C109A-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="fa703-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa703-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa703-139">Skript Beispiele für Windows Installer</span><span class="sxs-lookup"><span data-stu-id="fa703-139">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




