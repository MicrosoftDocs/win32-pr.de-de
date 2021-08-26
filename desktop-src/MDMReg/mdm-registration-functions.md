---
title: MDM-Registrierungsfunktionen
description: Die folgenden Funktionen werden in deklariert `mdmregistration.h` und von der MDM-Registrierung verwendet.
ms.assetid: 1b063a56-f59f-4b02-949f-c8b6bbf45a13
ms.localizationpriority: low
ms.topic: reference
ms.date: 11/19/2020
ms.openlocfilehash: f9149c4bd2f9f931a506dc35d05b5e1c641dc87445fbf88fd73ff9ad20ac514b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040370"
---
# <a name="mdm-registration-functions"></a>MDM-Registrierungsfunktionen

Die folgenden Funktionen werden in deklariert `mdmregistration.h` und von der MDM-Registrierung verwendet.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | BESCHREIBUNG |
|-|-|
| [**DiscoverManagementService**](/windows/win32/api/MDMRegistration/nf-mdmregistration-discovermanagementservice) | Ermittelt den MDM-Dienst. |
| [**DiscoverManagementServiceEx**](/windows/win32/api/MDMRegistration/nf-mdmregistration-discovermanagementserviceex) | Ermittelt den MDM-Dienst mithilfe eines Kandidatenservers. |
| [**GetDeviceManagementConfigInfo**](/windows/win32/api/mdmregistration/nf-mdmregistration-getdevicemanagementconfiginfo) | Ruft die Konfigurationsinformationen ab, die der Anbieter-ID zugeordnet sind. |
| [**GetDeviceRegistrationInfo**](/windows/win32/api/MDMRegistration/nf-mdmregistration-getdeviceregistrationinfo) | Ruft die Geräteregistrierungsinformationen ab. |
| [**GetManagementAppHyperlink**](/windows/win32/api/MDMRegistration/nf-mdmregistration-getmanagementapphyperlink) | Ruft den Verwaltungs-App-Link ab, der dem MDM-Dienst zugeordnet ist. |
| [**IsDeviceRegisteredWithManagement**](/windows/win32/api/MDMRegistration/nf-mdmregistration-isdeviceregisteredwithmanagement) | Überprüft, ob das Gerät bei einem MDM-Dienst registriert ist. |
| [**IsManagementRegistrationAllowed**](/windows/win32/api/MDMRegistration/nf-mdmregistration-ismanagementregistrationallowed) | Überprüft, ob die MDM-Registrierung durch eine lokale Richtlinie zulässig ist. |
| [**RegisterDeviceWithManagement**](/windows/win32/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagement) | Registriert ein Gerät mithilfe des [ \[ MS-MDE \] : Mobile Device Enrollment Protocol](/openspecs/windows_protocols/ms-mde/5c841535-042e-489e-913c-9d783d741267)bei einem MDM-Dienst. |
| [**RegisterDeviceWithManagementUsingAADCredentials**](/windows/win32/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagementusingaadcredentials) | Registriert ein Gerät mithilfe von AAD-Anmeldeinformationen (Azure Active Directory) bei einem MDM-Dienst. |
| [**SetDeviceManagementConfigInfo**](/windows/win32/api/mdmregistration/nf-mdmregistration-setdevicemanagementconfiginfo) | Legt die Konfigurationsinformationen fest, die der Anbieter-ID zugeordnet sind. |
| [**SetManagedExternally**](/windows/win32/api/MDMRegistration/nf-mdmregistration-setmanagedexternally) | Gibt dem MDM-Agent an, dass das Gerät extern verwaltet wird und nicht bei einem MDM-Dienst registriert werden soll. |
| [**UnregisterDeviceWithManagement**](/windows/win32/api/MDMRegistration/nf-mdmregistration-unregisterdevicewithmanagement) | Aufheben der Registrierung eines Geräts beim MDM-Dienst. |

## <a name="related-topics"></a>Zugehörige Themen

* [MDM-Registrierungsreferenz](./mdm-registration-reference.md)
