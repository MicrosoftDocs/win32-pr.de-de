---
title: Dynamische Firewallschlüsselwörterfunktionen
description: Dynamische Firewallschlüsselwörter enthalten die folgenden Funktionen.
keywords:
- Dynamische Firewallschlüsselwörter, Funktionen
ms.topic: article
ms.date: 05/13/2021
ms.localizationpriority: low
ms.openlocfilehash: 1aacc30ecac9cddca5f986878da1ff633660152144e8ca2fe1440fdecfd61e3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015650"
---
# <a name="firewall-dynamic-keywords-functions"></a>Dynamische Firewallschlüsselwörterfunktionen

Dynamische Firewallschlüsselwörter enthalten die folgenden Funktionen.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | BESCHREIBUNG |
|-|-|
| [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) | Fordert die Übermittlung von Benachrichtigungen zu Änderungen an bestimmten dynamischen Schlüsselwortadressenobjekten[(FW_DYNAMIC_KEYWORD_ADDRESS0](/windows/win32/api/netfw/ns-netfw-fw_dynamic_keyword_address0)) an. |
| [**FwpmDynamicKeywordUnsubscribe0**](/windows/win32/api/fwpmu/FwpmDynamicKeywordUnsubscribe0) | Bricht die Übermittlung von Benachrichtigungen zu Änderungen an bestimmten dynamischen Schlüsselwortadressenobjekten[(FW_DYNAMIC_KEYWORD_ADDRESS0](/windows/win32/api/netfw/ns-netfw-fw_dynamic_keyword_address0)) ab. |
| [**PFN_FWADDDYNAMICKEYWORDADDRESS0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) | Funktionszeigertyp des Einstiegspunkts im Dienst, den Sie aufrufen, um die angegebene dynamische Schlüsselwortadresse hinzuzufügen. |
| [**PFN_FWDELETEDYNAMICKEYWORDADDRESS0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0) | Funktionszeigertyp des Einstiegspunkts im Dienst, den Sie aufrufen, um die dynamische Schlüsselwortadresse mit der angegebenen ID zu löschen. |
| [**PFN_FWENUMDYNAMICKEYWORDADDRESSBYID0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) | Funktionszeigertyp des Einstiegspunkts im Dienst, den Sie aufrufen, um die spezifischen dynamischen Schlüsselwortadressen nach ID aufzählen. |
| [**PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) | Funktionszeigertyp des Einstiegspunkts im Dienst, den Sie aufrufen, um dynamische Schlüsselwortadressen nach Typ aufzählen. Sie können eine bestimmte Teilmenge von -Objekten basierend auf den übergebenen Enumerationsflags anfordern. |
| [**PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0) | Funktionszeigertyp des Einstiegspunkts in dem Dienst, den Sie aufrufen, um vom Dienst zugeordnete dynamische Schlüsselwort-Adressdatenstruktur frei zu geben. |
| [**PFN_FWUPDATEDYNAMICKEYWORDADDRESS0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0) | Funktionszeigertyp des Einstiegspunkts im Dienst, den Sie aufrufen, um die dynamische Schlüsselwortadresse mit der Eingabe-ID zu aktualisieren. |

## <a name="related-topics"></a>Zugehörige Themen

* [Referenz zu dynamischen Firewallschlüsselwörtern](firewall-dynamic-keywords-reference.md)
