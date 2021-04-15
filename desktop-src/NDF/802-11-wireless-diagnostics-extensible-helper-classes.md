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
# <a name="80211-wireless-diagnostics-extensible-helper-classes"></a><span data-ttu-id="d3b75-103">802,11 erweiterbare Hilfsklassen für die drahtlose Diagnose</span><span class="sxs-lookup"><span data-stu-id="d3b75-103">802.11 Wireless Diagnostics Extensible Helper Classes</span></span>

<span data-ttu-id="d3b75-104">Die integrierte drahtlose Diagnose Infrastruktur verfügt über zwei Erweiterungs Punkte.</span><span class="sxs-lookup"><span data-stu-id="d3b75-104">The built-in wireless diagnostics infrastructure has two extension points.</span></span>

| <span data-ttu-id="d3b75-105">Übergeordnete Hilfsklasse</span><span class="sxs-lookup"><span data-stu-id="d3b75-105">Parent Helper Class</span></span>                                | <span data-ttu-id="d3b75-106">Zweck</span><span class="sxs-lookup"><span data-stu-id="d3b75-106">Purpose</span></span>                                                           |
|----------------------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="d3b75-107">Erweiterte systemeigene WiFi-Hilfsklasse (rnwf)</span><span class="sxs-lookup"><span data-stu-id="d3b75-107">Revised Native Wifi (RNWF) Extensible Helper Class</span></span> | <span data-ttu-id="d3b75-108">Diagnose von Problemen im Zusammenhang mit 802,11 konnektivitätserweiterungen</span><span class="sxs-lookup"><span data-stu-id="d3b75-108">Diagnoses issues related to 802.11 connectivity extensions.</span></span>       |
| <span data-ttu-id="d3b75-109">L2Security Extensible Helper-Klasse</span><span class="sxs-lookup"><span data-stu-id="d3b75-109">L2Security Extensible Helper Class</span></span>                 | <span data-ttu-id="d3b75-110">Diagnostizieren von Problemen im Zusammenhang mit Layer 2-Sicherheitsprotokoll Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="d3b75-110">Diagnoses issues related to Layer 2 security protocol extensions.</span></span> |



 

> [!Note]  
> <span data-ttu-id="d3b75-111">Eine Hilfsklasse von Drittanbietern sollte sich bei beiden übergeordneten Hilfsklassen registrieren, um sicherzustellen, dass die Drittanbieter Klasse aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d3b75-111">A third-party helper class should register with both parent helper classes to ensure that the third-party class gets called.</span></span> <span data-ttu-id="d3b75-112">Weitere Informationen zur Registrierung finden Sie unter [Registrieren von NDF-Hilfsklassen Erweiterungen](registering-ndf-helper-class-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="d3b75-112">For more information about registration, see [Registering NDF Helper Class Extensions](registering-ndf-helper-class-extensions.md).</span></span>

 

## <a name="rnwf-extensible-helper-class"></a><span data-ttu-id="d3b75-113">Rnwf Extensible Helper-Klasse</span><span class="sxs-lookup"><span data-stu-id="d3b75-113">RNWF Extensible Helper Class</span></span>

<span data-ttu-id="d3b75-114">Name der übergeordneten Hilfsklasse</span><span class="sxs-lookup"><span data-stu-id="d3b75-114">Parent Helper Class Name</span></span>

``` syntax
Parent = L"RNWF Extensible Helper Class";
```

<span data-ttu-id="d3b75-115">Die überarbeitete erweiterbare Hilfsklasse von System eigenem WiFi (rnwf) ist das übergeordnete Element für Hilfsklassen von Drittanbietern, die Probleme im Zusammenhang mit der Erweiterung von 802,11-Protokollen, die von nativem WiFi</span><span class="sxs-lookup"><span data-stu-id="d3b75-115">The Revised Native Wifi (RNWF) extensible helper class is the parent for third-party helper classes that diagnose issues related to extending 802.11 protocols used by Native Wifi.</span></span>

<span data-ttu-id="d3b75-116">Die zwei Schlüssel Attribute, die von der rnwf-Hilfsklasse bereitgestellt werden, sind die GUID der Schnittstelle, auf der das Problem aufgetreten ist, und der Verbindungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="d3b75-116">The two key attributes provided by the RNWF helper class are the GUID of the interface where the issue occurred, and the connection context.</span></span>

-   <span data-ttu-id="d3b75-117">Schnittstellen-GUID: dieses Attribut hat den Namen "Interface ID" und ist vom Typ " **\_ GUID**".</span><span class="sxs-lookup"><span data-stu-id="d3b75-117">Interface GUID: This attribute is named "Interface ID" and is of type **AT\_GUID**.</span></span>

-   <span data-ttu-id="d3b75-118">Verbindungs Kontext: dieses Attribut heißt Netzwerk-ID und weist den Typ bei der \_ Oktett- \_ Zeichenfolge auf.</span><span class="sxs-lookup"><span data-stu-id="d3b75-118">Connection Context: This attribute is named Network ID and is of type AT\_OCTET\_STRING.</span></span> <span data-ttu-id="d3b75-119">Bei dieser Zeichenfolge handelt es sich tatsächlich um einen Puffer der \_ \_ \_ in wlanihv. h definierten wdiag IHV-WLAN-ID-Struktur.</span><span class="sxs-lookup"><span data-stu-id="d3b75-119">This string is actually a buffer the WDIAG\_IHV\_WLAN\_ID structure defined in Wlanihv.h.</span></span> <span data-ttu-id="d3b75-120">Diese Struktur wird wie folgt definiert.</span><span class="sxs-lookup"><span data-stu-id="d3b75-120">This structure is defined as follows.</span></span>

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
> <span data-ttu-id="d3b75-121">**Wdiag \_ Die \_ \_ \_ \_ Sicherheits \_ aktivierte IHV-WLAN-ID-Flag** ist der einzige mögliche **dwFlags** -Wert.</span><span class="sxs-lookup"><span data-stu-id="d3b75-121">**WDIAG\_IHV\_WLAN\_ID\_FLAG\_SECURITY\_ENABLED** is the only possible **dwFlags** value.</span></span>

 

<span data-ttu-id="d3b75-122">Das übereinstimmende Attribut für die Hilfsklasse von Drittanbietern sollte mit der Dienst-ID des entsprechenden Software Moduls identisch sein.</span><span class="sxs-lookup"><span data-stu-id="d3b75-122">The matching attribute for the third-party helper class should be the same as its corresponding software module's service ID.</span></span> <span data-ttu-id="d3b75-123">Dies ist auch derselbe Name, den der Drittanbieter in der Registrierung registrieren sollte.</span><span class="sxs-lookup"><span data-stu-id="d3b75-123">This is also the same name the third-party should be registered in the registry.</span></span> <span data-ttu-id="d3b75-124">Bei der drahtlos Diagnose wird die Dienst-ID während der drahtlos Sitzung abgefragt, in der das Problem aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="d3b75-124">Wireless diagnostics will query the service ID during the wireless session in which the issue occurred.</span></span> <span data-ttu-id="d3b75-125">Die Informationen werden an das NDF zurückgegeben, das bestimmt, ob die Hilfsklasse von Drittanbietern vorhanden und registriert ist, und ruft Sie dann auf.</span><span class="sxs-lookup"><span data-stu-id="d3b75-125">The information will be returned to NDF, which will determine whether the third-party helper class is present and registered, and then call it.</span></span>

<span data-ttu-id="d3b75-126">In der folgenden Tabelle sind die übereinstimmenden Attribute für die Extensible Helper-Klasse von rnwf aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d3b75-126">The following table lists the matching attributes for the RNWF extensible helper class.</span></span>



| <span data-ttu-id="d3b75-127">Name</span><span class="sxs-lookup"><span data-stu-id="d3b75-127">Name</span></span>          | <span data-ttu-id="d3b75-128">type</span><span class="sxs-lookup"><span data-stu-id="d3b75-128">Type</span></span>    | <span data-ttu-id="d3b75-129">Wert</span><span class="sxs-lookup"><span data-stu-id="d3b75-129">Value</span></span>                         |
|---------------|---------|-------------------------------|
| <span data-ttu-id="d3b75-130">Diagnosticsid</span><span class="sxs-lookup"><span data-stu-id="d3b75-130">DiagnosticsID</span></span> | <span data-ttu-id="d3b75-131">REG- \_ SZ</span><span class="sxs-lookup"><span data-stu-id="d3b75-131">REG\_SZ</span></span> | <span data-ttu-id="d3b75-132">\[Diagnosticsid- \_ GUID- \_ Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d3b75-132">\[DiagnosticsID\_GUID\_String</span></span> |



 

## <a name="l2security-extensible-helper-class"></a><span data-ttu-id="d3b75-133">L2Security Extensible Helper-Klasse</span><span class="sxs-lookup"><span data-stu-id="d3b75-133">L2Security Extensible Helper Class</span></span>

<span data-ttu-id="d3b75-134">Name der übergeordneten Hilfsklasse</span><span class="sxs-lookup"><span data-stu-id="d3b75-134">Parent Helper Class Name</span></span>

``` syntax
Parent = L"Extensible L2Sec Helper Class";
```

<span data-ttu-id="d3b75-135">Die erweiterbare Hilfsklasse Layer 2 (L2Security) ist das übergeordnete Element von Hilfsklassen von Drittanbietern, die Probleme im Zusammenhang mit entsprechenden Diensten und Softwaremodulen diagnostizieren, die die Sicherheitsfunktionen von Layer 2 ersetzen.</span><span class="sxs-lookup"><span data-stu-id="d3b75-135">The Layer 2 Security (L2Security) extensible helper class is the parent for third-party helper classes that diagnose issues related to corresponding services and software modules that replace Layer 2 Security functionality.</span></span>

<span data-ttu-id="d3b75-136">Die zwei Schlüssel Attribute, die von der Sicherheits Hilfsklasse Layer 2 bereitgestellt werden, sind die GUID der Schnittstelle, in der das Problem aufgetreten ist, und der Verbindungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="d3b75-136">The two key attributes provided by the Layer 2 Security helper class are the GUID of the interface where the issue occurred, and the connection context.</span></span>

-   <span data-ttu-id="d3b75-137">Schnittstellen-GUID: dieses Attribut hat den Namen "Interface ID" und ist vom Typ " **\_ GUID**".</span><span class="sxs-lookup"><span data-stu-id="d3b75-137">Interface GUID: This attribute is named "Interface ID" and is of type **AT\_GUID**.</span></span>

-   <span data-ttu-id="d3b75-138">Verbindungs Kontext: dieses Attribut heißt Netzwerk-ID und weist den Typ bei der \_ Oktett- \_ Zeichenfolge auf.</span><span class="sxs-lookup"><span data-stu-id="d3b75-138">Connection Context: This attribute is named Network ID and is of type AT\_OCTET\_STRING.</span></span> <span data-ttu-id="d3b75-139">Bei dieser Zeichenfolge handelt es sich tatsächlich um einen Puffer der \_ \_ \_ in wlanihv. h definierten wdiag IHV-WLAN-ID-Struktur.</span><span class="sxs-lookup"><span data-stu-id="d3b75-139">This string is actually a buffer the WDIAG\_IHV\_WLAN\_ID structure defined in wlanihv.h.</span></span> <span data-ttu-id="d3b75-140">Diese Struktur wird wie folgt definiert.</span><span class="sxs-lookup"><span data-stu-id="d3b75-140">This structure is defined as follows.</span></span>

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
> <span data-ttu-id="d3b75-141">**Wdiag \_ Die \_ \_ \_ \_ Sicherheits \_ aktivierte IHV-WLAN-ID-Flag** ist der einzige mögliche **dwFlags** -Wert.</span><span class="sxs-lookup"><span data-stu-id="d3b75-141">**WDIAG\_IHV\_WLAN\_ID\_FLAG\_SECURITY\_ENABLED** is the only possible **dwFlags** value.</span></span>

 

<span data-ttu-id="d3b75-142">Das übereinstimmende Attribut für die Hilfsklasse von Drittanbietern sollte mit der Dienst-ID des entsprechenden Software Moduls identisch sein.</span><span class="sxs-lookup"><span data-stu-id="d3b75-142">The matching attribute for the third-party helper class should be the same as its corresponding software module's service ID.</span></span> <span data-ttu-id="d3b75-143">Dies ist auch derselbe Name, den der Drittanbieter in der Registrierung registrieren sollte.</span><span class="sxs-lookup"><span data-stu-id="d3b75-143">This is also the same name the third-party should be registered in the registry.</span></span> <span data-ttu-id="d3b75-144">Bei der drahtlos Diagnose wird die Dienst-ID während der drahtlos Sitzung abgefragt, in der das Problem aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="d3b75-144">Wireless diagnostics will query the service ID during the wireless session in which the issue occurred.</span></span> <span data-ttu-id="d3b75-145">Die Informationen werden an das NDF zurückgegeben, das bestimmt, ob die Hilfsklasse von Drittanbietern vorhanden und registriert ist, und ruft Sie dann auf.</span><span class="sxs-lookup"><span data-stu-id="d3b75-145">The information will be returned to NDF, which will determine whether the third-party helper class is present and registered, and then call it.</span></span>

<span data-ttu-id="d3b75-146">In der folgenden Tabelle werden die übereinstimmenden Attribute für die Sicherheits erweiterbare Hilfsklasse Layer 2 aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d3b75-146">The following table lists the matching attributes for the Layer 2 Security extensible helper class.</span></span>



| <span data-ttu-id="d3b75-147">Name</span><span class="sxs-lookup"><span data-stu-id="d3b75-147">Name</span></span>          | <span data-ttu-id="d3b75-148">type</span><span class="sxs-lookup"><span data-stu-id="d3b75-148">Type</span></span>    | <span data-ttu-id="d3b75-149">Wert</span><span class="sxs-lookup"><span data-stu-id="d3b75-149">Value</span></span>                         |
|---------------|---------|-------------------------------|
| <span data-ttu-id="d3b75-150">Diagnosticsid</span><span class="sxs-lookup"><span data-stu-id="d3b75-150">DiagnosticsID</span></span> | <span data-ttu-id="d3b75-151">REG- \_ SZ</span><span class="sxs-lookup"><span data-stu-id="d3b75-151">REG\_SZ</span></span> | <span data-ttu-id="d3b75-152">\[Diagnosticsid- \_ GUID- \_ Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d3b75-152">\[DiagnosticsID\_GUID\_String</span></span> |



 

## <a name="matching-attributes"></a><span data-ttu-id="d3b75-153">Übereinstimmende Attribute</span><span class="sxs-lookup"><span data-stu-id="d3b75-153">Matching Attributes</span></span>

<span data-ttu-id="d3b75-154">**Diagnosticsid**</span><span class="sxs-lookup"><span data-stu-id="d3b75-154">**DiagnosticsID**</span></span>

<span data-ttu-id="d3b75-155">802,11 bei der drahtlosen Diagnose wird die *diagnosticsid* vom zentralen systemeigenen WiFi-Dienst abgefragt, um herauszufinden, ob drahtlos Erweiterungen oder Sicherheitsmodule von Drittanbietern installiert sind und an der Verbindung beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="d3b75-155">802.11 Wireless Diagnostics will query the *DiagnosticsID* from the core Native Wifi service in order to find out if any third-party wireless extensions or security modules are installed and involved in the connection.</span></span> <span data-ttu-id="d3b75-156">Die drahtlose Diagnose stellt dann mithilfe der *diagnosticsid* als übereinstimmendes Attribut Hypothese für diese Hilfsklassen von Drittanbietern bereit.</span><span class="sxs-lookup"><span data-stu-id="d3b75-156">Wireless Diagnostics will then provide hypotheses to these third-party helper classes using the *DiagnosticsID* as the matching attribute.</span></span> <span data-ttu-id="d3b75-157">Alle Hilfsklassen von Drittanbietern sollten in das zugehörige Treiber Paket eingeschlossen und dort installiert werden.</span><span class="sxs-lookup"><span data-stu-id="d3b75-157">Any third-party helper classes should be included in and installed with the associated driver package.</span></span> <span data-ttu-id="d3b75-158">Die *diagnosticsid* wird in der Mini Port-INF-Datei als Registrierungsschlüssel in der " [adressg](https://msdn.microsoft.com/library/ms794514.aspx) "-Direktive definiert.</span><span class="sxs-lookup"><span data-stu-id="d3b75-158">The *DiagnosticsID* will be defined in the miniport INF file as a registry key in the [AddReg](https://msdn.microsoft.com/library/ms794514.aspx) directive.</span></span>

``` syntax
HKR,Ndi\IHVExtensions, DiagnosticsID,0, "<Diagnostics ID GUID>"
```

<span data-ttu-id="d3b75-159">Dieser Schlüssel definiert die ID der drahtlosen Hilfsklasse für das Drittanbieter-Softwaremodul.</span><span class="sxs-lookup"><span data-stu-id="d3b75-159">This key defines the ID of the wireless helper class for the third-party software module.</span></span> <span data-ttu-id="d3b75-160">Dieser Schlüssel ist für das Erweiterbarkeit Framework optional. er ist jedoch erforderlich, wenn die Implementierung eine von IHV drahtlose Hilfsklasse enthält, die in NDF eingebunden ist und Konnektivitätsprobleme im Zusammenhang mit den rnwf-drahtlos-oder-Sicherheitserweiterungen diagnostizieren kann.</span><span class="sxs-lookup"><span data-stu-id="d3b75-160">This key is optional for the extensibility framework, but it is needed if the implementation includes an IHV Wireless Helper Class that plugs into NDF and can diagnose connectivity problems related to the RNWF wireless or security extensions.</span></span> <span data-ttu-id="d3b75-161">MS WLAN-diagnosehilfsobjekte Fragen diese ID aus dem drahtlosen automatischen Konfigurations Dienst ab, wenn IHV-Module installiert sind, und geben diese ID während einer Diagnose Sitzung als Verweis-oder abgleichsattribut für NDF an, sodass NDF bei Bedarf die geeignete drahtlos Hilfsklasse von Drittanbietern abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="d3b75-161">MS WLAN diagnostics helper classes will query this ID from the Wireless Auto Configuration Service when IHV modules are installed and will provide this ID as the reference or matching attribute to NDF during a diagnostics session so that NDF can call the appropriate third-party wireless helper class when necessary.</span></span>

<span data-ttu-id="d3b75-162">**\[Diagnosticsid- \_ GUID- \_ Zeichenfolge\]**</span><span class="sxs-lookup"><span data-stu-id="d3b75-162">**\[DiagnosticsID\_GUID\_String\]**</span></span>

<span data-ttu-id="d3b75-163">Dieser Wert muss eine Zeichenfolge aller Großbuchstaben sein.</span><span class="sxs-lookup"><span data-stu-id="d3b75-163">This value must be a string of all uppercase letters.</span></span> <span data-ttu-id="d3b75-164">Beispiel: "{12345678-9abc-def0-1234-56789abcdef0}".</span><span class="sxs-lookup"><span data-stu-id="d3b75-164">For example, "{12345678-9ABC-DEF0-1234-56789ABCDEF0}".</span></span>

## <a name="scope-of-80211-wireless-diagnostics-helper-classes"></a><span data-ttu-id="d3b75-165">Bereich von 802,11-Hilfsklassen für die drahtlose Diagnose</span><span class="sxs-lookup"><span data-stu-id="d3b75-165">Scope of 802.11 Wireless Diagnostics Helper Classes</span></span>

<span data-ttu-id="d3b75-166">802,11-Hilfsklassen für die drahtlose Diagnose diagnostizieren derzeit drahtlose Probleme in den folgenden Bereichen.</span><span class="sxs-lookup"><span data-stu-id="d3b75-166">802.11 wireless diagnostics helper classes currently diagnose wireless issues in the following areas.</span></span>

-   <span data-ttu-id="d3b75-167">Alle 802,11 Konnektivitätsprobleme einschließlich der 802,11-Zuordnung, 802,11-Authentifizierung, 802,11-Sicherheitseinstellungen im Zusammenhang mit 802,11-Standards & im Betriebssystem System intern unterstützten Protokollen und Leistungsprobleme.</span><span class="sxs-lookup"><span data-stu-id="d3b75-167">Any 802.11 connectivity issues including 802.11 association, 802.11 authentication, 802.11 security settings related to 802.11 standards & protocols natively supported in the operating system, and performance issues.</span></span>
-   <span data-ttu-id="d3b75-168">Layer 2-Sicherheitsprobleme im Hinblick auf 802.1 x-Konfigurationen und alle Probleme im Zusammenhang mit der Layer 2-Authentifizierung mithilfe von Methoden, die nativ unter Windows Vista und Windows Server 2008 unterstützt werden</span><span class="sxs-lookup"><span data-stu-id="d3b75-168">Layer 2 Security issues with regards to 802.1x configurations and any issues related to layer 2 authentication using methods natively supported on Windows Vista and Windows Server 2008.</span></span>
-   <span data-ttu-id="d3b75-169">Konfigurations Konflikte in den Profileinstellungen zwischen dem Client und dem Zugriffspunkt oder der Netzwerkinfrastruktur und den Diensten.</span><span class="sxs-lookup"><span data-stu-id="d3b75-169">Configuration mismatches in profile settings between the client and the Access Point or the network infrastructure and services.</span></span>

<span data-ttu-id="d3b75-170">802,11 die Hilfsklassen für die drahtlose Diagnose untersuchen derzeit keine drahtlos Probleme in den folgenden Bereichen.</span><span class="sxs-lookup"><span data-stu-id="d3b75-170">802.11 wireless diagnostics helper classes currently do not diagnose wireless issues in the following areas.</span></span>

-   <span data-ttu-id="d3b75-171">Probleme im Zusammenhang mit 802,11-Erweiterungen von Drittanbietern, einschließlich Profil-oder Treibereinstellungen in Bezug auf diese Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="d3b75-171">Issues related to third-party 802.11 extensions including any profile or driver settings related to these extensions.</span></span>
-   <span data-ttu-id="d3b75-172">Probleme im Zusammenhang mit EAP-Methoden von Drittanbietern.</span><span class="sxs-lookup"><span data-stu-id="d3b75-172">Issues related to third-party EAP methods.</span></span>
-   <span data-ttu-id="d3b75-173">Probleme bei drahtlosen Mini portieren.</span><span class="sxs-lookup"><span data-stu-id="d3b75-173">Wireless miniport driver issues.</span></span>
-   <span data-ttu-id="d3b75-174">Alle 802,11-und Layer 2-Sicherheitsprotokolle oder Standard bezogenen Probleme, die nicht nativ unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="d3b75-174">Any 802.11 and layer 2 security protocol or standards-related issues that are not natively supported.</span></span>
-   <span data-ttu-id="d3b75-175">Probleme auf System-oder Komponentenebene, die sich auf die drahtlose Konnektivität auswirken können, wie z. b. Energie Verwaltung, wenig Speicherplatz, Arbeitsspeicher und Hardwareprobleme.</span><span class="sxs-lookup"><span data-stu-id="d3b75-175">System or component-level issues that might impact wireless connectivity, such as power management, low disk space, memory conditions, and hardware problems.</span></span>

<span data-ttu-id="d3b75-176">Darüber hinaus analysiert die drahtlose Diagnose 802,11 keine [**highauslastungs**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-highutilization) Fälle.</span><span class="sxs-lookup"><span data-stu-id="d3b75-176">Additionally, 802.11 Wireless Diagnostics does not analyze [**HighUtilization**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-highutilization) cases.</span></span> <span data-ttu-id="d3b75-177">Identifizierte Probleme mit der drahtlos Leistung werden analysiert und als [**lowhealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth) -Fälle gemeldet.</span><span class="sxs-lookup"><span data-stu-id="d3b75-177">Identified wireless performance issues will be analyzed and reported as [**LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth) cases.</span></span>

 

 




