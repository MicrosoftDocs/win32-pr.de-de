---
description: .
ms.assetid: fb2c487a-d395-45eb-9010-936a61a414d0
title: Windows-Problembehandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eacea2f4f62852da7fbaefd51db5834907a323ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349638"
---
# <a name="windows-troubleshooting"></a><span data-ttu-id="7d229-103">Windows-Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="7d229-103">Windows Troubleshooting</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="7d229-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="7d229-104">Affected Platforms</span></span>

<span data-ttu-id="7d229-105">**Clients** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="7d229-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="7d229-106">**Server** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7d229-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="description"></a><span data-ttu-id="7d229-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7d229-107">Description</span></span>

<span data-ttu-id="7d229-108">Ein neues Windows 7-Wartungs Center (früher als Solutions Center bezeichnet) Feature, Windows-Problembehandlung, bietet eine systematische Problembehandlung für den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="7d229-108">A new Windows 7 Action Center (formerly known as Solutions Center) feature, Windows Troubleshooting, delivers a systematic troubleshooting experience for the user.</span></span> <span data-ttu-id="7d229-109">Das Aktions Center ist eines der fünf Symbole, die im Systray fixiert werden.</span><span class="sxs-lookup"><span data-stu-id="7d229-109">The Action Center is one of the five icons pinned in the systray.</span></span> <span data-ttu-id="7d229-110">Mithilfe der Windows-Problembehandlung können Sie die in-Box-Problem Behebungs Pakete suchen und die Problembehandlung bei Paketen durchsuchen, die auf einem Microsoft-Server im Internet gespeichert sind – ein besseres, wenn die Verbindung hergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7d229-110">Windows Troubleshooting allows you to browse or search for in-box troubleshooting packs and for troubleshooting packs that are stored on a Microsoft server on the Internet – a Better When Connected (BWC) experience.</span></span> <span data-ttu-id="7d229-111">Sie können ein Problem Behandlungspaket auswählen und ausführen, um zu versuchen, das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="7d229-111">You can select and run a troubleshooting pack to attempt to resolve their problem.</span></span> <span data-ttu-id="7d229-112">Wenn Sie keine Lösung für das Problem finden können, haben Sie die Möglichkeit, Hilfe, Communityinhalte, Support Artikel oder andere Problem Behandlungspakete für relevante verwandte Inhalte zu suchen.</span><span class="sxs-lookup"><span data-stu-id="7d229-112">If you cannot identify a resolution to the problem, you have the option of searching help, community content, and support articles, or other troubleshooting packs for relevant related content.</span></span> <span data-ttu-id="7d229-113">Sollten Sie keine Antwort auf das Problem haben, können Sie den PC auf einen Zeitpunkt vor dem Auftreten des Problems wiederherstellen oder Hilfe durch Remote Unterstützung erhalten.</span><span class="sxs-lookup"><span data-stu-id="7d229-113">Should that not provide an answer to the problem, you can restore the PC to a time prior to when the problem occurred or get help through remote assistance.</span></span> <span data-ttu-id="7d229-114">Ziel ist es, Ihnen das einfache und schnelle Auffinden einer Lösung für das Problem zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="7d229-114">The intent is to allow you to find a solution to the problem easily and quickly.</span></span>

## <a name="usage"></a><span data-ttu-id="7d229-115">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="7d229-115">Usage</span></span>

<span data-ttu-id="7d229-116">Das Wartungs Center ist deutlich sichtbar und über mehrere Standorte verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7d229-116">The Action Center is clearly visible and available from several locations.</span></span> <span data-ttu-id="7d229-117">Sie können Sie über das Kontextmenü des Aktions Centers im Systray starten, in der Systemsteuerung als Verknüpfungs Verknüpfung unter System und Wartung, auf der Hauptseite des Aktions Centers und in Hilfe Inhalt.</span><span class="sxs-lookup"><span data-stu-id="7d229-117">You can launch it from the context menu of the Action Center in the systray, from the control panel as a shortcut link under system and maintenance, from the main page of the Action Center, and from Help content.</span></span>

<span data-ttu-id="7d229-118">Fehler Behebungs Pakete basieren auf PowerShell-Skripts.</span><span class="sxs-lookup"><span data-stu-id="7d229-118">Troubleshooting packs are based upon powershell scripts.</span></span> <span data-ttu-id="7d229-119">Der Prozess der Erstellung und Veröffentlichung eines Problembehandlungs Pakets wird öffentlich gemacht, um OEMs, IHVs, ISVs und IT-Experten zu ermöglichen, eigene Problem Behandlungs Inhalte zu entwickeln und bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="7d229-119">The process of authoring and publishing a troubleshooting pack will be made public to allow OEMs, IHVs, ISVs, and IT Professionals to develop and ship their own troubleshooting content.</span></span>

<span data-ttu-id="7d229-120">Beachten Sie für eine konsistente Benutzer Darstellung die bewährten Methoden und Richtlinien, die im Windows-Problem Behandlungs-Toolkit beschrieben sind, wenn Sie Ihre eigenen Fehler Behebungs Pakete entwerfen.</span><span class="sxs-lookup"><span data-stu-id="7d229-120">For a consistent user experience, be sure to follow the best practices and guidelines described in the Windows troubleshooting toolkit when designing your own troubleshooting packs.</span></span>

 

 



