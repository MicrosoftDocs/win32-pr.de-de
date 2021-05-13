---
description: Wird von der Shell implementiert, damit Skripts und Microsoft Visual Basic Entwickler einige der in der Shell verfügbaren Features verwenden können. Das ShellUIHelper-Objekt verfügt nicht über Eigenschaften oder Ereignisse. Es werden Methoden zum Hinzufügen von Elementen zur Shell bereitgestellt.
title: ShellUIHelper-Objekt (Exdisp.h)
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
ms.openlocfilehash: b77d618c4c772859a9009f3cca761c59df83257a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842431"
---
# <a name="shelluihelper-object"></a><span data-ttu-id="7cf11-105">ShellUIHelper-Objekt</span><span class="sxs-lookup"><span data-stu-id="7cf11-105">ShellUIHelper object</span></span>

<span data-ttu-id="7cf11-106">Wird von der Shell implementiert, um Skripts und Microsoft Visual Basic Entwickler bei der Verwendung einiger der in der Shell verfügbaren Features zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7cf11-106">Implemented by the Shell to help script and Microsoft Visual Basic developers use some of the features available in the Shell.</span></span> <span data-ttu-id="7cf11-107">Das **ShellUIHelper-Objekt** verfügt nicht über Eigenschaften oder Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="7cf11-107">The **ShellUIHelper** object does not have any properties or events.</span></span> <span data-ttu-id="7cf11-108">Es werden Methoden zum Hinzufügen von Elementen zur Shell bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="7cf11-108">Methods are provided to add items to the Shell.</span></span>

## <a name="members"></a><span data-ttu-id="7cf11-109">Member</span><span class="sxs-lookup"><span data-stu-id="7cf11-109">Members</span></span>

<span data-ttu-id="7cf11-110">Das **ShellUIHelper-Objekt** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7cf11-110">The **ShellUIHelper** object has these types of members:</span></span>

-   [<span data-ttu-id="7cf11-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="7cf11-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7cf11-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="7cf11-112">Methods</span></span>

<span data-ttu-id="7cf11-113">Das **ShellUIHelper-Objekt** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="7cf11-113">The **ShellUIHelper** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="7cf11-114">Methode</span><span class="sxs-lookup"><span data-stu-id="7cf11-114">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="7cf11-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7cf11-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="7cf11-116"><a href="shelluihelper-addchannel.md"><strong>AddChannel</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cf11-116"><a href="shelluihelper-addchannel.md"><strong>AddChannel</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="7cf11-117">Fügt der Liste der Kanäle im Menü <strong>"Favoriten"</strong> Internet Explorer und der <strong>Kanalleiste</strong> auf dem Desktop einen neuen Kanal hinzu.</span><span class="sxs-lookup"><span data-stu-id="7cf11-117">Adds a new channel to the list of channels in the Internet Explorer <strong>Favorites</strong> menu and to the <strong>Channel</strong> bar on the desktop.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7cf11-118">Diese Methode wird unter Windows Vista nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7cf11-118">This method is no longer supported under Windows Vista.</span></span> <span data-ttu-id="7cf11-119">Unter diesem Betriebssystem wird E_NOTIMPL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7cf11-119">Under that operating system, it returns E_NOTIMPL.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="7cf11-120"><a href="shelluihelper-adddesktopcomponent.md"><strong>AddDesktopComponent</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cf11-120"><a href="shelluihelper-adddesktopcomponent.md"><strong>AddDesktopComponent</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="7cf11-121">Fügt dem Active Desktop ein Element hinzu.</span><span class="sxs-lookup"><span data-stu-id="7cf11-121">Adds an item to the Active Desktop.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="7cf11-122"><a href="shelluihelper-addfavorite.md"><strong>AddFavorite</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cf11-122"><a href="shelluihelper-addfavorite.md"><strong>AddFavorite</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="7cf11-123">Zeigt die Standardbenutzerschnittstelle zum Erstellen eines bevorzugten Elements an.</span><span class="sxs-lookup"><span data-stu-id="7cf11-123">Displays the default user interface for creating a favorite item.</span></span> <span data-ttu-id="7cf11-124">Die Benutzeroberfläche wird mit den angegebenen Parametern initialisiert.</span><span class="sxs-lookup"><span data-stu-id="7cf11-124">The user interface is initialized to the specified parameters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="7cf11-125"><a href="shelluihelper-issubscribed.md"><strong>IsSubscribed</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cf11-125"><a href="shelluihelper-issubscribed.md"><strong>IsSubscribed</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="7cf11-126">Gibt an, ob eine angegebene URL abonniert wird.</span><span class="sxs-lookup"><span data-stu-id="7cf11-126">Indicates whether a specified URL is subscribed to.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="7cf11-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7cf11-127">Requirements</span></span>



| <span data-ttu-id="7cf11-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7cf11-128">Requirement</span></span> | <span data-ttu-id="7cf11-129">Wert</span><span class="sxs-lookup"><span data-stu-id="7cf11-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cf11-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7cf11-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7cf11-131">Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7cf11-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7cf11-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7cf11-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7cf11-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7cf11-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7cf11-134">Header</span><span class="sxs-lookup"><span data-stu-id="7cf11-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cf11-135"><dt>Exdisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="7cf11-135"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="7cf11-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7cf11-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7cf11-137"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="7cf11-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




