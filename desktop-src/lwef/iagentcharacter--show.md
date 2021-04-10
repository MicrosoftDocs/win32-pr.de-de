---
title: Iagentcharacter anzeigen
description: Iagentcharacter anzeigen
ms.assetid: 5f13dcef-3777-41eb-827f-6162bad71a2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 997a9879d564644085bd92e4515460c3dde33208
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038993"
---
# <a name="iagentcharactershow"></a><span data-ttu-id="00cf2-103">Iagentcharacter:: Show</span><span class="sxs-lookup"><span data-stu-id="00cf2-103">IAgentCharacter::Show</span></span>

<span data-ttu-id="00cf2-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="00cf2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Show(
   long bFast,      // play Showing state animation flag
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="00cf2-105">Zeigt ein Zeichen an.</span><span class="sxs-lookup"><span data-stu-id="00cf2-105">Displays a character.</span></span>

-   <span data-ttu-id="00cf2-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="00cf2-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="00cf2-107">Wenn die Funktion zurückgibt, enthält *pdwreqid* die ID der Anforderung.</span><span class="sxs-lookup"><span data-stu-id="00cf2-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="00cf2-108"><span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*BFAST*</span><span class="sxs-lookup"><span data-stu-id="00cf2-108"><span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*bFast*</span></span>
</dt> <dd>

<span data-ttu-id="00cf2-109">Statusanimations-Flag wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="00cf2-109">Showing state animation flag.</span></span> <span data-ttu-id="00cf2-110">Wenn dieser Parameter **true** ist, wird die Status Animation **angezeigt** , nachdem das Zeichen sichtbar gemacht wurde. **false** gibt an, dass die Animation nicht wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="00cf2-110">If this parameter is **True**, the **Showing** state animation plays after making the character visible; if **False**, the animation does not play.</span></span>

</dd> <dt>

<span data-ttu-id="00cf2-111"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwreqid*</span><span class="sxs-lookup"><span data-stu-id="00cf2-111"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="00cf2-112">Adresse einer Variablen, [**die die**](/windows/desktop/lwef/iagentcharacter--show) anforderungsanforderungs-ID empfängt.</span><span class="sxs-lookup"><span data-stu-id="00cf2-112">Address of a variable that receives the [**Show**](/windows/desktop/lwef/iagentcharacter--show) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="00cf2-113">Vermeiden Sie, den *BFAST* -Parameter auf " **true** " festzulegen, ohne zuvor eine Animation zu spielen. andernfalls wird der Zeichen Rahmen möglicherweise angezeigt, aber es ist kein Bild zum Anzeigen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="00cf2-113">Avoid setting the *bFast* parameter to **True** without playing an animation beforehand, otherwise, the character frame may be displayed, but have no image to display.</span></span> <span data-ttu-id="00cf2-114">Beachten Sie insbesondere Folgendes: Wenn Sie " [**muveto**](iagentcharacter--moveto.md) " anrufen, wenn das Zeichen nicht sichtbar ist, wird keine Animation wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="00cf2-114">In particular, note that if you call [**MoveTo**](iagentcharacter--moveto.md) when the character is not visible, it does not play any animation.</span></span> <span data-ttu-id="00cf2-115">Wenn Sie die **Show** -Methode mit *BFAST* auf **true** festlegen, wird daher kein Bild angezeigt.</span><span class="sxs-lookup"><span data-stu-id="00cf2-115">Therefore, if you call the **Show** method with *bFast* set to **True**, no image will be displayed.</span></span> <span data-ttu-id="00cf2-116">Wenn Sie [**Ausblenden**](/windows/desktop/lwef/iagentcharacter--hide)und dann mit *BFAST* auf **true** festlegen, wird auch kein **Bild angezeigt.**</span><span class="sxs-lookup"><span data-stu-id="00cf2-116">Similarly, if you call [**Hide**](/windows/desktop/lwef/iagentcharacter--hide), then **Show** with *bFast* set to **True**, there will be no visible image.</span></span>

<span data-ttu-id="00cf2-117">Wenn Sie das HTTP-Protokoll für den Zugriff auf Zeichen-und Animationsdaten verwenden, verwenden Sie die [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) -Methode, um die Verfügbarkeit der **Anzeige** Zustands Animation sicherzustellen, bevor Sie diese Methode aufrufen</span><span class="sxs-lookup"><span data-stu-id="00cf2-117">When using the HTTP protocol to access character and animation data, use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to ensure the availability of the **Showing** state animation before calling this method.</span></span>

## <a name="see-also"></a><span data-ttu-id="00cf2-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="00cf2-118">See Also</span></span>

[<span data-ttu-id="00cf2-119">**Iagentcharacter:: Hide**</span><span class="sxs-lookup"><span data-stu-id="00cf2-119">**IAgentCharacter::Hide**</span></span>](iagentcharacter--hide.md)


 

 