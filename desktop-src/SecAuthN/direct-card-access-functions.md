---
description: Mithilfe des Smartcard-Subsystems können Sie mit Karten kommunizieren, die ggf. nicht den ISO 7816-Spezifikationen entsprechen.
ms.assetid: ea6cfa5a-2abf-4b7f-b3f4-99655266f030
title: Direkt Karten Zugriffs Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad360974210114a1069db3226ee814d08008cc98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861984"
---
# <a name="direct-card-access-functions"></a><span data-ttu-id="adc1b-103">Direkt Karten Zugriffs Funktionen</span><span class="sxs-lookup"><span data-stu-id="adc1b-103">Direct Card Access Functions</span></span>

<span data-ttu-id="adc1b-104">Mithilfe des [*Smartcard*](/windows/desktop/SecGloss/s-gly) -Subsystems können Sie mit Karten kommunizieren, die ggf. nicht den ISO 7816-Spezifikationen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="adc1b-104">By using the [*smart card*](/windows/desktop/SecGloss/s-gly) subsystem, you can communicate with cards that may not conform to the ISO 7816 specifications.</span></span> <span data-ttu-id="adc1b-105">Zu diesem Zweck können Sie mithilfe der folgenden Funktionen die Attribute der Kommunikation zwischen der Anwendung und der Karte steuern, indem Sie eine direkte Bearbeitung des [*Readers*](/windows/desktop/SecGloss/r-gly)auf niedriger Ebene ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="adc1b-105">To do this, the following functions let you control the attributes of the communications between the application and the card by giving you direct, low-level manipulation of the [*reader*](/windows/desktop/SecGloss/r-gly).</span></span>

<span data-ttu-id="adc1b-106">Um diese Funktionen zu verwenden, müssen Sie einen Bezeichner für das betreffende Attribut angeben.</span><span class="sxs-lookup"><span data-stu-id="adc1b-106">To use these functions, you have to supply an identifier for the attribute in question.</span></span> <span data-ttu-id="adc1b-107">Gültige Attribut Bezeichner und Werte finden Sie in der Tabelle 3-1 unter *Anforderungen für PC-Connected Schnittstellen Geräte*.</span><span class="sxs-lookup"><span data-stu-id="adc1b-107">For valid attribute identifiers and values, refer to Table 3-1 in *Requirements for PC-Connected Interface Devices*.</span></span>



| <span data-ttu-id="adc1b-108">Thema</span><span class="sxs-lookup"><span data-stu-id="adc1b-108">Topic</span></span>                                    | <span data-ttu-id="adc1b-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="adc1b-109">Description</span></span>                           |
|------------------------------------------|---------------------------------------|
| [<span data-ttu-id="adc1b-110">**Scardcontrol**</span><span class="sxs-lookup"><span data-stu-id="adc1b-110">**SCardControl**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardcontrol)     | <span data-ttu-id="adc1b-111">Bereitstellen der direkten Kontrolle des Readers.</span><span class="sxs-lookup"><span data-stu-id="adc1b-111">Provide direct control of the reader.</span></span> |
| [<span data-ttu-id="adc1b-112">**Scardgetattrib**</span><span class="sxs-lookup"><span data-stu-id="adc1b-112">**SCardGetAttrib**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardgetattrib) | <span data-ttu-id="adc1b-113">Leser Attribute erhalten.</span><span class="sxs-lookup"><span data-stu-id="adc1b-113">Get reader attributes.</span></span>                |
| [<span data-ttu-id="adc1b-114">**Scardsegtaterb**</span><span class="sxs-lookup"><span data-stu-id="adc1b-114">**SCardSetAttrib**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardsetattrib) | <span data-ttu-id="adc1b-115">Festlegen des Reader-Attributs.</span><span class="sxs-lookup"><span data-stu-id="adc1b-115">Set reader attribute.</span></span>                 |



 

 

 
