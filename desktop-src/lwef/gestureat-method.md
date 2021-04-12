---
title: Gestureat-Methode
description: Gestureat-Methode
ms.assetid: c84e9363-e905-476a-832b-9acf6ddee5f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7222c2c0529a486583999f4f9f363e3a30cafc02
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472804"
---
# <a name="gestureat-method"></a><span data-ttu-id="ebbcd-103">Gestureat-Methode</span><span class="sxs-lookup"><span data-stu-id="ebbcd-103">GestureAt Method</span></span>

<span data-ttu-id="ebbcd-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="ebbcd-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="ebbcd-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ebbcd-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="ebbcd-106">Gibt die gesturdende Animation für das angegebene Zeichen an der angegebenen Position wieder.</span><span class="sxs-lookup"><span data-stu-id="ebbcd-106">Plays the gesturing animation for the specified character at the specified location.</span></span>

</dd> <dt>

<span data-ttu-id="ebbcd-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="ebbcd-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="ebbcd-108">\*Agent ***. Zeichen ("*** Merkmal-ID \* \* *"). Gestureat* \*  *x, y*</span><span class="sxs-lookup"><span data-stu-id="ebbcd-108">*agent ***.Characters ("*** CharacterID\*\*\*").GestureAt*\* *x,y*</span></span>



| <span data-ttu-id="ebbcd-109">Teil</span><span class="sxs-lookup"><span data-stu-id="ebbcd-109">Part</span></span>  | <span data-ttu-id="ebbcd-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ebbcd-110">Description</span></span>                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebbcd-111">*x, y*</span><span class="sxs-lookup"><span data-stu-id="ebbcd-111">*x,y*</span></span> | <span data-ttu-id="ebbcd-112">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ebbcd-112">Required.</span></span> <span data-ttu-id="ebbcd-113">Ein ganzzahliger Wert, der die horizontale Bildschirm Koordinate (*x*) und die vertikale Bildschirm Koordinate (*y*) angibt, auf die das Zeichen zeigt.</span><span class="sxs-lookup"><span data-stu-id="ebbcd-113">An integer value that indicates the horizontal (*x*) screen coordinate and vertical (*y*) screen coordinate to which the character will gesture.</span></span> <span data-ttu-id="ebbcd-114">Diese Koordinaten müssen in Pixel angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ebbcd-114">These coordinates must be specified in pixels.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ebbcd-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ebbcd-115">Remarks</span></span>

<span data-ttu-id="ebbcd-116">Der Server übernimmt automatisch die entsprechende Animation, um an den angegebenen Speicherort zu Gesten.</span><span class="sxs-lookup"><span data-stu-id="ebbcd-116">The server automatically plays the appropriate animation to gesture toward the specified location.</span></span> <span data-ttu-id="ebbcd-117">Die Koordinaten sind immer relativ zum Bildschirm Ursprung (oben links).</span><span class="sxs-lookup"><span data-stu-id="ebbcd-117">The coordinates are always relative to the screen origin (upper left).</span></span>

<span data-ttu-id="ebbcd-118">Wenn Sie einen Objekt Verweis deklarieren und diesen auf diese Methode festlegen, wird ein [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ebbcd-118">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="ebbcd-119">Wenn die zugeordnete Animation nicht auf dem lokalen Computer geladen wurde, legt der Server außerdem die [**Status**](status-property.md) -Eigenschaft des **Anforderungs** Objekts auf "failed" (Fehler) mit einer entsprechenden Fehlernummer fest.</span><span class="sxs-lookup"><span data-stu-id="ebbcd-119">In addition, if the associated animation has not been loaded on the local machine, the server sets the **Request** object's [**Status**](status-property.md) property to "failed" with an appropriate error number.</span></span> <span data-ttu-id="ebbcd-120">Wenn Sie also das HTTP-Protokoll für den Zugriff auf Daten der Zeichen Animation verwenden, verwenden Sie die [**Get**](get-method.md) -Methode, um die **gestischen** Zustands Animationen zu laden, bevor Sie die **gestureat** -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ebbcd-120">Therefore, if you are using the HTTP protocol to access character animation data, use the [**Get**](get-method.md) method to load the **Gesturing** state animations before calling the **GestureAt** method.</span></span>

 

 