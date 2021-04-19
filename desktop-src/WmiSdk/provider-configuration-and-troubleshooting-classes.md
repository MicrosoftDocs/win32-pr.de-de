---
description: Die Klasse MSFT \_ Providers und die WMI-Fehler Behebungs Klassen sind eine Gruppe der MSFT-Ereignis Klassen, die mit WMI-Anbieter Ereignissen gekoppelt sind.
ms.assetid: 5eaf7026-87bf-416b-9a6d-7f92f85b0882
ms.tgt_platform: multiple
title: Anbieter Konfiguration und Fehler Behebungs Klassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be63fb5693898541bffae2abcb05b7595ae7fc9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349458"
---
# <a name="provider-configuration-and-troubleshooting-classes"></a><span data-ttu-id="fb045-103">Anbieter Konfiguration und Fehler Behebungs Klassen</span><span class="sxs-lookup"><span data-stu-id="fb045-103">Provider Configuration and Troubleshooting Classes</span></span>

<span data-ttu-id="fb045-104">Die Klasse [**MSFT \_ Providers**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) und die WMI-Fehler Behebungs Klassen sind eine Gruppe der [MSFT-Ereignis Klassen](msft-classes.md) , die mit WMI-Anbieter Ereignissen gekoppelt sind.</span><span class="sxs-lookup"><span data-stu-id="fb045-104">The [**MSFT\_Providers**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) class and the WMI troubleshooting classes are a group of the [MSFT event classes](msft-classes.md) coupled to WMI provider events.</span></span>

<span data-ttu-id="fb045-105">Die Klasse der [**MSFT- \_ Anbieter**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) enthält Konfigurationsinformationen für Anbieter und umfasst die folgenden Methoden, die es Ihnen ermöglichen, Anbieter zu laden und zu entladen oder Anbieter Vorgänge anzuhalten und fortzusetzen:</span><span class="sxs-lookup"><span data-stu-id="fb045-105">The [**MSFT\_Providers**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) class contains configuration information for providers and includes the following methods that allow you to load and unload providers, or suspend and resume provider operations:</span></span>

-   [<span data-ttu-id="fb045-106">**Load-Methode der Klasse der MSFT- \_ Anbieter**</span><span class="sxs-lookup"><span data-stu-id="fb045-106">**Load Method of the MSFT\_Providers Class**</span></span>](/previous-versions/windows/desktop/wmisystemprov/load-method-in-class-msft-providers)
-   [<span data-ttu-id="fb045-107">**Entlade Methode der Klasse der MSFT- \_ Anbieter**</span><span class="sxs-lookup"><span data-stu-id="fb045-107">**UnLoad Method of the MSFT\_Providers Class**</span></span>](/previous-versions/windows/desktop/wmisystemprov/unload-method-in-class-msft-providers)
-   [<span data-ttu-id="fb045-108">**Resume-Methode der Klasse der MSFT- \_ Anbieter**</span><span class="sxs-lookup"><span data-stu-id="fb045-108">**Resume Method of the MSFT\_Providers Class**</span></span>](/previous-versions/windows/desktop/wmisystemprov/resume-method-in-class-msft-providers)
-   [<span data-ttu-id="fb045-109">**Suspend-Methode der Klasse der MSFT- \_ Anbieter**</span><span class="sxs-lookup"><span data-stu-id="fb045-109">**Suspend Method of the MSFT\_Providers Class**</span></span>](/previous-versions/windows/desktop/wmisystemprov/suspend-method-in-class-msft-providers)

<span data-ttu-id="fb045-110">Die [WMI-Fehler Behebungs Klassen](wmi-troubleshooting-classes.md) werden benannt, um anzugeben, ob das Ereignis vor oder nach einem Anbieter Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="fb045-110">The [WMI troubleshooting classes](wmi-troubleshooting-classes.md) are named to indicate whether the event is fired before or after a provider event.</span></span> <span data-ttu-id="fb045-111">Beispielsweise wird das Objekt " [**MSFT \_ WMIProvider \_ Access Check \_ Pre**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-pre) " unmittelbar vor dem Aufruf der Implementierung von **iwbemeventsecurity:: AccessCheck** des Anbieters generiert, während das Objekt " [**MSFT \_ WMIProvider \_ AccessCheck \_ Post**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-post) " unmittelbar nach aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="fb045-111">For example, the [**MSFT\_WmiProvider\_AccessCheck\_Pre**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-pre) object is generated immediately before calling the provider's implementation of **IWbemEventSecurity::AccessCheck**, while the [**MSFT\_WmiProvider\_AccessCheck\_Post**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-post) object is called immediately after.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb045-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fb045-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb045-113">WMI-Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="fb045-113">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="fb045-114">WMI-Fehler Behebungs Klassen</span><span class="sxs-lookup"><span data-stu-id="fb045-114">WMI Troubleshooting Classes</span></span>](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
