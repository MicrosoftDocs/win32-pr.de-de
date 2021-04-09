---
title: Sicherheits Kanaleinstellungen
description: Mit den Sicherheits Kanaleinstellungen wird gesteuert, wie die Sicherheit auf einem Kanal angewendet und überprüft wird.
ms.assetid: ad964874-0bc7-4f03-8ceb-33627ff99f08
keywords:
- Sicherheits Kanaleinstellungen Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fcd0b42b2d5581a5b7c489e9ada70f32abfefa
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104102574"
---
# <a name="security-channel-settings"></a><span data-ttu-id="832d3-106">Sicherheits Kanaleinstellungen</span><span class="sxs-lookup"><span data-stu-id="832d3-106">Security Channel Settings</span></span>

<span data-ttu-id="832d3-107">Mit den Sicherheits Kanaleinstellungen wird gesteuert, wie die Sicherheit auf einem Kanal angewendet und überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="832d3-107">Security channel settings control the way security is applied and verified on a channel.</span></span> <span data-ttu-id="832d3-108">Jede Sicherheits Kanal Einstellung wird durch eine Auflistung von Eigenschaften-Wert-Paaren dargestellt, wobei die Eigenschafts Schlüssel durch die Enumeration [**WS- \_ Sicherheits \_ Eigenschaften- \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)definiert werden.</span><span class="sxs-lookup"><span data-stu-id="832d3-108">Each security channel setting is represented by a collection of property-value pairs, with the property keys defined by the enumeration [**WS\_SECURITY\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id).</span></span> <span data-ttu-id="832d3-109">Jede Eigenschaft in der Auflistung weist einen angemessenen Standardwert auf.</span><span class="sxs-lookup"><span data-stu-id="832d3-109">Each property in the collection has a reasonable default value.</span></span> <span data-ttu-id="832d3-110">Aufgrund dieser Standardwerte ist es möglich, eine Sicherheits Beschreibung zu definieren und zu verwenden, ohne die Sicherheits Kanaleinstellungen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="832d3-110">Because of these default values, it is possible to define and use a security description without specifying any of the security channel settings.</span></span>


<span data-ttu-id="832d3-111">[Sicherheitsbindungs Einstellungen](security-binding-settings.md) enthalten ähnliche Auflistungen von Eigenschafts-Wert-Paaren, deren Schlüssel durch die [**WS- \_ \_ sicherheitsbindungs- \_ Eigenschafts**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property) Struktur definiert werden.</span><span class="sxs-lookup"><span data-stu-id="832d3-111">[Security binding settings](security-binding-settings.md) contain similar collections of property-value pairs whose keys are defined by the [**WS\_SECURITY\_BINDING\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property) structure.</span></span> <span data-ttu-id="832d3-112">Der Unterschied zwischen diesen beiden Arten von Einstellungen besteht darin, dass die Sicherheits Kanaleinstellungen auf eine Sicherheits Beschreibung beschränkt sind (d. h., Sie enthalten channelweite Sicherheitseigenschaften), während die sicherheitsbindungs Einstellungen auf eine der Sicherheits Bindungen beschränkt sind und möglicherweise viele Sicherheits Bindungen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="832d3-112">The difference between these two sorts of settings is that the security channel settings are scoped to a security description (that is, they contain channel-wide security properties), whereas security binding settings are scoped to one of the security bindings, and there may be many security bindings.</span></span> <span data-ttu-id="832d3-113">Folglich hat beispielsweise eine benutzerdefinierte Sicherheits Beschreibung, die drei Sicherheits Bindungen enthält, einen Sicherheits Kanal-Einstellungs Behälter für den gesamten Kanal und drei Einstellungen für die sicherheitsbindungs Einstellungen, eine für jede Sicherheitsbindung.</span><span class="sxs-lookup"><span data-stu-id="832d3-113">Consequently, for example, a custom security description that contains three security bindings will have one security channel settings bag for the entire channel and three security binding settings bags, one for each security binding.</span></span>

<span data-ttu-id="832d3-114">Die folgenden Enumerationen werden mit den Sicherheits Kanaleinstellungen verwendet:</span><span class="sxs-lookup"><span data-stu-id="832d3-114">The following enumerations are used with security channel settings:</span></span>

-   [<span data-ttu-id="832d3-115">**WS- \_ Schutz \_ Ebene**</span><span class="sxs-lookup"><span data-stu-id="832d3-115">**WS\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level)
-   [<span data-ttu-id="832d3-116">**WS- \_ Anforderungs \_ Sicherheits Token-Eigenschaften- \_ \_ \_ ID**</span><span class="sxs-lookup"><span data-stu-id="832d3-116">**WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id)
-   [<span data-ttu-id="832d3-117">**WS- \_ Sicherheits \_ Algorithmus- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="832d3-117">**WS\_SECURITY\_ALGORITHM\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_algorithm_id)
-   [<span data-ttu-id="832d3-118">**Eigenschaften-ID für WS- \_ Sicherheits \_ Algorithmus \_ \_**</span><span class="sxs-lookup"><span data-stu-id="832d3-118">**WS\_SECURITY\_ALGORITHM\_PROPERTY\_ID**</span></span>](/windows/win32/api/webservices/ne-webservices-ws_move_to)
-   [<span data-ttu-id="832d3-119">**WS- \_ Sicherheits \_ Header \_ Layout**</span><span class="sxs-lookup"><span data-stu-id="832d3-119">**WS\_SECURITY\_HEADER\_LAYOUT**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_header_layout)
-   [<span data-ttu-id="832d3-120">**WS- \_ Sicherheits \_ Header \_ Version**</span><span class="sxs-lookup"><span data-stu-id="832d3-120">**WS\_SECURITY\_HEADER\_VERSION**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_header_version)
-   [<span data-ttu-id="832d3-121">**WS- \_ Sicherheits \_ Eigenschaften- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="832d3-121">**WS\_SECURITY\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)
-   [<span data-ttu-id="832d3-122">**WS- \_ Sicherheits \_ Zeitstempel- \_ Verwendung**</span><span class="sxs-lookup"><span data-stu-id="832d3-122">**WS\_SECURITY\_TIMESTAMP\_USAGE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage)
-   [<span data-ttu-id="832d3-123">**WS- \_ XML- \_ Sicherheits Token-Eigenschaften- \_ \_ \_ ID**</span><span class="sxs-lookup"><span data-stu-id="832d3-123">**WS\_XML\_SECURITY\_TOKEN\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_security_token_property_id)

<span data-ttu-id="832d3-124">Die folgenden Strukturen werden mit den Sicherheits Kanaleinstellungen verwendet:</span><span class="sxs-lookup"><span data-stu-id="832d3-124">The following structures are used with security channel settings:</span></span>

-   [<span data-ttu-id="832d3-125">**WS- \_ Anforderungs \_ Sicherheits Token ( \_ \_ Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="832d3-125">**WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property)
-   [<span data-ttu-id="832d3-126">**WS- \_ Sicherheits \_ Algorithmus ( \_ Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="832d3-126">**WS\_SECURITY\_ALGORITHM\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_algorithm_property)
-   [<span data-ttu-id="832d3-127">**WS \_ - \_ Sicherheitsalgorithmussuite \_**</span><span class="sxs-lookup"><span data-stu-id="832d3-127">**WS\_SECURITY\_ALGORITHM\_SUITE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_algorithm_suite)
-   [<span data-ttu-id="832d3-128">**WS- \_ Sicherheits \_ Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="832d3-128">**WS\_SECURITY\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_property)
-   [<span data-ttu-id="832d3-129">**WS \_ XML- \_ Sicherheits \_ Token ( \_ Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="832d3-129">**WS\_XML\_SECURITY\_TOKEN\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_security_token_property)

 

 




