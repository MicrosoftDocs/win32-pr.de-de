---
title: Iagentcharakteriex settungmodeid
description: Iagentcharakteriex settungmodeid
ms.assetid: 66ed792a-1693-45dc-b9a8-eebe772c5af9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34392e65fcb8f3a46db6251f01f59ad76aba278d
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104389978"
---
# <a name="iagentcharacterexsetttsmodeid"></a><span data-ttu-id="b67de-103">Iagentcharakteriex:: settungmodeid</span><span class="sxs-lookup"><span data-stu-id="b67de-103">IAgentCharacterEx::SetTTSModeID</span></span>

<span data-ttu-id="b67de-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="b67de-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetTTSModeID(
   BSTR bszModeID  // TTS engine ID
);
```

<span data-ttu-id="b67de-105">Legt die Mode-ID des TTS-Engine-Satzes für das Zeichen fest.</span><span class="sxs-lookup"><span data-stu-id="b67de-105">Sets the mode ID of the TTS engine set for the character.</span></span>

-   <span data-ttu-id="b67de-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="b67de-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="b67de-107"><span id="bszModeID"></span><span id="bszmodeid"></span><span id="BSZMODEID"></span>*bszmodeid*</span><span class="sxs-lookup"><span data-stu-id="b67de-107"><span id="bszModeID"></span><span id="bszmodeid"></span><span id="BSZMODEID"></span>*bszModeID*</span></span>
</dt> <dd>

<span data-ttu-id="b67de-108">Die Modus-ID-Einstellung der TTS-Engine für das Zeichen.</span><span class="sxs-lookup"><span data-stu-id="b67de-108">The mode ID setting of the TTS engine for the character.</span></span>

> [!Note]  
> <span data-ttu-id="b67de-109">**Iagentcharakteriex: setttmodeid** kann fehlschlagen, wenn Speech.dll nicht installiert ist und die angegebene Engine nicht der kompilierten TTS-Moduseinstellung des Zeichens entspricht.</span><span class="sxs-lookup"><span data-stu-id="b67de-109">**IAgentCharacterEx:SetTTSModeID** can fail if Speech.dll is not installed and the engine you specify does not match the character's compiled TTS mode setting.</span></span>

 

</dd> </dl>

<span data-ttu-id="b67de-110">Diese Einstellung bestimmt den bevorzugten Engine-Modus für die gesprochene TTS-Ausgabe eines Zeichens.</span><span class="sxs-lookup"><span data-stu-id="b67de-110">This setting determines the preferred engine mode for a character's spoken TTS output.</span></span> <span data-ttu-id="b67de-111">Die Mode-ID für eine TTS-Engine (Text-to-Speech) ist die GUID, die vom Sprachanbieter definiert wird, der den Modus der Engine eindeutig identifiziert (mit geschweiften Klammern und Bindestrichen formatiert).</span><span class="sxs-lookup"><span data-stu-id="b67de-111">The mode ID for a TTS (text-to-speech) engine is the GUID defined by the speech vendor that uniquely identifies the mode of the engine (formatted with braces and dashes).</span></span> <span data-ttu-id="b67de-112">Weitere Informationen finden Sie in der [Microsoft Speech SDK-Dokumentation](https://msdn.microsoft.com/library/ee705648.aspx).</span><span class="sxs-lookup"><span data-stu-id="b67de-112">For more information, see the [Microsoft Speech SDK documentation](https://msdn.microsoft.com/library/ee705648.aspx).</span></span>

<span data-ttu-id="b67de-113">Wenn Sie eine TTS-Modus-ID festlegen, überschreibt Sie den Server Versuch, eine Sprach-Engine auf Grundlage der kompilierten TTS-Modus-ID des Zeichens, der aktuellen Systemsprachen-ID und der aktuellen Sprach-ID des Zeichens abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="b67de-113">If you set a TTS mode ID, it overrides the server attempt to match a speech engine based on the character's compiled TTS mode ID, the current system language ID, and the character's current language ID.</span></span> <span data-ttu-id="b67de-114">Wenn Sie jedoch versuchen, eine Modus-ID festzulegen, wenn der Benutzer die Sprachausgabe auf der Eigenschaften Seite des Microsoft-Agents deaktiviert hat oder wenn das zugehörige Modul nicht installiert ist, tritt bei diesem Vorgang ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="b67de-114">However, if you attempt to set a mode ID when the user has disabled speech output in the Microsoft Agent property sheet or when the associated engine is not installed, this call will fail.</span></span>

<span data-ttu-id="b67de-115">Wenn Sie keine ID des TTS-Engine-Modus für das Zeichen festlegen, legt der Server ein Modul fest, das mit der Spracheinstellung des Zeichens (über Microsoft Speech API-Schnittstellen) übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="b67de-115">If you do not set a TTS engine mode ID for the character, the server sets an engine that matches the character's language setting (using Microsoft Speech API interfaces).</span></span> <span data-ttu-id="b67de-116">Wenn Sie diese Eigenschaft festlegen, wird die zugeordnete Engine geladen, wenn Sie nicht bereits geladen ist.</span><span class="sxs-lookup"><span data-stu-id="b67de-116">Setting this property will load the associated engine if it is not already loaded.</span></span>

<span data-ttu-id="b67de-117">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="b67de-117">This property applies to only your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="b67de-118">Die Sprach-Engine-Anforderungen von Microsoft Agent basieren auf der Microsoft Speech-API.</span><span class="sxs-lookup"><span data-stu-id="b67de-118">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="b67de-119">Module, die die SAPI-Anforderungen von Microsoft Agent unterstützen, können installiert und mit dem-Agent verwendet werden</span><span class="sxs-lookup"><span data-stu-id="b67de-119">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

## <a name="see-also"></a><span data-ttu-id="b67de-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b67de-120">See Also</span></span>

[<span data-ttu-id="b67de-121">**Iagentcharakteriex: getttmodeid**</span><span class="sxs-lookup"><span data-stu-id="b67de-121">**IAgentCharacterEx:GetTTSModeID**</span></span>](iagentcharacterex--getttsmodeid.md)


 

 




