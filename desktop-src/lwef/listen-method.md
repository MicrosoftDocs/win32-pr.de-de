---
title: Abhör Methode
description: Abhör Methode
ms.assetid: ceb3b62f-2a33-4a13-b608-4cfa800be38a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6813fb155074c4cc47a51ec7241eddd332edbcc3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038861"
---
# <a name="listen-method"></a><span data-ttu-id="bc7b2-103">Abhör Methode</span><span class="sxs-lookup"><span data-stu-id="bc7b2-103">Listen Method</span></span>

<span data-ttu-id="bc7b2-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="bc7b2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="bc7b2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bc7b2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="bc7b2-106">Schaltet den Empfangsmodus (Spracherkennung) für einen zeitgesteuerten Zeitraum ein.</span><span class="sxs-lookup"><span data-stu-id="bc7b2-106">Turns on Listening mode (speech recognition) for a timed period.</span></span>

</dd> <dt>

<span data-ttu-id="bc7b2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="bc7b2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="bc7b2-108">\*Agent. ***Zeichen \* \* \* \* ("*** Merkmal-ID \* \* *").* \*  *Status* lauschen</span><span class="sxs-lookup"><span data-stu-id="bc7b2-108">*agent.\*\*\*Characters\*\*\*\*("*\*\* CharacterID\***").Listen** *State*</span></span>



| <span data-ttu-id="bc7b2-109">Teil</span><span class="sxs-lookup"><span data-stu-id="bc7b2-109">Part</span></span>    | <span data-ttu-id="bc7b2-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bc7b2-110">Description</span></span>                                                                                                                                                                      |
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc7b2-111">*Zustand*</span><span class="sxs-lookup"><span data-stu-id="bc7b2-111">*State*</span></span> | <span data-ttu-id="bc7b2-112">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bc7b2-112">Required.</span></span> <span data-ttu-id="bc7b2-113">Ein boolescher Wert, der bestimmt, ob der Empfangsmodus aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="bc7b2-113">A Boolean value that determines whether to turn Listening mode on or off.</span></span> <span data-ttu-id="bc7b2-114">**True** Schaltet den Modus für die Überwachung ein.</span><span class="sxs-lookup"><span data-stu-id="bc7b2-114">**True** Turns Listening mode on.</span></span> <br/> <span data-ttu-id="bc7b2-115">**False** Schaltet den Lesemodus aus.</span><span class="sxs-lookup"><span data-stu-id="bc7b2-115">**False** Turns Listening mode off.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bc7b2-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc7b2-116">Remarks</span></span>

<span data-ttu-id="bc7b2-117">Wenn diese Methode auf **true** festgelegt wird, wird der Empfangsmodus (aktiviert die Spracherkennung) für einen festgelegten Zeitraum (10 Sekunden) aktiviert.</span><span class="sxs-lookup"><span data-stu-id="bc7b2-117">Setting this method to **True** enables Listening mode (turns on speech recognition) for a fixed period of time (10 seconds).</span></span> <span data-ttu-id="bc7b2-118">Obwohl Sie den Wert für das Timeout nicht festlegen können, können Sie den Empfangsmodus deaktivieren, bevor das Timeout abläuft.</span><span class="sxs-lookup"><span data-stu-id="bc7b2-118">While you cannot set the value of the time-out, you can turn off Listening mode before the time-out expires.</span></span> <span data-ttu-id="bc7b2-119">Wenn Sie (oder ein anderer Client) den Empfangsmodus für erfolgreich festgelegt haben und Sie versuchen, diese Eigenschaft vor Ablauf des Timeouts auf **true** festzulegen, wird die Methode erfolgreich ausgeführt, und das Timeout wird zurückgesetzt. Wenn der Überwachungsmodus jedoch auf ON eingestellt ist, da der Benutzer die Abhör Taste drückt, wird die Methode erfolgreich ausgeführt, aber das Timeout wird ignoriert, und der Empfangsmodus wird basierend auf der Interaktion des Benutzers mit dem lauschenden Schlüssel beendet.</span><span class="sxs-lookup"><span data-stu-id="bc7b2-119">If you (or another client) successfully set Listening mode on and you attempt to set this property to **True** before the time-out expires, the method succeeds and resets the time-out. However, if the Listening mode is on because the user is pressing the Listening key, the method succeeds, but the time-out is ignored and the Listening mode ends based on the user's interaction with the Listening key.</span></span>

<span data-ttu-id="bc7b2-120">Diese Methode ist nur erfolgreich, wenn Sie vom Eingabe aktiven Client aufgerufen wird und die Sprachdienste gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="bc7b2-120">This method succeeds only when called by the input-active client and if speech services have been started.</span></span> <span data-ttu-id="bc7b2-121">Um sicherzustellen, dass Sprachdienste gestartet wurden, Fragen Sie die [**srmodeid**](srmodeid-property.md) ab, oder legen Sie Sie fest, oder legen Sie die [**sprach**](voice-property.md) Einstellung für einen [**Befehl**](/windows/desktop/lwef/the-command-object) fest, bevor Sie **lauschen**</span><span class="sxs-lookup"><span data-stu-id="bc7b2-121">To ensure that speech services have been started, query or set the [**SRModeID**](srmodeid-property.md) or set the [**Voice**](voice-property.md) setting for a [**Command**](/windows/desktop/lwef/the-command-object) before you call **Listen** otherwise the method will fail.</span></span> <span data-ttu-id="bc7b2-122">Um den Erfolg dieser Methode zu erkennen, nennen Sie Sie als Funktion, und Sie gibt einen booleschen Wert zurück, der angibt, ob die Methode erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="bc7b2-122">To detect the success of this method, call it as a function and it will return a Boolean value indicating whether the method succeeded.</span></span>


```
   If Genie.Listen(True) Then
      'The method succeeded

   Else
      ' The method failed

   End If
```



<span data-ttu-id="bc7b2-123">Die-Methode schlägt auch fehl, wenn der Benutzer die Abhör Taste drückt, und Sie versuchen, das **lauschen** auf **false** festzulegen.</span><span class="sxs-lookup"><span data-stu-id="bc7b2-123">The method also fails if the user is pressing the Listening key and you attempt to set **Listen** to **False**.</span></span> <span data-ttu-id="bc7b2-124">Wenn der Benutzer jedoch keinen Timeout für den abhörenden Schlüssel hat und kein Timeout aufgetreten ist, wird er erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bc7b2-124">However, if the user has released the Listening key and Listening mode has not timed out, it will succeed.</span></span>

<span data-ttu-id="bc7b2-125">**Lauschen** schlägt auch fehl, wenn keine kompatible Sprach-Engine verfügbar ist, die mit der [**LanguageID**](languageid-property.md) -Einstellung des Zeichens übereinstimmt, der Benutzer die Spracheingabe mithilfe der Eigenschaften Seite "Microsoft-Agent" deaktiviert hat oder das Audiogerät ausgelastet ist.</span><span class="sxs-lookup"><span data-stu-id="bc7b2-125">**Listen** also fails if there is no compatible speech engine available that matches the character's [**LanguageID**](languageid-property.md) setting, the user has disabled speech input using the Microsoft Agent property sheet, or the audio device is busy.</span></span>

<span data-ttu-id="bc7b2-126">Wenn Sie diese Methode erfolgreich auf **true** festgelegt haben, löst der Server das [**ListenStart**](listenstart-event.md) -Ereignis aus.</span><span class="sxs-lookup"><span data-stu-id="bc7b2-126">When you successfully set this method to **True**, the server triggers the [**ListenStart**](listenstart-event.md) event.</span></span> <span data-ttu-id="bc7b2-127">Der Server sendet [**listencomplete**](listencomplete-event.md) , wenn das Timeout für den Lesemodus abgeschlossen ist, oder wenn Sie **lauschen** auf **false** festlegen.</span><span class="sxs-lookup"><span data-stu-id="bc7b2-127">The server sends [**ListenComplete**](listencomplete-event.md) when the Listening mode time-out completes or when you set **Listen** to **False**.</span></span>

<span data-ttu-id="bc7b2-128">Diese Methode ruft nicht automatisch " [**Beenden**](stop-method.md) " auf und wiedergeben eine Animation zum lauschen des Zustands, wenn der Server beim Drücken der Abhör Taste gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="bc7b2-128">This method does not automatically call [**Stop**](stop-method.md) and play a Listening state animation as the server does when the Listening key is pressed.</span></span> <span data-ttu-id="bc7b2-129">Auf diese Weise können Sie bestimmen, ob die aktuelle Animation mithilfe der [**ListenStart**](listenstart-event.md) -Animation unterbrechen werden soll, indem Sie " **stoppen** " aufrufen und ihre eigene passende Animation wiedergeben</span><span class="sxs-lookup"><span data-stu-id="bc7b2-129">This enables you to determine whether to interrupt the current animation using the [**ListenStart**](listenstart-event.md) animation by calling **Stop** and playing your own appropriate animation.</span></span> <span data-ttu-id="bc7b2-130">Der Server ruft jedoch " **Beenden** " auf und spielt eine Animation für den hörzustand, wenn eine Benutzer Äußerung erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="bc7b2-130">However, the server does call **Stop** and plays a Hearing state animation when a user utterance is detected.</span></span>

## <a name="see-also"></a><span data-ttu-id="bc7b2-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bc7b2-131">See Also</span></span>

<span data-ttu-id="bc7b2-132">[**LanguageID-Eigenschaft**](languageid-property.md), [**listencomplete-Ereignis**](listencomplete-event.md), [**ListenStart-Ereignis**](listenstart-event.md)</span><span class="sxs-lookup"><span data-stu-id="bc7b2-132">[**LanguageID property**](languageid-property.md), [**ListenComplete event**](listencomplete-event.md), [**ListenStart event**](listenstart-event.md)</span></span>


 

