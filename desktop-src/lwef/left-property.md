---
title: Left-Eigenschaft (Character-Objekt)
description: Left-Eigenschaft
ms.assetid: f496f075-6430-4806-a237-1c7b626d355e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a318e659405883c56f296a9371eba7e9423662b1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106337897"
---
# <a name="left-property-characters-object"></a><span data-ttu-id="038cc-103">Left-Eigenschaft (Character-Objekt)</span><span class="sxs-lookup"><span data-stu-id="038cc-103">Left Property (Characters Object)</span></span>

<span data-ttu-id="038cc-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="038cc-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="038cc-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="038cc-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="038cc-106">Gibt den linken Rand des Frames des angegebenen Zeichens zurück oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="038cc-106">Returns or sets the left edge of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="038cc-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="038cc-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="038cc-108">\*Agent \***. Zeichen ("**_Merkmal-ID_\*_"). Linker_ \*  \[  =  *Wert*\]</span><span class="sxs-lookup"><span data-stu-id="038cc-108">*agent\***.Characters ("**_CharacterID_*_").Left_\* \[ = *value*\]</span></span>



| <span data-ttu-id="038cc-109">Teil</span><span class="sxs-lookup"><span data-stu-id="038cc-109">Part</span></span>    | <span data-ttu-id="038cc-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="038cc-110">Description</span></span>                                                           |
|---------|-----------------------------------------------------------------------|
| <span data-ttu-id="038cc-111">*value*</span><span class="sxs-lookup"><span data-stu-id="038cc-111">*value*</span></span> | <span data-ttu-id="038cc-112">Eine lange ganze Zahl, die den linken Rand des Frames des Zeichens angibt.</span><span class="sxs-lookup"><span data-stu-id="038cc-112">A Long integer that specifies the left edge of the character's frame.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="038cc-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="038cc-113">Remarks</span></span>

<span data-ttu-id="038cc-114">Die **left** -Eigenschaft wird immer in Pixel ausgedrückt, relativ zum Bildschirm Ursprung (oben links).</span><span class="sxs-lookup"><span data-stu-id="038cc-114">The **Left** property is always expressed in pixels, relative to screen origin (upper left).</span></span> <span data-ttu-id="038cc-115">Diese Eigenschafts Einstellung gilt für alle Clients des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="038cc-115">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="038cc-116">Obwohl das Zeichen in einem unregelmäßig formatierte Regions Fenster angezeigt wird, basiert der Speicherort des Zeichens auf den externen Dimensionen des rechteckigen Animations Rahmens, der verwendet wurde, als das Zeichen mit dem Microsoft-Agent-Zeichen-Editor kompiliert wurde.</span><span class="sxs-lookup"><span data-stu-id="038cc-116">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




