---
title: Play-Methode (Features der Legacy-Windows-Umgebung)
description: Play-Methode
ms.assetid: 7e89341a-b4d3-4bea-8e7f-31c649ff06b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d06f4275d7b4c0959a59536c8b20a95c14ab1c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106338104"
---
# <a name="play-method-legacy-windows-environment-features"></a><span data-ttu-id="9b403-103">Play-Methode (Features der Legacy-Windows-Umgebung)</span><span class="sxs-lookup"><span data-stu-id="9b403-103">Play Method (Legacy Windows Environment Features)</span></span>

<span data-ttu-id="9b403-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="9b403-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="9b403-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9b403-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="9b403-106">Gibt die angegebene Animation für das angegebene Zeichen wieder.</span><span class="sxs-lookup"><span data-stu-id="9b403-106">Plays the specified animation for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="9b403-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="9b403-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="9b403-108">\*Agent \***. Zeichen ("**_Merkmal-ID_*_"). Play_* "*animationname*"</span><span class="sxs-lookup"><span data-stu-id="9b403-108">*agent\***.Characters ("**_CharacterID_*_").Play_\* "*AnimationName*"</span></span>

</dd> </dl> 

| <span data-ttu-id="9b403-109">Teil</span><span class="sxs-lookup"><span data-stu-id="9b403-109">Part</span></span>            | <span data-ttu-id="9b403-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b403-110">Description</span></span>                                                          |
|-----------------|----------------------------------------------------------------------|
| <span data-ttu-id="9b403-111">*Animationname*</span><span class="sxs-lookup"><span data-stu-id="9b403-111">*AnimationName*</span></span> | <span data-ttu-id="9b403-112">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9b403-112">Required.</span></span> <span data-ttu-id="9b403-113">Eine Zeichenfolge, die den Namen einer Animationssequenz angibt.</span><span class="sxs-lookup"><span data-stu-id="9b403-113">A string that specifies the name of an animation sequence.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9b403-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b403-114">Remarks</span></span>

<span data-ttu-id="9b403-115">Der Name einer Animation wird definiert, wenn das Zeichen mit dem Microsoft-Agent-Zeichen-Editor kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="9b403-115">An animation's name is defined when the character is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="9b403-116">Vor der Wiedergabe der angegebenen Animation versucht der Server, die Rückgabe Animation für die vorherige Animation **wiederzugeben** , sofern eine zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="9b403-116">Before playing the specified animation, the server attempts to play the **Return** animation for the previous animation, if one has been assigned.</span></span>

<span data-ttu-id="9b403-117">Wenn Sie mithilfe eines herkömmlichen Datei Protokolls auf die Animationen eines Zeichens zugreifen, können Sie einfach die **Play** -Methode verwenden, um den Namen der Animation anzugeben.</span><span class="sxs-lookup"><span data-stu-id="9b403-117">When accessing a character's animations using a conventional file protocol, you can simply use the **Play** method specifying the name of the animation.</span></span> <span data-ttu-id="9b403-118">Wenn Sie jedoch das HTTP-Protokoll verwenden, um auf Daten der Zeichen Animation zuzugreifen, verwenden Sie die **Get** -Methode, um die Animation vor dem Aufrufen der **Play** -Methode zu laden.</span><span class="sxs-lookup"><span data-stu-id="9b403-118">However, if you are using the HTTP protocol to access character animation data, use the **Get** method to load the animation before calling the **Play** method.</span></span>

<span data-ttu-id="9b403-119">Weitere Informationen finden Sie unter der **Get** -Methode.</span><span class="sxs-lookup"><span data-stu-id="9b403-119">For more information, see the **Get** method.</span></span>

<span data-ttu-id="9b403-120">Um die Syntax zu vereinfachen, können Sie einen Objekt Verweis deklarieren und ihn so festlegen, dass er auf das [**Zeichen**](/windows/desktop/lwef/the-characters-object) Objekt in der [**Zeichen**](/windows/desktop/lwef/the-characters-object) Auflistung verweist, und den Verweis als Teil der **Play** -Anweisungen verwenden:</span><span class="sxs-lookup"><span data-stu-id="9b403-120">To simplify your syntax, you can declare an object reference and set it to reference the [**Character**](/windows/desktop/lwef/the-characters-object) object in the [**Characters**](/windows/desktop/lwef/the-characters-object) collection and use the reference as part of your **Play** statements:</span></span>


```
   Dim Genie   
   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent1.Characters ("Genie")
   
   Genie.Get "state", "Showing"
   Genie.Show

   Genie.Get "animation", "Greet, GreetReturn"
   Genie.Play "Greet"
   Genie.Speak "Hello."
```



<span data-ttu-id="9b403-121">Wenn Sie einen Objekt Verweis deklarieren und diesen auf diese Methode festlegen, wird ein [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9b403-121">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="9b403-122">Wenn Sie außerdem eine Animation angeben, die nicht geladen wurde, oder wenn das Zeichen nicht erfolgreich geladen wurde, legt der Server die [**Status**](status-property.md) -Eigenschaft des **Anforderungs** Objekts auf "failed" (Fehler) mit einer entsprechenden Fehlernummer fest.</span><span class="sxs-lookup"><span data-stu-id="9b403-122">In addition, if you specify an animation that is not loaded or if the character has not been successfully loaded, the server sets the [**Status**](status-property.md) property of **Request** object to "failed" with an appropriate error number.</span></span> <span data-ttu-id="9b403-123">Wenn die Animation jedoch nicht vorhanden ist und die Daten des Zeichens bereits erfolgreich geladen wurden, löst der Server einen Fehler aus.</span><span class="sxs-lookup"><span data-stu-id="9b403-123">However, if the animation does not exist and the character's data has already been successfully loaded, the server raises an error.</span></span>

<span data-ttu-id="9b403-124">Die **Play** -Methode macht das Zeichen nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="9b403-124">The **Play** method does not make the character visible.</span></span> <span data-ttu-id="9b403-125">Wenn das Zeichen nicht sichtbar ist, spielt der Server die Animation unsichtbar und legt die Eigenschaft [**Status**](status-property.md) des [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekts fest.</span><span class="sxs-lookup"><span data-stu-id="9b403-125">If the character is not visible, the server plays the animation invisibly, and sets the [**Status**](status-property.md) property of the [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

 

 
