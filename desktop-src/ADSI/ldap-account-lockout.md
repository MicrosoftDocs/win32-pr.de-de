---
title: Kontosperrung (LDAP-Anbieter)
description: Wenn die Anzahl der fehlgeschlagenen Anmeldeversuche überschritten wird, wird das Benutzerkonto für einen Zeitraum gesperrt, der durch das LockoutDuration-Attribut angegeben wird.
ms.assetid: bf86f6ac-8209-4306-8736-99ce53c93617
ms.tgt_platform: multiple
keywords:
- Kontosperrung (LDAP-Anbieter) ADSI
- Kontosperrung ADSI, LDAP-Anbieter
- LDAP-Anbieter ADSI, Beispiele für die Benutzerverwaltung, Kontosperrung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 697b7a25943debfd08469ce9a28463c88159ded9
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106339298"
---
# <a name="account-lockout-ldap-provider"></a>Kontosperrung (LDAP-Anbieter)

Wenn die Anzahl der fehlgeschlagenen Anmeldeversuche überschritten wird, wird das Benutzerkonto für einen Zeitraum gesperrt, der durch das [**LockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) -Attribut angegeben wird. Die Eigenschaft " [**IADsUser. isaccountlocked**](iadsuser-property-methods.md) " scheint die Eigenschaft zu sein, die zum Lesen und Ändern des Sperr Zustands eines Benutzerkontos verwendet werden soll. der LDAP ADSI-Anbieter unterstützt die **isaccountlocked** -Eigenschaft jedoch nicht genau. Verwenden Sie den WinNT-Anbieter, um genaue Konto Sperr Daten abzurufen und festzulegen. Weitere Informationen zur Verwendung der **isaccountlocked** -Eigenschaft mit dem WinNT-Anbieter finden Sie unter [Konto Sperre (WinNT-Anbieter)](winnt-account-lockout.md).

 

 