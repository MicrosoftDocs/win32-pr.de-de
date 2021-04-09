---
title: Iagentcharakteriex getttmodeid
description: Iagentcharakteriex getttmodeid
ms.assetid: e7b3c576-dc3c-40de-8d09-8e7f4b79250b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62a77e78755345c0993ed5723080b0b3f4b8297a
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104038633"
---
# <a name="iagentcharacterexgetttsmodeid"></a><span data-ttu-id="d4138-103">Iagentcharakteriex:: getttmodeid</span><span class="sxs-lookup"><span data-stu-id="d4138-103">IAgentCharacterEx::GetTTSModeID</span></span>

<span data-ttu-id="d4138-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="d4138-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetTTSModeID(
   BSTR * pbszModeID  // address of TTS engine ID
);
```

<span data-ttu-id="d4138-105">Ruft die Modus-ID des TTS-Engine-Satzes für das Zeichen ab.</span><span class="sxs-lookup"><span data-stu-id="d4138-105">Retrieves the mode ID of the TTS engine set for the character.</span></span>

-   <span data-ttu-id="d4138-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="d4138-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="d4138-107"><span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszmodeid*</span><span class="sxs-lookup"><span data-stu-id="d4138-107"><span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*</span></span>
</dt> <dd>

<span data-ttu-id="d4138-108">Adresse eines BSTR, der die Modus-ID-Einstellung der TTS-Engine für das Zeichen empfängt.</span><span class="sxs-lookup"><span data-stu-id="d4138-108">Address of a BSTR that receives the mode ID setting of the TTS engine for the character.</span></span>

</dd> </dl>

<span data-ttu-id="d4138-109">Diese Einstellung gibt die ID des TTS (Text-zu-Sprache-Engine) für die gesprochene Ausgabe eines Zeichens zurück.</span><span class="sxs-lookup"><span data-stu-id="d4138-109">This setting returns the TTS (text-to-speech) engine mode ID for a character's spoken output.</span></span> <span data-ttu-id="d4138-110">Die Mode-ID für eine TTS-Engine ist eine Zeichen folgen Darstellung der GUID (mit geschweiften Klammern und Bindestrichen formatiert), die durch den Sprachanbieter definiert wird, der die Engine eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d4138-110">The mode ID for a TTS engine is a string representation of the GUID (formatted with braces and dashes) defined by the speech vendor uniquely identifying the engine.</span></span> <span data-ttu-id="d4138-111">Weitere Informationen finden Sie in der [Microsoft Speech SDK-Dokumentation](https://msdn.microsoft.com/library/ee705648.aspx).</span><span class="sxs-lookup"><span data-stu-id="d4138-111">For more information, see the [Microsoft Speech SDK documentation](https://msdn.microsoft.com/library/ee705648.aspx).</span></span> <span data-ttu-id="d4138-112">Wenn Sie diese Eigenschaft Abfragen, wird die zugeordnete Engine geladen, wenn Sie nicht bereits geladen ist.</span><span class="sxs-lookup"><span data-stu-id="d4138-112">Querying this property will load the associated engine if it is not already loaded.</span></span>

<span data-ttu-id="d4138-113">Wenn Sie keine ID des TTS-Engine-Modus für das Zeichen festlegen, versucht der Server, eine Engine zurückzugeben, die (über Microsoft Speech API-Schnittstellen) die kompilierte TTS-Einstellung des Zeichens und die aktuelle Spracheinstellung des Zeichens abgleicht.</span><span class="sxs-lookup"><span data-stu-id="d4138-113">If you do not set a TTS engine mode ID for the character, the server attempts to return an engine that matches (using Microsoft Speech API interfaces) the character's compiled TTS setting and the character's current language setting.</span></span> <span data-ttu-id="d4138-114">Wenn diese unterschiedlich sind, wird die Einstellung für den erstellten Modus durch die Spracheinstellung des Zeichens überschrieben.</span><span class="sxs-lookup"><span data-stu-id="d4138-114">If these are different, then the character's language setting overrides its authored mode setting.</span></span> <span data-ttu-id="d4138-115">Wenn Sie die Spracheinstellung des Zeichens nicht festgelegt haben, ist die Sprache des Zeichens die Standardsprachen-ID des Benutzers, und der Server versucht, die Entsprechung basierend auf dieser Sprach-ID zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d4138-115">If you have not set the character's language setting, the character's language is the user default language ID, and the server attempts the match based on that language ID.</span></span>

<span data-ttu-id="d4138-116">Diese Funktion schlägt fehl, wenn [**iagentaudioobjectproperties:: GetEnabled**](https://www.bing.com/search?q=**IAgentAudioObjectProperties::GetEnabled**) **false** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d4138-116">This function does not fail if the [**IAgentAudioObjectProperties::GetEnabled**](https://www.bing.com/search?q=**IAgentAudioObjectProperties::GetEnabled**) returns **False**.</span></span>

<span data-ttu-id="d4138-117">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="d4138-117">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="d4138-118">Die Sprach-Engine-Anforderungen von Microsoft Agent basieren auf der Microsoft Speech-API.</span><span class="sxs-lookup"><span data-stu-id="d4138-118">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="d4138-119">Module, die die SAPI-Anforderungen von Microsoft Agent unterstützen, können installiert und mit dem-Agent verwendet werden</span><span class="sxs-lookup"><span data-stu-id="d4138-119">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

## <a name="see-also"></a><span data-ttu-id="d4138-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d4138-120">See Also</span></span>

[<span data-ttu-id="d4138-121">**Iagentcharakteriex:: settungmodeid**</span><span class="sxs-lookup"><span data-stu-id="d4138-121">**IAgentCharacterEx::SetTTSModeID**</span></span>](iagentcharacterex--setttsmodeid.md)


 

 




