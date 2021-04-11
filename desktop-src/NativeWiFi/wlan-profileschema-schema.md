---
description: Definiert ein WLAN-Profil, das vom systemeigenen WiFi-AutoConfig-Dienst verwendet wird.
ms.assetid: 8312d213-1d01-4bd0-a8d9-65ca23560888
title: WLAN_profile-Schema
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d484215ca53ddcd97dbef4adf4aac17cd8457b3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128840"
---
# <a name="wlan_profile-schema"></a><span data-ttu-id="ddcf6-103">WLAN- \_ Profil Schema</span><span class="sxs-lookup"><span data-stu-id="ddcf6-103">WLAN\_profile Schema</span></span>

<span data-ttu-id="ddcf6-104">Das WLAN- \_ Profil Schema definiert ein WLAN-Profil, das vom systemeigenen WiFi-AutoConfig-Dienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-104">The WLAN\_profile Schema defines a WLAN profile used by the Native Wifi AutoConfig service.</span></span>

<span data-ttu-id="ddcf6-105">Der AutoConfig-Dienst akzeptiert drahtlos Profile vom Gruppenrichtlinie-Agent, von der Scripting Interface (**netsh**), von der Benutzeroberfläche oder von der USB-Flash-Konfigurationsschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-105">The AutoConfig service accepts wireless profiles from the Group Policy Agent, the scripting interface (**netsh**), the user interface, or from the USB flash configuration interface.</span></span>

<span data-ttu-id="ddcf6-106">Ein Profil, das von einem dieser Systeme empfangen wird, wird dem WLAN \_ -Profil Schema zugeordnet und im Profil Speicher gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-106">A profile received from one of these systems is mapped to the WLAN\_profile schema and stored in the profile store.</span></span> <span data-ttu-id="ddcf6-107">Profile können mithilfe von Netsh-Befehlen oder mithilfe von API-Elementen wie [**wlangetprofile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)aus dem Profil Speicher exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-107">Profiles can be exported from the profile store using netsh commands or using API elements such as [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile).</span></span>

<span data-ttu-id="ddcf6-108">Das Stamm Element eines WLAN-Profils ist das [**wlanprofile**](wlan-profileschema-wlanprofile-element.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-108">The root element of a WLAN profile is the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span> <span data-ttu-id="ddcf6-109">Jedes Profil weist genau ein Stamm Element auf.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-109">Each profile will have exactly one root element.</span></span> <span data-ttu-id="ddcf6-110">Das **wlanprofile** -Element befindet sich im-Namespace `https://www.microsoft.com/networking/WLAN/profile/v1` .</span><span class="sxs-lookup"><span data-stu-id="ddcf6-110">The **WLANProfile** element is in the namespace `https://www.microsoft.com/networking/WLAN/profile/v1`.</span></span>

<span data-ttu-id="ddcf6-111">Beispiel-WLAN-Profile finden Sie unter [Beispiele für drahtlos profile](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="ddcf6-111">To view sample WLAN profiles, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

-   [<span data-ttu-id="ddcf6-112">WLAN- \_ Profil Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="ddcf6-112">WLAN\_profile Schema Elements</span></span>](wlan-profileschema-elements.md)
-   [<span data-ttu-id="ddcf6-113">Einfache Typen von WLAN- \_ Profil Schemas</span><span class="sxs-lookup"><span data-stu-id="ddcf6-113">WLAN\_profile Schema Simple Types</span></span>](wlan-profileschema-simple-types.md)

## <a name="related-topics"></a><span data-ttu-id="ddcf6-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ddcf6-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ddcf6-115">[Netsh-Befehle für WLAN (Wireless Local Area Network)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="ddcf6-115">[Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))</span></span>
</dt> </dl>

 

 
