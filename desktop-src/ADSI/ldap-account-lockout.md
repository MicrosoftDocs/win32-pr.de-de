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
# <a name="account-lockout-ldap-provider"></a><span data-ttu-id="3ddb7-106">Kontosperrung (LDAP-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="3ddb7-106">Account Lockout (LDAP Provider)</span></span>

<span data-ttu-id="3ddb7-107">Wenn die Anzahl der fehlgeschlagenen Anmeldeversuche überschritten wird, wird das Benutzerkonto für einen Zeitraum gesperrt, der durch das [**LockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) -Attribut angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3ddb7-107">When the number of failed logon attempts is exceeded, the user account is locked out for a time period specified by the [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) attribute.</span></span> <span data-ttu-id="3ddb7-108">Die Eigenschaft " [**IADsUser. isaccountlocked**](iadsuser-property-methods.md) " scheint die Eigenschaft zu sein, die zum Lesen und Ändern des Sperr Zustands eines Benutzerkontos verwendet werden soll. der LDAP ADSI-Anbieter unterstützt die **isaccountlocked** -Eigenschaft jedoch nicht genau.</span><span class="sxs-lookup"><span data-stu-id="3ddb7-108">The [**IADsUser.IsAccountLocked**](iadsuser-property-methods.md) property appears to be the property to use to read and modify the lockout state of a user account, but the LDAP ADSI provider does not accurately support the **IsAccountLocked** property.</span></span> <span data-ttu-id="3ddb7-109">Verwenden Sie den WinNT-Anbieter, um genaue Konto Sperr Daten abzurufen und festzulegen.</span><span class="sxs-lookup"><span data-stu-id="3ddb7-109">To obtain and set accurate account lockout data, use the WinNT provider.</span></span> <span data-ttu-id="3ddb7-110">Weitere Informationen zur Verwendung der **isaccountlocked** -Eigenschaft mit dem WinNT-Anbieter finden Sie unter [Konto Sperre (WinNT-Anbieter)](winnt-account-lockout.md).</span><span class="sxs-lookup"><span data-stu-id="3ddb7-110">For more information about using the **IsAccountLocked** property with the WinNT provider, see [Account Lockout (WinNT Provider)](winnt-account-lockout.md).</span></span>

 

 