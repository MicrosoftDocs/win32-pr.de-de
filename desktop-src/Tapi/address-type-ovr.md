---
description: Der Geräte Adresstyp beschreibt die Formen der Adressierung, die für eine Adresse zulässig sind, z. b. eine Telefonnummer oder eine IP-Adresse.
ms.assetid: b474dfca-c4a6-4aab-a4dd-5aec7be3e02a
title: Adresstyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9438c200c9b09dd4f78342ea18d412eaaf23b646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357888"
---
# <a name="address-type"></a><span data-ttu-id="d3478-103">Adresstyp</span><span class="sxs-lookup"><span data-stu-id="d3478-103">Address Type</span></span>

<span data-ttu-id="d3478-104">Der Geräte Adresstyp beschreibt die Formen der Adressierung, die für eine Adresse zulässig sind, z. b. eine Telefonnummer oder eine IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="d3478-104">The device address type describes the forms of addressing permissible on an address, such as a phone number or an IP address.</span></span> <span data-ttu-id="d3478-105">Ein bestimmtes Gerät versteht mindestens einen Adress Typ.</span><span class="sxs-lookup"><span data-stu-id="d3478-105">A given device will understand one or more address types.</span></span> <span data-ttu-id="d3478-106">Eine Liste der von TAPI unterstützten Adresstypen finden Sie unter [lineadresstype- \_ Konstanten](lineaddresstype--constants.md).</span><span class="sxs-lookup"><span data-stu-id="d3478-106">For a list of address types supported by TAPI, see [LINEADDRESSTYPE\_ Constants](lineaddresstype--constants.md).</span></span> <span data-ttu-id="d3478-107">[Address Translation](initiate-a-session-ovr.md) kann verwendet werden, um eine Adresse von einem Typ in einen anderen zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="d3478-107">[Address translation](initiate-a-session-ovr.md) may be used to convert an address from one type to another.</span></span>

<span data-ttu-id="d3478-108">Allgemeine Informationen zu Adressen finden Sie unter [Adresse](address-ovr.md) unter " [Gerätekategorien](device-categories.md)".</span><span class="sxs-lookup"><span data-stu-id="d3478-108">For general information on addresses, see [Address](address-ovr.md) under [Device Categories](device-categories.md).</span></span>

<span data-ttu-id="d3478-109">Der [adreetstyp für eine Sitzung](address-type-for-a-session-ovr.md) ist eine Teilmenge der Geräte Adresstypen.</span><span class="sxs-lookup"><span data-stu-id="d3478-109">The [address type for a session](address-type-for-a-session-ovr.md) will be a subset of the device address types.</span></span>

<span data-ttu-id="d3478-110">**TAPI 2. x:** Weitere Informationen finden Sie unter [**linegetdevcaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) und den **dwadresssstype** -Member von [**linedevcaps**](/windows/win32/api/tapi/ns-tapi-linedevcaps).</span><span class="sxs-lookup"><span data-stu-id="d3478-110">**TAPI 2.x:** See [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) and the **dwAddressType** member of [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps).</span></span>

<span data-ttu-id="d3478-111">**TAPI 3. x:** Weitere Informationen finden Sie unter [**itaddresscapability:: get \_ addresscapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability), wobei *addresscap* auf den **AC \_ addresssstypes** -Member der [**Address- \_ Funktion**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability)festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d3478-111">**TAPI 3.x:** See [**ITAddressCapabilities::get\_AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability), with *AddressCap* set to the **AC\_ADDRESSTYPES** member of [**ADDRESS\_CAPABILITY**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability).</span></span>

 

 
