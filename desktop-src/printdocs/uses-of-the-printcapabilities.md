---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: ea75a7ac-d4d7-42b6-91e9-e28607fd684c
title: Verwendung der Print-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63dda5b21d1472ec8d4162c8d7229ff47264fb55
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "103961253"
---
# <a name="uses-of-the-printcapabilities"></a><span data-ttu-id="21443-104">Verwendung der Print-Funktionen</span><span class="sxs-lookup"><span data-stu-id="21443-104">Uses of the PrintCapabilities</span></span>

<span data-ttu-id="21443-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="21443-105">This topic is not current.</span></span> <span data-ttu-id="21443-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="21443-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="21443-107">Die printfunktionen dienen als Darstellung konfigurierbarer Geräte Attribute als Funktions-/optionskonstrukte oder Parameterkonstrukte.</span><span class="sxs-lookup"><span data-stu-id="21443-107">The PrintCapabilities are intended to represent configurable device attributes as either Feature/Option constructs or parameter constructs.</span></span> <span data-ttu-id="21443-108">Diese Informationen definieren den Konfigurationsbereich des Geräts und können von einem Benutzeroberflächen Client verwendet werden, um eine Benutzeroberfläche zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="21443-108">This information defines the configuration space of the device and can be used by a user interface (UI) client to construct a UI.</span></span> <span data-ttu-id="21443-109">Die Schlüsselwörter des Druck Schemas definieren einen Satz von Standard Funktions Instanzen, Options Instanzen für die Standard Funktions Instanzen und ParameterDef-Instanzen.</span><span class="sxs-lookup"><span data-stu-id="21443-109">The Print Schema Keywords define a set of standard Feature instances, Option instances for the standard Feature instances, and ParameterDef instances.</span></span>

<span data-ttu-id="21443-110">Die Feature/Option-oder Parameterkonstrukte in den Print-Funktionen sollen Eigenschaften-oder ScoredProperty-Instanzen enthalten, die ein Gerät beschreiben und vom Spooler-Subsystem unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="21443-110">The Feature/Option or parameter constructs in the PrintCapabilities are intended to hold Property or ScoredProperty instances that describe a device, and that are supported by the spooler subsystem.</span></span> <span data-ttu-id="21443-111">Diese Eigenschaften-und ScoredProperty-Instanzen sind für Clients des Geräts von allgemeinem Interesse und enthalten die Informationen, die von den Win32 devcaps-Funktionen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="21443-111">These Property and ScoredProperty instances are of general interest to clients of the device, and contain the information that is provided by the Win32 DevCaps functions.</span></span> <span data-ttu-id="21443-112">Die Schlüsselwörter des Druck Schemas definieren einen Satz von Standardeigenschaften-und ScoredProperty-Instanzen.</span><span class="sxs-lookup"><span data-stu-id="21443-112">The Print Schema Keywords define a set of standard Property and ScoredProperty instances.</span></span>

<span data-ttu-id="21443-113">Es muss betont werden, dass das Printworks-Dokument nur einwertige Daten darstellen soll: Daten, die nicht von einer bestimmten Konfiguration des Geräts abhängen.</span><span class="sxs-lookup"><span data-stu-id="21443-113">It should be emphasized that the PrintCapabilities document is intended to represent only single-valued data: data that does not depend on a particular configuration of the device.</span></span> <span data-ttu-id="21443-114">Das printfunktionalitäten-Dokument stellt nur eine Momentaufnahme von Konfigurations abhängigen Daten bereit.</span><span class="sxs-lookup"><span data-stu-id="21443-114">The PrintCapabilities document provides only a snapshot of configuration-dependent data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="21443-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="21443-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21443-116">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="21443-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



