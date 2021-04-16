---
title: Iagentcharakteriex--rzrmodeid
description: Iagentcharakteriex--rzrmodeid
ms.assetid: 8f9072ec-1f64-4f5c-972d-cd6799ce028c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390d7e0126fe5ef62273cf6d7d23ada25c26bbdb
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104472260"
---
# <a name="iagentcharacterexsetsrmodeid"></a><span data-ttu-id="a692b-103">Iagentcharakteriex::-rzrmodeid</span><span class="sxs-lookup"><span data-stu-id="a692b-103">IAgentCharacterEx::SetSRModeID</span></span>

<span data-ttu-id="a692b-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="a692b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetSRModeID(
   BSTR bszModeID  // speech recognition engine ID
);
```

<span data-ttu-id="a692b-105">Legt die Mode-ID des sprach Erkennungs Moduls für das Zeichen fest.</span><span class="sxs-lookup"><span data-stu-id="a692b-105">Sets the mode ID of the speech recognition engine set for the character.</span></span>

-   <span data-ttu-id="a692b-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="a692b-106">Returns S\_OK to indicate the operation was successful.</span></span>

<span data-ttu-id="a692b-107">bszmodeid</span><span class="sxs-lookup"><span data-stu-id="a692b-107">bszModeID</span></span>

<span data-ttu-id="a692b-108">Die Modus-ID-Einstellung der sprach Erkennungs-Engine für das Zeichen.</span><span class="sxs-lookup"><span data-stu-id="a692b-108">The mode ID setting of the speech recognition engine for the character.</span></span>

<span data-ttu-id="a692b-109">Mit dieser Einstellung wird die-Engine für die Spracheingabe eines Zeichens festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a692b-109">This setting sets the engine for a character's speech input.</span></span> <span data-ttu-id="a692b-110">Die Mode-ID für eine Spracherkennungs-Engine ist die GUID, die vom Sprachanbieter definiert wird, der den Modus der Engine eindeutig identifiziert (mit geschweiften Klammern und Bindestrichen formatiert).</span><span class="sxs-lookup"><span data-stu-id="a692b-110">The mode ID for a speech recognition engine is the GUID defined by the speech vendor that uniquely identifies the engine's mode (formatted with braces and dashes).</span></span> <span data-ttu-id="a692b-111">Weitere Informationen finden Sie in der [Microsoft Speech SDK-Dokumentation](https://msdn.microsoft.com/library/ee705648.aspx).</span><span class="sxs-lookup"><span data-stu-id="a692b-111">For more information, see the [Microsoft Speech SDK documentation](https://msdn.microsoft.com/library/ee705648.aspx).</span></span>

<span data-ttu-id="a692b-112">Wenn Sie eine Mode-ID angeben, die nicht mit der Spracheinstellung des Zeichens identisch ist, tritt bei diesem Vorgang ein Fehler auf, wenn der Benutzer die Spracherkennung deaktiviert hat (auf dem Eigenschaften Blatt des Microsoft-Agents) oder die-Engine nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="a692b-112">If you specify a mode ID that does not match the character's language setting, if the user has disabled speech recognition (in the Microsoft Agent property sheet), or the engine is not installed, this call will fail.</span></span> <span data-ttu-id="a692b-113">Wenn Sie keine sprach Erkennungs-Engine-Modus-ID für das Zeichen festlegen, legt der Server einen fest, der mit der Spracheinstellung des Zeichens (über die Microsoft Speech API-Schnittstellen) übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="a692b-113">If you do not set a speech recognition engine mode ID for the character, the server sets one that matches the character's language setting (using Microsoft Speech API interfaces).</span></span>

<span data-ttu-id="a692b-114">Wenn die Spracheingabe auf der Eigenschaften Seite des-Agents aktiviert ist (erweiterte Zeichen Optionen), wird durch das Festlegen dieser Eigenschaft die zugeordnete Engine geladen (sofern Sie nicht bereits geladen wurde) und Sprachdienste starten.</span><span class="sxs-lookup"><span data-stu-id="a692b-114">When speech input is enabled in the Agent property sheet (Advanced Character Options), setting this property will load the associated engine (if it is not already loaded), and start speech services.</span></span> <span data-ttu-id="a692b-115">Das heißt, der lauschende Schlüssel ist verfügbar, und der Abhör Tipp kann angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a692b-115">That is, the Listening key is available, and the Listening Tip is displayable.</span></span> <span data-ttu-id="a692b-116">(Der Abhör Schlüssel und der lauschtip sind nur aktiviert, wenn Sie auch in erweiterten Zeichen Optionen aktiviert sind.) Wenn Sie jedoch die-Eigenschaft Abfragen, wenn die Sprache deaktiviert ist, startet der Server die Sprachdienste nicht.</span><span class="sxs-lookup"><span data-stu-id="a692b-116">(The Listening key and Listening tip are enabled only if they are also enabled in Advanced Character Options.) However, if you query the property when speech is disabled, the server does not start speech services.</span></span>

<span data-ttu-id="a692b-117">Diese Eigenschaft gilt nur für den Client des Zeichens. die Einstellung entspricht nicht der Einstellung für andere Clients des Zeichens oder anderen Zeichen des Clients.</span><span class="sxs-lookup"><span data-stu-id="a692b-117">This property applies to only the client of the character; the setting does not reflect the setting for other clients of the character or other characters of the client.</span></span>

<span data-ttu-id="a692b-118">Die Sprach-Engine-Anforderungen von Microsoft Agent basieren auf der Microsoft Speech-API.</span><span class="sxs-lookup"><span data-stu-id="a692b-118">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="a692b-119">Module, die die SAPI-Anforderungen von Microsoft Agent unterstützen, können installiert und mit dem-Agent verwendet werden</span><span class="sxs-lookup"><span data-stu-id="a692b-119">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

## <a name="see-also"></a><span data-ttu-id="a692b-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a692b-120">See Also</span></span>

[<span data-ttu-id="a692b-121">**Iagentcharakteriex:: gezrmodeid**</span><span class="sxs-lookup"><span data-stu-id="a692b-121">**IAgentCharacterEx::GetSRModeID**</span></span>](iagentcharacterex--getsrmodeid.md)


 

 




