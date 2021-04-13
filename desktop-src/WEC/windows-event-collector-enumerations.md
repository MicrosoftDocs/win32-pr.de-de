---
title: Windows-Ereignis Sammler-Enumerationen
description: In der folgenden Tabelle sind die Enumerationen des Windows-Ereignis Sammler-SDK aufgeführt.
ms.assetid: 3775aa7c-ef35-4534-b709-15624fd7a90d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32d2617c6eb0052ec1ac41d5f197d9216c253054
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388399"
---
# <a name="windows-event-collector-enumerations"></a><span data-ttu-id="8c871-103">Windows-Ereignis Sammler-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="8c871-103">Windows Event Collector Enumerations</span></span>

<span data-ttu-id="8c871-104">In der folgenden Tabelle sind die Enumerationen des Windows-Ereignis Sammler-SDK aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="8c871-104">The following table lists the enumerations of the Windows Event Collector SDK.</span></span>



| <span data-ttu-id="8c871-105">Enumeration</span><span class="sxs-lookup"><span data-stu-id="8c871-105">Enumeration</span></span>                                                                                               | <span data-ttu-id="8c871-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8c871-106">Description</span></span>                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c871-107">**\_ \_ Konfigurations \_ Modus des EC-Abonnements**</span><span class="sxs-lookup"><span data-stu-id="8c871-107">**EC\_SUBSCRIPTION\_CONFIGURATION\_MODE**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_configuration_mode)                       | <span data-ttu-id="8c871-108">Gibt verschiedene Konfigurations Modi an, die die Standardeinstellungen für ein Abonnement ändern.</span><span class="sxs-lookup"><span data-stu-id="8c871-108">Specifies different configuration modes that change the default settings for a subscription.</span></span>                                            |
| [<span data-ttu-id="8c871-109">**\_ \_ Inhalts \_ Format des EC-Abonnements**</span><span class="sxs-lookup"><span data-stu-id="8c871-109">**EC\_SUBSCRIPTION\_CONTENT\_FORMAT**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_content_format)                               | <span data-ttu-id="8c871-110">Gibt an, wie Ereignisse auf dem Computer gerendert werden, der die Ereignisse sendet, bevor die Ereignisse an den Ereignis Sammler Computer gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="8c871-110">Specifies how events will be rendered on the computer that sends the events before the events are sent to the event collector computer.</span></span> |
| [<span data-ttu-id="8c871-111">**Anmelde Informationen für das EC- \_ Abonnement \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8c871-111">**EC\_SUBSCRIPTION\_CREDENTIALS\_TYPE**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_credentials_type)                           | <span data-ttu-id="8c871-112">Gibt den Typ der Anmelde Informationen an, die bei der Kommunikation mit Ereignis Quellen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8c871-112">Specifies the type of credentials to use when communicating with event sources.</span></span>                                                         |
| [<span data-ttu-id="8c871-113">**EC-Abonnement Übermittlungs \_ \_ \_ Modus**</span><span class="sxs-lookup"><span data-stu-id="8c871-113">**EC\_SUBSCRIPTION\_DELIVERY\_MODE**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_delivery_mode)                                 | <span data-ttu-id="8c871-114">Gibt an, wie Ereignisse über ein Ereignis Abonnement (mit einem Push-oder Pull-Modell) übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="8c871-114">Specifies how events are delivered through an event subscription (using a push or pull model).</span></span>                                          |
| [<span data-ttu-id="8c871-115">**Eigenschaften-ID des EC- \_ Abonnements \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8c871-115">**EC\_SUBSCRIPTION\_PROPERTY\_ID**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id)                                     | <span data-ttu-id="8c871-116">Definiert Werte zur Identifizierung von Ereignis Abonnement Eigenschaften, die für die Abonnement Konfiguration verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8c871-116">Defines values to identify event subscription properties used for subscription configuration.</span></span>                                           |
| [<span data-ttu-id="8c871-117">**Status \_ des \_ \_ \_ aktiven \_ Status des EC-Abonnements**</span><span class="sxs-lookup"><span data-stu-id="8c871-117">**EC\_SUBSCRIPTION\_RUNTIME\_STATUS\_ACTIVE\_STATUS**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_runtime_status_active_status) | <span data-ttu-id="8c871-118">Gibt den Status eines Abonnements oder einer Ereignis Quelle in Bezug auf ein Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="8c871-118">Specifies the status of a subscription or an event source with respect to a subscription.</span></span>                                               |
| [<span data-ttu-id="8c871-119">**\_ID des \_ Lauf \_ Zeit \_ Status \_ der EC-Abonnements**</span><span class="sxs-lookup"><span data-stu-id="8c871-119">**EC\_SUBSCRIPTION\_RUNTIME\_STATUS\_INFO\_ID**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_runtime_status_info_id)             | <span data-ttu-id="8c871-120">Gibt einen Wert an, der eine Eigenschaft des Lauf Zeit Status einer Ereignis Quelle oder eines Abonnements angibt.</span><span class="sxs-lookup"><span data-stu-id="8c871-120">Specifies a value that identifies a property of the runtime status of an event source or a subscription.</span></span>                                |
| [<span data-ttu-id="8c871-121">**EC \_ - \_ Abonnementtyp**</span><span class="sxs-lookup"><span data-stu-id="8c871-121">**EC\_SUBSCRIPTION\_TYPE**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_type)                                                    | <span data-ttu-id="8c871-122">Gibt den Typ des zu verwendenden Abonnements an (ein von der Quelle initiiertes oder vom Collector initiiertes Abonnement).</span><span class="sxs-lookup"><span data-stu-id="8c871-122">Specifies the type of subscription to use (a source initiated or collector initiated subscription).</span></span>                                     |
| [<span data-ttu-id="8c871-123">**Typ der EC- \_ Variante \_**</span><span class="sxs-lookup"><span data-stu-id="8c871-123">**EC\_VARIANT\_TYPE**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_variant_type)                                                              | <span data-ttu-id="8c871-124">Definiert die Werte, die die Datentypen angeben, die in den Windows-Ereignis Sammlungs Funktionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8c871-124">Defines the values that specify the data types that are used in the Windows Event Collector functions.</span></span>                                  |



 

 

 




