---
title: Erweiterter Speicher ist jetzt für die WinPE-und Server-SKU optional.
description: Erweiterter Speicher ist jetzt für die WinPE-und Server-SKU optional.
ms.assetid: 8A6B6194-5867-4B76-BD7B-152FD8A7DD77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7601ee35e6d4be35a39874dd85650f051c1c718
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "104316598"
---
# <a name="enhanced-storage-is-now-optional-for-winpe-and-server-sku"></a><span data-ttu-id="2ceda-103">Erweiterter Speicher ist jetzt für die WinPE-und Server-SKU optional.</span><span class="sxs-lookup"><span data-stu-id="2ceda-103">Enhanced storage is now optional for WINPE and server SKU</span></span>

## <a name="platforms"></a><span data-ttu-id="2ceda-104">Plattformen</span><span class="sxs-lookup"><span data-stu-id="2ceda-104">Platforms</span></span>

<span data-ttu-id="2ceda-105">**Clients** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="2ceda-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="2ceda-106">**Server** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2ceda-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="2ceda-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2ceda-107">Description</span></span>

<span data-ttu-id="2ceda-108">Erweiterter Speicher war immer auf Windows 7-USB-Geräten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2ceda-108">Enhanced storage was always available in Windows 7 USB devices.</span></span> <span data-ttu-id="2ceda-109">Mit der Veröffentlichung von Windows 8 ist es für alle Speichergeräte verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2ceda-109">With the release of Windows 8, it is available for all storage devices.</span></span> <span data-ttu-id="2ceda-110">In Client basierten Geräten ist es standardmäßig aktiviert. auf Server Geräten ist es optional und muss über Windows Preinstallation Environment (WinPE) bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="2ceda-110">In client-based devices, it is enabled by default; in server devices it is optional and must be provisioned through Windows Preinstallation Environment (WinPE).</span></span>

## <a name="manifestation"></a><span data-ttu-id="2ceda-111">Ausstrahlung</span><span class="sxs-lookup"><span data-stu-id="2ceda-111">Manifestation</span></span>

<span data-ttu-id="2ceda-112">Das Server Gerät schlägt fehl, wenn der erweiterte Speicher nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2ceda-112">The server device will fail if enhanced storage is not enabled.</span></span>

<span data-ttu-id="2ceda-113">Start Geräte müssen mithilfe von WinPE bereitgestellt werden, wenn diese Option aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2ceda-113">Boot devices must be provisioned through WinPE with this enabled.</span></span>

## <a name="solution"></a><span data-ttu-id="2ceda-114">Lösung</span><span class="sxs-lookup"><span data-stu-id="2ceda-114">Solution</span></span>

<span data-ttu-id="2ceda-115">Da der erweiterte Speicher für den Lauf Zeitserver optional ist, müssen Entwickler ihn zur Bereitstellung und Aktivierung dieser Laufwerke zu WinPE hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2ceda-115">Because enhanced storage is optional for runtime server, developers must add it to WinPE for provisioning and activation of those drives.</span></span> <span data-ttu-id="2ceda-116">Weitere Informationen finden Sie im Bereitstellungs Handbuch.</span><span class="sxs-lookup"><span data-stu-id="2ceda-116">See the deployment guide for details.</span></span>

<span data-ttu-id="2ceda-117">Server Administratoren müssen dann Ihren Server explizit für die Verwendung von erweitertem Speicher konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="2ceda-117">Server administrators must then explicitly configure their server to use enhanced storage.</span></span>

 

 




