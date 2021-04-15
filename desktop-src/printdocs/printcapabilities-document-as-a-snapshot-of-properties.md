---
title: Dokument als Momentaufnahme von Eigenschaften
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 476c98e6-face-42cf-874d-cfa7a54b0666
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d73fc190ed8c259e64fdd60cc291c6ae5b58f80
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104393882"
---
# <a name="printcapabilities-document-as-a-snapshot-of-properties"></a><span data-ttu-id="2c82c-104">Printfunktionalitäten-Dokument als Momentaufnahme von Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2c82c-104">PrintCapabilities Document as a Snapshot of Properties</span></span>

<span data-ttu-id="2c82c-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="2c82c-105">This topic is not current.</span></span> <span data-ttu-id="2c82c-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2c82c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2c82c-107">Das Gerät, das von PrintProperties beschrieben wird, verfügt möglicherweise über Eigenschaften, die vom Zustand oder der Konfiguration des Geräts abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="2c82c-107">The device described by the PrintCapabilities might have properties that depend on the state or configuration of the device.</span></span> <span data-ttu-id="2c82c-108">Obwohl printfunktionen den vollständigen Konfigurationsbereich eines Geräts darstellt, erzeugt der Printworks-Anbieter eine Konfigurations abhängige Instanz der Print-Funktionen, die als printfunktionalitäten-Dokument bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="2c82c-108">While the PrintCapabilities represents the full configuration space of a device, the PrintCapabilities provider produces a configuration-dependent instance of the PrintCapabilities called the PrintCapabilities document.</span></span> <span data-ttu-id="2c82c-109">Dieses Konfigurations abhängige Printworks-Dokument vermeidet, das printfunktionalitäten-Schema durch die Komplexität der Darstellung mehr wertiger Daten zu belasten.</span><span class="sxs-lookup"><span data-stu-id="2c82c-109">This configuration-dependent PrintCapabilities document avoids burdening the PrintCapabilities Schema with the complexity of representing multivalued data.</span></span> <span data-ttu-id="2c82c-110">Noch wichtiger ist, dass es für alle Eigenschaften-und ScoredProperty-Instanzen in einem printfunktionalitäten-Dokument einwertig sein muss, um einen Consumer des Printworks-Dokuments von der Aufgabe zu entlasten, den entsprechenden Wert aus einer mehrwertigen Datendarstellung zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="2c82c-110">More importantly, to relieve a consumer of the PrintCapabilities document from the burden of extracting the appropriate value from a multivalued data representation, all Property and ScoredProperty instances in a PrintCapabilities document are required to be single-valued.</span></span> <span data-ttu-id="2c82c-111">Anders ausgedrückt: jede Eigenschaft und eine ScoredProperty-Instanz in einem Printworks-Dokument müssen einen Fixed-Wert aufweisen, der relativ zur Eingabe Konfiguration ist.</span><span class="sxs-lookup"><span data-stu-id="2c82c-111">In other words, each Property and ScoredProperty instance in a PrintCapabilities document must have a fixed Value, relative to the input configuration.</span></span> <span data-ttu-id="2c82c-112">Jedes Dokument von printfunktionen kann als eine Momentaufnahme der Eigenschaften des Geräts betrachtet werden, wenn sich das Gerät in einem bestimmten Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="2c82c-112">Each PrintCapabilities document can be thought of as a snapshot of the properties of the device when the device is in a particular state.</span></span> <span data-ttu-id="2c82c-113">Folglich muss die zu verwendende Konfiguration bereitgestellt werden, bevor ein printfunktionalitäten-Dokument erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="2c82c-113">Consequently, before a PrintCapabilities document can be constructed, the configuration to be used must be provided.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c82c-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2c82c-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c82c-115">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="2c82c-115">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



