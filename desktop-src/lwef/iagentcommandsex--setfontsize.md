---
title: Iagentcommandsex SetFontSize
description: Iagentcommandsex SetFontSize
ms.assetid: 095f78d2-ef91-4880-ad49-dd9a94f02891
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19bb9a638141dc3cebe683748500510ea848a664
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472860"
---
# <a name="iagentcommandsexsetfontsize"></a><span data-ttu-id="7a326-103">Iagentcommandsex:: SetFontSize</span><span class="sxs-lookup"><span data-stu-id="7a326-103">IAgentCommandsEx::SetFontSize</span></span>

<span data-ttu-id="7a326-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="7a326-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontSize(
   long lFontSize  // font size displayed in character's pop-up menu
);
```

<span data-ttu-id="7a326-105">Legt die Größe der Schriftart fest, die im Popupmenü des Zeichens angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7a326-105">Sets the size of the font displayed in the character's pop-up menu.</span></span>

-   <span data-ttu-id="7a326-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="7a326-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="7a326-107"><span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lfontsize*</span><span class="sxs-lookup"><span data-stu-id="7a326-107"><span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*</span></span>
</dt> <dd>

<span data-ttu-id="7a326-108">Der Schriftgrad.</span><span class="sxs-lookup"><span data-stu-id="7a326-108">The size of the font.</span></span>

</dd> </dl>

<span data-ttu-id="7a326-109">Diese Eigenschaft bestimmt die Punktgröße der Schriftart, die zum Anzeigen von Text im Popupmenü des Zeichens verwendet wird, wenn die Client Anwendung aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="7a326-109">This property determines the point size of the font used to display text in the character's pop-up menu when your client application is input-active.</span></span> <span data-ttu-id="7a326-110">Der Standardwert für die Schriftart Einstellung basiert auf der Einstellung für die Einstellung des Menüs für die Sprach-ID-Einstellung des Zeichens oder, wenn dies nicht festgelegt ist, der Standard Spracheinstellung des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="7a326-110">The default value for the font setting is based on the menu font setting for the character's language ID setting-or if that's not set-the user default language setting.</span></span> <span data-ttu-id="7a326-111">Wenn die Eingabe nicht aktiv ist, wird der Text der [**Befehls**](/windows/desktop/lwef/the-command-object) [**Beschriftung**](caption-property.md) der Client Anwendung in der für den Eingabe aktiven Client angegebenen Punktgröße angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7a326-111">If not input-active, your client application's [**Command**](/windows/desktop/lwef/the-command-object) [**Caption**](caption-property.md) text appears in the point size specified for the input-active client.</span></span>

<span data-ttu-id="7a326-112">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="7a326-112">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="7a326-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7a326-113">See Also</span></span>

<span data-ttu-id="7a326-114">[**Iagentcommandsex:: GetFontSize**](iagentcommandsex--getfontsize.md), [**iagentcommandsex:: getfontname**](iagentcommandsex--getfontname.md), [**iagentcommandsex:: setfontname**](iagentcommandsex--setfontname.md)</span><span class="sxs-lookup"><span data-stu-id="7a326-114">[**IAgentCommandsEx::GetFontSize**](iagentcommandsex--getfontsize.md), [**IAgentCommandsEx::GetFontName**](iagentcommandsex--getfontname.md), [**IAgentCommandsEx::SetFontName**](iagentcommandsex--setfontname.md)</span></span>


 

 