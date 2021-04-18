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
# <a name="address-type"></a>Adresstyp

Der Geräte Adresstyp beschreibt die Formen der Adressierung, die für eine Adresse zulässig sind, z. b. eine Telefonnummer oder eine IP-Adresse. Ein bestimmtes Gerät versteht mindestens einen Adress Typ. Eine Liste der von TAPI unterstützten Adresstypen finden Sie unter [lineadresstype- \_ Konstanten](lineaddresstype--constants.md). [Address Translation](initiate-a-session-ovr.md) kann verwendet werden, um eine Adresse von einem Typ in einen anderen zu konvertieren.

Allgemeine Informationen zu Adressen finden Sie unter [Adresse](address-ovr.md) unter " [Gerätekategorien](device-categories.md)".

Der [adreetstyp für eine Sitzung](address-type-for-a-session-ovr.md) ist eine Teilmenge der Geräte Adresstypen.

**TAPI 2. x:** Weitere Informationen finden Sie unter [**linegetdevcaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) und den **dwadresssstype** -Member von [**linedevcaps**](/windows/win32/api/tapi/ns-tapi-linedevcaps).

**TAPI 3. x:** Weitere Informationen finden Sie unter [**itaddresscapability:: get \_ addresscapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability), wobei *addresscap* auf den **AC \_ addresssstypes** -Member der [**Address- \_ Funktion**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability)festgelegt ist.

 

 
