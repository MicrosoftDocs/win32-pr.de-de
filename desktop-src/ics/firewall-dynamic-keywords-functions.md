---
title: Dynamische Firewallschlüsselwortfunktionen
description: Dynamische Firewallschlüsselwörter enthalten die folgenden Funktionen.
keywords:
- Dynamische Firewallschlüsselwörter, Funktionen
ms.topic: article
ms.date: 05/13/2021
ms.localizationpriority: low
ms.openlocfilehash: d086c3aeb3caf7ff85a7fceeec17943c7112a7e0
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2021
ms.locfileid: "112681155"
---
# <a name="firewall-dynamic-keywords-functions"></a>Dynamische Firewallschlüsselwortfunktionen

Dynamische Firewallschlüsselwörter enthalten die folgenden Funktionen.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | Beschreibung |
|-|-|
| [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) | Fordert die Übermittlung von Benachrichtigungen zu Änderungen an bestimmten dynamischen Schlüsselwortadressenobjekten[(FW_DYNAMIC_KEYWORD_ADDRESS0](/windows/win32/api/netfw/ns-netfw-fw_dynamic_keyword_address0)) an. |
| [**FwpmDynamicKeywordUnsubscribe0**](/windows/win32/api/fwpmu/FwpmDynamicKeywordUnsubscribe0) | Bricht die Übermittlung von Benachrichtigungen zu Änderungen an bestimmten dynamischen Schlüsselwortadressenobjekten[(FW_DYNAMIC_KEYWORD_ADDRESS0](/windows/win32/api/netfw/ns-netfw-fw_dynamic_keyword_address0)) ab. |
| [**PFN_FWADDDYNAMICKEYWORDADDRESS0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) | Funktionszeigertyp des Einstiegspunkts im Dienst, den Sie aufrufen, um die angegebene dynamische Schlüsselwortadresse hinzuzufügen. |
| [**PFN_FWDELETEDYNAMICKEYWORDADDRESS0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0) | Funktionszeigertyp des Einstiegspunkts im Dienst, den Sie aufrufen, um die adresse des dynamischen Schlüsselworts mit der angegebenen ID zu löschen. |
| [**PFN_FWENUMDYNAMICKEYWORDADDRESSBYID0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) | Funktionszeigertyp des Einstiegspunkts im Dienst, den Sie aufrufen, um die spezifischen dynamischen Schlüsselwortadressen anhand der ID aufzuzählen. |
| [**PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) | Funktionszeigertyp des Einstiegspunkts im Dienst, den Sie aufrufen, um dynamische Schlüsselwortadressen nach Typ aufzuzählen. Sie können eine bestimmte Teilmenge von -Objekten basierend auf den übergebenen Enumerationsflags anfordern. |
| [**PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0) | Funktionszeigertyp des Einstiegspunkts im Dienst, den Sie aufrufen, um die vom Dienst zugeordneten dynamischen Schlüsselwortadressdaten-Strukturen freizugeben. |
| [**PFN_FWUPDATEDYNAMICKEYWORDADDRESS0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0) | Funktionszeigertyp des Einstiegspunkts im Dienst, den Sie aufrufen, um die Adresse des dynamischen Schlüsselworts mit der Eingabe-ID zu aktualisieren. |

## <a name="related-topics"></a>Zugehörige Themen

* [Referenz zu dynamischen Firewallschlüsselwörtern](firewall-dynamic-keywords-reference.md)
