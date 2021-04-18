---
title: Activate-Methode
description: Activate-Methode
ms.assetid: 8111139d-1453-416e-8f08-38c06669ff4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21df1965abaeed35e9e440a0f559f5e12d68d6fe
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106340489"
---
# <a name="activate-method"></a><span data-ttu-id="d5d7e-103">Activate-Methode</span><span class="sxs-lookup"><span data-stu-id="d5d7e-103">Activate Method</span></span>

<span data-ttu-id="d5d7e-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="d5d7e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="d5d7e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>[**Beschreibung**](../wmformat/description.md)</span><span class="sxs-lookup"><span data-stu-id="d5d7e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>[**Description**](../wmformat/description.md)</span></span>
</dt> <dd>

<span data-ttu-id="d5d7e-106">Legt den aktiven Client oder das Zeichen fest.</span><span class="sxs-lookup"><span data-stu-id="d5d7e-106">Sets the active client or character.</span></span>

</dd> <dt>

<span data-ttu-id="d5d7e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="d5d7e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="d5d7e-108">\*Agent ***. Zeichen ("*** Merkmal-ID \* \* *").* \*  \[ *Zustand* aktivieren\]</span><span class="sxs-lookup"><span data-stu-id="d5d7e-108">*agent ***.Characters ("*** CharacterID\*\*\*").Activate*\* \[*State*\]</span></span>



| <span data-ttu-id="d5d7e-109">Teil</span><span class="sxs-lookup"><span data-stu-id="d5d7e-109">Part</span></span>    | <span data-ttu-id="d5d7e-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d5d7e-110">Description</span></span>                                                                                                                                                                           |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5d7e-111">*Zustand*</span><span class="sxs-lookup"><span data-stu-id="d5d7e-111">*State*</span></span> | <span data-ttu-id="d5d7e-112">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="d5d7e-112">Optional.</span></span> <span data-ttu-id="d5d7e-113">Sie können die folgenden Werte für diesen Parameter angeben: 0 nicht der aktive Client.</span><span class="sxs-lookup"><span data-stu-id="d5d7e-113">You can specify the following values for this parameter: 0 Not the active client.</span></span><br/> <span data-ttu-id="d5d7e-114">1 der aktive Client.</span><span class="sxs-lookup"><span data-stu-id="d5d7e-114">1 The active client.</span></span> <br/> <span data-ttu-id="d5d7e-115">2 (Standard) das oberste Zeichen.</span><span class="sxs-lookup"><span data-stu-id="d5d7e-115">2 (Default) The topmost character.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d5d7e-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5d7e-116">Remarks</span></span>

<span data-ttu-id="d5d7e-117">Wenn mehrere Zeichen sichtbar sind, empfängt nur eines der Zeichen Spracheingaben gleichzeitig.</span><span class="sxs-lookup"><span data-stu-id="d5d7e-117">When multiple characters are visible, only one of the characters receives speech input at a time.</span></span> <span data-ttu-id="d5d7e-118">Wenn mehrere Client Anwendungen dasselbe Zeichen gemeinsam verwenden, empfängt auch nur einer der Clients Maus Eingaben (z. b. Click-oder Drag-Ereignisse der Microsoft-agentsteuerung).</span><span class="sxs-lookup"><span data-stu-id="d5d7e-118">Similarly, when multiple client applications share the same character, only one of the clients receives mouse input (for example, Microsoft Agent control click or drag events).</span></span> <span data-ttu-id="d5d7e-119">Der Zeichensatz für den Empfang von Maus-und Spracheingaben ist das oberste Zeichen, und der Client, der die Eingabe empfängt, ist der aktive Client dieses Zeichens.</span><span class="sxs-lookup"><span data-stu-id="d5d7e-119">The character set to receive mouse and speech input is the topmost character and the client that receives the input is the active client of that character.</span></span> <span data-ttu-id="d5d7e-120">(Das Fenster des obersten Zeichens wird auch am oberen Rand der z-Reihenfolge des Zeichen Fensters angezeigt.) In der Regel bestimmt der Benutzer das oberste Zeichen, indem das Zeichen explizit ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="d5d7e-120">(The topmost character's window also appears at the top of the character window's z-order.) Typically, the user determines the topmost character by explicitly selecting the character.</span></span> <span data-ttu-id="d5d7e-121">Die oberste Aktivierung ändert sich jedoch auch, wenn ein Zeichen angezeigt oder ausgeblendet wird (das Zeichen wird zu oder ist nicht mehr die oberste Stelle).</span><span class="sxs-lookup"><span data-stu-id="d5d7e-121">However, topmost activation also changes when a character is shown or hidden (the character becomes or is no longer topmost, respectively.)</span></span>

<span data-ttu-id="d5d7e-122">Sie können diese Methode auch verwenden, um explizit zu verwalten, wann der Client Eingaben erhält, die an das Zeichen weitergeleitet werden, z. b. wenn die Anwendung selbst aktiv wird</span><span class="sxs-lookup"><span data-stu-id="d5d7e-122">You can also use this method to explicitly manage when your client receives input directed to the character such as when your application itself becomes active.</span></span> <span data-ttu-id="d5d7e-123">Wenn Sie z. b. " *State* " auf "2" festlegen, wird das Zeichen am meisten, und der Client empfängt alle Maus-und Spracheingabe Ereignisse, die von der Benutzerinteraktion mit dem</span><span class="sxs-lookup"><span data-stu-id="d5d7e-123">For example, setting *State* to 2 makes the character topmost and your client receives all mouse and speech input events generated from user interaction with the character.</span></span> <span data-ttu-id="d5d7e-124">Daher wird der Client auch zum Eingabe aktiven Client des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="d5d7e-124">Therefore, it also makes your client the input-active client of the character.</span></span>

<span data-ttu-id="d5d7e-125">Sie können sich jedoch auch als aktiver Client für ein Zeichen festlegen, ohne das Zeichen am höchsten zu machen, indem Sie *State* auf 1 festlegen.</span><span class="sxs-lookup"><span data-stu-id="d5d7e-125">However, you can also set yourself to be the active client for a character without making the character topmost, by setting *State* to 1.</span></span> <span data-ttu-id="d5d7e-126">Dadurch kann der Client Eingaben empfangen, die an dieses Zeichen weitergeleitet werden, wenn das Zeichen über den höchsten Wert verfügt.</span><span class="sxs-lookup"><span data-stu-id="d5d7e-126">This enables your client to receive input directed to that character when the character becomes topmost.</span></span> <span data-ttu-id="d5d7e-127">Auf ähnliche Weise können Sie festlegen, dass der Client nicht der aktive Client (nicht für den Empfang von Eingaben) ist, wenn das Zeichen am meisten ist, indem Sie den *Status* auf 0 festlegen.</span><span class="sxs-lookup"><span data-stu-id="d5d7e-127">Similarly, you can set your client to not be the active client (not to receive input) when the character becomes topmost, by setting *State* to 0.</span></span>

<span data-ttu-id="d5d7e-128">Vermeiden Sie das Aufrufen dieser Methode direkt nach einer [**Show**](/previous-versions/visualstudio/foxpro/d79z7xxa(v=vs.71)) -Methode.</span><span class="sxs-lookup"><span data-stu-id="d5d7e-128">Avoid calling this method directly after a [**Show**](/previous-versions/visualstudio/foxpro/d79z7xxa(v=vs.71)) method.</span></span> <span data-ttu-id="d5d7e-129">**Anzeigen** legt automatisch den Eingabe aktiven Client fest.</span><span class="sxs-lookup"><span data-stu-id="d5d7e-129">**Show** automatically sets the input-active client.</span></span> <span data-ttu-id="d5d7e-130">Wenn das Zeichen ausgeblendet ist, kann der [**Aktivierungs**](/previous-versions/visualstudio/foxpro/01ayxx68(v=vs.71)) Befehl fehlschlagen, wenn er verarbeitet wird, bevor die **Show** -Methode abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="d5d7e-130">When the character is hidden, the [**Activate**](/previous-versions/visualstudio/foxpro/01ayxx68(v=vs.71)) call may fail if it gets processed before the **Show** method completes.</span></span>

<span data-ttu-id="d5d7e-131">Wenn Sie diese Methode für eine Funktion aufzurufen, wird ein boolescher Wert zurückgegeben, der angibt, ob die Methode erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="d5d7e-131">If you call this method to a function, it returns a Boolean value that indicates whether the method succeeded.</span></span> <span data-ttu-id="d5d7e-132">Wenn Sie versuchen, diese Methode mit dem *State* -Parameter aufzurufen, wenn das angegebene Zeichen ausgeblendet ist, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="d5d7e-132">Attempting to call this method with the *State* parameter set to 2 when the specified character is hidden will fail.</span></span> <span data-ttu-id="d5d7e-133">Wenn Sie den *Status* auf 0 festlegen und die Anwendung der einzige Client ist, tritt bei diesem Vorgang ein Fehler auf, da ein Zeichen immer über den obersten Client verfügen muss.</span><span class="sxs-lookup"><span data-stu-id="d5d7e-133">Similarly, if you set *State* to 0 and your application is the only client, this call fails because a character must always have a topmost client.</span></span>


```
   Dim Genie as Object

   Sub FormLoad()

   Agent1.Characters.Load "Genie", "Genie.acs"

   Set Genie = Agent1.Characters ("Genie")

   If (Genie. Activate = True) Then
      'I'm active

   Else
      'I must be hidden or something

   End If 
   
   End Sub
```



> [!Note]  
> <span data-ttu-id="d5d7e-134">Wenn Sie diese Methode mit einem auf 1 festgelegten *Zustand* aufrufen, wird in der Regel kein [**activateinput**](https://www.bing.com/search?q=**ActivateInput**) -Ereignis generiert, es sei denn, es sind keine anderen Zeichen geladen, oder die Anwendung ist bereits Eingabe aktiv.</span><span class="sxs-lookup"><span data-stu-id="d5d7e-134">Calling this method with *State* set to 1 does not typically generate an [**ActivateInput**](https://www.bing.com/search?q=**ActivateInput**) event unless there are no other characters loaded or your application is already input-active.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="d5d7e-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d5d7e-135">See Also</span></span>

<span data-ttu-id="d5d7e-136">[**Activateinput-Ereignis**](activateinput-event.md), [ **Ereignis "deaktiviert** "](deactivateinput-event.md)</span><span class="sxs-lookup"><span data-stu-id="d5d7e-136">[**ActivateInput event**](activateinput-event.md), [**DeactivateInput event**](deactivateinput-event.md)</span></span>


 

