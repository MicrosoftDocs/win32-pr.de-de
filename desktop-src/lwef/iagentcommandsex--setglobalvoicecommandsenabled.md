---
title: Iagentcommandsex setglobalvoicecommandsenabled
description: Iagentcommandsex setglobalvoicecommandsenabled
ms.assetid: f456b1d3-60aa-4b90-90d0-6c695947fa8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87a576a36d3df4b3ddf0ca71f5709a712a3c9e1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101562"
---
# <a name="iagentcommandsexsetglobalvoicecommandsenabled"></a><span data-ttu-id="0ca25-103">Iagentcommandsex:: setglobalvoicecommandsenabled</span><span class="sxs-lookup"><span data-stu-id="0ca25-103">IAgentCommandsEx::SetGlobalVoiceCommandsEnabled</span></span>

<span data-ttu-id="0ca25-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="0ca25-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetGlobalVoiceCommandsEnabled(
 long bEnable  // Enabled setting for Agent's global voice commands
);
```

<span data-ttu-id="0ca25-105">Legt die [**aktivierte**](enabled-property.md) Eigenschaft für die Sprachgrammatik der globalen Befehle des Microsoft-Agents fest.</span><span class="sxs-lookup"><span data-stu-id="0ca25-105">Sets the [**Enabled**](enabled-property.md) property for the voice grammar of Microsoft Agent's global commands.</span></span>

-   <span data-ttu-id="0ca25-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="0ca25-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="0ca25-107"><span id="bEnable"></span><span id="benable"></span><span id="BENABLE"></span>*benabel*</span><span class="sxs-lookup"><span data-stu-id="0ca25-107"><span id="bEnable"></span><span id="benable"></span><span id="BENABLE"></span>*bEnable*</span></span>
</dt> <dd>

<span data-ttu-id="0ca25-108">Ein boolescher Wert, der festlegt, ob die Sprachgrammatik der globalen Befehle des Agents aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="0ca25-108">A Boolean value that sets whether the voice grammar of Agent's global commands is enabled.</span></span> <span data-ttu-id="0ca25-109">**True** aktiviert die Sprachgrammatik; **False** deaktiviert es.</span><span class="sxs-lookup"><span data-stu-id="0ca25-109">**True** enables the voice grammar; **False** disables it.</span></span>

</dd> </dl>

<span data-ttu-id="0ca25-110">Der Microsoft-Agent fügt automatisch sprach Parameter (Grammatik) zum Öffnen und Schließen des Sprachbefehle Fensters und zum ein-und Ausblenden des Zeichens hinzu.</span><span class="sxs-lookup"><span data-stu-id="0ca25-110">Microsoft Agent automatically adds voice parameters (grammar) for opening and closing the Voice Commands Window and for showing and hiding the character.</span></span> <span data-ttu-id="0ca25-111">Wenn diese Einstellung auf " **false**" festgelegt ist, deaktiviert der-Agent alle sprach Parameter für diese Befehle sowie die sprach Parameter für die [**Beschriftung**](caption-property.md) der [**Befehls**](/windows/desktop/lwef/the-command-object) Objekte anderer Clients.</span><span class="sxs-lookup"><span data-stu-id="0ca25-111">When set to **False**, Agent disables any voice parameters for these commands as well as the voice parameters for the [**Caption**](caption-property.md) of other client's [**Command**](/windows/desktop/lwef/the-command-object) objects.</span></span> <span data-ttu-id="0ca25-112">Dies ermöglicht es Ihnen, diese aus der aktuellen aktiven Grammatik Ihres Clients auszuschließen.</span><span class="sxs-lookup"><span data-stu-id="0ca25-112">This enables you to eliminate these from your client's current active grammar.</span></span> <span data-ttu-id="0ca25-113">Da dadurch jedoch möglicherweise der sprach Zugriff auf andere Clients blockiert wird, setzen Sie diese Eigenschaft nach dem Verarbeiten der Spracheingabe des Benutzers auf " **true** " zurück.</span><span class="sxs-lookup"><span data-stu-id="0ca25-113">However, because this potentially blocks voice access to other clients, reset this property to **True** after processing the user's voice input.</span></span>

<span data-ttu-id="0ca25-114">Das Deaktivieren der Eigenschaft wirkt sich nicht auf das Popup Menü des Zeichens aus.</span><span class="sxs-lookup"><span data-stu-id="0ca25-114">Disabling the property does not affect the character's pop-up menu.</span></span> <span data-ttu-id="0ca25-115">Die vom Server hinzugefügten globalen Befehle werden weiterhin angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0ca25-115">The global commands added by the server will still appear.</span></span> <span data-ttu-id="0ca25-116">Sie können Sie nicht aus dem Popupmenü entfernen.</span><span class="sxs-lookup"><span data-stu-id="0ca25-116">You cannot remove them from the pop-up menu.</span></span>

## <a name="see-also"></a><span data-ttu-id="0ca25-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0ca25-117">See Also</span></span>

[<span data-ttu-id="0ca25-118">**Iagentcommandsex:: getglobalvoicecommandsenabled**</span><span class="sxs-lookup"><span data-stu-id="0ca25-118">**IAgentCommandsEx::GetGlobalVoiceCommandsEnabled**</span></span>](iagentcommandsex--getglobalvoicecommandsenabled.md)


 

 