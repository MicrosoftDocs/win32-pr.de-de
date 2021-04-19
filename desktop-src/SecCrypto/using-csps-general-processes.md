---
description: Beachten Sie bei der Verwendung von Kryptografiedienstanbietern (CSPs) die folgenden Konventionen.
ms.assetid: 70053b89-4d39-4a86-985a-0e8f05fbc9c0
title: 'Verwenden von CSPs: allgemeine Prozesse'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93f067ef0e3cd837b1b347daac3e3da21543047d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343751"
---
# <a name="using-csps-general-processes"></a><span data-ttu-id="6a37b-103">Verwenden von CSPs: allgemeine Prozesse</span><span class="sxs-lookup"><span data-stu-id="6a37b-103">Using CSPs: General Processes</span></span>

<span data-ttu-id="6a37b-104">Beachten Sie bei der Verwendung von [*Kryptografiedienstanbietern*](../secgloss/c-gly.md) (CSPs) die folgenden Konventionen.</span><span class="sxs-lookup"><span data-stu-id="6a37b-104">When using [*cryptographic service providers*](../secgloss/c-gly.md) CSPs, keep the following conventions in mind.</span></span>

## <a name="private-key-caching"></a><span data-ttu-id="6a37b-105">Zwischenspeichern von privaten Schlüsseln</span><span class="sxs-lookup"><span data-stu-id="6a37b-105">Private Key Caching</span></span>

<span data-ttu-id="6a37b-106">Ein CSP kann einige [*private Schlüssel*](../secgloss/p-gly.md)Zwischenspeichern.</span><span class="sxs-lookup"><span data-stu-id="6a37b-106">A CSP can cache some [*private keys*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="6a37b-107">Es ist möglich, diese private Schlüssel Zwischenspeicherung auf globaler, aber nicht auf anwendungsspezifischer Basis zu steuern.</span><span class="sxs-lookup"><span data-stu-id="6a37b-107">It is possible to control this private key caching on a global, but not an application-specific, basis.</span></span> <span data-ttu-id="6a37b-108">Das Zwischenspeichern von Änderungen wird durch Ändern bestimmter Registrierungs Einstellungen vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="6a37b-108">Caching changes are made by modifying certain registry settings.</span></span> <span data-ttu-id="6a37b-109">Weitere Informationen finden Sie unter Caching für die Zwischenspeicherung von [**privaten Schlüsseln**](private-key-caching-constants.md).</span><span class="sxs-lookup"><span data-stu-id="6a37b-109">For more information, see [**Private Key Caching Constants**](private-key-caching-constants.md).</span></span>

## <a name="example-code-conventions"></a><span data-ttu-id="6a37b-110">Beispiel Code Konventionen</span><span class="sxs-lookup"><span data-stu-id="6a37b-110">Example Code Conventions</span></span>

<span data-ttu-id="6a37b-111">Um präziseren, besser lesbaren Code bereitzustellen, werden in den Beispielen nicht immer einige Grundsätze von bewährten Programmierpraktiken befolgt.</span><span class="sxs-lookup"><span data-stu-id="6a37b-111">To provide more concise, more readable code, some principles of good programming practice are not always followed in the examples.</span></span> <span data-ttu-id="6a37b-112">Dies gilt insbesondere für:</span><span class="sxs-lookup"><span data-stu-id="6a37b-112">In particular:</span></span>

-   <span data-ttu-id="6a37b-113">Nur eingeschränkte Fehler Antworten werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6a37b-113">Only limited error responses are shown.</span></span> <span data-ttu-id="6a37b-114">Ordnungsgemäß geschriebene, vollständige Programme überprüft zurückgegebene Fehlercodes und führt beim Auftreten eines Fehlers geeignete Aktionen aus.</span><span class="sxs-lookup"><span data-stu-id="6a37b-114">Well-written, complete programs check returned error codes and perform appropriate actions when an error is encountered.</span></span>
-   <span data-ttu-id="6a37b-115">Nur eingeschränkte Arbeitsspeicher-und Ressourcenverwaltung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="6a37b-115">Only limited memory and resource management is done.</span></span> <span data-ttu-id="6a37b-116">Gut geschriebene, vollständige Programme zerstören alle Schlüssel und Hashwerte, geben den gesamten zugeordneten Arbeitsspeicher frei, schließen alle [*Dateien und geben*](../secgloss/h-gly.md)alle Handles frei.</span><span class="sxs-lookup"><span data-stu-id="6a37b-116">Well-written, complete programs destroy all keys and [*hashes*](../secgloss/h-gly.md), free all allocated memory, close all files, and release all handles.</span></span> <span data-ttu-id="6a37b-117">In diesen Beispielen wird nur eine begrenzte Demonstration der Verwendung von Funktionen bereitgestellt, die diese Aufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="6a37b-117">These examples provide only limited demonstrations of the use of functions that perform these tasks.</span></span> <span data-ttu-id="6a37b-118">In diesen Beispielen werden keine Arbeitsspeicher-oder Ressourcen Verwaltungsaufgaben ausgeführt, wenn die Programm Beendigung aufgrund von Fehlern auftritt.</span><span class="sxs-lookup"><span data-stu-id="6a37b-118">These examples perform no memory or resource management tasks in the case of program termination due to errors.</span></span>

<span data-ttu-id="6a37b-119">Die folgenden Themen enthalten allgemeine Informationen zu Prozedur Beispielen und Beispielcode.</span><span class="sxs-lookup"><span data-stu-id="6a37b-119">The following topics present general information about procedure examples as well as sample code.</span></span>

-   [<span data-ttu-id="6a37b-120">Abrufen von Daten mit unbekannter Länge</span><span class="sxs-lookup"><span data-stu-id="6a37b-120">Retrieving Data of Unknown Length</span></span>](retrieving-data-of-unknown-length.md)
-   [<span data-ttu-id="6a37b-121">Auflisten unterstützter Protokolle</span><span class="sxs-lookup"><span data-stu-id="6a37b-121">Enumerating Supported Protocols</span></span>](enumerating-supported-protocols.md)

 

 
