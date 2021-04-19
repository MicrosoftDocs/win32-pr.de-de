---
description: Nach der Adresszuweisung weist TAPI Adress Bezeichner den Adressen zu.
ms.assetid: 19394db1-4408-4ba6-be48-b408c1fa0f30
title: Adress Bezeichner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb80ee463271a4d7fe9e4dcec086b08c37326551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346710"
---
# <a name="address-identifiers"></a><span data-ttu-id="00457-103">Adress Bezeichner</span><span class="sxs-lookup"><span data-stu-id="00457-103">Address Identifiers</span></span>

<span data-ttu-id="00457-104">Nach der Adresszuweisung weist TAPI Adress Bezeichner den Adressen zu.</span><span class="sxs-lookup"><span data-stu-id="00457-104">After address assignment, TAPI assigns address identifiers to the addresses.</span></span> <span data-ttu-id="00457-105">Ein *Adress Bezeichner* ist eine Zahl zwischen 0 und der Anzahl der Adressen in der Zeile minus 1.</span><span class="sxs-lookup"><span data-stu-id="00457-105">An *address identifier* is a number between 0 and the number of addresses on the line minus one.</span></span> <span data-ttu-id="00457-106">Ein Adress Bezeichner ist eine permanente Zahl, die einem bestimmten Gerät zugewiesen ist und auch bei Betriebssystem Upgrades konstant bleibt.</span><span class="sxs-lookup"><span data-stu-id="00457-106">An address identifier is a permanent number assigned to a given device and remains constant even across operating system upgrades.</span></span> <span data-ttu-id="00457-107">Durch die Kombination von [Geräte Bezeichner](device-identifier-ovr.md) und Adress Bezeichner wird eine bestimmte Adresse eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="00457-107">The combination of [device identifier](device-identifier-ovr.md) and address identifier uniquely identifies a given address.</span></span>

<span data-ttu-id="00457-108">**TAPI 2. x:** Anwendungen erhalten bei einem Aufruf von [**linemakecall**](/windows/win32/api/tapi/nf-tapi-linemakecall) oder [**linegetcallinfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), in der [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) -Struktur oder in einem Aufruf von [**linegetadressssid**](/windows/win32/api/tapi/nf-tapi-linegetaddressid)einen Adress Bezeichner (und einen Geräte Bezeichner).</span><span class="sxs-lookup"><span data-stu-id="00457-108">**TAPI 2.x:** Applications obtain an address identifier (and device identifier) during a call to [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall) or [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), in the [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) structure, or in a call to [**lineGetAddressID**](/windows/win32/api/tapi/nf-tapi-linegetaddressid).</span></span>

<span data-ttu-id="00457-109">**TAPI 3. x:** Die [**itaddresscapability:: get- \_ addresscapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) , die auf den **AC \_ -adressationsmember** der Address- [**\_ Funktion**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability) festgelegt ist, gibt zurück, wobei der *plcapability* -Parameter auf die aktuelle Adress-ID *festgelegt ist* .</span><span class="sxs-lookup"><span data-stu-id="00457-109">**TAPI 3.x:** The [**ITAddressCapabilities::get\_AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) called *AddressCap* set to the **AC\_ADDRESSID** member of [**ADDRESS\_CAPABILITY**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability) will return with the *plCapability* parameter set to the current address ID.</span></span>

 

 
