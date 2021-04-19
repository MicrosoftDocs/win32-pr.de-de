---
description: WPD-Anwendungsprogrammierschnittstelle
ms.assetid: 3e2be15f-7af7-4e76-89b1-f9bc591c4f1b
title: WPD-Anwendungsprogrammierschnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c44dbcf731aa46941599b99766e52fa67a5c5a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356965"
---
# <a name="wpd-application-programming-interface"></a><span data-ttu-id="e50ca-103">WPD-Anwendungsprogrammierschnittstelle</span><span class="sxs-lookup"><span data-stu-id="e50ca-103">WPD Application Programming Interface</span></span>

<span data-ttu-id="e50ca-104">Anwendungen, die auf tragbaren Windows-Geräten basieren, können ein Gerät untersuchen, Inhalte senden und empfangen und sogar das Gerät steuern, z. b. ein Bild erstellen oder eine Textnachricht senden.</span><span class="sxs-lookup"><span data-stu-id="e50ca-104">Applications built on Windows Portable Devices can explore a device, send and receive content, and even control the device, for example, take a picture or send a text message.</span></span> <span data-ttu-id="e50ca-105">Das System ist so konzipiert, dass es so flexibel ist, dass viele Arten von Geräten untersucht und erweitert werden können, sodass Treiber Entwickler benutzerdefinierte Eigenschaften und Befehle für benutzerdefinierte Geräte definieren können.</span><span class="sxs-lookup"><span data-stu-id="e50ca-105">The system is designed to be flexible so that many types of devices can be explored, and extensible so that driver developers can define custom properties and commands for custom devices.</span></span>

<span data-ttu-id="e50ca-106">In der folgenden Tabelle werden die Hauptthemen dieser Dokumentation beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e50ca-106">The following table describes the main topics of this documentation.</span></span>



| <span data-ttu-id="e50ca-107">Thema</span><span class="sxs-lookup"><span data-stu-id="e50ca-107">Topic</span></span>                                                                                                                  | <span data-ttu-id="e50ca-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e50ca-108">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e50ca-109">Allgemeine Anforderungen für die Anwendungsentwicklung</span><span class="sxs-lookup"><span data-stu-id="e50ca-109">General Requirements for Application Development</span></span>](general-requirements-for-application-development.md)               | <span data-ttu-id="e50ca-110">Hardware-und Softwareanforderungen für die Entwicklung von Treibern und Anwendungen mithilfe von tragbaren Windows-Geräten.</span><span class="sxs-lookup"><span data-stu-id="e50ca-110">Hardware and software requirements to develop drivers and applications using Windows Portable Devices.</span></span>     |
| [<span data-ttu-id="e50ca-111">Anforderungen für Windows Media DRM-Enabled-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="e50ca-111">Requirements for Windows Media DRM-Enabled Applications</span></span>](requirements-for-windows-media-drm-enabled-applications.md) | <span data-ttu-id="e50ca-112">Eigenschaften, die erforderlich sind, um von Windows Media DRM geschützte Inhalts Übertragungen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="e50ca-112">Properties that are required to enable Windows Media DRM-protected content transfers.</span></span>                      |
| [<span data-ttu-id="e50ca-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e50ca-113">Samples</span></span>](sample.md)                                                                                                  | <span data-ttu-id="e50ca-114">Beschreibung von zwei Desktop Anwendungen für die Befehlszeile, die mit diesem Software Development Kit bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="e50ca-114">Description of two command-line desktop applications that are supplied with this software development kit.</span></span> |
| [<span data-ttu-id="e50ca-115">Anwendungs Übersicht</span><span class="sxs-lookup"><span data-stu-id="e50ca-115">Application Overview</span></span>](application-overview.md)                                                                       | <span data-ttu-id="e50ca-116">Wichtige Konzepte, die auf tragbaren Windows-Geräten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e50ca-116">Key concepts used in Windows Portable Devices.</span></span>                                                             |
| [<span data-ttu-id="e50ca-117">Programmierhandbuch</span><span class="sxs-lookup"><span data-stu-id="e50ca-117">Programming Guide</span></span>](programming-guide.md)                                                                             | <span data-ttu-id="e50ca-118">Wichtige Aufgaben, die eine Anwendung ausführen wird, mit Schritt-für-Schritt-Anleitungen und Code Ausschnitten.</span><span class="sxs-lookup"><span data-stu-id="e50ca-118">Key tasks that an application will perform, with step-by-step instructions and code snippets.</span></span>              |
| [<span data-ttu-id="e50ca-119">Programmierverzeichnis</span><span class="sxs-lookup"><span data-stu-id="e50ca-119">Programming Reference</span></span>](programming-reference.md)                                                                     | <span data-ttu-id="e50ca-120">Referenzhandbuch zu den Schnittstellen und Datentypen, die von tragbaren Windows-Geräten definiert werden.</span><span class="sxs-lookup"><span data-stu-id="e50ca-120">Reference guide to the interfaces and data types defined by Windows Portable Devices.</span></span>                      |



 

<span data-ttu-id="e50ca-121">Anwendungen, die auf Windows Media Device Manager oder Windows-Abbild Käufen basieren, können über eine Kompatibilitätsschicht auf tragbare Windows-Geräte zugreifen.</span><span class="sxs-lookup"><span data-stu-id="e50ca-121">Applications built on Windows Media Device Manager or Windows Image Acquisition can access Windows Portable Devices through a compatibility layer.</span></span>

<span data-ttu-id="e50ca-122">Microsoft stellt verschiedene Treiber für Standardprotokolle und-Geräte bereit, einschließlich Media Transport Protocol (MTP)-Geräten und MSC-Geräten (Massenspeicher Klasse).</span><span class="sxs-lookup"><span data-stu-id="e50ca-122">Microsoft provides several drivers for standard protocols and devices, including Media Transport Protocol (MTP) devices and Mass Storage Class (MSC) devices.</span></span> <span data-ttu-id="e50ca-123">Wenn Sie mit dem User-Mode Driver-Framework vertraut sind, können Sie eigene Treiber für benutzerdefinierte Geräte entwickeln.</span><span class="sxs-lookup"><span data-stu-id="e50ca-123">If you are familiar with the User-Mode Driver Framework, you can develop your own drivers for custom devices.</span></span>

 

 



