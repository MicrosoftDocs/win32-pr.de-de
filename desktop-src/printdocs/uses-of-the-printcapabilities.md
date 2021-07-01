---
description: Erfahren Sie mehr über die Verwendungsmöglichkeiten von PrintCapabilities. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: ea75a7ac-d4d7-42b6-91e9-e28607fd684c
title: Verwendungsmöglichkeiten der PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f09882d42814930ef5ba08e087f1df87e0d0e9bc
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119425"
---
# <a name="uses-of-the-printcapabilities"></a><span data-ttu-id="1378a-105">Verwendungsmöglichkeiten der PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="1378a-105">Uses of the PrintCapabilities</span></span>

<span data-ttu-id="1378a-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="1378a-106">This topic is not current.</span></span> <span data-ttu-id="1378a-107">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="1378a-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1378a-108">Die PrintCapabilities sollen konfigurierbare Geräteattribute entweder als Feature-/Optionskonstrukte oder als Parameterkonstrukte darstellen.</span><span class="sxs-lookup"><span data-stu-id="1378a-108">The PrintCapabilities are intended to represent configurable device attributes as either Feature/Option constructs or parameter constructs.</span></span> <span data-ttu-id="1378a-109">Diese Informationen definieren den Konfigurationsraum des Geräts und können von einem Benutzeroberflächenclient verwendet werden, um eine Benutzeroberfläche zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1378a-109">This information defines the configuration space of the device and can be used by a user interface (UI) client to construct a UI.</span></span> <span data-ttu-id="1378a-110">Die Druckschemaschlüsselwörter definieren eine Reihe von Standardfunktionsinstanzen, Optionsinstanzen für die Standardfunktionsinstanzen und ParameterDef-Instanzen.</span><span class="sxs-lookup"><span data-stu-id="1378a-110">The Print Schema Keywords define a set of standard Feature instances, Option instances for the standard Feature instances, and ParameterDef instances.</span></span>

<span data-ttu-id="1378a-111">Die Feature-/Options- oder Parameterkonstrukte in printCapabilities sind für Property- oder ScoredProperty-Instanzen vorgesehen, die ein Gerät beschreiben und vom Spoolersubsystem unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="1378a-111">The Feature/Option or parameter constructs in the PrintCapabilities are intended to hold Property or ScoredProperty instances that describe a device, and that are supported by the spooler subsystem.</span></span> <span data-ttu-id="1378a-112">Diese Property- und ScoredProperty-Instanzen sind für Clients des Geräts von allgemeinem Interesse und enthalten die Informationen, die von den Win32 DevCaps-Funktionen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1378a-112">These Property and ScoredProperty instances are of general interest to clients of the device, and contain the information that is provided by the Win32 DevCaps functions.</span></span> <span data-ttu-id="1378a-113">Die Druckschemaschlüsselwörter definieren einen Satz von Standardeigenschaften- und ScoredProperty-Instanzen.</span><span class="sxs-lookup"><span data-stu-id="1378a-113">The Print Schema Keywords define a set of standard Property and ScoredProperty instances.</span></span>

<span data-ttu-id="1378a-114">Es sollte hervorgehoben werden, dass das PrintCapabilities-Dokument nur einwertige Daten darstellen soll: Daten, die nicht von einer bestimmten Konfiguration des Geräts abhängen.</span><span class="sxs-lookup"><span data-stu-id="1378a-114">It should be emphasized that the PrintCapabilities document is intended to represent only single-valued data: data that does not depend on a particular configuration of the device.</span></span> <span data-ttu-id="1378a-115">Das PrintCapabilities-Dokument stellt nur eine Momentaufnahme konfigurationsabhängiger Daten bereit.</span><span class="sxs-lookup"><span data-stu-id="1378a-115">The PrintCapabilities document provides only a snapshot of configuration-dependent data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1378a-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1378a-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1378a-117">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="1378a-117">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



