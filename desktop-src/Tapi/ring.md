---
description: Ein einzelnes Telefon kann ggf. mit unterschiedlichen ringmodi Klingeln.
ms.assetid: c5ddcb3c-183c-4f97-9429-977d5cc32668
title: Ring
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f671aac6ead1938ff5b35ecb4996e4bc072a66d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959711"
---
# <a name="ring"></a><span data-ttu-id="3a124-103">Ring</span><span class="sxs-lookup"><span data-stu-id="3a124-103">Ring</span></span>

<span data-ttu-id="3a124-104">Ein einzelnes Telefon kann ggf. mit unterschiedlichen ringmodi Klingeln.</span><span class="sxs-lookup"><span data-stu-id="3a124-104">A single phone may be able to ring with different ring modes.</span></span> <span data-ttu-id="3a124-105">Aufgrund der Vielzahl von verfügbaren ringmodi werden die ringmodi anhand ihrer ringmodusnummer identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3a124-105">Given the wide variety of ring modes available, ring modes are identified by means of their ring mode number.</span></span> <span data-ttu-id="3a124-106">Eine ringmodusnummer liegt zwischen 0 und der Anzahl der verfügbaren ringmodi minus 1.</span><span class="sxs-lookup"><span data-stu-id="3a124-106">A ring mode number ranges from zero to the number of available ring modes minus one.</span></span>

<span data-ttu-id="3a124-107">Die Funktionen, die eine Anwendung zum Steuern der ringmodi eines Telefon Geräts verwenden würde, sind [**phonesetring**](/windows/desktop/api/Tapi/nf-tapi-phonesetring), wodurch ein geöffnetes Telefongerät entsprechend einem bestimmten Ring Modus und [**phonegetring**](/windows/desktop/api/Tapi/nf-tapi-phonegetring), das den aktuellen Ring Modus eines geöffneten Telefon Geräts zurückgibt, geklingelt wird.</span><span class="sxs-lookup"><span data-stu-id="3a124-107">The functions an application would use to control a phone device's ring modes are [**phoneSetRing**](/windows/desktop/api/Tapi/nf-tapi-phonesetring), which rings an open phone device according to a given ring mode, and [**phoneGetRing**](/windows/desktop/api/Tapi/nf-tapi-phonegetring), which returns the current ring mode of an opened phone device.</span></span>

<span data-ttu-id="3a124-108">Wenn der Ring Modus eines Telefon Geräts geändert wird, wird eine [**Telefon \_ Zustands**](phone-state.md) Meldung an die Anwendung gesendet, um die Anwendung über die Statusänderung zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="3a124-108">When the ring mode of a phone device is changed, a [**PHONE\_STATE**](phone-state.md) message is sent to the application to notify the application about the state change.</span></span> <span data-ttu-id="3a124-109">Die Parameter für diese Nachricht geben Aufschluss über die Änderung.</span><span class="sxs-lookup"><span data-stu-id="3a124-109">Parameters to this message provide an indication of the change.</span></span>

 

 



