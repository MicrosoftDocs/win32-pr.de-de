---
title: Geräte Zugriffs-API
description: Verwenden Sie die Geräte Zugriffs-API zum Schreiben von Windows Store-Geräte-Apps für spezialisierte Geräte, die benutzerdefinierte Treiber verwenden.
ms.assetid: 51329746-291e-4ac6-9029-ebe4727d5d7d
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 6f054167d81f33ce852f7707e194058f4cee3c75
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104391180"
---
# <a name="device-access-api"></a><span data-ttu-id="330b5-103">Geräte Zugriffs-API</span><span class="sxs-lookup"><span data-stu-id="330b5-103">Device Access API</span></span>

## <a name="purpose"></a><span data-ttu-id="330b5-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="330b5-104">Purpose</span></span>

<span data-ttu-id="330b5-105">Sie können die Geräte Zugriffs-API zum Schreiben von Windows Store-Geräte-Apps für spezialisierte Geräte verwenden, die benutzerdefinierte Treiber verwenden.</span><span class="sxs-lookup"><span data-stu-id="330b5-105">You can use the Device Access API to write Windows Store device apps for specialized devices that use custom drivers.</span></span> <span data-ttu-id="330b5-106">Die API stellt Methoden zum Senden von Steuerungs Codes für die Kommunikation mit dem benutzerdefinierten Treiber des Geräts bereit.</span><span class="sxs-lookup"><span data-stu-id="330b5-106">The API provides methods for sending control codes to communicate with the device's custom driver.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="330b5-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="330b5-107">In this section</span></span>

| <span data-ttu-id="330b5-108">Thema</span><span class="sxs-lookup"><span data-stu-id="330b5-108">Topic</span></span> | <span data-ttu-id="330b5-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="330b5-109">Description</span></span> |
|---|---|
| [<span data-ttu-id="330b5-110">Informationen zur Geräte Zugriffs-API</span><span class="sxs-lookup"><span data-stu-id="330b5-110">About the Device Access API</span></span>](about-the-device-access-api.md)<br/> | <span data-ttu-id="330b5-111">Die Geräte Zugriffs-API ist für C++-Entwickler gedacht, die eine Windows Store-App für die Interaktion mit spezialisierten Geräten in Windows 8 erstellen.</span><span class="sxs-lookup"><span data-stu-id="330b5-111">The Device Access API is for C++ developers who are creating a Windows Store app to interact with specialized devices in Windows 8.</span></span> <span data-ttu-id="330b5-112">In diesem Thema werden die Szenarien beschrieben, auf die sich die Geräte Zugriffs-API bezieht.</span><span class="sxs-lookup"><span data-stu-id="330b5-112">This topic describes the scenarios that the Device Access API applies to.</span></span> <span data-ttu-id="330b5-113">Außerdem wird erläutert, wie die Geräte Zugriffs-API Sicherheitsregeln für Windows Store-Apps in Windows 8 anwendet.</span><span class="sxs-lookup"><span data-stu-id="330b5-113">It also explains how the Device Access API applies security rules for Windows Store apps in Windows 8.</span></span><br/> |
| [<span data-ttu-id="330b5-114">Verwenden der Geräte Zugriffs-API</span><span class="sxs-lookup"><span data-stu-id="330b5-114">How to Use the Device Access API</span></span>](using-the-device-access-api.md)<br/> | <span data-ttu-id="330b5-115">Dieses Thema enthält Aufgaben und Entwurfs Überlegungen für die Verwendung der Geräte Zugriffs-API.</span><span class="sxs-lookup"><span data-stu-id="330b5-115">This topic contains tasks and design considerations for using the Device Access API.</span></span><br/> |
| [<span data-ttu-id="330b5-116">Geräte Zugriffs-API C++ Programmier Referenz</span><span class="sxs-lookup"><span data-stu-id="330b5-116">Device Access API C++ Programming Reference</span></span>](device-access-api-c---programming-reference.md)<br/> | <span data-ttu-id="330b5-117">Stellt Referenzseiten für die Funktionen und Schnittstellen in der Geräte Zugriffs-API bereit.</span><span class="sxs-lookup"><span data-stu-id="330b5-117">Provides reference pages for the functions and interfaces in the Device Access API.</span></span><br/> |
| [<span data-ttu-id="330b5-118">Glossar für den Gerätezugriff</span><span class="sxs-lookup"><span data-stu-id="330b5-118">Device Access Glossary</span></span>](deviceaccess-glossary.md)<br/> | <span data-ttu-id="330b5-119">Die folgenden Begriffe werden in der gesamten Dokumentation für die Geräte Zugriffs-API verwendet.</span><span class="sxs-lookup"><span data-stu-id="330b5-119">The following are terms used throughout the documentation for the Device Access API.</span></span><br/> |
| [<span data-ttu-id="330b5-120">Andere APIs</span><span class="sxs-lookup"><span data-stu-id="330b5-120">Other APIs</span></span>](other-apis.md)<br/> | <span data-ttu-id="330b5-121">Diese Schnittstellen werden nicht unterstützt und sollten nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="330b5-121">These interfaces are not supported and should not be used.</span></span> <span data-ttu-id="330b5-122">Verwenden Sie stattdessen die APIs in der [C++-Programmier Referenz für die Geräte Zugriffs-API](device-access-api-c---programming-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="330b5-122">Use the APIs in the [Device Access API C++ Programming Reference](device-access-api-c---programming-reference.md) instead.</span></span><br/> |

## <a name="developer-audience"></a><span data-ttu-id="330b5-123">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="330b5-123">Developer audience</span></span>

<span data-ttu-id="330b5-124">Die Geräte Zugriffs-API ist für unabhängige Hardwarehersteller (IHV) und OEM-Entwickler konzipiert, die mit C++ und Component Object Model (com) vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="330b5-124">The Device Access API is designed for independent hardware vendor (IHV) and OEM developers who are familiar with C++ and Component Object Model (COM).</span></span>

## <a name="related-topics"></a><span data-ttu-id="330b5-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="330b5-125">Related topics</span></span>

<span data-ttu-id="330b5-126">[Beispiel für benutzerdefinierten Treiber Zugriff](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [UWP-Geräte-Apps für interne Geräte](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Hardware dev Center](/windows-hardware/drivers/)</span><span class="sxs-lookup"><span data-stu-id="330b5-126">[Custom Driver Access Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [UWP device apps for internal devices](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Hardware Dev Center](/windows-hardware/drivers/)</span></span>
