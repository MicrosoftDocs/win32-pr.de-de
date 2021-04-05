---
title: Iagentcharakteriex gezrmodeid
description: Iagentcharakteriex gezrmodeid
ms.assetid: 28049680-8245-49f3-9ecd-13c7605f10ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0bba237fb1bc1b5d769f7e8ecf983b58718c18e
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "103723813"
---
# <a name="iagentcharacterexgetsrmodeid"></a><span data-ttu-id="62cee-103">Iagentcharakteriex:: gezrmodeid</span><span class="sxs-lookup"><span data-stu-id="62cee-103">IAgentCharacterEx::GetSRModeID</span></span>

<span data-ttu-id="62cee-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="62cee-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSRModeID(
   BSTR * pbszModeID  // address of speech recognition engine ID
);
```

<span data-ttu-id="62cee-105">Ruft die Mode-ID des sprach Erkennungs Moduls für das Zeichen ab.</span><span class="sxs-lookup"><span data-stu-id="62cee-105">Retrieves the mode ID of the speech recognition engine set for the character.</span></span>

-   <span data-ttu-id="62cee-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="62cee-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="62cee-107"><span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszmodeid*</span><span class="sxs-lookup"><span data-stu-id="62cee-107"><span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*</span></span>
</dt> <dd>

<span data-ttu-id="62cee-108">Adresse eines BSTR, der die Modus-ID-Einstellung der sprach Erkennungs-Engine für das Zeichen empfängt.</span><span class="sxs-lookup"><span data-stu-id="62cee-108">Address of a BSTR that receives the mode ID setting of the speech recognition engine for the character.</span></span>

</dd> </dl>

<span data-ttu-id="62cee-109">Diese Einstellung gibt den Engine-Satz für die Spracheingabe eines Zeichens zurück.</span><span class="sxs-lookup"><span data-stu-id="62cee-109">This setting returns the engine set for a character's speech input.</span></span> <span data-ttu-id="62cee-110">Die Mode-ID für eine Spracherkennungs-Engine ist eine Zeichen folgen Darstellung der GUID (mit geschweiften Klammern und Bindestrichen formatiert), indem der Sprachanbieter die Engine eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="62cee-110">The mode ID for a speech recognition engine is a string representation of the GUID (formatted with braces and dashes) by the speech vendor uniquely identifying the engine.</span></span> <span data-ttu-id="62cee-111">Weitere Informationen finden Sie in der [Microsoft Speech SDK-Dokumentation](https://msdn.microsoft.com/library/ee705648.aspx).</span><span class="sxs-lookup"><span data-stu-id="62cee-111">For more information, see the [Microsoft Speech SDK documentation](https://msdn.microsoft.com/library/ee705648.aspx).</span></span>

<span data-ttu-id="62cee-112">Wenn Sie keine sprach Erkennungs-Engine-Modus-ID für das Zeichen festlegen, gibt der Server eine Engine zurück, die der Spracheinstellung des Zeichens (über die Microsoft Speech API-Schnittstellen) entspricht.</span><span class="sxs-lookup"><span data-stu-id="62cee-112">If you do not set a speech recognition engine mode ID for the character, the server returns an engine that matches the character's language setting (using Microsoft Speech API interfaces).</span></span> <span data-ttu-id="62cee-113">Wenn keine übereinstimmende sprach Erkennungs-Engine für das Zeichen verfügbar ist, gibt der Server eine NULL-Zeichenfolge (leere Zeichenfolge) zurück.</span><span class="sxs-lookup"><span data-stu-id="62cee-113">If there is no matching speech recognition engine available for the character, the server returns a null (empty) string.</span></span>

<span data-ttu-id="62cee-114">Wenn die Spracheingabe aktiviert ist (im Fenster Erweiterte Zeichen Optionen), wird durch das Abfragen oder Festlegen dieser Eigenschaft die zugeordnete Engine geladen (falls Sie nicht bereits geladen wurde), und die Sprachdienste werden gestartet.</span><span class="sxs-lookup"><span data-stu-id="62cee-114">When speech input is enabled (in the Advanced Character Options window), querying or setting this property will load the associated engine (if it is not already loaded), and start speech services.</span></span> <span data-ttu-id="62cee-115">Das heißt, der lauschende Schlüssel ist verfügbar, und der Abhör Tipp kann angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="62cee-115">That is, the Listening key is available, and the Listening Tip is displayable.</span></span> <span data-ttu-id="62cee-116">(Der Abhör Schlüssel und der lauschtip sind nur aktiviert, wenn Sie auch in erweiterten Zeichen Optionen aktiviert sind.) Wenn Sie jedoch die-Eigenschaft Abfragen, wenn die Sprache deaktiviert ist, startet der Server keine Sprachdienste und gibt eine NULL-Zeichenfolge (leere Zeichenfolge) zurück.</span><span class="sxs-lookup"><span data-stu-id="62cee-116">(The Listening key and Listening Tip are enabled only if they are also enabled in Advanced Character Options.) However, if you query the property when speech is disabled, the server does not start speech services and it returns a null string (empty string).</span></span>

<span data-ttu-id="62cee-117">Diese Funktion gibt nur die Einstellung für die Verwendung des Zeichens durch die Client Anwendung zurück. die Einstellung entspricht nicht anderen Clients des Zeichens oder anderen Zeichen ihrer Client Anwendung.</span><span class="sxs-lookup"><span data-stu-id="62cee-117">This function returns only the setting for your client application's use of the character; the setting does not reflect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="62cee-118">Diese Funktion schlägt fehl, wenn [**iagentspeechinputproperties:: GetEnabled**](iagentspeechinputproperties--getenabled.md) **false** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="62cee-118">This function does not fail if the [**IAgentSpeechInputProperties::GetEnabled**](iagentspeechinputproperties--getenabled.md) returns **False**.</span></span>

<span data-ttu-id="62cee-119">Die Sprach-Engine-Anforderungen von Microsoft Agent basieren auf der Microsoft Speech-API.</span><span class="sxs-lookup"><span data-stu-id="62cee-119">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="62cee-120">Module, die die SAPI-Anforderungen von Microsoft Agent unterstützen, können installiert und mit dem-Agent verwendet werden</span><span class="sxs-lookup"><span data-stu-id="62cee-120">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

## <a name="see-also"></a><span data-ttu-id="62cee-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="62cee-121">See Also</span></span>

[<span data-ttu-id="62cee-122">**Iagentcharakteriex::-rzrmodeid**</span><span class="sxs-lookup"><span data-stu-id="62cee-122">**IAgentCharacterEx::SetSRModeID**</span></span>](iagentcharacterex--setsrmodeid.md)


 

 




