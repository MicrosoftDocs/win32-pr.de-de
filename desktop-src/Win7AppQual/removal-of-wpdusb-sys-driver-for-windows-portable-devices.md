---
description: .
ms.assetid: 3ad0c892-8b19-465d-af2f-9207f98e27b7
title: Entfernen von WPDUSB.SYS Treiber für tragbare Windows-Geräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1d602c8277a5c256332b3eaec6a383997d5c63d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362919"
---
# <a name="removal-of-wpdusbsys-driver-for-windows-portable-devices"></a><span data-ttu-id="016c0-103">Entfernen von WPDUSB.SYS Treiber für tragbare Windows-Geräte</span><span class="sxs-lookup"><span data-stu-id="016c0-103">Removal of WPDUSB.SYS Driver for Windows Portable Devices</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="016c0-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="016c0-104">Affected Platforms</span></span>

<span data-ttu-id="016c0-105">**Clients** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="016c0-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="016c0-106">**Server** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="016c0-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="016c0-107">Auswirkungen von Features</span><span class="sxs-lookup"><span data-stu-id="016c0-107">Feature Impact</span></span>

 <span data-ttu-id="016c0-108">**Schweregrad** -niedrig</span><span class="sxs-lookup"><span data-stu-id="016c0-108">**Severity** - Low</span></span>  
<span data-ttu-id="016c0-109">**Häufigkeit** -niedrig</span><span class="sxs-lookup"><span data-stu-id="016c0-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="016c0-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="016c0-110">Description</span></span>

<span data-ttu-id="016c0-111">Microsoft hat die Kernelmoduskomponente des Windows Vista-USB-Treiber Stapels (WPDUSB.SYS) für Windows Portable Devices (WPD) mit dem generischen WINUSB.SYS-Treiber ersetzt.</span><span class="sxs-lookup"><span data-stu-id="016c0-111">Microsoft has replaced the kernel mode component of the Windows Vista USB driver stack (WPDUSB.SYS) for Windows Portable Devices (WPD) with the generic WINUSB.SYS driver.</span></span> <span data-ttu-id="016c0-112">Die Kommunikation mit dem ursprünglichen WPDUSB.SYS Treiber erfolgte über private e/a-Steuerungs Codes (IOCTL). Diese Unterstützung wurde ebenfalls entfernt.</span><span class="sxs-lookup"><span data-stu-id="016c0-112">Communication with the original WPDUSB.SYS driver was via private I/O Control (IOCTL) codes; support of these has also been removed.</span></span>

<span data-ttu-id="016c0-113">Jeder Consumer dieser ioctl-Codes wäre für die ordnungsgemäße Interpretation und Implementierung von MTP (Media Transfer Protocol) verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="016c0-113">Any consumer of these IOCTL codes would have been responsible for proper interpretation and implementation of the Media Transfer Protocol (MTP).</span></span> <span data-ttu-id="016c0-114">Die Verwendung dieser ioctl-Codes durch Drittanbieter Anwendungen wurde von Windows Vista nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="016c0-114">Windows Vista did not support use of these IOCTL codes by third-party applications.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="016c0-115">Erscheinung der Auswirkung</span><span class="sxs-lookup"><span data-stu-id="016c0-115">Manifestation of Impact</span></span>

<span data-ttu-id="016c0-116">Alle Anwendungen, die von der Verfügbarkeit dieser privaten ioctl-Codes abhängen, haben keinen Zugriff mehr auf USB-verbundene MTP-Geräte.</span><span class="sxs-lookup"><span data-stu-id="016c0-116">Any application that depended on the availability of these private IOCTL codes would no longer have access to USB-connected MTP devices.</span></span>

## <a name="mitigation"></a><span data-ttu-id="016c0-117">Minderung</span><span class="sxs-lookup"><span data-stu-id="016c0-117">Mitigation</span></span>

<span data-ttu-id="016c0-118">Benutzer einer Anwendung, die von den privaten ioctl-Codes abhängig ist, müssen eine andere Anwendung (oder eine aktualisierte Version der Anwendung) verwenden, um auf das USB-verbundene MTP-Gerät zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="016c0-118">Users of an application that depends on the private IOCTL codes must use a different application (or an updated version of the application) to access the USB-connected MTP device.</span></span>

## <a name="solution"></a><span data-ttu-id="016c0-119">Lösung</span><span class="sxs-lookup"><span data-stu-id="016c0-119">Solution</span></span>

<span data-ttu-id="016c0-120">Anwendungen sollten mithilfe der WPD-API (Portable Devices) von Windows beliebige WPD-Geräte suchen und mit ihnen interagieren.</span><span class="sxs-lookup"><span data-stu-id="016c0-120">Applications should use the Windows Portable Devices (WPD) API to find and interact with any WPD Device.</span></span> <span data-ttu-id="016c0-121">Obwohl ein erheblicher Prozentsatz von WPD-Geräten MTP für die Kommunikation mit dem PC implementiert, ist WPD nicht auf MTP-Geräte beschränkt.</span><span class="sxs-lookup"><span data-stu-id="016c0-121">Although a significant percentage of WPD devices implement MTP for communication with the PC, WPD is not limited to just MTP devices.</span></span> <span data-ttu-id="016c0-122">Darüber hinaus erweitert der direkte Zugriff auf das Gerät über die private IOCTLs die Anwendung auf die Kommunikation mit nur USB-Geräten, die mithilfe der WPD-API die Liste der Konnektivitätsoptionen auf andere Kommunikationsprotokolle (z. b. Wi-Fi) erweitert.</span><span class="sxs-lookup"><span data-stu-id="016c0-122">In addition, where direct access to the device via the private IOCTLs would have limited the application to communication with only USB-connected devices, use of the WPD API expands the list of connectivity options to other communication protocols (for example, Wi-Fi).</span></span> <span data-ttu-id="016c0-123">In den seltenen Fällen, in denen die Anwendung MTP-fähig sein muss, stellt die WPD-API einen Pass-Through-Mechanismus für unformatierte MTP-Befehle bereit.</span><span class="sxs-lookup"><span data-stu-id="016c0-123">In the rare cases when the application must be MTP-aware, the WPD API provides a pass-through mechanism for raw MTP commands.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="016c0-124">Nutzen von Featurefunktionen</span><span class="sxs-lookup"><span data-stu-id="016c0-124">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="016c0-125">Die WPD-API wird in Windows XP (über das Windows-Format-SDK), Windows Vista und Windows 7 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="016c0-125">The WPD API is supported in Windows XP (via the Windows Format SDK), Windows Vista and Windows 7.</span></span> <span data-ttu-id="016c0-126">Die Windows 7-Implementierung von WPD bietet Unterstützung für MTP über Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="016c0-126">The Windows 7 implementation of WPD adds support for MTP over Bluetooth.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="016c0-127">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="016c0-127">Links to Other Resources</span></span>

[<span data-ttu-id="016c0-128">Tragbare Windows-Geräte</span><span class="sxs-lookup"><span data-stu-id="016c0-128">Windows Portable Devices</span></span>](../windows-portable-devices.md)

 

 
