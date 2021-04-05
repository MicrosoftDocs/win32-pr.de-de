---
title: Iagentcommandsex setfontname
description: Iagentcommandsex setfontname
ms.assetid: c676ceb6-c098-4ac0-9103-ece469317ad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9a4b76a58fc3651c02bedc43f8d372f607c2df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708159"
---
# <a name="iagentcommandsexsetfontname"></a><span data-ttu-id="957e8-103">Iagentcommandsex:: setfontname</span><span class="sxs-lookup"><span data-stu-id="957e8-103">IAgentCommandsEx::SetFontName</span></span>

<span data-ttu-id="957e8-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="957e8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontName(
   BSTR bszFontName  // font to be displayed in character's pop-up menu
);
```

<span data-ttu-id="957e8-105">Legt die im Popupmenü des Zeichens angezeigte Schriftart fest.</span><span class="sxs-lookup"><span data-stu-id="957e8-105">Sets the font displayed in the character's pop-up menu.</span></span>

-   <span data-ttu-id="957e8-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="957e8-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="957e8-107"><span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszfontname*</span><span class="sxs-lookup"><span data-stu-id="957e8-107"><span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszFontName*</span></span>
</dt> <dd>

<span data-ttu-id="957e8-108">Ein BSTR, das die im Popupmenü des Zeichens angezeigte Schriftart festlegt.</span><span class="sxs-lookup"><span data-stu-id="957e8-108">A BSTR that sets the font displayed in the character's pop-up menu.</span></span>

</dd> </dl>

<span data-ttu-id="957e8-109">Diese Eigenschaft bestimmt die Schriftart, die zum Anzeigen von Text im Popupmenü des Zeichens verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="957e8-109">This property determines the font used to display text in the character's pop-up menu.</span></span> <span data-ttu-id="957e8-110">Der Standardwert für die Schriftart Einstellung basiert auf der Menü Schriftart Einstellung für die Sprach-ID-Einstellung des Zeichens-oder, wenn dies nicht festgelegt ist, der Standardeinstellung für die Benutzereinstellung für die Sprache.</span><span class="sxs-lookup"><span data-stu-id="957e8-110">The default value for the font setting is based on the menu font setting for the character's language ID setting-or if that's not set-the user default language ID setting.</span></span>

<span data-ttu-id="957e8-111">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="957e8-111">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="957e8-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="957e8-112">See Also</span></span>

<span data-ttu-id="957e8-113">[**Iagentcommandsex:: getfontname**](iagentcommandsex--getfontname.md), [**iagentcommandsex:: GetFontSize**](iagentcommandsex--getfontsize.md), [**iagentcommandsex:: SetFontSize**](iagentcommandsex--setfontsize.md)</span><span class="sxs-lookup"><span data-stu-id="957e8-113">[**IAgentCommandsEx::GetFontName**](iagentcommandsex--getfontname.md), [**IAgentCommandsEx::GetFontSize**](iagentcommandsex--getfontsize.md), [**IAgentCommandsEx::SetFontSize**](iagentcommandsex--setfontsize.md)</span></span>


 

 




