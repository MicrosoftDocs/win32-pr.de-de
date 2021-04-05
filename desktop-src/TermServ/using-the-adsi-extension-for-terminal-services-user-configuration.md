---
title: Verwenden der ADSI-Erweiterung für Remotedesktopdienste Benutzerkonfiguration
description: Die Verwaltung Remotedesktopdienste spezifischer Benutzereigenschaften ist möglich, indem die von der ADSI-Erweiterung (Active Directory Service Interfaces) implementierten Methoden verwendet werden, die mit der Dynamic Link Library-Tsuserex.dll verpackt werden.
ms.assetid: f6355730-9686-4446-b118-630562548fc9
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste Remotedesktopdienste mit der ADSI-Erweiterung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f115fecf1cce5c518e93206402f76e077109611
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949046"
---
# <a name="using-the-adsi-extension-for-remote-desktop-services-user-configuration"></a><span data-ttu-id="6bd0d-104">Verwenden der ADSI-Erweiterung für Remotedesktopdienste Benutzerkonfiguration</span><span class="sxs-lookup"><span data-stu-id="6bd0d-104">Using the ADSI Extension for Remote Desktop Services User Configuration</span></span>

<span data-ttu-id="6bd0d-105">Die ADSI-Erweiterung (Active Directory Service Interfaces) für Remotedesktopdienste Benutzerkonfiguration ist eine Bibliothek, die mit der Tsuserex.dll der Dynamic Link Library verpackt ist.</span><span class="sxs-lookup"><span data-stu-id="6bd0d-105">The Active Directory Service Interfaces (ADSI) extension for Remote Desktop Services user configuration is a library that is packaged with the dynamic-link library Tsuserex.dll.</span></span> <span data-ttu-id="6bd0d-106">Die Verwaltung Remotedesktopdienste spezifischer Benutzereigenschaften ist mithilfe der von der Erweiterung implementierten Methoden möglich.</span><span class="sxs-lookup"><span data-stu-id="6bd0d-106">Administration of Remote Desktop Services-specific user properties is possible using the methods implemented by the extension.</span></span> <span data-ttu-id="6bd0d-107">Die-Methoden ermöglichen das Konfigurieren der Eigenschaften, die in der Erweiterungsschnittstelle für Remotedesktopdienste Benutzer verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="6bd0d-107">The methods allow configuration of the properties that are available in the extension interface for Remote Desktop Services users.</span></span>

<span data-ttu-id="6bd0d-108">Die ADSI-Erweiterung für Remotedesktopdienste Benutzerkonfiguration unterstützt die Prüfung und Bearbeitung von Remotedesktopdienste Benutzereigenschaften, die in der Verzeichnisdienst-Datenbank gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="6bd0d-108">The ADSI extension for Remote Desktop Services user configuration supports the examination and manipulation of Remote Desktop Services user properties stored in the Directory Service database.</span></span> <span data-ttu-id="6bd0d-109">Die Erweiterung unterstützt auch die Konfiguration von Benutzereigenschaften, die in der Active Directory gespeichert sind, über die LDAP-API (Lightweight Directory Access Protocol).</span><span class="sxs-lookup"><span data-stu-id="6bd0d-109">The extension also supports configuration of user properties that are stored in the Active Directory, through the Lightweight Directory Access Protocol (LDAP) API.</span></span>

<span data-ttu-id="6bd0d-110">Der Anbieter implementiert die folgenden Methoden:</span><span class="sxs-lookup"><span data-stu-id="6bd0d-110">The provider implements the following methods:</span></span>

-   <span data-ttu-id="6bd0d-111">[**IADs:: Get**](/windows/desktop/api/iads/nf-iads-iads-get).</span><span class="sxs-lookup"><span data-stu-id="6bd0d-111">[**IADs::Get**](/windows/desktop/api/iads/nf-iads-iads-get).</span></span> <span data-ttu-id="6bd0d-112">Diese Methode sucht eine bestimmte Eigenschaft oder einen Satz von Eigenschaften für eine Instanz der-Klasse.</span><span class="sxs-lookup"><span data-stu-id="6bd0d-112">This method searches for a specific property or set of properties on an instance of the class.</span></span>
-   <span data-ttu-id="6bd0d-113">[**IADs::P UT**](/windows/desktop/api/iads/nf-iads-iads-put).</span><span class="sxs-lookup"><span data-stu-id="6bd0d-113">[**IADs::Put**](/windows/desktop/api/iads/nf-iads-iads-put).</span></span> <span data-ttu-id="6bd0d-114">Diese Methode konfiguriert eine bestimmte Eigenschaft oder einen Satz von Eigenschaften für eine Instanz der-Klasse.</span><span class="sxs-lookup"><span data-stu-id="6bd0d-114">This method configures a specific property or set of properties on an instance of the class.</span></span>

<span data-ttu-id="6bd0d-115">Eine Liste der spezifischen Remotedesktopdienste Benutzereigenschaften, die Sie konfigurieren können, finden Sie in der [Referenz zur ADSI-Erweiterung für Remotedesktopdienste Benutzerkonfiguration](reference-for-the-adsi-extension-for-terminal-services-user-configuration.md) .</span><span class="sxs-lookup"><span data-stu-id="6bd0d-115">See the [Reference for the ADSI Extension for Remote Desktop Services User Configuration](reference-for-the-adsi-extension-for-terminal-services-user-configuration.md) for a list of the specific Remote Desktop Services user properties you can configure.</span></span>

<span data-ttu-id="6bd0d-116">Weitere Informationen zum Zugreifen auf und Ändern von Attributen mit ADSI finden Sie unter Zugreifen auf und Bearbeiten von [Daten mit ADSI](/windows/desktop/ADSI/accessing-and-manipulating-data-with-adsi).</span><span class="sxs-lookup"><span data-stu-id="6bd0d-116">For more information about accessing and modifying attributes with ADSI, see [Accessing and Manipulating Data with ADSI](/windows/desktop/ADSI/accessing-and-manipulating-data-with-adsi).</span></span>

<span data-ttu-id="6bd0d-117">Weitere Informationen zur Verwendung von ADSI-Benennungs Konventionen und ADsPath-Zeichen folgen finden Sie in den Informationen zu einzelnen [ADSI-Dienstanbietern](/windows/desktop/ADSI/adsi-system-providers) in der Dokumentation zum [Active Directory Service Interfaces](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="6bd0d-117">For more information about using ADSI naming conventions and AdsPath strings, see the information about individual [ADSI Service Providers](/windows/desktop/ADSI/adsi-system-providers) in the [Active Directory Service Interfaces](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) Platform Software Development Kit (SDK) documentation.</span></span>

 

 