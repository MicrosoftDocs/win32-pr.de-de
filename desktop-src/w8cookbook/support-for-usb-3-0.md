---
title: Unterstützung für USB 3,0
description: Unterstützung für USB 3,0
ms.assetid: AACE4B57-A03F-40C7-AFDD-514D29F24521
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2f6fa342efa5e7b4fd95287a2061482fa0cbb9
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "103730760"
---
# <a name="support-for-usb-30"></a><span data-ttu-id="9abf2-103">Unterstützung für USB 3,0</span><span class="sxs-lookup"><span data-stu-id="9abf2-103">Support for USB 3.0</span></span>

## <a name="platforms"></a><span data-ttu-id="9abf2-104">Plattformen</span><span class="sxs-lookup"><span data-stu-id="9abf2-104">Platforms</span></span>

<span data-ttu-id="9abf2-105">**Clients** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="9abf2-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="9abf2-106">**Server** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9abf2-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="9abf2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9abf2-107">Description</span></span>

<span data-ttu-id="9abf2-108">In Windows 8 und Windows Server 2012 haben wir Unterstützung für USB 3,0 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9abf2-108">In Windows 8 and Windows Server 2012, we added support for USB 3.0.</span></span> <span data-ttu-id="9abf2-109">Hierzu haben wir einen neuen Software Stapel hinzugefügt, um den USB 3,0-Host Controller (erweiterbarer Host Controller, XHC) zu schalten.</span><span class="sxs-lookup"><span data-stu-id="9abf2-109">We did this by adding a new software stack to power the USB 3.0 host controller, called an eXtensible Host Controller (XHC).</span></span> <span data-ttu-id="9abf2-110">Wir haben Schnittstellen Parität, iriql-Ebene, Aufruferkontext, Fehlerstatus, Wiederholungs Häufigkeit usw. beibehalten.</span><span class="sxs-lookup"><span data-stu-id="9abf2-110">We maintained interface parity, IRQL level, caller context, error status, retry frequency, and so on.</span></span> <span data-ttu-id="9abf2-111">Bei der Interaktion mit einem Gerät, das über USB 2,0 und USB 3,0 verbunden ist, sollten Sie keinen Unterschied haben.</span><span class="sxs-lookup"><span data-stu-id="9abf2-111">There should be no difference for you when interacting with a device connected over USB 2.0 versus USB 3.0.</span></span>

<span data-ttu-id="9abf2-112">Wenn Sie jedoch einen Treiber für ein neues USB 3,0-Gerät schreiben, entscheiden Sie sich definitiv für neue USB 3,0-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="9abf2-112">However, if you are writing a driver for a new, USB 3.0 device, definitely opt for new USB 3.0 capabilities.</span></span>

## <a name="manifestation"></a><span data-ttu-id="9abf2-113">Ausstrahlung</span><span class="sxs-lookup"><span data-stu-id="9abf2-113">Manifestation</span></span>

<span data-ttu-id="9abf2-114">Geräte Übertragungen werden schneller und weniger Energieverbrauch von PCs durch USB-Geräte beansprucht.</span><span class="sxs-lookup"><span data-stu-id="9abf2-114">Device transfers are faster and less power is consumed from a PC by USB devices overall.</span></span> <span data-ttu-id="9abf2-115">Wenn eine Verbindung mit einem USB 3,0-Port besteht, besteht das Risiko, dass vorhandene USB-Geräte nicht ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="9abf2-115">There is a risk that existing USB devices may not function correctly when connected to a USB 3.0 port.</span></span> <span data-ttu-id="9abf2-116">Dies sollte nicht der Fall sein, und es ist nicht zu erwarten, aber da die Software, die USB 3,0 unterstützt, neu ist, ist dies ein Risiko.</span><span class="sxs-lookup"><span data-stu-id="9abf2-116">This should not happen, and is not expected, but, because the software that powers USB 3.0 is new, it is a risk.</span></span>

 

 




