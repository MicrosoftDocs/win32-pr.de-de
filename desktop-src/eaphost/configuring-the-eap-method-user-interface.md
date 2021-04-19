---
title: Konfigurieren der Benutzeroberfläche der EAP-Methode
description: Erläutert das Konfigurieren des Supplicant durch Bereitstellen einer EAP-Methoden Konfiguration für EAPHost.
ms.assetid: f6a23201-e221-4098-863f-71a81735d927
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9b82debadc075b1fcc12dad06484c0fd3617874
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "106341907"
---
# <a name="configuring-the-eap-method-user-interface"></a><span data-ttu-id="d0248-103">Konfigurieren der Benutzeroberfläche der EAP-Methode</span><span class="sxs-lookup"><span data-stu-id="d0248-103">Configuring the EAP Method User Interface</span></span>

<span data-ttu-id="d0248-104">In diesem Thema wird erläutert, wie Sie den Supplicant konfigurieren, indem Sie EAPHost eine EAP-Methoden Konfiguration bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d0248-104">This topic explains how to configure the supplicant by supplying an EAP method configuration to EAPHost.</span></span>

<span data-ttu-id="d0248-105">Damit ein Supplicant eine EAP-basierte Authentifizierung mithilfe von EAPHost ausführen kann, muss ein Supplicant eine EAP-Methoden Konfiguration für EAPHost über die [**eaphostpeerbeginsession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) -Funktion bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d0248-105">For a supplicant to perform an EAP-based authentication using EAPHost, a supplicant must supply an EAP method configuration to EAPHost through the [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) function.</span></span>

1.  <span data-ttu-id="d0248-106">Um die EAP-Methoden Konfiguration zu erhalten, fragt ein Supplicant in der Regel EAPHost mithilfe von [**eaphostpeergetmethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) ab, um den gesamten Satz von EAP-Methoden zu erlernen, die auf dem lokalen Computer verfügbar und installiert sind.</span><span class="sxs-lookup"><span data-stu-id="d0248-106">To obtain the EAP method configuration, a supplicant typically queries EAPHost using [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) to learn the complete set of EAP methods that are available and installed on the local machine.</span></span> <span data-ttu-id="d0248-107">Die Liste der Methoden wird dem Benutzer in der Regel in einem Kombinations Feld oder einem anderen UI-Steuerelement angezeigt, das es dem Benutzer ermöglicht, die gewünschte Methode auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="d0248-107">The list of methods is typically presented to the user in a combination box or other UI control that allows the user to select the method they want.</span></span>
    > [!Note]  
    > <span data-ttu-id="d0248-108">Der Supplicant kann die angezeigte Liste der Methoden basierend auf den in der **EAP-Methoden \_ \_ Info. eapproperties** angezeigten Methoden Eigenschaften Bits filtern.</span><span class="sxs-lookup"><span data-stu-id="d0248-108">The supplicant may choose to filter the displayed list of methods based on the method property bits indicated in **EAP\_METHOD\_INFO.eapProperties**.</span></span> <span data-ttu-id="d0248-109">Einige Methoden sind möglicherweise nicht für die Sicherheitsmerkmale des vom Supplicant bereitgestellten Transports geeignet.</span><span class="sxs-lookup"><span data-stu-id="d0248-109">Some methods may not be appropriate for the security characteristics of the transport provided by the supplicant, for example.</span></span>

     

2.  <span data-ttu-id="d0248-110">Sobald das UI-Steuerelement mit dem Satz möglicher EAP-Methoden aufgefüllt ist, wählt der Benutzer die Methode aus, die Sie konfigurieren möchten.</span><span class="sxs-lookup"><span data-stu-id="d0248-110">Once the UI control is populated with the set of possible EAP methods, the user selects the method they want to configure.</span></span> <span data-ttu-id="d0248-111">In der Regel stellt der Supplicant eine **Konfigurations** -oder **Eigenschaften** Schaltfläche bereit, damit der Benutzer auf die Konfigurations Eigenschaften der ausgewählten EAP-Methode zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="d0248-111">Typically, the supplicant provides a **Configuration** or **Properties** button for the user to access configuration properties of the selected EAP method.</span></span>
    > [!Note]
    > <span data-ttu-id="d0248-112">Der Supplicant weiß, dass es vom benutzerkonfigurierbare Eigenschaften gibt, die auf dem in den **EAP-Methoden Info (EAP- \_ Methoden \_ Info**) aktivierten **eappropsupportsconfig** -Bit basieren.</span><span class="sxs-lookup"><span data-stu-id="d0248-112">The supplicant is aware that there are user-configurable properties based on the **eapPropSupportsConfig** bit being enabled in **EAP\_METHOD\_INFO.eapProperties**.</span></span>
    >
    > <span data-ttu-id="d0248-113">Weitere Informationen finden Sie unter [**Eigenschaften der EAP-Methode**](eap-method-properties.md).</span><span class="sxs-lookup"><span data-stu-id="d0248-113">For more information, see [**EAP Method Properties**](eap-method-properties.md).</span></span>

     

3.  <span data-ttu-id="d0248-114">Wenn der Benutzer auf das entsprechende UI-Steuerelement klickt, ruft der Supplicant [**eaphostpeerinvokeconfigui**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui)auf und übergibt an die Funktion den **HWND** -Wert für die eigene Benutzeroberfläche des Supplicant, die [**EAP- \_ \_ Methodentyp**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) Struktur, die von der Abfrage an die [**EAP- \_ Methoden \_ Informations**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info) Struktur und andere erforderliche Parameter abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d0248-114">When the user clicks the appropriate UI control, the supplicant calls [**EapHostPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui), passing into the function the **HWND** value for the supplicant's own UI, the [**EAP\_METHOD\_TYPE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) structure obtained from the query to [**EAP\_METHOD\_INFO**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info) structure and other required parameters.</span></span>
4.  <span data-ttu-id="d0248-115">Durch Aufrufen von [**eaphostpeerinvokeconfigui**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui) wird die eigene Konfigurations Benutzeroberfläche einer EAP-Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="d0248-115">Calling [**EapHostPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui) invokes an EAP method's own configuration UI.</span></span> <span data-ttu-id="d0248-116">Bei der Rückgabe von **eaphostpeerinvokeconfigui** gibt die Funktion ein EAP-methodenkonfigurationsblob als out-Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="d0248-116">On return from **EapHostPeerInvokeConfigUI**, the function will return an EAP method configuration BLOB as an out-parameter.</span></span>
5.  <span data-ttu-id="d0248-117">Der Supplicant speichert das konfigurationsblob zusammen mit der [**EAP \_ - \_ Methodentyp**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) Struktur zur Verwendung mit [**eaphostpeerbeginsession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession).</span><span class="sxs-lookup"><span data-stu-id="d0248-117">The supplicant stores the configuration BLOB, along with the [**EAP\_METHOD\_TYPE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) structure for use with [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession).</span></span>
6.  <span data-ttu-id="d0248-118">Die genaue Methode zum Speichern des Konfiguration für-BLOBs ist vollständig auf dem Supplicant.</span><span class="sxs-lookup"><span data-stu-id="d0248-118">The precise method for storing the configuraiton BLOB is entirely up to the supplicant.</span></span> <span data-ttu-id="d0248-119">Der Supplicant sollte die Konfiguration jedoch immer auf geeignete, sichere Weise speichern, die für Konfigurationsdaten der System-und Benutzerauthentifizierung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="d0248-119">However, the supplicant should always store the configuration in a suitable, secure manner appropriate for system and user authentication configuration data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0248-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d0248-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0248-121">Aktivieren von Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="d0248-121">Enabling Group Policy</span></span>](enabling-group-policy.md)
</dt> <dt>

[<span data-ttu-id="d0248-122">Implementieren In-Band NAP-Unterstützung für EAP-Methoden</span><span class="sxs-lookup"><span data-stu-id="d0248-122">Implementing In-Band NAP Support for EAP Methods</span></span>](enabling-in-band-nap-support.md)
</dt> <dt>

[<span data-ttu-id="d0248-123">Implementieren der NAP-Unterstützung für EAP-Methoden</span><span class="sxs-lookup"><span data-stu-id="d0248-123">Implementing NAP Support for EAP Methods</span></span>](implementing-nap-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="d0248-124">Übertragen von Daten zwischen den Supplicant-und EAP-Methoden</span><span class="sxs-lookup"><span data-stu-id="d0248-124">Transferring Data Between the Supplicant and EAP Methods</span></span>](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="d0248-125">EAPHost-Supplicants</span><span class="sxs-lookup"><span data-stu-id="d0248-125">EAPHost Supplicants</span></span>](eaphost-supplicants.md)
</dt> </dl>

 

 




