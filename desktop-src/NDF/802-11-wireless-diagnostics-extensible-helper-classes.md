---
title: 802,11 erweiterbare Hilfsklassen für die drahtlose Diagnose
description: Die integrierte drahtlose Diagnose Infrastruktur verfügt über zwei Erweiterungs Punkte. Das übergeordnete Hilfsprogramm classpurposerevised Native WiFi (rnwf) erweiterbare Hilfsobjekte, die mit 802,11-konnektivitätserweiterungen verknüpft sind.
ms.assetid: b54f836d-4fae-4e71-bf7b-af5a6e9e615c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bde49561c68044157c9d518571b8241c49dcf25
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104516634"
---
# <a name="80211-wireless-diagnostics-extensible-helper-classes"></a>802,11 erweiterbare Hilfsklassen für die drahtlose Diagnose

Die integrierte drahtlose Diagnose Infrastruktur verfügt über zwei Erweiterungs Punkte.

| Übergeordnete Hilfsklasse                                | Zweck                                                           |
|----------------------------------------------------|-------------------------------------------------------------------|
| Erweiterte systemeigene WiFi-Hilfsklasse (rnwf) | Diagnose von Problemen im Zusammenhang mit 802,11 konnektivitätserweiterungen       |
| L2Security Extensible Helper-Klasse                 | Diagnostizieren von Problemen im Zusammenhang mit Layer 2-Sicherheitsprotokoll Erweiterungen. |



 

> [!Note]  
> Eine Hilfsklasse von Drittanbietern sollte sich bei beiden übergeordneten Hilfsklassen registrieren, um sicherzustellen, dass die Drittanbieter Klasse aufgerufen wird. Weitere Informationen zur Registrierung finden Sie unter [Registrieren von NDF-Hilfsklassen Erweiterungen](registering-ndf-helper-class-extensions.md).

 

## <a name="rnwf-extensible-helper-class"></a>Rnwf Extensible Helper-Klasse

Name der übergeordneten Hilfsklasse

``` syntax
Parent = L"RNWF Extensible Helper Class";
```

Die überarbeitete erweiterbare Hilfsklasse von System eigenem WiFi (rnwf) ist das übergeordnete Element für Hilfsklassen von Drittanbietern, die Probleme im Zusammenhang mit der Erweiterung von 802,11-Protokollen, die von nativem WiFi

Die zwei Schlüssel Attribute, die von der rnwf-Hilfsklasse bereitgestellt werden, sind die GUID der Schnittstelle, auf der das Problem aufgetreten ist, und der Verbindungs Kontext.

-   Schnittstellen-GUID: dieses Attribut hat den Namen "Interface ID" und ist vom Typ " **\_ GUID**".

-   Verbindungs Kontext: dieses Attribut heißt Netzwerk-ID und weist den Typ bei der \_ Oktett- \_ Zeichenfolge auf. Bei dieser Zeichenfolge handelt es sich tatsächlich um einen Puffer der \_ \_ \_ in wlanihv. h definierten wdiag IHV-WLAN-ID-Struktur. Diese Struktur wird wie folgt definiert.

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
> **Wdiag \_ Die \_ \_ \_ \_ Sicherheits \_ aktivierte IHV-WLAN-ID-Flag** ist der einzige mögliche **dwFlags** -Wert.

 

Das übereinstimmende Attribut für die Hilfsklasse von Drittanbietern sollte mit der Dienst-ID des entsprechenden Software Moduls identisch sein. Dies ist auch derselbe Name, den der Drittanbieter in der Registrierung registrieren sollte. Bei der drahtlos Diagnose wird die Dienst-ID während der drahtlos Sitzung abgefragt, in der das Problem aufgetreten ist. Die Informationen werden an das NDF zurückgegeben, das bestimmt, ob die Hilfsklasse von Drittanbietern vorhanden und registriert ist, und ruft Sie dann auf.

In der folgenden Tabelle sind die übereinstimmenden Attribute für die Extensible Helper-Klasse von rnwf aufgeführt.



| Name          | type    | Wert                         |
|---------------|---------|-------------------------------|
| Diagnosticsid | REG- \_ SZ | \[Diagnosticsid- \_ GUID- \_ Zeichenfolge |



 

## <a name="l2security-extensible-helper-class"></a>L2Security Extensible Helper-Klasse

Name der übergeordneten Hilfsklasse

``` syntax
Parent = L"Extensible L2Sec Helper Class";
```

Die erweiterbare Hilfsklasse Layer 2 (L2Security) ist das übergeordnete Element von Hilfsklassen von Drittanbietern, die Probleme im Zusammenhang mit entsprechenden Diensten und Softwaremodulen diagnostizieren, die die Sicherheitsfunktionen von Layer 2 ersetzen.

Die zwei Schlüssel Attribute, die von der Sicherheits Hilfsklasse Layer 2 bereitgestellt werden, sind die GUID der Schnittstelle, in der das Problem aufgetreten ist, und der Verbindungs Kontext.

-   Schnittstellen-GUID: dieses Attribut hat den Namen "Interface ID" und ist vom Typ " **\_ GUID**".

-   Verbindungs Kontext: dieses Attribut heißt Netzwerk-ID und weist den Typ bei der \_ Oktett- \_ Zeichenfolge auf. Bei dieser Zeichenfolge handelt es sich tatsächlich um einen Puffer der \_ \_ \_ in wlanihv. h definierten wdiag IHV-WLAN-ID-Struktur. Diese Struktur wird wie folgt definiert.

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
> **Wdiag \_ Die \_ \_ \_ \_ Sicherheits \_ aktivierte IHV-WLAN-ID-Flag** ist der einzige mögliche **dwFlags** -Wert.

 

Das übereinstimmende Attribut für die Hilfsklasse von Drittanbietern sollte mit der Dienst-ID des entsprechenden Software Moduls identisch sein. Dies ist auch derselbe Name, den der Drittanbieter in der Registrierung registrieren sollte. Bei der drahtlos Diagnose wird die Dienst-ID während der drahtlos Sitzung abgefragt, in der das Problem aufgetreten ist. Die Informationen werden an das NDF zurückgegeben, das bestimmt, ob die Hilfsklasse von Drittanbietern vorhanden und registriert ist, und ruft Sie dann auf.

In der folgenden Tabelle werden die übereinstimmenden Attribute für die Sicherheits erweiterbare Hilfsklasse Layer 2 aufgelistet.



| Name          | type    | Wert                         |
|---------------|---------|-------------------------------|
| Diagnosticsid | REG- \_ SZ | \[Diagnosticsid- \_ GUID- \_ Zeichenfolge |



 

## <a name="matching-attributes"></a>Übereinstimmende Attribute

**Diagnosticsid**

802,11 bei der drahtlosen Diagnose wird die *diagnosticsid* vom zentralen systemeigenen WiFi-Dienst abgefragt, um herauszufinden, ob drahtlos Erweiterungen oder Sicherheitsmodule von Drittanbietern installiert sind und an der Verbindung beteiligt sind. Die drahtlose Diagnose stellt dann mithilfe der *diagnosticsid* als übereinstimmendes Attribut Hypothese für diese Hilfsklassen von Drittanbietern bereit. Alle Hilfsklassen von Drittanbietern sollten in das zugehörige Treiber Paket eingeschlossen und dort installiert werden. Die *diagnosticsid* wird in der Mini Port-INF-Datei als Registrierungsschlüssel in der " [adressg](https://msdn.microsoft.com/library/ms794514.aspx) "-Direktive definiert.

``` syntax
HKR,Ndi\IHVExtensions, DiagnosticsID,0, "<Diagnostics ID GUID>"
```

Dieser Schlüssel definiert die ID der drahtlosen Hilfsklasse für das Drittanbieter-Softwaremodul. Dieser Schlüssel ist für das Erweiterbarkeit Framework optional. er ist jedoch erforderlich, wenn die Implementierung eine von IHV drahtlose Hilfsklasse enthält, die in NDF eingebunden ist und Konnektivitätsprobleme im Zusammenhang mit den rnwf-drahtlos-oder-Sicherheitserweiterungen diagnostizieren kann. MS WLAN-diagnosehilfsobjekte Fragen diese ID aus dem drahtlosen automatischen Konfigurations Dienst ab, wenn IHV-Module installiert sind, und geben diese ID während einer Diagnose Sitzung als Verweis-oder abgleichsattribut für NDF an, sodass NDF bei Bedarf die geeignete drahtlos Hilfsklasse von Drittanbietern abrufen kann.

**\[Diagnosticsid- \_ GUID- \_ Zeichenfolge\]**

Dieser Wert muss eine Zeichenfolge aller Großbuchstaben sein. Beispiel: "{12345678-9abc-def0-1234-56789abcdef0}".

## <a name="scope-of-80211-wireless-diagnostics-helper-classes"></a>Bereich von 802,11-Hilfsklassen für die drahtlose Diagnose

802,11-Hilfsklassen für die drahtlose Diagnose diagnostizieren derzeit drahtlose Probleme in den folgenden Bereichen.

-   Alle 802,11 Konnektivitätsprobleme einschließlich der 802,11-Zuordnung, 802,11-Authentifizierung, 802,11-Sicherheitseinstellungen im Zusammenhang mit 802,11-Standards & im Betriebssystem System intern unterstützten Protokollen und Leistungsprobleme.
-   Layer 2-Sicherheitsprobleme im Hinblick auf 802.1 x-Konfigurationen und alle Probleme im Zusammenhang mit der Layer 2-Authentifizierung mithilfe von Methoden, die nativ unter Windows Vista und Windows Server 2008 unterstützt werden
-   Konfigurations Konflikte in den Profileinstellungen zwischen dem Client und dem Zugriffspunkt oder der Netzwerkinfrastruktur und den Diensten.

802,11 die Hilfsklassen für die drahtlose Diagnose untersuchen derzeit keine drahtlos Probleme in den folgenden Bereichen.

-   Probleme im Zusammenhang mit 802,11-Erweiterungen von Drittanbietern, einschließlich Profil-oder Treibereinstellungen in Bezug auf diese Erweiterungen.
-   Probleme im Zusammenhang mit EAP-Methoden von Drittanbietern.
-   Probleme bei drahtlosen Mini portieren.
-   Alle 802,11-und Layer 2-Sicherheitsprotokolle oder Standard bezogenen Probleme, die nicht nativ unterstützt werden.
-   Probleme auf System-oder Komponentenebene, die sich auf die drahtlose Konnektivität auswirken können, wie z. b. Energie Verwaltung, wenig Speicherplatz, Arbeitsspeicher und Hardwareprobleme.

Darüber hinaus analysiert die drahtlose Diagnose 802,11 keine [**highauslastungs**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-highutilization) Fälle. Identifizierte Probleme mit der drahtlos Leistung werden analysiert und als [**lowhealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth) -Fälle gemeldet.

 

 




