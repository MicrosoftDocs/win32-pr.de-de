---
title: Sensor Plattform
description: Windows 7 hat sich geändert, wie Entwickler Sensoren verwenden.
ms.assetid: ed323658-dfd6-4c1b-ada2-5d68ebb56482
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98fe94fd48ffa16080054a22b4d377ab4757d61d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039227"
---
# <a name="sensor-platform"></a><span data-ttu-id="fc5a0-103">Sensor Plattform</span><span class="sxs-lookup"><span data-stu-id="fc5a0-103">Sensor Platform</span></span>

<span data-ttu-id="fc5a0-104">Windows 7 hat sich geändert, wie Entwickler Sensoren verwenden.</span><span class="sxs-lookup"><span data-stu-id="fc5a0-104">Windows 7 has changed how developers use sensors.</span></span> <span data-ttu-id="fc5a0-105">Es umfasst systemeigene Unterstützung für Sensoren, erweitert durch eine neue Entwicklungsplattform für die Verwendung von Sensoren, einschließlich Standort Sensoren wie z. b. Global Positionierungs Systems (GPS).</span><span class="sxs-lookup"><span data-stu-id="fc5a0-105">It includes native support for sensors, expanded by a new development platform for working with sensors, including location sensors, such as Global Positioning Systems (GPS) devices.</span></span>

<span data-ttu-id="fc5a0-106">Die *Windows-Location*-APIs basieren auf der Sensor Plattform und sind ein neues Feature von Windows 7, mit dem Anwendungsentwickler auf die Informationen zum physischen Standort des Benutzers zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="fc5a0-106">Built on the Sensor Platform, the *Windows Location* APIs are a new Windows 7 feature that enables application developers to access the user's physical location information.</span></span> <span data-ttu-id="fc5a0-107">Mit den *Windows-Location*-APIs können Hardware abstrahiert, mehrere Anwendungen gleichzeitig unterstützt und nahtlos zwischen verschiedenen Technologien gewechselt werden, sodass der Anwendungsentwickler die Last der Verwaltung dieser Einschränkungen trägt.</span><span class="sxs-lookup"><span data-stu-id="fc5a0-107">The *Windows Location* APIs can abstract hardware, simultaneously support multiple applications, and seamlessly switch between different technologies, relieving the application developer of the burden of managing these constraints.</span></span> <span data-ttu-id="fc5a0-108">Die *Location*-APIs können von Programmierern über die Programmiersprache C++ (von Programmierern, die mit Component Object Model (com) vertraut sind) oder durch die Verwendung von COM-Objekten in Skriptsprachen wie Microsoft JScript verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fc5a0-108">The *Location* APIs can be used by programmers through the C++ programming language (by programmers familiar with Component Object Model (COM)), or by using COM objects in scripting languages, such as Microsoft JScript.</span></span> <span data-ttu-id="fc5a0-109">Die Skriptunterstützung ermöglicht den einfachen Zugriff auf Speicherort Daten für Projekte wie Mini Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="fc5a0-109">Scripting support gives easy access to location data for projects such as gadgets.</span></span>

<span data-ttu-id="fc5a0-110">Windows 7 bietet eine solide, leicht zu verwendende Plattform für die Verwendung von Sensorgeräten, z. b. einem Umgebungslichtsensor oder einem Temperaturmessgerät, um Umweltbewusstsein in Windows-Anwendungen zu schaffen.</span><span class="sxs-lookup"><span data-stu-id="fc5a0-110">Windows 7 provides a solid, easy-to-use platform for using sensor devices, such as an ambient light sensor or a temperature gauge, to create environmental awareness in Windows applications.</span></span> <span data-ttu-id="fc5a0-111">PCs können Sensoren verwenden, die in den Computer integriert sind, über Kabel-oder drahtlos Verbindungen verbunden sind oder über ein Netzwerk oder das *Internet* verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="fc5a0-111">PCs can use sensors that are built into the computer, connected through wired or wireless connections, or connected through a network or the *Internet*.</span></span>

<span data-ttu-id="fc5a0-112">Die *Sensor* -und *Location*-APIs bieten eine Standardmethode zum Ermitteln von Sensoren und zum programmgesteuerten Zugriff auf Daten, die von Sensoren bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="fc5a0-112">The *Sensor* and *Location* APIs provide a standard way to discover sensors, and to programmatically access data that sensors provide.</span></span>

<span data-ttu-id="fc5a0-113">In der Systemsteuerung des *Sensors* können Benutzer Sensoren aktivieren oder deaktivieren, den Zugriff auf Sensoren steuern, die sensible Daten verfügbar machen, Sensor Eigenschaften anzeigen und die Beschreibungen der Sensoren ändern.</span><span class="sxs-lookup"><span data-stu-id="fc5a0-113">The *Sensor* control panel lets users enable or disable sensors, control access to sensors that might expose sensitive data, view sensor properties, and change the descriptions of sensors.</span></span>

<span data-ttu-id="fc5a0-114">Die [Sensor Klassen Erweiterung](/windows-hardware/drivers/sensors/about-the-sensor-class-extension) ist ein zentraler Bestandteil des Treiber Entwicklungsmodells für die Sensorplattform.</span><span class="sxs-lookup"><span data-stu-id="fc5a0-114">The [Sensor Class Extension](/windows-hardware/drivers/sensors/about-the-sensor-class-extension) is a core part of the driver development model for the Sensor Platform.</span></span> <span data-ttu-id="fc5a0-115">Es stellt die folgenden Mechanismen bereit, die verwendet werden, wenn ein Treiber für den [Benutzermodus-Treiber-Frameworks (Endf)](https://developer.microsoft.com/windows/hardware) geschrieben wird:</span><span class="sxs-lookup"><span data-stu-id="fc5a0-115">It provides the following mechanisms, which are used when writing a [User-Mode Driver Framework (UMDF)](https://developer.microsoft.com/windows/hardware) sensor driver:</span></span>

-   <span data-ttu-id="fc5a0-116">Integration mit der Sensor Plattform</span><span class="sxs-lookup"><span data-stu-id="fc5a0-116">Integration with the Sensor Platform</span></span>
-   <span data-ttu-id="fc5a0-117">Sicherheits Durchsetzung</span><span class="sxs-lookup"><span data-stu-id="fc5a0-117">Security enforcement</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc5a0-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fc5a0-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc5a0-119">Sensor-API</span><span class="sxs-lookup"><span data-stu-id="fc5a0-119">Sensor API</span></span>](../sensorsapi/portal.md)
</dt> <dt>