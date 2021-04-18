---
description: 'Weitere Informationen: Einschränkungen des Skript Modells'
ms.assetid: b8ddbfac-5b5e-4aff-beea-82e7fc984790
title: Einschränkungen des Skript Modells
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 36ef43cd2cf2133b126eee065c2b33e463eb6401
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347778"
---
# <a name="limitations-of-the-scripting-model"></a><span data-ttu-id="e235d-103">Einschränkungen des Skript Modells</span><span class="sxs-lookup"><span data-stu-id="e235d-103">Limitations of the Scripting Model</span></span>

> [!Note]  
> <span data-ttu-id="e235d-104">Dieses Skript System wurde durch die Windows-Abbild Erwerbs-Automatisierungs Schicht (WIA) ersetzt.</span><span class="sxs-lookup"><span data-stu-id="e235d-104">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="e235d-105">Weitere Informationen finden Sie unter [Automatisierungs Schicht für Windows-Abbild](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)</span><span class="sxs-lookup"><span data-stu-id="e235d-105">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="e235d-106">Das WIA-Skript Modell (Windows Image Acquisition) stellt eine Teilmenge der WIA-Funktionalität zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="e235d-106">The Windows Image Acquisition (WIA) scripting model exposes a subset of WIA functionality.</span></span> <span data-ttu-id="e235d-107">In der folgenden Tabelle finden Sie Beschreibungen der Einschränkungen des Skript Modells.</span><span class="sxs-lookup"><span data-stu-id="e235d-107">The following table provides descriptions of the limitations of the scripting model.</span></span> 

| <span data-ttu-id="e235d-108">WIA-Funktionalität</span><span class="sxs-lookup"><span data-stu-id="e235d-108">WIA Functionality</span></span>               | <span data-ttu-id="e235d-109">Skript Modell Einschränkung</span><span class="sxs-lookup"><span data-stu-id="e235d-109">Scripting Model Limitation</span></span>                                                                                                                                                                                                                                               |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e235d-110">Unterdrücken der Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="e235d-110">Suppressing the user interface</span></span>  | <span data-ttu-id="e235d-111">Die Benutzeroberfläche zum Festlegen von Geräte/Übertragungseigenschaften kann nicht unterdrückt werden.</span><span class="sxs-lookup"><span data-stu-id="e235d-111">Cannot suppress the user interface for setting device/transfer properties.</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="e235d-112">Festlegen von Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e235d-112">Setting properties</span></span>              | <span data-ttu-id="e235d-113">Geräte-oder Element Eigenschaften können nicht festgelegt (geschrieben) werden.</span><span class="sxs-lookup"><span data-stu-id="e235d-113">Cannot set (write) any device or item properties.</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="e235d-114">Registrieren für Rückruf Ereignisse</span><span class="sxs-lookup"><span data-stu-id="e235d-114">Registering for callback events</span></span> | <span data-ttu-id="e235d-115">Es können nur Benachrichtigungen für drei angegebene Ereignisse empfangen werden: [**ontransfercomplete**](-wia--iwiaevents-ontransfercomplete.md), [**ondeviceconnected**](-wia--iwiaevents-ondeviceconnected.md)und [**ondevicedevi.**](-wia--iwiaevents-ondevicedisconnected.md)</span><span class="sxs-lookup"><span data-stu-id="e235d-115">Can only receive notification for three specified events: [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md), [**OnDeviceConnected**](-wia--iwiaevents-ondeviceconnected.md), and [**OnDeviceDisconnected**](-wia--iwiaevents-ondevicedisconnected.md).</span></span> |
| <span data-ttu-id="e235d-116">Behandlung von Fehlern</span><span class="sxs-lookup"><span data-stu-id="e235d-116">Handling errors</span></span>                 | <span data-ttu-id="e235d-117">WIA-Fehler können nicht behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="e235d-117">Cannot handle WIA errors.</span></span>                                                                                                                                                                                                                                                |



 

 

 
