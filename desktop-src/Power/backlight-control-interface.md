---
description: Die Timeout-Steuerungs Schnittstelle ist eine standardisierte ioctl-Schnittstelle zum Steuern der Helligkeit des LCD-Timeout.
ms.assetid: edf2b7ed-2676-483a-80ba-f148951e0e58
title: Backlight-Steuerungs Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ecbcc3d635d120c1049f8ec586d7296a953dfac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368746"
---
# <a name="backlight-control-interface"></a><span data-ttu-id="0102a-103">Backlight-Steuerungs Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="0102a-103">Backlight Control Interface</span></span>

<span data-ttu-id="0102a-104">Die Timeout-Steuerungs Schnittstelle ist eine standardisierte ioctl-Schnittstelle zum Steuern der Helligkeit des LCD-Timeout.</span><span class="sxs-lookup"><span data-stu-id="0102a-104">The backlight control interface is a standardized IOCTL interface for controlling the brightness of the LCD backlight.</span></span>

<span data-ttu-id="0102a-105">Anwendungen, die eine programmgesteuerte Steuerung der Hintergrund Helligkeit erfordern oder Steuerelemente für den Benutzer bereitstellen sollten, sollten diese Schnittstelle anstelle einer proprietären Schnittstelle verwenden. Andernfalls kann das System die aktuelle Hardware Helligkeit nicht Abfragen und wird möglicherweise nicht synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="0102a-105">Applications that require programmatic control of the backlight brightness or provide controls for the user to do so should use this interface rather than a proprietary interface; otherwise, the system cannot query the current hardware brightness and may become unsynchronized.</span></span>

<span data-ttu-id="0102a-106">Der erste Schritt besteht darin, das Gerät mit der von der [**IOCTL- \_ Video \_ Abfrage \_ unterstützten \_ Helligkeits**](ioctl-video-query-supported-brightness.md) Steuerungs Code auf die unterstützte Helligkeit abzufragen.</span><span class="sxs-lookup"><span data-stu-id="0102a-106">The first step is to query the device for the supported brightness using the [**IOCTL\_VIDEO\_QUERY\_SUPPORTED\_BRIGHTNESS**](ioctl-video-query-supported-brightness.md) control code.</span></span> <span data-ttu-id="0102a-107">Dieser Vorgang gibt einen Puffer zurück, der die verfügbaren Helligkeits Ebenen angibt.</span><span class="sxs-lookup"><span data-stu-id="0102a-107">This operation returns a buffer that specifies the available brightness levels.</span></span> <span data-ttu-id="0102a-108">Als nächstes können Sie das Gerät mit dem Bildschirm Helligkeit-Steuercode der [**IOCTL- \_ Video \_ \_ \_ Abfrage**](ioctl-video-query-display-brightness.md) auf die aktuelle Anzeige Helligkeit Abfragen.</span><span class="sxs-lookup"><span data-stu-id="0102a-108">Next, you can query the device for the current display brightness using the [**IOCTL\_VIDEO\_QUERY\_DISPLAY\_BRIGHTNESS**](ioctl-video-query-display-brightness.md) control code.</span></span> <span data-ttu-id="0102a-109">Mit diesem Vorgang werden die aktuellen Einstellungen für die abwechselnde Helligkeit (AC), die Current Current (DC)-Helligkeit und den Energiezustand zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0102a-109">This operation returns the current settings for alternating current (AC) brightness, direct current (DC) brightness, and the power state.</span></span>

<span data-ttu-id="0102a-110">Um die Anzeige Helligkeit zu ändern, verwenden Sie den [**IOCTL- \_ \_ Videosatz \_ Anzeige \_ Helligkeit**](ioctl-video-set-display-brightness.md) -Steuerungs Code.</span><span class="sxs-lookup"><span data-stu-id="0102a-110">To change the display brightness, use the [**IOCTL\_VIDEO\_SET\_DISPLAY\_BRIGHTNESS**](ioctl-video-set-display-brightness.md) control code.</span></span> <span data-ttu-id="0102a-111">Sie können die Wechsel stromhelligkeit, die Domänen Controller Helligkeit oder beides festlegen.</span><span class="sxs-lookup"><span data-stu-id="0102a-111">You can set the AC brightness, the DC brightness, or both.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0102a-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0102a-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0102a-113">Informationen zur Energie Verwaltung</span><span class="sxs-lookup"><span data-stu-id="0102a-113">About Power Management</span></span>](about-power-management.md)
</dt> </dl>

 

 



