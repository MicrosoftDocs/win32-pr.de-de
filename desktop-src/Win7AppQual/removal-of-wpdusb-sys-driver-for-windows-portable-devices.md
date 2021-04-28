---
description: Entfernen des WPDUSB.SYS-Treibers für portable Windows-Geräte
ms.assetid: 3ad0c892-8b19-465d-af2f-9207f98e27b7
title: Entfernen des WPDUSB.SYS-Treibers für portable Windows-Geräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5931b63c5abb4534b2c8dd6619b4a3ead8b339be
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116248"
---
# <a name="removal-of-wpdusbsys-driver-for-windows-portable-devices"></a><span data-ttu-id="6d891-103">Entfernen des WPDUSB.SYS-Treibers für portable Windows-Geräte</span><span class="sxs-lookup"><span data-stu-id="6d891-103">Removal of WPDUSB.SYS Driver for Windows Portable Devices</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="6d891-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="6d891-104">Affected Platforms</span></span>

<span data-ttu-id="6d891-105">**Clients** – Windows 7</span><span class="sxs-lookup"><span data-stu-id="6d891-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="6d891-106">**Server** – Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6d891-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="6d891-107">Auswirkung von Features</span><span class="sxs-lookup"><span data-stu-id="6d891-107">Feature Impact</span></span>

 <span data-ttu-id="6d891-108">**Schweregrad:** Niedrig</span><span class="sxs-lookup"><span data-stu-id="6d891-108">**Severity** - Low</span></span>  
<span data-ttu-id="6d891-109">**Häufigkeit** – Niedrig</span><span class="sxs-lookup"><span data-stu-id="6d891-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="6d891-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6d891-110">Description</span></span>

<span data-ttu-id="6d891-111">Microsoft hat die Kernelmoduskomponente des Windows Vista-USB-Treiberstapels (WPDUSB.SYS) für Windows Portable Devices (WPD) durch den generischen WINUSB.SYS ersetzt.</span><span class="sxs-lookup"><span data-stu-id="6d891-111">Microsoft has replaced the kernel mode component of the Windows Vista USB driver stack (WPDUSB.SYS) for Windows Portable Devices (WPD) with the generic WINUSB.SYS driver.</span></span> <span data-ttu-id="6d891-112">Die Kommunikation mit dem ursprünglichen WPDUSB.SYS-Treiber erfolgt über private I/O-Steuerungscodes (IOCTL). Die Unterstützung dieser wurde ebenfalls entfernt.</span><span class="sxs-lookup"><span data-stu-id="6d891-112">Communication with the original WPDUSB.SYS driver was via private I/O Control (IOCTL) codes; support of these has also been removed.</span></span>

<span data-ttu-id="6d891-113">Jeder Consumer dieser IOCTL-Codes wäre für die ordnungsgemäße Interpretation und Implementierung des Media Transfer Protocol (MTP) verantwortlich gewesen.</span><span class="sxs-lookup"><span data-stu-id="6d891-113">Any consumer of these IOCTL codes would have been responsible for proper interpretation and implementation of the Media Transfer Protocol (MTP).</span></span> <span data-ttu-id="6d891-114">Windows Vista hat die Verwendung dieser IOCTL-Codes durch Drittanbieteranwendungen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6d891-114">Windows Vista did not support use of these IOCTL codes by third-party applications.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="6d891-115">Auswirkungen</span><span class="sxs-lookup"><span data-stu-id="6d891-115">Manifestation of Impact</span></span>

<span data-ttu-id="6d891-116">Jede Anwendung, die von der Verfügbarkeit dieser privaten IOCTL-Codes abhängig ist, hat keinen Zugriff mehr auf mit USB verbundene MTP-Geräte.</span><span class="sxs-lookup"><span data-stu-id="6d891-116">Any application that depended on the availability of these private IOCTL codes would no longer have access to USB-connected MTP devices.</span></span>

## <a name="mitigation"></a><span data-ttu-id="6d891-117">Minderung</span><span class="sxs-lookup"><span data-stu-id="6d891-117">Mitigation</span></span>

<span data-ttu-id="6d891-118">Benutzer einer Anwendung, die von den privaten IOCTL-Codes abhängig ist, müssen eine andere Anwendung (oder eine aktualisierte Version der Anwendung) verwenden, um auf das mit USB verbundene MTP-Gerät zu zugreifen.</span><span class="sxs-lookup"><span data-stu-id="6d891-118">Users of an application that depends on the private IOCTL codes must use a different application (or an updated version of the application) to access the USB-connected MTP device.</span></span>

## <a name="solution"></a><span data-ttu-id="6d891-119">Lösung</span><span class="sxs-lookup"><span data-stu-id="6d891-119">Solution</span></span>

<span data-ttu-id="6d891-120">Anwendungen sollten die WPD-API (Windows Portable Devices) verwenden, um wpd-Geräte zu suchen und mit ihnen zu interagieren.</span><span class="sxs-lookup"><span data-stu-id="6d891-120">Applications should use the Windows Portable Devices (WPD) API to find and interact with any WPD Device.</span></span> <span data-ttu-id="6d891-121">Obwohl ein signifikanter Prozentsatz der WPD-Geräte MTP für die Kommunikation mit dem PC implementiert, ist WPD nicht nur auf MTP-Geräte beschränkt.</span><span class="sxs-lookup"><span data-stu-id="6d891-121">Although a significant percentage of WPD devices implement MTP for communication with the PC, WPD is not limited to just MTP devices.</span></span> <span data-ttu-id="6d891-122">Wenn der direkte Zugriff auf das Gerät über die privaten IOCTLs die Anwendung auf die Kommunikation mit geräten mit USB-Verbindung beschränkt hätte, erweitert die Verwendung der WPD-API die Liste der Konnektivitätsoptionen auf andere Kommunikationsprotokolle (z. B. WLAN).</span><span class="sxs-lookup"><span data-stu-id="6d891-122">In addition, where direct access to the device via the private IOCTLs would have limited the application to communication with only USB-connected devices, use of the WPD API expands the list of connectivity options to other communication protocols (for example, Wi-Fi).</span></span> <span data-ttu-id="6d891-123">In den seltenen Fällen, in denen die Anwendung MTP-bewusst sein muss, stellt die WPD-API einen Pass-Through-Mechanismus für unformatierte MTP-Befehle bereit.</span><span class="sxs-lookup"><span data-stu-id="6d891-123">In the rare cases when the application must be MTP-aware, the WPD API provides a pass-through mechanism for raw MTP commands.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="6d891-124">Nutzen von Featurefunktionen</span><span class="sxs-lookup"><span data-stu-id="6d891-124">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="6d891-125">Die WPD-API wird in Windows XP (über das Windows Format SDK), Windows Vista und Windows 7 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6d891-125">The WPD API is supported in Windows XP (via the Windows Format SDK), Windows Vista and Windows 7.</span></span> <span data-ttu-id="6d891-126">Die Windows 7-Implementierung von WPD fügt Unterstützung für MTP über Bluetooth hinzu.</span><span class="sxs-lookup"><span data-stu-id="6d891-126">The Windows 7 implementation of WPD adds support for MTP over Bluetooth.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="6d891-127">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6d891-127">Links to Other Resources</span></span>

[<span data-ttu-id="6d891-128">Portable Windows-Geräte</span><span class="sxs-lookup"><span data-stu-id="6d891-128">Windows Portable Devices</span></span>](../windows-portable-devices.md)

 

 
