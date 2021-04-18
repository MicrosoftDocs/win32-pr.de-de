---
title: Stopmethode (Features der Legacy-Windows-Umgebung)
description: Stop-Methode
ms.assetid: 68372f72-db9c-447c-a3e4-488940c730d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20192634c197559ca54bb8af3d8a29f37beb53e2
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106337280"
---
# <a name="stop-method-legacy-windows-environment-features"></a><span data-ttu-id="c7029-103">Stopmethode (Features der Legacy-Windows-Umgebung)</span><span class="sxs-lookup"><span data-stu-id="c7029-103">Stop Method (Legacy Windows Environment Features)</span></span>

<span data-ttu-id="c7029-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="c7029-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="c7029-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c7029-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="c7029-106">Beendet die Animation für das angegebene Zeichen.</span><span class="sxs-lookup"><span data-stu-id="c7029-106">Stops the animation for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="c7029-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="c7029-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="c7029-108">\*Agent \***. Zeichen ("**_Merkmal-ID_\*_")._ \*  \[ *Anforderung* Abbrechen\]</span><span class="sxs-lookup"><span data-stu-id="c7029-108">*agent\***.Characters ("**_CharacterID_*_").Stop_\* \[*Request*\]</span></span>



| <span data-ttu-id="c7029-109">Teil</span><span class="sxs-lookup"><span data-stu-id="c7029-109">Part</span></span>      | <span data-ttu-id="c7029-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c7029-110">Description</span></span>                                                                                   |
|-----------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7029-111">*Anforderung*</span><span class="sxs-lookup"><span data-stu-id="c7029-111">*Request*</span></span> | <span data-ttu-id="c7029-112">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="c7029-112">Optional.</span></span> <span data-ttu-id="c7029-113">Ein [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt, das einen bestimmten Animations Rückruf angibt.</span><span class="sxs-lookup"><span data-stu-id="c7029-113">A [**Request**](/windows/desktop/lwef/the-request-object) object specifying a particular animation call.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7029-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7029-114">Remarks</span></span>

<span data-ttu-id="c7029-115">Um den Anforderungs Parameter anzugeben, müssen Sie eine Variable erstellen und die Animations Anforderung zuweisen, die Sie abbrechen möchten.</span><span class="sxs-lookup"><span data-stu-id="c7029-115">To specify the request parameter, you must create a variable and assign the animation request you want to stop.</span></span> <span data-ttu-id="c7029-116">Wenn Sie den **Anforderungs** Parameter nicht festlegen, beendet der Server alle Animationen für das Zeichen, einschließlich [**Get**](get-method.md) -aufrufen in der Warteschlange, und löscht seine Animations Warteschlange, es sei denn, das Zeichen wird gerade ausgeblendet oder **zeigt** **eine Animation** an.</span><span class="sxs-lookup"><span data-stu-id="c7029-116">If you don't set the **Request** parameter, the server stops all animations for the character, including queued [**Get**](get-method.md) calls, and clears its animation queue unless the character is currently playing its **Hiding** or **Showing** animation.</span></span> <span data-ttu-id="c7029-117">Diese Methode beendet keine **Get** -Aufrufe, die nicht in der Warteschlange stehen.</span><span class="sxs-lookup"><span data-stu-id="c7029-117">This method does not stop non-queued **Get** calls.</span></span>

<span data-ttu-id="c7029-118">Um eine bestimmte Animation oder einen [**Get**](get-method.md) -Befehl zu beenden, deklarieren Sie eine Objekt Variable, und weisen Sie die Animations Anforderung dieser Variablen zu:</span><span class="sxs-lookup"><span data-stu-id="c7029-118">To stop a specific animation or [**Get**](get-method.md) call, declare an object variable and assign your animation request to that variable:</span></span>


```
   Dim MyRequest
   Dim Genie

   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent1.Characters ("Genie")

   Genie.Get "state", "Showing"
   Genie.Get "animation", "Greet, GreetReturn"

   Genie.Show
   
   'This animation will never play
   Set MyRequest = Genie.Play ("Greet")
   
   Genie.Stop MyRequest
```



<span data-ttu-id="c7029-119">Diese Methode generiert kein [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt.</span><span class="sxs-lookup"><span data-stu-id="c7029-119">This method will not generate a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="c7029-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c7029-120">See Also</span></span>

[<span data-ttu-id="c7029-121">**StopAll-Methode**</span><span class="sxs-lookup"><span data-stu-id="c7029-121">**StopAll method**</span></span>](stopall-method.md)


 

 
