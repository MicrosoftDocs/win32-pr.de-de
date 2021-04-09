---
title: Globalvoicecommandsenabled (Eigenschaft)
description: Globalvoicecommandsenabled (Eigenschaft)
ms.assetid: d4f74019-fa33-41fc-abe7-01791ff188f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8f523171187c9956a7741afc0fabcc7ec794071
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948751"
---
# <a name="globalvoicecommandsenabled-property"></a><span data-ttu-id="1a4e6-103">Globalvoicecommandsenabled (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1a4e6-103">GlobalVoiceCommandsEnabled Property</span></span>

<span data-ttu-id="1a4e6-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="1a4e6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="1a4e6-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1a4e6-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="1a4e6-106">Gibt zurück oder legt fest, ob Voice für die globalen Befehle des Agents aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1a4e6-106">Returns or sets whether voice is enabled for Agent's global commands.</span></span>

</dd> <dt>

<span data-ttu-id="1a4e6-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="1a4e6-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="1a4e6-108">*Büros. ***Zeichen ("*** Merkmal-ID \* \* *"). Commands. globalvoicecommandsenabled**</span><span class="sxs-lookup"><span data-stu-id="1a4e6-108">*agent.\*\*\*Characters("*\*\* CharacterID\***").Commands.GlobalVoiceCommandsEnabled**</span></span>

<span data-ttu-id="1a4e6-109">\[ = *booleschen*\]</span><span class="sxs-lookup"><span data-stu-id="1a4e6-109">\[ = *boolean*\]</span></span>



| <span data-ttu-id="1a4e6-110">Teil</span><span class="sxs-lookup"><span data-stu-id="1a4e6-110">Part</span></span>      | <span data-ttu-id="1a4e6-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1a4e6-111">Description</span></span>                                                                                                                                                                                                            |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a4e6-112">*boolean*</span><span class="sxs-lookup"><span data-stu-id="1a4e6-112">*boolean*</span></span> | <span data-ttu-id="1a4e6-113">Ein boolescher Ausdruck, der angibt, ob sprach Parameter für die globalen Befehle des Agents aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="1a4e6-113">A Boolean expression that indicates whether voice parameters for Agent's global commands are enabled.</span></span> <span data-ttu-id="1a4e6-114">**True** (Standard) sprach Parameter sind aktiviert.</span><span class="sxs-lookup"><span data-stu-id="1a4e6-114">**True** (Default) Voice parameters are enabled.</span></span> <br/> <span data-ttu-id="1a4e6-115">**False** Sprach Parameter sind deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="1a4e6-115">**False** Voice parameters are disabled.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a4e6-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1a4e6-116">Remarks</span></span>

<span data-ttu-id="1a4e6-117">Der Microsoft-Agent fügt automatisch sprach Parameter (Grammatik) zum Öffnen und Schließen des Sprachbefehle Fensters und zum ein-und Ausblenden des Zeichens hinzu.</span><span class="sxs-lookup"><span data-stu-id="1a4e6-117">Microsoft Agent automatically adds voice parameters (grammar) for opening and closing the Voice Commands Window and for showing and hiding the character.</span></span> <span data-ttu-id="1a4e6-118">Wenn Sie **globalvoicecommandsenabled** auf **false** festlegen, deaktiviert der-Agent alle sprach Parameter für diese Befehle sowie die sprach Parameter für die [**Beschriftung**](caption-property.md) der [**Befehls**](/windows/desktop/lwef/the-commands-collection-object) Objekte anderer Clients.</span><span class="sxs-lookup"><span data-stu-id="1a4e6-118">If you set **GlobalVoiceCommandsEnabled** to **False**, Agent disables any voice parameters for these commands as well as the voice parameters for the [**Caption**](caption-property.md) of other client's [**Commands**](/windows/desktop/lwef/the-commands-collection-object) objects.</span></span> <span data-ttu-id="1a4e6-119">Dies ermöglicht es Ihnen, diese aus der aktuellen aktiven Grammatik Ihres Clients auszuschließen.</span><span class="sxs-lookup"><span data-stu-id="1a4e6-119">This enables you to eliminate these from your client's current active grammar.</span></span> <span data-ttu-id="1a4e6-120">Da dadurch jedoch möglicherweise der sprach Zugriff auf andere Clients blockiert wird, setzen Sie diese Eigenschaft nach dem Verarbeiten der Spracheingabe des Benutzers auf " **true** " zurück.</span><span class="sxs-lookup"><span data-stu-id="1a4e6-120">However, because this potentially blocks voice access to other clients, reset this property to **True** after processing the user's voice input.</span></span>

<span data-ttu-id="1a4e6-121">Das Deaktivieren der Eigenschaft wirkt sich nicht auf das Popup Menü des Zeichens aus.</span><span class="sxs-lookup"><span data-stu-id="1a4e6-121">Disabling the property does not affect the character's pop-up menu.</span></span> <span data-ttu-id="1a4e6-122">Die vom Server hinzugefügten globalen Befehle werden weiterhin angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1a4e6-122">The global commands added by the server will still appear.</span></span> <span data-ttu-id="1a4e6-123">Sie können Sie nicht aus dem Popupmenü entfernen.</span><span class="sxs-lookup"><span data-stu-id="1a4e6-123">You cannot remove them from the pop-up menu.</span></span>

 

