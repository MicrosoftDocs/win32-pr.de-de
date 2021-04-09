---
title: Hide-Methode
description: Hide-Methode
ms.assetid: c30eda78-0951-43b4-8ae1-daccbd41170d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd50c3f7b8e3d2e60ebe4c00c42375737c05eb04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101566"
---
# <a name="hide-method"></a><span data-ttu-id="03427-103">Hide-Methode</span><span class="sxs-lookup"><span data-stu-id="03427-103">Hide Method</span></span>

<span data-ttu-id="03427-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="03427-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="03427-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="03427-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="03427-106">Blendet das angegebene Zeichen aus.</span><span class="sxs-lookup"><span data-stu-id="03427-106">Hides the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="03427-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="03427-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="03427-108">\*Agent ***. Zeichen ("*** Merkmal-ID \* \* *").* \*  \[ *Schnell* ausblenden\]</span><span class="sxs-lookup"><span data-stu-id="03427-108">*agent ***.Characters ("*** CharacterID\*\*\*").Hide*\* \[*Fast*\]</span></span>



| <span data-ttu-id="03427-109">Teil</span><span class="sxs-lookup"><span data-stu-id="03427-109">Part</span></span>   | <span data-ttu-id="03427-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="03427-110">Description</span></span>                                                                                                                                                                                                                                      |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03427-111">*Fast*</span><span class="sxs-lookup"><span data-stu-id="03427-111">*Fast*</span></span> | <span data-ttu-id="03427-112">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="03427-112">Optional.</span></span> <span data-ttu-id="03427-113">Ein boolescher Wert, der angibt, ob die Animation übersprungen werden soll, die mit dem Ausblenden des Zeichens verknüpft ist. **true** gibt die **versteckte** Animation nicht wieder.</span><span class="sxs-lookup"><span data-stu-id="03427-113">A Boolean value that indicates whether to skip the animation associated with the character's Hiding state **True** Does not play the **Hiding** animation.</span></span> <br/> <span data-ttu-id="03427-114">**False** (Standard) gibt die **versteckte** Animation wieder.</span><span class="sxs-lookup"><span data-stu-id="03427-114">**False** (Default) Plays the **Hiding** animation.</span></span> <br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="03427-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03427-115">Remarks</span></span>

<span data-ttu-id="03427-116">Der Server fügt die Aktionen der **Hide** -Methode in die Warteschlange des Zeichens ein, damit Sie das Zeichen nach einer Sequenz anderer Animationen ausblenden können.</span><span class="sxs-lookup"><span data-stu-id="03427-116">The server queues the actions of the **Hide** method in the character's queue, so you can use it to hide the character after a sequence of other animations.</span></span> <span data-ttu-id="03427-117">Sie können die Aktion sofort wiedergeben, indem Sie die Methode " [**Ende**](stop-method.md) " verwenden, bevor Sie diese Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="03427-117">You can play the action immediately by using the [**Stop**](stop-method.md) method before calling this method.</span></span>

<span data-ttu-id="03427-118">Wenn Sie einen Objekt Verweis deklarieren und diesen auf diese Methode festlegen, wird ein [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="03427-118">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="03427-119">Wenn die zugeordnete Ausblenden der **Animation nicht** geladen wurde und Sie den **fast** -Parameter nicht als **true** angegeben haben, legt der Server die Eigenschaft **Anforderungs** Objekt [**Status**](status-property.md) auf "failed" (Fehler) mit einer entsprechenden Fehlernummer fest.</span><span class="sxs-lookup"><span data-stu-id="03427-119">In addition, if the associated **Hiding** animation has not been loaded and you have not specified the **Fast** parameter as **True**, the server sets the **Request** object [**Status**](status-property.md) property to "failed" with an appropriate error number.</span></span> <span data-ttu-id="03427-120">Wenn Sie also das HTTP-Protokoll für den Zugriff auf Zeichen-oder Animationsdaten verwenden, verwenden Sie die [**Get**](get-method.md) -Methode, und geben Sie den ausblenden **Status zum** Laden der Animation an, bevor Sie die **Hide** -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="03427-120">Therefore, if you are using the HTTP protocol to access character or animation data, use the [**Get**](get-method.md) method and specify the **Hiding** state to load the animation before calling the **Hide** method.</span></span>

<span data-ttu-id="03427-121">Das Ausblenden eines Zeichens kann auch dazu führen, dass das [**activateinput**](activateinput-event.md) -Ereignis eines anderen Clients ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="03427-121">Hiding a character can also result in triggering the [**ActivateInput**](activateinput-event.md) event of another client.</span></span>

> [!Note]  
> <span data-ttu-id="03427-122">Versteckte Zeichen können nicht auf den Audiokanal zugreifen.</span><span class="sxs-lookup"><span data-stu-id="03427-122">Hidden characters cannot access the audio channel.</span></span> <span data-ttu-id="03427-123">Der Server übergibt einen Fehlerstatus im [**requestcomplete**](requestcomplete-event.md) -Ereignis zurück, wenn Sie eine Animations Anforderung generieren und das Zeichen ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="03427-123">The server will pass back a failure status in the [**RequestComplete**](requestcomplete-event.md) event if you generate an animation request and the character is hidden.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="03427-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="03427-124">See Also</span></span>

[<span data-ttu-id="03427-125">**Show-Methode**</span><span class="sxs-lookup"><span data-stu-id="03427-125">**Show method**</span></span>](show-method.md)


 

