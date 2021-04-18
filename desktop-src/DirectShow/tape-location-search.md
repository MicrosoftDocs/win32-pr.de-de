---
description: Band Speicherort Suche
ms.assetid: 17fb4eba-4b2c-41c2-94e2-e58586f92e53
title: Band Speicherort Suche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33d1fb719f3b43374e5aa86f34c60e5b8f14d536
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352634"
---
# <a name="tape-location-search"></a><span data-ttu-id="bce87-103">Band Speicherort Suche</span><span class="sxs-lookup"><span data-stu-id="bce87-103">Tape Location Search</span></span>

<span data-ttu-id="bce87-104">Die DV-Geräte unterstützen zwar einen Befehl für die Suche nach Zeit Code oder mit der absoluten Spur Nummer (ATN), der msdv-Treiber verfügt jedoch nicht über eine standardmäßige geräteunabhängige Methode, um auf diese Funktionen zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="bce87-104">Although DV devices support a command to search by time code or by absolute track number (ATN), the MSDV driver does not have a standard, device-independent way to access these functions.</span></span> <span data-ttu-id="bce87-105">Die einzige Möglichkeit besteht darin, einen unformatierten AV/c-Befehl an den Treiber zu senden, wie im Thema [ausgeben von unformatierten AV/c-Befehlen](issuing-raw-av-c-commands.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bce87-105">The only option is to send a raw AV/C command to the driver as described in the topic [Issuing Raw AV/C Commands](issuing-raw-av-c-commands.md).</span></span>

<span data-ttu-id="bce87-106">Der UVC-Treiber unterstützt einen Eigenschaften Satz für die Suche nach bandorten.</span><span class="sxs-lookup"><span data-stu-id="bce87-106">The UVC driver supports a property set for tape location searches.</span></span> <span data-ttu-id="bce87-107">Um einen Suchbefehl zu senden, verwenden Sie die " **ikscontrol** "-Schnittstelle, und legen Sie die Eigenschaft "propsetid \_ \_</span><span class="sxs-lookup"><span data-stu-id="bce87-107">To send a search command, use the **IKsControl** interface and set the PROPSETID\_EXT\_TRANSPORT property.</span></span> <span data-ttu-id="bce87-108">Die Verwendung eines Eigenschaften Satzes ist sicherer als das Senden von unformatierten AV/c-Befehlen an das Gerät, da der Filter durch die AV/c-Befehle umgangen und direkt zum Gerätetreiber geleitet wird.</span><span class="sxs-lookup"><span data-stu-id="bce87-108">Using a property set is safer than sending raw AV/C commands to the device, because AV/C commands bypass the filter and go directly to the device driver.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bce87-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bce87-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bce87-110">Steuern eines DV-Camcorder</span><span class="sxs-lookup"><span data-stu-id="bce87-110">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> <dt>

[<span data-ttu-id="bce87-111">Eigenschaften Satz für externen Geräte Transport</span><span class="sxs-lookup"><span data-stu-id="bce87-111">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
</dt> </dl>

 

 



