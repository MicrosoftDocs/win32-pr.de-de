---
description: Wird von der Shell implementiert, damit Skripts und Microsoft Visual Basic-Entwicklern einige der in der Shell verfügbaren Features verwenden können. Das shelluihelper-Objekt hat keine Eigenschaften oder Ereignisse. Es werden Methoden bereitgestellt, um der Shell Elemente hinzuzufügen.
title: Shelluihelper-Objekt (Exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9fffebc8-29b9-4064-b60c-c8c63690a79e
ms.openlocfilehash: f0df3b02624a802c19663b67cbcab508c3e0e487
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980720"
---
# <a name="shelluihelper-object"></a><span data-ttu-id="7f55f-105">Shelluihelper-Objekt</span><span class="sxs-lookup"><span data-stu-id="7f55f-105">ShellUIHelper object</span></span>

<span data-ttu-id="7f55f-106">Wird von der Shell implementiert, damit Skripts und Microsoft Visual Basic-Entwicklern einige der in der Shell verfügbaren Features verwenden können.</span><span class="sxs-lookup"><span data-stu-id="7f55f-106">Implemented by the Shell to help script and Microsoft Visual Basic developers use some of the features available in the Shell.</span></span> <span data-ttu-id="7f55f-107">Das **shelluihelper** -Objekt hat keine Eigenschaften oder Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="7f55f-107">The **ShellUIHelper** object does not have any properties or events.</span></span> <span data-ttu-id="7f55f-108">Es werden Methoden bereitgestellt, um der Shell Elemente hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="7f55f-108">Methods are provided to add items to the Shell.</span></span>

## <a name="members"></a><span data-ttu-id="7f55f-109">Member</span><span class="sxs-lookup"><span data-stu-id="7f55f-109">Members</span></span>

<span data-ttu-id="7f55f-110">Das **shelluihelper** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7f55f-110">The **ShellUIHelper** object has these types of members:</span></span>

-   [<span data-ttu-id="7f55f-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="7f55f-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7f55f-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="7f55f-112">Methods</span></span>

<span data-ttu-id="7f55f-113">Das **shelluihelper** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="7f55f-113">The **ShellUIHelper** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="7f55f-114">Methode</span><span class="sxs-lookup"><span data-stu-id="7f55f-114">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="7f55f-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7f55f-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="7f55f-116"><a href="shelluihelper-addchannel.md"><strong>Addchannel</strong></a></span><span class="sxs-lookup"><span data-stu-id="7f55f-116"><a href="shelluihelper-addchannel.md"><strong>AddChannel</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="7f55f-117">Fügt der Liste der Channels im Internet Explorer-Menü " <strong>Favoriten</strong> " und der <strong>Kanal</strong> Leiste auf dem Desktop einen neuen Kanal hinzu.</span><span class="sxs-lookup"><span data-stu-id="7f55f-117">Adds a new channel to the list of channels in the Internet Explorer <strong>Favorites</strong> menu and to the <strong>Channel</strong> bar on the desktop.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7f55f-118">Diese Methode wird unter Windows Vista nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7f55f-118">This method is no longer supported under Windows Vista.</span></span> <span data-ttu-id="7f55f-119">Unter diesem Betriebssystem wird E_NOTIMPL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7f55f-119">Under that operating system, it returns E_NOTIMPL.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="7f55f-120"><a href="shelluihelper-adddesktopcomponent.md"><strong>Adddesktopcomponent</strong></a></span><span class="sxs-lookup"><span data-stu-id="7f55f-120"><a href="shelluihelper-adddesktopcomponent.md"><strong>AddDesktopComponent</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="7f55f-121">Fügt dem aktiven Desktop ein Element hinzu.</span><span class="sxs-lookup"><span data-stu-id="7f55f-121">Adds an item to the Active Desktop.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="7f55f-122"><a href="shelluihelper-addfavorite.md"><strong>Addfavorit</strong></a></span><span class="sxs-lookup"><span data-stu-id="7f55f-122"><a href="shelluihelper-addfavorite.md"><strong>AddFavorite</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="7f55f-123">Zeigt die Standardbenutzer Oberfläche zum Erstellen eines bevorzugten Elements an.</span><span class="sxs-lookup"><span data-stu-id="7f55f-123">Displays the default user interface for creating a favorite item.</span></span> <span data-ttu-id="7f55f-124">Die Benutzeroberfläche wird mit den angegebenen Parametern initialisiert.</span><span class="sxs-lookup"><span data-stu-id="7f55f-124">The user interface is initialized to the specified parameters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="7f55f-125"><a href="shelluihelper-issubscribed.md"><strong>IsSubscribed</strong></a></span><span class="sxs-lookup"><span data-stu-id="7f55f-125"><a href="shelluihelper-issubscribed.md"><strong>IsSubscribed</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="7f55f-126">Gibt an, ob eine angegebene URL abonniert ist.</span><span class="sxs-lookup"><span data-stu-id="7f55f-126">Indicates whether a specified URL is subscribed to.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="7f55f-127">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="7f55f-127">Requirements</span></span>



| <span data-ttu-id="7f55f-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f55f-128">Requirement</span></span> | <span data-ttu-id="7f55f-129">Wert</span><span class="sxs-lookup"><span data-stu-id="7f55f-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f55f-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7f55f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7f55f-131">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7f55f-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7f55f-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7f55f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7f55f-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7f55f-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7f55f-134">Header</span><span class="sxs-lookup"><span data-stu-id="7f55f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f55f-135"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f55f-135"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="7f55f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7f55f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f55f-137"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="7f55f-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




