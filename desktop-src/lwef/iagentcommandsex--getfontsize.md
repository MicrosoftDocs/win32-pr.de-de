---
title: Iagentcommandsex GetFontSize
description: Iagentcommandsex GetFontSize
ms.assetid: 8173e026-d28f-43d8-a8b4-96d1d97a8b68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a2450d94e89dd9dddc00a11af7f37bf4837558
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388414"
---
# <a name="iagentcommandsexgetfontsize"></a><span data-ttu-id="c5beb-103">Iagentcommandsex:: GetFontSize</span><span class="sxs-lookup"><span data-stu-id="c5beb-103">IAgentCommandsEx::GetFontSize</span></span>

<span data-ttu-id="c5beb-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="c5beb-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontSize(
   long * plFontSize  // address of variable for font size 
);                    // for font displayed in character's pop-up menu
```

<span data-ttu-id="c5beb-105">Ruft den Wert für die Größe der Schriftart ab, die im Popupmenü des Zeichens angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c5beb-105">Retrieves the value for the size of the font displayed in the character's pop-up menu.</span></span>

-   <span data-ttu-id="c5beb-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="c5beb-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="c5beb-107"><span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plfontsize*</span><span class="sxs-lookup"><span data-stu-id="c5beb-107"><span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plFontSize*</span></span>
</dt> <dd>

<span data-ttu-id="c5beb-108">Die Adresse eines Werts, der die Größe der Schriftart erhält.</span><span class="sxs-lookup"><span data-stu-id="c5beb-108">The address of a value that receives the size of the font.</span></span>

</dd> </dl>

<span data-ttu-id="c5beb-109">Die Punktgröße der zurückgegebenen Schriftart entspricht der Größe, die für die Anzeige von Text im Popup Menü des Zeichens definiert ist, wenn der Client für die Eingabe aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c5beb-109">The point size of the font returned corresponds to the size defined to display text in the character's pop-up menu when your client is input-active.</span></span> <span data-ttu-id="c5beb-110">Der Standardwert für die Schriftart Einstellung basiert auf der Einstellung für die Menü Schriftart für die Sprach-ID-Einstellung des Zeichens oder, wenn nicht festgelegt, der Standard Spracheinstellung des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="c5beb-110">The default value for the font setting is based on the menu font setting for the character's language ID setting, or if not set, the user default language setting.</span></span>

<span data-ttu-id="c5beb-111">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="c5beb-111">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="c5beb-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c5beb-112">See Also</span></span>

<span data-ttu-id="c5beb-113">[**Iagentcommandsex:: SetFontSize**](iagentcommandsex--setfontsize.md), [ **iagentcommandsex:: setfontname**](iagentcommandsex--setfontname.md)</span><span class="sxs-lookup"><span data-stu-id="c5beb-113">[**IAgentCommandsEx::SetFontSize**](iagentcommandsex--setfontsize.md), [**IAgentCommandsEx::SetFontName**](iagentcommandsex--setfontname.md)</span></span>


 

 




