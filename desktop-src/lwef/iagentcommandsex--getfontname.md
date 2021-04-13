---
title: Iagentcommandsex getfontname
description: Iagentcommandsex getfontname
ms.assetid: cd0d0d93-839e-471c-9cfa-9f47dcce841b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 215f08cbe1e5e97b218f9279baff5e3affd74956
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388415"
---
# <a name="iagentcommandsexgetfontname"></a><span data-ttu-id="15785-103">Iagentcommandsex:: getfontname</span><span class="sxs-lookup"><span data-stu-id="15785-103">IAgentCommandsEx::GetFontName</span></span>

<span data-ttu-id="15785-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="15785-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontName(
   BSTR * pbszFontName  // address of variable for font displayed 
);                      // in character's pop-up menu
```

<span data-ttu-id="15785-105">Ruft den Wert für die Schriftart ab, die im Popupmenü des Zeichens angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="15785-105">Retrieves the value for the font displayed in the character's pop-up menu.</span></span>

-   <span data-ttu-id="15785-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="15785-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="15785-107"><span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszfontname*</span><span class="sxs-lookup"><span data-stu-id="15785-107"><span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*</span></span>
</dt> <dd>

<span data-ttu-id="15785-108">Die Adresse eines BSTR, der den im Popupmenü des Zeichens angezeigten Schriftart Namen empfängt.</span><span class="sxs-lookup"><span data-stu-id="15785-108">The address of a BSTR that receives the font name displayed in the character's pop-up menu.</span></span>

</dd> </dl>

<span data-ttu-id="15785-109">Der zurückgegebene Schriftart Name entspricht der Schriftart, die zum Anzeigen von Text im Popupmenü des Zeichens verwendet wird, wenn die Client Anwendung aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="15785-109">The font name returned corresponds to the font used to display text in the character's pop-up menu when your client application is input-active.</span></span> <span data-ttu-id="15785-110">Der Standardwert für die Schriftart Einstellung basiert auf der Einstellung für die Menü Schriftart für die Sprach-ID-Einstellung des Zeichens oder, wenn nicht festgelegt, der Standardeinstellung für die Benutzereinstellung für die Sprache.</span><span class="sxs-lookup"><span data-stu-id="15785-110">The default value for the font setting is based on the menu font setting for the character's language ID setting, or if not set, the user default language ID setting.</span></span>

<span data-ttu-id="15785-111">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="15785-111">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="15785-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="15785-112">See Also</span></span>

<span data-ttu-id="15785-113">[**Iagentcommandsex:: setfontname**](iagentcommandsex--setfontname.md), [ **iagentcommandsex:: SetFontSize**](iagentcommandsex--setfontsize.md)</span><span class="sxs-lookup"><span data-stu-id="15785-113">[**IAgentCommandsEx::SetFontName**](iagentcommandsex--setfontname.md), [**IAgentCommandsEx::SetFontSize**](iagentcommandsex--setfontsize.md)</span></span>


 

 




