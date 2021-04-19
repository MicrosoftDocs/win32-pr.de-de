---
title: UI_PKEY_FontProperties_Size
description: Gibt die Größe der Eigenschaft "UI- \_ pkey \_ fontproperties" an \_ .
ms.assetid: bd426910-9852-48e1-91c8-b94be5ef7199
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ae991cfe5f91b4aca4fe0b49a7b7c547e71b0fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339791"
---
# <a name="ui_pkey_fontproperties_size"></a><span data-ttu-id="0d617-103">Größe der Benutzeroberflächen- \_ pkey- \_ fontproperties \_</span><span class="sxs-lookup"><span data-stu-id="0d617-103">UI\_PKEY\_FontProperties\_Size</span></span>

<span data-ttu-id="0d617-104">Gibt die Größe der Eigenschaft "UI- \_ pkey \_ fontproperties" an \_ .</span><span class="sxs-lookup"><span data-stu-id="0d617-104">Identifies the UI\_PKEY\_FontProperties\_Size property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Size
   shellPKey = UI_PKEY_FontProperties_Size
   formatID = 00000302-7363-696e-8441798acf5aebb7
   propID = 302
   typeInfo
      type = VT_DECIMAL
```

## <a name="remarks"></a><span data-ttu-id="0d617-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0d617-105">Remarks</span></span>

<span data-ttu-id="0d617-106">\_Die Größe der UI-pkey- \_ fontproperties \_ wird von einer Anwendung verwendet, um den Wert des Steuer Elements für die **Schriftgröße** abzufragen.</span><span class="sxs-lookup"><span data-stu-id="0d617-106">UI\_PKEY\_FontProperties\_Size is used by an application to query the value of the **Font size** control.</span></span>

<span data-ttu-id="0d617-107">Gültige Werte für diese Eigenschaft liegen zwischen 1 und 9999 (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="0d617-107">Valid values for this property range from 1 to 9999, inclusive.</span></span> <span data-ttu-id="0d617-108">Wenn ein Benutzer versucht, einen ungültigen Wert einzugeben, wird der Eintrag abgelehnt, und das **Schriftart Größen** Steuerelement wird auf den letzten gültigen Wert zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="0d617-108">If a user tries to enter an invalid value, the entry is rejected and the **Font size** control reverts to the last valid value.</span></span>

<span data-ttu-id="0d617-109">Wenn eine Anwendung versucht, die Schriftgröße Programm gesteuert auf einen Wert außerhalb des gültigen Bereichs festzulegen, werden alle Schriftart Eigenschaften für das Menüband-Framework ungültig und die Schriftart Steuerelemente (**Schrift** Grad und **Schriftart**) auf leer oder auf ihren Standardzustand (soweit zutreffend) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0d617-109">If an application attempts to set font size programmatically to a value outside the valid range, the Ribbon framework invalidates all font properties and sets the font controls (**Font size** and **Font face**) to blank or to their default state, where appropriate.</span></span>

<span data-ttu-id="0d617-110">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="0d617-110">The default value is 0.</span></span>

<span data-ttu-id="0d617-111">Der Wert 0 gibt an, dass keine einzelne Punktgröße ausgewählt ist (entweder kein Text oder eine ausgewertegröße mit Hetero gener Größe).</span><span class="sxs-lookup"><span data-stu-id="0d617-111">A value of 0 specifies that no single point size is selected (either no text, or a run of heterogeneously sized text, is selected).</span></span>

<span data-ttu-id="0d617-112">Ein Benutzer kann das Steuerelement für die **Schriftgröße** nicht auf 0 festlegen.</span><span class="sxs-lookup"><span data-stu-id="0d617-112">A user cannot set the **Font size** control to 0.</span></span>

<span data-ttu-id="0d617-113">Ein anderer Wert als 0 gibt an, dass gültige Werte für \_ \_ die Eigenschaften der UI-pkey-fontproperties \_ zwischen *MinimumFontSize* und *maximumfontsize* liegen, wie im [Schriftart-Steuer](windowsribbon-controls-fontcontrol.md) Element Markup deklariert.</span><span class="sxs-lookup"><span data-stu-id="0d617-113">Other than 0, valid values for UI\_PKEY\_FontProperties\_Size range between *MinimumFontSize* and *MaximumFontSize* as declared in the [Font Control](windowsribbon-controls-fontcontrol.md) markup.</span></span>

> [!Note]  
> <span data-ttu-id="0d617-114">Das **Schriftart Größe** -Steuerelement wird auf leer festgelegt, wenn der Schrift Grad Programm gesteuert auf 0 festgelegt ist, z. b. Wenn ein Text mit einer heterogenen Größe hervorgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="0d617-114">The **Font size** control is set to blank when the font size is programmatically set to 0, such as when a run of heterogeneously sized text is highlighted.</span></span>

 

<span data-ttu-id="0d617-115">Wenn ein Text mit heterogener Größe ausgewählt wird, muss die Anwendung die [UI \_ pkey \_ fontproperties \_ Delta size](windowsribbon-reference-properties-uipkey-fontproperties-deltasize.md) Abfragen, um die Befehle zum **vergrößern Schriftart** und zum **Verkleinern der Schriftart** zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="0d617-115">Where a run of heterogeneously sized text is selected, the application should query [UI\_PKEY\_FontProperties\_DeltaSize](windowsribbon-reference-properties-uipkey-fontproperties-deltasize.md) to capture **Grow font** and **Shrink font** commands.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d617-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0d617-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d617-117">Schriftart Steuerelement-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0d617-117">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="0d617-118">Schriftart-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="0d617-118">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 




