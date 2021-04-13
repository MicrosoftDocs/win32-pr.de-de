---
title: Iagentcharakteriex-Überwachung
description: Iagentcharakteriex-Überwachung
ms.assetid: 8d4cdb6c-04e1-498c-867f-fddbe6e2791a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12c479936a8d2dc43e2f2da5a680a51705af2885
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310388"
---
# <a name="iagentcharacterexlisten"></a><span data-ttu-id="97895-103">Iagentcharakteriex:: lauschen</span><span class="sxs-lookup"><span data-stu-id="97895-103">IAgentCharacterEx::Listen</span></span>

<span data-ttu-id="97895-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="97895-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Listen(
   long bListen  // listening mode flag
);
```

<span data-ttu-id="97895-105">Schaltet den Lesemodus (sprach Erkennungs Eingabe) ein oder aus.</span><span class="sxs-lookup"><span data-stu-id="97895-105">Turns Listening mode (speech recognition input) on or off.</span></span>

-   <span data-ttu-id="97895-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="97895-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="97895-107"><span id="bListen"></span><span id="blisten"></span><span id="BLISTEN"></span>*blisten*</span><span class="sxs-lookup"><span data-stu-id="97895-107"><span id="bListen"></span><span id="blisten"></span><span id="BLISTEN"></span>*bListen*</span></span>
</dt> <dd>

<span data-ttu-id="97895-108">Flag zum lauschen des Modus.</span><span class="sxs-lookup"><span data-stu-id="97895-108">Listening mode flag.</span></span> <span data-ttu-id="97895-109">Wenn dieser Parameter **true** ist, wird der Empfangsmodus aktiviert. der Wert **false** gibt an, dass der Überwachungsmodus deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="97895-109">If this parameter is **True**, the Listening mode is turned on; if **False**, Listening mode is turned off.</span></span>

</dd> </dl>

<span data-ttu-id="97895-110">Wenn diese Methode auf **true** festgelegt wird, wird der Empfangsmodus (aktiviert die Spracherkennung) für einen festgelegten Zeitraum aktiviert.</span><span class="sxs-lookup"><span data-stu-id="97895-110">Setting this method to **True** enables the Listening mode (turns on speech recognition) for a fixed period of time.</span></span> <span data-ttu-id="97895-111">Obwohl Sie den Wert für das Timeout nicht festlegen können, können Sie den Empfangsmodus deaktivieren, bevor das Timeout abläuft.</span><span class="sxs-lookup"><span data-stu-id="97895-111">While you cannot set the value of the time-out, you can turn off Listening mode before the time-out expires.</span></span> <span data-ttu-id="97895-112">Wenn der Überwachungsmodus bereits aktiviert ist, weil Sie (oder ein anderer Client) die-Methode erfolgreich auf **true** festgelegt haben, bevor das Timeout abläuft, wird die-Methode erfolgreich ausgeführt, und das Timeout wird zurückgesetzt. Wenn der Überwachungsmodus jedoch bereits auf ON eingestellt ist, da der Benutzer die Abhör Taste drückt, wird die Methode erfolgreich ausgeführt, aber das Timeout wird ignoriert, und der Empfangsmodus wird basierend auf der Interaktion des Benutzers mit dem lauschenden Schlüssel beendet.</span><span class="sxs-lookup"><span data-stu-id="97895-112">In addition, if the Listening mode is already on because you (or another client) successfully set the method to **True** before the time-out expires, the method succeeds and resets the time-out. However, if Listening mode is already on because the user is pressing the Listening key, the method succeeds, but the time-out is ignored and the Listening mode ends based on the user's interaction with the Listening key.</span></span>

<span data-ttu-id="97895-113">Diese Methode ist nur erfolgreich, wenn Sie vom Eingabe aktiven Client aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="97895-113">This method will succeed only when called by the input-active client.</span></span> <span data-ttu-id="97895-114">Daher schlägt die Methode fehl, wenn der Client nicht der aktive Client des obersten Zeichens ist.</span><span class="sxs-lookup"><span data-stu-id="97895-114">Therefore, the method will fail if your client is not the active client of the topmost character.</span></span> <span data-ttu-id="97895-115">Die-Methode schlägt auch fehl, wenn Sie versuchen, die-Methode auf **false** festzulegen, und der Benutzer die Abhör Taste drückt.</span><span class="sxs-lookup"><span data-stu-id="97895-115">The method will also fail if you attempt to set the method to **False** and the user is pressing the Listening key.</span></span> <span data-ttu-id="97895-116">Dies kann auch fehlschlagen, wenn keine kompatible Sprach-Engine verfügbar ist, die mit der Sprach-ID-Einstellung des Zeichens übereinstimmt, oder der Benutzer die Spracheingabe mithilfe der Eigenschaften Seite des Microsoft-Agents deaktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="97895-116">It can also fail if there is no compatible speech engine available that matches the character's language ID setting or the user has disabled speech input using the Microsoft Agent property sheet.</span></span> <span data-ttu-id="97895-117">Die Methode schlägt jedoch nicht fehl, wenn das Audiogerät ausgelastet ist.</span><span class="sxs-lookup"><span data-stu-id="97895-117">However, the method will not fail if the audio device is busy.</span></span>

<span data-ttu-id="97895-118">Wenn Sie diese Methode erfolgreich auf **true** festgelegt haben, löst der Server das [**iagentnotifysinkex:: listeningstate**](iagentnotifysinkex--listeningstate.md) -Ereignis aus.</span><span class="sxs-lookup"><span data-stu-id="97895-118">When you successfully set this method to **True**, the server triggers the [**IAgentNotifySinkEx::ListeningState**](iagentnotifysinkex--listeningstate.md) event.</span></span> <span data-ttu-id="97895-119">Der Server sendet auch **iagentnotifysinkex:: listeningstate** , wenn der Timeout für das Ansichtsmodus abgeschlossen ist oder wenn Sie [**iagentcharakteriex::**](https://www.bing.com/search?q=**IAgentCharacterEx::Listen**) Listening auf **false** festlegen.</span><span class="sxs-lookup"><span data-stu-id="97895-119">The server also sends **IAgentNotifySinkEx::ListeningState** when the Listening mode time-out completes or when you set [**IAgentCharacterEx::Listen**](https://www.bing.com/search?q=**IAgentCharacterEx::Listen**) to **False**.</span></span>

<span data-ttu-id="97895-120">Diese Methode ruft nicht automatisch [**iagentcharacter:: stopAll**](iagentcharacter--stopall.md) auf und wiederholt eine Animation zum lauschen des Zeichens, wenn der Benutzer die Abhör Taste drückt.</span><span class="sxs-lookup"><span data-stu-id="97895-120">This method does not automatically call [**IAgentCharacter::StopAll**](iagentcharacter--stopall.md) and play a Listening state animation of the character as occurs when the user presses the Listening key.</span></span> <span data-ttu-id="97895-121">Dies ermöglicht es Ihnen, das [**iagentnotifysinkex:: listeningstate**](iagentnotifysinkex--listeningstate.md) -Ereignis zu verwenden, um zu bestimmen, ob Sie die aktuelle Animation abbrechen und ihre eigene passende Animation wiedergeben möchten.</span><span class="sxs-lookup"><span data-stu-id="97895-121">This enables you to use the [**IAgentNotifySinkEx::ListeningState**](iagentnotifysinkex--listeningstate.md) event to determine whether you wish to stop the current animation and play your own appropriate animation.</span></span> <span data-ttu-id="97895-122">Nachdem jedoch eine Benutzer Äußerung erkannt wurde, ruft der Server automatisch **iagentcharacter:: stopAll** auf und spielt eine Animation für den hörzustand.</span><span class="sxs-lookup"><span data-stu-id="97895-122">However, once a user utterance is detected, the server automatically calls **IAgentCharacter::StopAll** and plays a Hearing state animation.</span></span>

## <a name="see-also"></a><span data-ttu-id="97895-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="97895-123">See Also</span></span>

<span data-ttu-id="97895-124">[**Iagentnotifysinkex:: listeningstate**](iagentnotifysinkex--listeningstate.md), [ **iagentspeechinputproperties:: GetEnabled**](iagentspeechinputproperties--getenabled.md)</span><span class="sxs-lookup"><span data-stu-id="97895-124">[**IAgentNotifySinkEx::ListeningState**](iagentnotifysinkex--listeningstate.md), [**IAgentSpeechInputProperties::GetEnabled**](iagentspeechinputproperties--getenabled.md)</span></span>


 

 




