---
title: 802.11 Wireless Diagnostics Extensible Helper Classes
description: Die integrierte Drahtlose Diagnoseinfrastruktur verfügt über zwei Erweiterungspunkte. Parent Helper ClassPurposeRevised Native Wifi (RNWF) Extensible Helper ClassDiagnoses issues related to 802.11 connectivity extensions .
ms.assetid: b54f836d-4fae-4e71-bf7b-af5a6e9e615c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3b7ac72cb42b12a96e5c57db0897a13d49d76370126e119ac2f5ed457d55c9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133445"
---
# <a name="80211-wireless-diagnostics-extensible-helper-classes"></a>802.11 Wireless Diagnostics Extensible Helper Classes

Die integrierte Drahtlose Diagnoseinfrastruktur verfügt über zwei Erweiterungspunkte.

| Übergeordnete Hilfsklasse                                | Zweck                                                           |
|----------------------------------------------------|-------------------------------------------------------------------|
| Extensible Helper-Klasse für überarbeitetes natives Wlan (RNWF) | Diagnostiziert Probleme im Zusammenhang mit 802.11-Konnektivitätserweiterungen.       |
| L2Security Extensible Helper-Klasse                 | Diagnostiziert Probleme im Zusammenhang mit Layer 2-Sicherheitsprotokollerweiterungen. |



 

> [!Note]  
> Eine Hilfsklasse eines Drittanbieters sollte sich bei beiden übergeordneten Hilfsklassen registrieren, um sicherzustellen, dass die Drittanbieterklasse aufgerufen wird. Weitere Informationen zur Registrierung finden Sie unter [Registrieren von NDF-Hilfsklassenerweiterungen.](registering-ndf-helper-class-extensions.md)

 

## <a name="rnwf-extensible-helper-class"></a>RNWF Extensible Helper-Klasse

Name der übergeordneten Hilfsklasse

``` syntax
Parent = L"RNWF Extensible Helper Class";
```

Die erweiterbare Hilfsklasse Revised Native Wifi (RNWF) ist das übergeordnete Element für Hilfsklassen von Drittanbietern, die Probleme im Zusammenhang mit der Erweiterung von 802.11-Protokollen diagnostizieren, die von Native Wifi verwendet werden.

Die beiden von der RNWF-Hilfsklasse bereitgestellten Schlüsselattribute sind die GUID der Schnittstelle, an der das Problem aufgetreten ist, und der Verbindungskontext.

-   Schnittstellen-GUID: Dieses Attribut heißt "Schnittstellen-ID" und hat den Typ **AT \_ GUID**.

-   Verbindungskontext: Dieses Attribut heißt Netzwerk-ID und hat den Typ AT \_ OCTET \_ STRING. Diese Zeichenfolge ist eigentlich ein Puffer der \_ \_ WDIAG-IHV-WLAN-ID-Struktur, \_ die in Wlanihv.h definiert ist. Diese Struktur ist wie folgt definiert.

    ``` syntax
#define WDIAG_IHV_WLAN_ID_FLAG_SECURITY_ENABLED               0x00000001
    typedef
    struct _WDIAG_IHV_WLAN_ID
    {
        WCHAR                        strProfileName [MS_MAX_PROFILE_NAME_LENGTH];
        DOT11_SSID                   Ssid;
        DOT11_BSS_TYPE               BssType;
        DWORD                        dwFlags;           // Flags defined above
        DWORD                        dwReasonCode;      // Set only when an applicable reason code is available
    }
    WDIAG_IHV_WLAN_ID, *PWDIAG_IHV_WLAN_ID;
    ```

> [!Note]  
> **WDIAG \_ IHV \_ WLAN ID FLAG SECURITY \_ \_ \_ \_ ENABLED** ist der einzige mögliche **dwFlags-Wert.**

 

Das übereinstimmende Attribut für die Hilfsklasse des Drittanbieters sollte mit der Dienst-ID des entsprechenden Softwaremoduls identisch sein. Dies ist auch derselbe Name, den der Drittanbieter in der Registrierung registrieren sollte. Bei der Drahtlosen Diagnose wird die Dienst-ID während der Funksitzung abgefragt, in der das Problem aufgetreten ist. Die Informationen werden an NDF zurückgegeben, wodurch bestimmt wird, ob die Hilfsklasse des Drittanbieters vorhanden und registriert ist, und dann aufgerufen wird.

In der folgenden Tabelle sind die übereinstimmenden Attribute für die erweiterbare HILFSKLASSE RNWF aufgeführt.



| Name          | Typ    | Wert                         |
|---------------|---------|-------------------------------|
| DiagnosticsID | REG \_ SZ | \[DiagnosticsID \_ GUID \_ String |



 

## <a name="l2security-extensible-helper-class"></a>L2Security Extensible Helper-Klasse

Name der übergeordneten Hilfsklasse

``` syntax
Parent = L"Extensible L2Sec Helper Class";
```

Die erweiterbare Hilfsklasse Layer 2 Security (L2Security) ist das übergeordnete Element für Hilfsklassen von Drittanbietern, die Probleme im Zusammenhang mit entsprechenden Diensten und Softwaremodulen diagnostizieren, die die Layer 2-Sicherheitsfunktionalität ersetzen.

Die beiden wichtigsten Attribute, die von der Layer 2-Sicherheitshilfsklasse bereitgestellt werden, sind die GUID der Schnittstelle, an der das Problem aufgetreten ist, und der Verbindungskontext.

-   Schnittstellen-GUID: Dieses Attribut heißt "Schnittstellen-ID" und hat den Typ **AT \_ GUID**.

-   Verbindungskontext: Dieses Attribut heißt Netzwerk-ID und hat den Typ AT \_ OCTET \_ STRING. Diese Zeichenfolge ist eigentlich ein Puffer der \_ \_ WDIAG-IHV-WLAN-ID-Struktur, \_ die in wlanihv.h definiert ist. Diese Struktur ist wie folgt definiert.

    ``` syntax
#define WDIAG_IHV_WLAN_ID_FLAG_SECURITY_ENABLED               0x00000001
    typedef
    struct _WDIAG_IHV_WLAN_ID
    {
        WCHAR                        strProfileName [MS_MAX_PROFILE_NAME_LENGTH];
        DOT11_SSID                   Ssid;
        DOT11_BSS_TYPE               BssType;
        DWORD                        dwFlags;           // Flags defined above
        DWORD                        dwReasonCode;      // Set only when an applicable reason code is available
    }
    WDIAG_IHV_WLAN_ID, *PWDIAG_IHV_WLAN_ID;
    ```

> [!Note]  
> **WDIAG \_ IHV \_ WLAN ID FLAG SECURITY \_ \_ \_ \_ ENABLED** ist der einzige mögliche **dwFlags-Wert.**

 

Das übereinstimmende Attribut für die Hilfsklasse des Drittanbieters sollte mit der Dienst-ID des entsprechenden Softwaremoduls identisch sein. Dies ist auch derselbe Name, den der Drittanbieter in der Registrierung registrieren sollte. Bei der Drahtlosen Diagnose wird die Dienst-ID während der Funksitzung abgefragt, in der das Problem aufgetreten ist. Die Informationen werden an NDF zurückgegeben, wodurch bestimmt wird, ob die Hilfsklasse des Drittanbieters vorhanden und registriert ist, und dann aufgerufen wird.

In der folgenden Tabelle sind die übereinstimmenden Attribute für die erweiterbare Layer 2 Security-Hilfsklasse aufgeführt.



| Name          | Typ    | Wert                         |
|---------------|---------|-------------------------------|
| DiagnosticsID | REG \_ SZ | \[DiagnosticsID \_ GUID \_ String |



 

## <a name="matching-attributes"></a>Übereinstimmende Attribute

**DiagnosticsID**

802.11 Wireless Diagnostics fragen die *DiagnosticsID* vom Native Wifi-Kerndienst ab, um herauszufinden, ob Drahtloserweiterungen oder Sicherheitsmodule von Drittanbietern installiert sind und an der Verbindung beteiligt sind. Die Drahtlose Diagnose stellt dann Hypothesen für diese Hilfsklassen von Drittanbietern bereit, indem die *DiagnosticsID* als übereinstimmendes Attribut verwendet wird. Alle Hilfsklassen von Drittanbietern sollten in das zugeordnete Treiberpaket eingeschlossen und mit diesem installiert werden. Die *DiagnosticsID* wird in der MINIPORT-INF-Datei als Registrierungsschlüssel in der [AddReg-Direktive](https://msdn.microsoft.com/library/ms794514.aspx) definiert.

``` syntax
HKR,Ndi\IHVExtensions, DiagnosticsID,0, "<Diagnostics ID GUID>"
```

Dieser Schlüssel definiert die ID der Drahtloshilfsklasse für das Drittanbietersoftwaremodul. Dieser Schlüssel ist für das Erweiterbarkeitsframework optional. Er ist jedoch erforderlich, wenn die Implementierung eine IHV Wireless Helper-Klasse enthält, die in NDF integriert ist und Konnektivitätsprobleme im Zusammenhang mit den FUNK- oder Sicherheitserweiterungen von RNWF diagnostizieren kann. MS WLAN-Diagnosehilfsklassen fragen diese ID vom Dienst für die automatische Drahtloskonfiguration ab, wenn IHV-Module installiert sind, und geben diese ID als Verweis- oder Abgleichsattribut für NDF während einer Diagnosesitzung an, damit NDF bei Bedarf die entsprechende Funkhilfsklasse eines Drittanbieters aufrufen kann.

**\[DiagnosticsID \_ GUID \_ String\]**

Dieser Wert muss eine Zeichenfolge aller Großbuchstaben sein. Beispiel: "{12345678-9ABC-DEF0-1234-56789ABCDEF0}".

## <a name="scope-of-80211-wireless-diagnostics-helper-classes"></a>Bereich von 802.11 Wireless Diagnostics Helper-Klassen

Hilfsklassen für die 802.11-Funkdiagnose diagnostizieren derzeit Drahtlose Probleme in den folgenden Bereichen.

-   Alle 802.11-Konnektivitätsprobleme, einschließlich 802.11-Zuordnung, 802.11-Authentifizierung, 802.11-Sicherheitseinstellungen im Zusammenhang mit 802.11-Standards & Protokollen, die nativ im Betriebssystem unterstützt werden, und Leistungsprobleme.
-   Sicherheitsprobleme der Ebene 2 in Bezug auf 802.1x-Konfigurationen und Probleme im Zusammenhang mit der Layer-2-Authentifizierung mit methoden, die auf Windows Vista und Windows Server 2008 nativ unterstützt werden.
-   Konfigurationskonflikte in den Profileinstellungen zwischen dem Client und dem Zugriffspunkt oder der Netzwerkinfrastruktur und den Diensten.

802.11 Wireless Diagnostics Helper-Klassen diagnostizieren derzeit keine Drahtlose Probleme in den folgenden Bereichen.

-   Probleme im Zusammenhang mit 802.11-Erweiterungen von Drittanbietern, einschließlich aller Profil- oder Treibereinstellungen im Zusammenhang mit diesen Erweiterungen.
-   Probleme im Zusammenhang mit EAP-Methoden von Drittanbietern.
-   Probleme mit dem Drahtlosen Miniporttreiber.
-   Alle 802.11- und Layer 2-Sicherheitsprotokoll- oder standardsbezogenen Probleme, die nicht nativ unterstützt werden.
-   Probleme auf System- oder Komponentenebene, die sich auf die Drahtloskonnektivität auswirken können, z. B. Energieverwaltung, wenig Speicherplatz, Arbeitsspeicherbedingungen und Hardwareprobleme.

Darüber hinaus analysiert die 802.11-Funkdiagnose keine [**HighUtilization-Fälle.**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-highutilization) Identifizierte Drahtlose Leistungsprobleme werden analysiert und als [**LowHealth-Fälle**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth) gemeldet.

 

 




