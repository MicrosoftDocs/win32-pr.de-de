---
title: Tastatur Behandlung in Steuerelementen
description: Tastatur Behandlung in Steuerelementen
ms.assetid: 33affb3f-5d52-4ada-9751-0775b31a375e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f32610732ddbf88c6a587d5bc0fd7de1188152d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338622"
---
# <a name="keyboard-handling-in-controls"></a><span data-ttu-id="98763-103">Tastatur Behandlung in Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="98763-103">Keyboard Handling in Controls</span></span>

<span data-ttu-id="98763-104">Die Unterstützung der Tastatur Behandlung für die folgenden Funktionen wird dringend empfohlen, auch wenn erkannt wird, dass Sie nicht auf alle Container anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="98763-104">Keyboard handling support for the following functionality is strongly recommended, although it is recognized that it is not applicable to all containers.</span></span>

-   <span data-ttu-id="98763-105">Unterstützung für OLEMISC \_ actslikelabel-und OLEMISC \_ actslikebutton-Status Bits.</span><span class="sxs-lookup"><span data-stu-id="98763-105">Support for OLEMISC\_ACTSLIKELABEL and OLEMISC\_ACTSLIKEBUTTON status bits.</span></span>
-   <span data-ttu-id="98763-106">Implementieren der Eigenschaft DisplayAsDefault Ambient (wenn Sie vorhanden ist, kann Sie **false** zurückgeben).</span><span class="sxs-lookup"><span data-stu-id="98763-106">Implementing the DisplayAsDefault ambient property (if it exists, it can return **FALSE**).</span></span>
-   <span data-ttu-id="98763-107">Implementieren von Registerkarten Behandlung, einschließlich Aktivier Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="98763-107">Implementing tab handling, including tab order.</span></span>

<span data-ttu-id="98763-108">Einige Container verwenden ActiveX-Steuerelemente in herkömmlichen Verbund Dokument Szenarien.</span><span class="sxs-lookup"><span data-stu-id="98763-108">Some containers will use ActiveX controls in traditional compound document scenarios.</span></span> <span data-ttu-id="98763-109">Beispielsweise kann ein Benutzer mit einer Tabelle ein ActiveX-Steuerelement in ein Arbeitsblatt einbetten.</span><span class="sxs-lookup"><span data-stu-id="98763-109">For example, a spreadsheet may allow a user to embed an ActiveX control into a worksheet.</span></span> <span data-ttu-id="98763-110">In solchen Szenarios würde der Container die Tastatur Verarbeitung anders durchführen, da die Tastaturschnittstelle mit den Erwartungen des Benutzers in Übereinstimmung bleiben soll.</span><span class="sxs-lookup"><span data-stu-id="98763-110">In such scenarios, the container would do keyboard handling differently, because the keyboard interface should remain consistent with the user's expectations of a spreadsheet.</span></span> <span data-ttu-id="98763-111">Die Dokumentation für derartige Produkte sollte Benutzer über Unterschiede bei der Steuerungs Behandlung in diesen verschiedenen Szenarien informieren.</span><span class="sxs-lookup"><span data-stu-id="98763-111">Documentation for such products should inform users of differences in control handling in these different scenarios.</span></span> <span data-ttu-id="98763-112">Andere Container sollten die oben genannten Funktionen ordnungsgemäß beachten, einschließlich der mnetmonischen Handhabung.</span><span class="sxs-lookup"><span data-stu-id="98763-112">Other containers should endeavor to honor the above functionality correctly, including Mnemonic handling.</span></span>

## <a name="related-topics"></a><span data-ttu-id="98763-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="98763-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98763-114">Container</span><span class="sxs-lookup"><span data-stu-id="98763-114">Containers</span></span>](containers.md)
</dt> </dl>

 

 




