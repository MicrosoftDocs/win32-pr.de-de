---
title: Muveto-Methode
description: Muveto-Methode
ms.assetid: cca2b1b8-0d44-4272-9f0b-f7afd091d802
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d6a7f215de9ea6e323870ec7e10967462ab4174
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038991"
---
# <a name="moveto-method"></a><span data-ttu-id="ce54d-103">Muveto-Methode</span><span class="sxs-lookup"><span data-stu-id="ce54d-103">MoveTo Method</span></span>

<span data-ttu-id="ce54d-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="ce54d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="ce54d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ce54d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="ce54d-106">Verschiebt das angegebene Zeichen an den angegebenen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="ce54d-106">Moves the specified character to the specified location.</span></span>

</dd> <dt>

<span data-ttu-id="ce54d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="ce54d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="ce54d-108">\*Agent ***. Zeichen ("*** Merkmal-ID \* \* *"). Muveto* \*  *x, y*- \[ *Geschwindigkeit*\]</span><span class="sxs-lookup"><span data-stu-id="ce54d-108">*agent ***.Characters ("*** CharacterID\*\*\*").MoveTo*\* *x,y*\[*Speed*\]</span></span>



| <span data-ttu-id="ce54d-109">Teil</span><span class="sxs-lookup"><span data-stu-id="ce54d-109">Part</span></span>    | <span data-ttu-id="ce54d-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ce54d-110">Description</span></span>                                                                                                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce54d-111">*x, y*</span><span class="sxs-lookup"><span data-stu-id="ce54d-111">*x,y*</span></span>   | <span data-ttu-id="ce54d-112">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ce54d-112">Required.</span></span> <span data-ttu-id="ce54d-113">Ein *ganzzahliger* Wert, der den linken Rand (*x*) und den oberen Rand (y) des Animations Rahmens angibt.</span><span class="sxs-lookup"><span data-stu-id="ce54d-113">An integer value that indicates the left edge (*x*) and top edge (*y*) of the animation frame.</span></span> <span data-ttu-id="ce54d-114">Ausgedrückt diese Koordinaten in Pixel.</span><span class="sxs-lookup"><span data-stu-id="ce54d-114">Express these coordinates in pixels.</span></span>                                                   |
| <span data-ttu-id="ce54d-115">*Geschwindigkeit*</span><span class="sxs-lookup"><span data-stu-id="ce54d-115">*Speed*</span></span> | <span data-ttu-id="ce54d-116">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ce54d-116">Optional.</span></span> <span data-ttu-id="ce54d-117">Ein Long Integer-Wert, der in Millisekunden angibt, wie schnell der Rahmen des Zeichens bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="ce54d-117">A Long integer value specifying in milliseconds how quickly the character's frame moves.</span></span> <span data-ttu-id="ce54d-118">Der Standardwert lautet „1000“.</span><span class="sxs-lookup"><span data-stu-id="ce54d-118">The default value is 1000.</span></span> <span data-ttu-id="ce54d-119">Durch die Angabe von NULL (0) wird der Frame verschoben, ohne eine Animation zu spielen.</span><span class="sxs-lookup"><span data-stu-id="ce54d-119">Specifying zero (0) moves the frame without playing an animation.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ce54d-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce54d-120">Remarks</span></span>

<span data-ttu-id="ce54d-121">Der Server spielt automatisch die entsprechende Animation, die den **Verschiebungs Zuständen zugewiesen** ist.</span><span class="sxs-lookup"><span data-stu-id="ce54d-121">The server automatically plays the appropriate animation assigned to the **Moving** states.</span></span> <span data-ttu-id="ce54d-122">Die Position eines Zeichens basiert auf der linken oberen Ecke des Rahmens.</span><span class="sxs-lookup"><span data-stu-id="ce54d-122">The location of a character is based on the upper left corner of its frame.</span></span>

<span data-ttu-id="ce54d-123">Wenn Sie eine Objekt Variable deklarieren und diese Methode auf diese Methode festlegen, wird ein [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ce54d-123">If you declare an object variable and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="ce54d-124">Wenn die zugeordnete Animation nicht auf dem lokalen Computer geladen wurde, legt der Server außerdem die [**Status**](status-property.md) -Eigenschaft des **Anforderungs** Objekts auf "failed" (Fehler) mit einer entsprechenden Fehlernummer fest.</span><span class="sxs-lookup"><span data-stu-id="ce54d-124">In addition, if the associated animation has not been loaded on the local machine, the server sets the **Request** object's [**Status**](status-property.md) property to "failed" with an appropriate error number.</span></span> <span data-ttu-id="ce54d-125">Wenn Sie also das HTTP-Protokoll **für den Zugriff** auf Zeichen-oder Animationsdaten verwenden, verwenden Sie die [**Get**](get-method.md) -Methode, um die Verschiebungs Zustands Animationen vor dem Aufrufen der Methode " **muveto** " zu laden.</span><span class="sxs-lookup"><span data-stu-id="ce54d-125">Therefore, if you are using the HTTP protocol to access character or animation data, use the [**Get**](get-method.md) method to load the **Moving** state animations before calling the **MoveTo** method.</span></span>

<span data-ttu-id="ce54d-126">Auch wenn die Animation nicht geladen ist, verschiebt der Server den Frame noch immer.</span><span class="sxs-lookup"><span data-stu-id="ce54d-126">Even if the animation is not loaded, the server still moves the frame.</span></span>

> [!Note]  
> <span data-ttu-id="ce54d-127">Wenn Sie vor dem Anzeigen des Zeichens " **muveto** " mit einem Wert ungleich 0 (null) aufruft, wird ein Fehlerstatus zurückgegeben, wenn Sie ihm ein [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt zugewiesen haben, da der Wert ungleich 0 (null) angibt, dass Sie versuchen, eine Animation wiederzugeben, wenn das Zeichen nicht sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="ce54d-127">If you call **MoveTo** with a nonzero value before the character is shown, it will return a failure status if you assigned it a [**Request**](/windows/desktop/lwef/the-request-object) object, because the nonzero value indicates that you are attempting to play an animation when the character is not visible.</span></span>

 

> [!Note]  
> <span data-ttu-id="ce54d-128">Der tatsächliche Effekt des *Geschwindigkeits* Parameters kann je nach Geschwindigkeit des Prozessors des Computers und der Priorität anderer Tasks, die auf dem System ausgeführt werden, variieren.</span><span class="sxs-lookup"><span data-stu-id="ce54d-128">The *Speed* parameter's actual effect may vary based on the speed of the processor of the computer and the priority of other tasks running on the system.</span></span>

 

 

 