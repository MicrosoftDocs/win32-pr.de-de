---
title: Iagentcharakteriex gezrstatus
description: Iagentcharakteriex gezrstatus
ms.assetid: ccb34108-8078-421a-a883-731b51fae179
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4396e325f5afba161046f2a001cebb29033d709b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036776"
---
# <a name="iagentcharacterexgetsrstatus"></a><span data-ttu-id="d40d3-103">Iagentcharakteriex:: gezrstatus</span><span class="sxs-lookup"><span data-stu-id="d40d3-103">IAgentCharacterEx::GetSRStatus</span></span>

<span data-ttu-id="d40d3-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="d40d3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSRStatus(
   long * plStatus  // address of the speech input status
);
```

<span data-ttu-id="d40d3-105">Ruft den Status der Bedingung ab, die zur Unterstützung der Spracheingabe erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d40d3-105">Retrieves the status of the condition necessary to support speech input.</span></span>

-   <span data-ttu-id="d40d3-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="d40d3-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="d40d3-107"><span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plstatus*</span><span class="sxs-lookup"><span data-stu-id="d40d3-107"><span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*</span></span>
</dt> <dd>

<span data-ttu-id="d40d3-108">Adresse einer Variablen, die einen der folgenden Werte für die Zustands Einstellung empfängt:</span><span class="sxs-lookup"><span data-stu-id="d40d3-108">Address of a variable that receives one of the following values for the state setting:</span></span>



| <span data-ttu-id="d40d3-109">Wert</span><span class="sxs-lookup"><span data-stu-id="d40d3-109">Value</span></span>                                                                               | <span data-ttu-id="d40d3-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d40d3-110">Description</span></span>                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d40d3-111">Status von **konstant gestattenunsigned Long** - **lauschen \_ \_ = 0;**</span><span class="sxs-lookup"><span data-stu-id="d40d3-111">**const unsigned long** **LISTEN\_STATUS\_CANLISTEN = 0;**</span></span><br/>               | <span data-ttu-id="d40d3-112">Bedingungen unterstützen Spracheingaben.</span><span class="sxs-lookup"><span data-stu-id="d40d3-112">Conditions support speech input.</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="d40d3-113">"Konstante **nicht signiertes langes** **lauschen" \_ -Status " \_ noaudio= 1;** "</span><span class="sxs-lookup"><span data-stu-id="d40d3-113">**const unsigned long** **LISTEN\_STATUS\_NOAUDIO = 1;**</span></span><br/>                 | <span data-ttu-id="d40d3-114">Auf diesem System ist kein Audioeingabegerät verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d40d3-114">There is no audio input device available on this system.</span></span> <span data-ttu-id="d40d3-115">(Beachten Sie, dass hierdurch nicht erkannt wird, ob ein Mikrofon installiert ist. es kann nur erkennen, ob der Benutzer über eine ordnungsgemäß installierte Audiokarte mit einem funktionierenden Treiber verfügt.)</span><span class="sxs-lookup"><span data-stu-id="d40d3-115">(Note that this does not detect whether a microphone is installed; it can only detect whether the user has a properly installed input-enabled sound card with a working driver.)</span></span> |
| <span data-ttu-id="d40d3-116">konstanter **nicht signierter Long** **- \_ \_ lausch Status, Status:**</span><span class="sxs-lookup"><span data-stu-id="d40d3-116">**const unsigned long** **LISTEN\_STATUS\_NOTTOPMOST = 2;**</span></span><br/>              | <span data-ttu-id="d40d3-117">Ein anderer Client ist der aktive Client dieses Zeichens, oder das aktuelle Zeichen ist nicht oberstes Zeichen.</span><span class="sxs-lookup"><span data-stu-id="d40d3-117">Another client is the active client of this character, or the current character is not topmost.</span></span>                                                                                                                                           |
| <span data-ttu-id="d40d3-118">konstanter **nicht signierter langer** lausch **\_ Status \_ kanopenaudio= 3;**</span><span class="sxs-lookup"><span data-stu-id="d40d3-118">**const unsigned long** **LISTEN\_STATUS\_CANTOPENAUDIO = 3;**</span></span><br/>           | <span data-ttu-id="d40d3-119">Die Audioeingabe oder der Ausgabekanal ist derzeit ausgelastet, eine andere Anwendung verwendet Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="d40d3-119">The audio input or output channel is currently busy, some other application is using audio.</span></span>                                                                                                                                               |
| <span data-ttu-id="d40d3-120">der Konstante **Ganzzahl ohne Vorzeichen long** -lausch **\_ Status \_ konnte dntinitializespeech = 4;**</span><span class="sxs-lookup"><span data-stu-id="d40d3-120">**const unsigned long** **LISTEN\_STATUS\_COULDNTINITIALIZESPEECH = 4;**</span></span><br/> | <span data-ttu-id="d40d3-121">Beim Initialisieren des sprach Erkennungs Subsystems ist ein nicht spezifizierter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d40d3-121">An unspecified error occurred in the process of initializing the speech recognition subsystem.</span></span> <span data-ttu-id="d40d3-122">Dies schließt die Möglichkeit ein, dass keine Sprach-Engine verfügbar ist, die der Spracheinstellung des Zeichens entspricht.</span><span class="sxs-lookup"><span data-stu-id="d40d3-122">This includes the possibility that there is no speech engine available matching the character's language setting.</span></span>                          |
| <span data-ttu-id="d40d3-123">**Ganzzahl ohne Vorzeichen long** -lausch **\_ Status \_ -Status**</span><span class="sxs-lookup"><span data-stu-id="d40d3-123">**const unsigned long** **LISTEN\_STATUS\_SPEECHDISABLED = 5;**</span></span><br/>          | <span data-ttu-id="d40d3-124">Der Benutzer hat die Spracheingabe im Fenster "erweiterte Zeichen Optionen" deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d40d3-124">The user has disabled speech input in the Advanced Character Options window.</span></span>                                                                                                                                                              |
| <span data-ttu-id="d40d3-125">Status Fehler für "lange Überwachung ( **lange) nicht signiert** **\_ \_ = 6;** "</span><span class="sxs-lookup"><span data-stu-id="d40d3-125">**const unsigned long** **LISTEN\_STATUS\_ERROR = 6;**</span></span><br/>                   | <span data-ttu-id="d40d3-126">Beim Überprüfen des Audiostatus ist ein Fehler aufgetreten, aber die Ursache des Fehlers wurde vom System nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d40d3-126">An error occurred in checking the audio status, but the cause of the error was not returned by the system.</span></span>                                                                                                                                |



 

</dd> </dl>

<span data-ttu-id="d40d3-127">Mit dieser Funktion können Sie Abfragen, ob aktuelle Bedingungen sprach Erkennungs Eingaben unterstützen, einschließlich des Status des Audiogeräts.</span><span class="sxs-lookup"><span data-stu-id="d40d3-127">This function enables you to query whether current conditions support speech recognition input, including the status of the audio device.</span></span> <span data-ttu-id="d40d3-128">Wenn Ihre Anwendung die [**iagentcharakteriex::**](iagentcharacterex--listen.md) Listener-Methode verwendet, können Sie diese Funktion verwenden, um sicherzustellen, dass der-Vorgang erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d40d3-128">If your application uses the [**IAgentCharacterEx::Listen**](iagentcharacterex--listen.md) method, you can use this function to better ensure that the call will succeed.</span></span> <span data-ttu-id="d40d3-129">Wenn Sie diese Methode aufrufen, wird auch die Sprach-Engine geladen, wenn Sie nicht bereits geladen ist.</span><span class="sxs-lookup"><span data-stu-id="d40d3-129">Calling this method also loads the speech engine if it is not already loaded.</span></span> <span data-ttu-id="d40d3-130">Der Überwachungsmodus wird jedoch nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d40d3-130">However, it does not turn on Listening mode.</span></span>

<span data-ttu-id="d40d3-131">Wenn die Spracheingabe auf der Eigenschaften Seite des-Agents aktiviert ist (erweiterte Zeichen Optionen), wird durch Abfragen des Status die zugeordnete Engine geladen (sofern Sie nicht bereits geladen wurde) und Sprachdienste starten.</span><span class="sxs-lookup"><span data-stu-id="d40d3-131">When speech input is enabled in the Agent property sheet (Advanced Character Options), querying the status will load the associated engine (if it is not already loaded), and start speech services.</span></span> <span data-ttu-id="d40d3-132">Das heißt, der lauschende Schlüssel ist verfügbar, und der Abhör Tipp kann angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d40d3-132">That is, the Listening key is available, and the Listening Tip is displayable.</span></span> <span data-ttu-id="d40d3-133">(Der Abhör Schlüssel und der lauschtip sind nur aktiviert, wenn Sie auch in erweiterten Zeichen Optionen aktiviert sind.) Wenn Sie jedoch die-Eigenschaft Abfragen, wenn die Sprache deaktiviert ist, startet der Server die Sprachdienste nicht.</span><span class="sxs-lookup"><span data-stu-id="d40d3-133">(The Listening key and Listening Tip are enabled only if they are also enabled in Advanced Character Options.) However, if you query the property when speech is disabled, the server does not start speech services.</span></span>

<span data-ttu-id="d40d3-134">Diese Funktion gibt nur die Einstellung für die Verwendung des Zeichens durch die Client Anwendung zurück. die Einstellung entspricht nicht anderen Clients des Zeichens oder anderen Zeichen ihrer Client Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d40d3-134">This function returns only the setting for your client application's use of the character; the setting does not reflect other clients of the character or other characters of your client application.</span></span>

 

 





