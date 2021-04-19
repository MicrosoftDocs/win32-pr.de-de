---
description: Das Unimodem oder der universelle Modem Treiber, TSP (Unimdm. TSP), bietet Zugriff auf fast alle Standard Modems.
ms.assetid: 1ea60477-f6c9-44ae-969c-515dfb0c607e
title: Unimodem-TSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 115cc4fd159b2e62062171131f583bad19dc9b00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363334"
---
# <a name="unimodem-tsp"></a><span data-ttu-id="138b7-103">Unimodem-TSP</span><span class="sxs-lookup"><span data-stu-id="138b7-103">Unimodem TSP</span></span>

<span data-ttu-id="138b7-104">Das Unimodem oder der universelle Modem Treiber, TSP (Unimdm. TSP), bietet Zugriff auf fast alle Standard Modems.</span><span class="sxs-lookup"><span data-stu-id="138b7-104">The Unimodem, or Universal Modem Driver, TSP (Unimdm.tsp) provides access to nearly all standard modems.</span></span> <span data-ttu-id="138b7-105">Es unterstützt Sprachmodems, die das Halbduplex Streaming ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="138b7-105">It supports voice modems that allow half-duplex streaming.</span></span> <span data-ttu-id="138b7-106">Sie werden von der Wave-MSP unterstützt, und die Datenstrom Steuerung ist möglich.</span><span class="sxs-lookup"><span data-stu-id="138b7-106">They are supported by the Wave MSP and stream control is possible.</span></span> <span data-ttu-id="138b7-107">(Beachten Sie, dass Unimodem unter Windows NT 4,0 oder früher keine Sprachmodems unterstützt, daher ist die direkte Datenstrom Steuerung nicht möglich.)</span><span class="sxs-lookup"><span data-stu-id="138b7-107">(Note that Unimodem on Windows NT 4.0 or earlier does not support voice modems, so direct stream control is not possible.)</span></span>

<span data-ttu-id="138b7-108">Dieser TSP unterstützt den [**Adresstyp**](./lineaddresstype--constants.md) Wert lineadresssstype \_ PhoneNumber.</span><span class="sxs-lookup"><span data-stu-id="138b7-108">This TSP supports an [**address type**](./lineaddresstype--constants.md) value of LINEADDRESSTYPE\_PHONENUMBER.</span></span> <span data-ttu-id="138b7-109">Wenn der Programmierer die Wähl Regeln verwenden möchte, muss die TAPI 3 [**itadresstranslations**](/windows/win32/api/tapi3if/nn-tapi3if-itaddresstranslation) -Schnittstelle oder die TAPI 2 [**linetranslateaddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) -Funktion verwendet werden, um eine als zulässig einsetzbare Zeichenfolge aus einer Telefonnummer im kanonischen Format abzurufen.</span><span class="sxs-lookup"><span data-stu-id="138b7-109">If the programmer wants to use the dialing rules, the TAPI 3 [**ITAddressTranslation**](/windows/win32/api/tapi3if/nn-tapi3if-itaddresstranslation) interface or the TAPI 2 [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) function must be used to obtain a dialable string from a phone number in canonical format.</span></span>

<span data-ttu-id="138b7-110">Der Unimodem-TSP wird mit den Betriebssystemen Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Millennium Edition, Windows 98 und Windows 95 installiert.</span><span class="sxs-lookup"><span data-stu-id="138b7-110">The Unimodem TSP is installed with Windows Server 2003 operating systems, Windows XP, Windows 2000, Windows NT, Windows Millennium Edition, Windows 98, and Windows 95.</span></span>

 

 
