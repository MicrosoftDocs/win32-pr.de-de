---
title: Iagentcharacter SetName
description: Iagentcharacter SetName
ms.assetid: 4944f910-60e9-446b-82e9-2794f445789a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec058e338adfa8c998bf26a1223ae71f0c7de3d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341269"
---
# <a name="iagentcharactersetname"></a><span data-ttu-id="18980-103">Iagentcharacter:: SetName</span><span class="sxs-lookup"><span data-stu-id="18980-103">IAgentCharacter::SetName</span></span>

<span data-ttu-id="18980-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="18980-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetName(
   BSTR bszName   // character name
);
```

<span data-ttu-id="18980-105">Legt den Namen des Zeichens fest.</span><span class="sxs-lookup"><span data-stu-id="18980-105">Sets the name of the character.</span></span>

-   <span data-ttu-id="18980-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="18980-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="18980-107"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszname*</span><span class="sxs-lookup"><span data-stu-id="18980-107"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*</span></span>
</dt> <dd>

<span data-ttu-id="18980-108">Ein BSTR, das den Namen des Zeichens festlegt.</span><span class="sxs-lookup"><span data-stu-id="18980-108">A BSTR that sets the character's name.</span></span> <span data-ttu-id="18980-109">Der Standardname eines Zeichens wird bei der Kompilierung mit dem Microsoft-Agent-Zeichen-Editor definiert.</span><span class="sxs-lookup"><span data-stu-id="18980-109">A character's default name is defined when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="18980-110">Sie können es mit **iagentcharacter:: SetName**; ändern. Dadurch wird jedoch der Zeichen Name für alle aktuellen Clients des Zeichens geändert.</span><span class="sxs-lookup"><span data-stu-id="18980-110">You can change it using **IAgentCharacter::SetName**; however, this changes the character name for all current clients of the character.</span></span> <span data-ttu-id="18980-111">Diese Eigenschaft ist nicht persistent (wird permanent gespeichert).</span><span class="sxs-lookup"><span data-stu-id="18980-111">This property is not persistent (stored permanently).</span></span> <span data-ttu-id="18980-112">Der Name des Zeichens wird auf den Standardnamen zurückgesetzt, wenn das Zeichen zuerst von einem Client geladen wird.</span><span class="sxs-lookup"><span data-stu-id="18980-112">The character's name reverts to its default name whenever the character is first loaded by a client.</span></span>

<span data-ttu-id="18980-113">Der Name des Zeichens kann auch von seiner Sprach-ID abhängen.</span><span class="sxs-lookup"><span data-stu-id="18980-113">The character's name may also depend on its language ID.</span></span> <span data-ttu-id="18980-114">Zeichen können mit unterschiedlichen Namen für verschiedene Sprachen kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="18980-114">Characters can be compiled with different names for different languages.</span></span>

<span data-ttu-id="18980-115">Der Server verwendet die namens Einstellung des Zeichens in Teilen der Benutzeroberfläche des Microsoft-Agents, z. b. den Titel des sprach Befehls Fensters, wenn das Zeichen ein Eingabe-aktiv ist, und im Popup Menü der Microsoft-agenttaskleiste.</span><span class="sxs-lookup"><span data-stu-id="18980-115">The server uses the character's name setting in parts of the Microsoft Agent's interface, such as the Voice Commands Window title when the character is input-active and in the Microsoft Agent taskbar pop-up menu.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="18980-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="18980-116">See Also</span></span>

[<span data-ttu-id="18980-117">**Iagentcharacter:: GetName**</span><span class="sxs-lookup"><span data-stu-id="18980-117">**IAgentCharacter::GetName**</span></span>](iagentcharacter--getname.md)


 

 




