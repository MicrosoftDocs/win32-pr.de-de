---
description: Werte definieren einen bestimmten SAS-Typ.
ms.assetid: c0a1269b-f9d4-49e1-89ca-526fef148134
title: WLX_SAS_TYPE_XXX (winwlx. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a75c7d7a71855700c4c8c233db3cfc18e06b9d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369731"
---
# <a name="wlx_sas_type_xxx"></a><span data-ttu-id="017ae-103">wlx \_ SAS- \_ Typ \_ xxx</span><span class="sxs-lookup"><span data-stu-id="017ae-103">WLX\_SAS\_TYPE\_XXX</span></span>

<span data-ttu-id="017ae-104">\[Die Konstante "wlx \_ SAS \_ Type \_ xxx" ist nicht mehr für die Verwendung ab Windows Server 2008 und Windows Vista verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="017ae-104">\[The WLX\_SAS\_TYPE\_XXX constant is no longer available for use as of Windows Server 2008 and Windows Vista.\]</span></span>

<span data-ttu-id="017ae-105">Die Werte für den **wlx- \_ SAS- \_ Typ \_ xxx** definieren einen bestimmten SAS-Typ.</span><span class="sxs-lookup"><span data-stu-id="017ae-105">The **WLX\_SAS\_TYPE\_XXX** values define a specific SAS type.</span></span>

> [!Note]  
> <span data-ttu-id="017ae-106">Gina-DLLs werden in Windows Vista ignoriert.</span><span class="sxs-lookup"><span data-stu-id="017ae-106">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="017ae-107">Alle Werte von 0 bis 127 sind für von Microsoft definierte Typen reserviert.</span><span class="sxs-lookup"><span data-stu-id="017ae-107">All values from zero to 127 are reserved for Microsoft-defined types.</span></span> <span data-ttu-id="017ae-108">Werte oberhalb von 127 sind für Kunden definierte Typen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="017ae-108">Values above 127 are available for customer-defined types.</span></span> <span data-ttu-id="017ae-109">Die folgenden Typen werden an Funktionen übergeben, die einen *dwsastype* -Parameter aufweisen.</span><span class="sxs-lookup"><span data-stu-id="017ae-109">The following types are passed to functions that have a *dwSasType* parameter.</span></span>



| <span data-ttu-id="017ae-110">Konstante</span><span class="sxs-lookup"><span data-stu-id="017ae-110">Constant</span></span>                                                                                                                                                                                                         | <span data-ttu-id="017ae-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="017ae-111">Description</span></span>                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WLX_SAS_TYPE_CTRL_ALT_DEL"></span><span id="wlx_sas_type_ctrl_alt_del"></span><dl> <span data-ttu-id="017ae-112"><dt>**wlx \_ SAS \_ Type \_ STRG \_ alt \_ del**</dt></span><span class="sxs-lookup"><span data-stu-id="017ae-112"><dt>**WLX\_SAS\_TYPE\_CTRL\_ALT\_DEL**</dt></span></span> </dl>            | <span data-ttu-id="017ae-113">Gibt an, dass ein Benutzer die standardmäßige STRG + ALT + ENTF-SAS eingegeben hat.</span><span class="sxs-lookup"><span data-stu-id="017ae-113">Indicates a user has typed the standard CTRL+ALT+DEL SAS.</span></span><br/>                                                                                     |
| <span id="WLX_SAS_TYPE_SC_INSERT"></span><span id="wlx_sas_type_sc_insert"></span><dl> <span data-ttu-id="017ae-114"><dt>**wlx \_ SAS \_ Type \_ SC \_ Insert**</dt></span><span class="sxs-lookup"><span data-stu-id="017ae-114"><dt>**WLX\_SAS\_TYPE\_SC\_INSERT**</dt></span></span> </dl>                      | <span data-ttu-id="017ae-115">Gibt an, dass eine [*Smartcard*](../secgloss/s-gly.md) in ein kompatibles Gerät eingefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="017ae-115">Indicates that a [*smart card*](../secgloss/s-gly.md) has been inserted into a compatible device.</span></span><br/> |
| <span id="WLX_SAS_TYPE_SC_REMOVE"></span><span id="wlx_sas_type_sc_remove"></span><dl> <span data-ttu-id="017ae-116"><dt>**wlx \_ SAS \_ Type \_ SC \_ Remove**</dt></span><span class="sxs-lookup"><span data-stu-id="017ae-116"><dt>**WLX\_SAS\_TYPE\_SC\_REMOVE**</dt></span></span> </dl>                      | <span data-ttu-id="017ae-117">Gibt an, dass eine Smartcard von einem kompatiblen Gerät entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="017ae-117">Indicates that a smart card has been removed from a compatible device.</span></span><br/>                                                                        |
| <span id="WLX_SAS_TYPE_SCRNSVR_ACTIVITY"></span><span id="wlx_sas_type_scrnsvr_activity"></span><dl> <span data-ttu-id="017ae-118"><dt>**\_ \_ \_ scrnsvr-Aktivität für wlx-SAS-Typ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="017ae-118"><dt>**WLX\_SAS\_TYPE\_SCRNSVR\_ACTIVITY**</dt></span></span> </dl> | <span data-ttu-id="017ae-119">Gibt an, dass die Tastatur-oder Maus Aktivität aufgetreten ist, während ein sicherer Bildschirmschoner aktiv war.</span><span class="sxs-lookup"><span data-stu-id="017ae-119">Indicates that keyboard or mouse activity occurred while a secure screen saver was active.</span></span><br/>                                                    |
| <span id="WLX_SAS_TYPE_SCRNSVR_TIMEOUT"></span><span id="wlx_sas_type_scrnsvr_timeout"></span><dl> <span data-ttu-id="017ae-120"><dt>**\_ \_ \_ scrnsvr-Timeout für wlx-SAS-Typ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="017ae-120"><dt>**WLX\_SAS\_TYPE\_SCRNSVR\_TIMEOUT**</dt></span></span> </dl>    | <span data-ttu-id="017ae-121">Gibt an, dass die Bildschirmschoner-Aktivierung aufgrund von Tastatur-und Maus Inaktivität aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="017ae-121">Indicates that screen saver activation has occurred due to keyboard and mouse inactivity.</span></span><br/>                                                     |
| <span id="WLX_SAS_TYPE_TIMEOUT"></span><span id="wlx_sas_type_timeout"></span><dl> <span data-ttu-id="017ae-122"><dt>**Timeout für wlx- \_ SAS- \_ Typ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="017ae-122"><dt>**WLX\_SAS\_TYPE\_TIMEOUT**</dt></span></span> </dl>                             | <span data-ttu-id="017ae-123">Gibt an, dass innerhalb des angegebenen Timeout Zeitraums keine Benutzereingaben empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="017ae-123">Indicates that no user input was received within the specified time-out period.</span></span><br/>                                                               |
| <span id="WLX_SAS_TYPE_USER_LOGOFF"></span><span id="wlx_sas_type_user_logoff"></span><dl> <span data-ttu-id="017ae-124"><dt>**Benutzer Abmeldung zum wlx- \_ SAS- \_ Typ \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="017ae-124"><dt>**WLX\_SAS\_TYPE\_USER\_LOGOFF**</dt></span></span> </dl>                | <span data-ttu-id="017ae-125">Gibt an, dass der Benutzer vom System abgemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="017ae-125">Indicates the user is being logged off the system.</span></span><br/>                                                                                            |



## <a name="requirements"></a><span data-ttu-id="017ae-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="017ae-126">Requirements</span></span>



| <span data-ttu-id="017ae-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="017ae-127">Requirement</span></span> | <span data-ttu-id="017ae-128">Wert</span><span class="sxs-lookup"><span data-stu-id="017ae-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="017ae-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="017ae-129">Minimum supported client</span></span><br/> | <span data-ttu-id="017ae-130">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="017ae-130">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="017ae-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="017ae-131">Minimum supported server</span></span><br/> | <span data-ttu-id="017ae-132">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="017ae-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="017ae-133">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="017ae-133">End of client support</span></span><br/>    | <span data-ttu-id="017ae-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="017ae-134">Windows XP</span></span><br/>                                                               |
| <span data-ttu-id="017ae-135">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="017ae-135">End of server support</span></span><br/>    | <span data-ttu-id="017ae-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="017ae-136">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="017ae-137">Header</span><span class="sxs-lookup"><span data-stu-id="017ae-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="017ae-138"><dt>Winwlx. h</dt></span><span class="sxs-lookup"><span data-stu-id="017ae-138"><dt>Winwlx.h</dt></span></span> </dl> |



 

 
