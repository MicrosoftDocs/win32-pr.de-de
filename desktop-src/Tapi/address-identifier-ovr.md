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
# <a name="address-identifiers"></a>Adress Bezeichner

Nach der Adresszuweisung weist TAPI Adress Bezeichner den Adressen zu. Ein *Adress Bezeichner* ist eine Zahl zwischen 0 und der Anzahl der Adressen in der Zeile minus 1. Ein Adress Bezeichner ist eine permanente Zahl, die einem bestimmten Gerät zugewiesen ist und auch bei Betriebssystem Upgrades konstant bleibt. Durch die Kombination von [Geräte Bezeichner](device-identifier-ovr.md) und Adress Bezeichner wird eine bestimmte Adresse eindeutig identifiziert.

**TAPI 2. x:** Anwendungen erhalten bei einem Aufruf von [**linemakecall**](/windows/win32/api/tapi/nf-tapi-linemakecall) oder [**linegetcallinfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), in der [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) -Struktur oder in einem Aufruf von [**linegetadressssid**](/windows/win32/api/tapi/nf-tapi-linegetaddressid)einen Adress Bezeichner (und einen Geräte Bezeichner).

**TAPI 3. x:** Die [**itaddresscapability:: get- \_ addresscapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) , die auf den **AC \_ -adressationsmember** der Address- [**\_ Funktion**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability) festgelegt ist, gibt zurück, wobei der *plcapability* -Parameter auf die aktuelle Adress-ID *festgelegt ist* .

 

 
