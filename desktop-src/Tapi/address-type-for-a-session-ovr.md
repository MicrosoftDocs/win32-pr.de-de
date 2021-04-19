---
description: Der adrestyp gibt das für eine Adresse erforderliche Format an. Wenn der Typ z. b. "lineadresssstype \_ PhoneNumber" ist, muss die Adresse, die zum Einwählen der Sitzung verwendet wird, eine Telefonnummer sein.
ms.assetid: bea48bde-927a-400a-9a7e-a77e30ba35eb
title: Adresstyp für eine Sitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42499c19a08d67ce2e6e7ea5741053686c32aa6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359070"
---
# <a name="address-type-for-a-session"></a>Adresstyp für eine Sitzung

Der [**adrestyp**](lineaddresstype--constants.md) gibt das für eine Adresse erforderliche Format an. Wenn der Typ z. b. "lineadresssstype \_ PhoneNumber" ist, muss die Adresse, die zum Einwählen der Sitzung verwendet wird, eine Telefonnummer sein.

Ein bestimmtes Gerät und ein angegebener Dienstanbieter unterstützen einen oder mehrere Adresstypen. Informationen dazu, wie Sie ein Gerät für die unterstützten Adressformate abrufen, finden Sie unter [Adresstypen für ein Gerät](address-type-ovr.md) .

**TAPI 2. x:** Weitere Informationen finden Sie unter [**linegetcallinfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwadresssstype** -Member von [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo).

**TAPI 3. x:** Siehe [**itcallinfo:: get \_ callinfolong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), aufgerufen mit dem **cil \_ calleridadresssstype**-, **cil \_ calledidadresssstype**-und **cil \_ connectedidadressstype** -Member von [**CallInfo \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).

 

 
