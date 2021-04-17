---
title: Pitch-Eigenschaft
description: Pitch-Eigenschaft
ms.assetid: 98b2ada3-93c6-4fa1-bf12-353eb229c30c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 998ee4bcf77878062425086d67066040f5d58421
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388762"
---
# <a name="pitch-property"></a><span data-ttu-id="0213e-103">Pitch-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0213e-103">Pitch Property</span></span>

<span data-ttu-id="0213e-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="0213e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="0213e-105"><span id="Description_"></span><span id="description_"></span><span id="DESCRIPTION_"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0213e-105"><span id="Description_"></span><span id="description_"></span><span id="DESCRIPTION_"></span>**Description**</span></span> 
</dt> <dd>

<span data-ttu-id="0213e-106">Gibt eine lange ganze Zahl für die Einstellung für die Sprachausgabe (TTS) der angegebenen Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="0213e-106">Returns a Long integer for the specified character's speech output (TTS) pitch setting.</span></span>

</dd> <dt>

<span data-ttu-id="0213e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="0213e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="0213e-108">*Agent ***. Zeichen ("*** Merkmal-ID \* \* *"). Spur**</span><span class="sxs-lookup"><span data-stu-id="0213e-108">*agent ***.Characters ("*** CharacterID\*\*\*").Pitch*\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0213e-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0213e-109">Remarks</span></span>

<span data-ttu-id="0213e-110">Diese Eigenschaft gilt nur für Zeichen, die für die TTS-Ausgabe konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="0213e-110">This property applies only to characters configured for TTS output.</span></span> <span data-ttu-id="0213e-111">Wenn das Zeichen keine TTS-Ausgabe unterstützt, gibt diese Eigenschaft 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="0213e-111">If the character does not support TTS output, this property returns zero (0).</span></span>

<span data-ttu-id="0213e-112">Obwohl Ihre Anwendung diesen Wert nicht schreiben kann, können Sie **Pit** -Tags (Pitch-Tags) in den Ausgabetext einschließen, um die Größe für eine bestimmte Äußerung vorübergehend zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="0213e-112">Although your application cannot write this value, you can include **Pit** (pitch) tags in your output text that will temporarily increase the pitch for a particular utterance.</span></span> <span data-ttu-id="0213e-113">Wenn Sie das **boxtag** zum Ändern der Tonhöhe verwenden, ändert sich die Einstellung der Eigenschaft " **Pitch** " jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="0213e-113">However, using the **Pit** tag to change the pitch will not change the **Pitch** property setting.</span></span> <span data-ttu-id="0213e-114">Weitere Informationen finden Sie unter [Sprachausgabe Tags](pit-tag.md).</span><span class="sxs-lookup"><span data-stu-id="0213e-114">For further information, see [Speech Output Tags](pit-tag.md).</span></span>

 

 




