---
title: Lauf Zeit Schnittstellen RemoteApp-und Desktopverbindung
description: Unterstützt Schnittstellen, die die Entwicklung benutzerdefinierter Clients in RemoteApp-und Desktopverbindung ermöglichen.
ms.assetid: 4580df05-5e44-40d0-8765-5d9b4e1d339e
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste Remotedesktopdienste, RemoteApp-und Desktopverbindung Runtime-API-Referenz
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6b7c3c2fd3841cfe797fc559ba1aa30d3479436
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104100942"
---
# <a name="remoteapp-and-desktop-connection-runtime-interfaces"></a><span data-ttu-id="5df7b-104">Lauf Zeit Schnittstellen RemoteApp-und Desktopverbindung</span><span class="sxs-lookup"><span data-stu-id="5df7b-104">RemoteApp and Desktop Connection Runtime interfaces</span></span>

<span data-ttu-id="5df7b-105">Die RemoteApp-und Desktopverbindung Runtime-API unterstützt Schnittstellen, die die Entwicklung benutzerdefinierter Clients in RemoteApp-und Desktopverbindung ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="5df7b-105">The RemoteApp and Desktop Connection Runtime API supports interfaces that allow the development of custom clients in RemoteApp and Desktop Connection.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5df7b-106">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="5df7b-106">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="5df7b-107">**Iworkspace**</span><span class="sxs-lookup"><span data-stu-id="5df7b-107">**IWorkspace**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspace)
</dt> <dd>

<span data-ttu-id="5df7b-108">Macht Methoden verfügbar, die Informationen zu einer Verbindung in RemoteApp-und Desktopverbindung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5df7b-108">Exposes methods that provide information about a connection in RemoteApp and Desktop Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="5df7b-109">**IWorkspace2**</span><span class="sxs-lookup"><span data-stu-id="5df7b-109">**IWorkspace2**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspace2)
</dt> <dd>

<span data-ttu-id="5df7b-110">Macht zusätzliche Methoden verfügbar, die Informationen zu einer Verbindung in RemoteApp-und Desktopverbindung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5df7b-110">Exposes additional methods that provide information about a connection in RemoteApp and Desktop Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="5df7b-111">**IWorkspace3**</span><span class="sxs-lookup"><span data-stu-id="5df7b-111">**IWorkspace3**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspace3)
</dt> <dd>

<span data-ttu-id="5df7b-112">Macht Methoden verfügbar, die Informationen zu einer Verbindung in RemoteApp-und Desktopverbindung bereitstellen, und bietet die Möglichkeit, ein Anspruchs Token abzurufen oder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="5df7b-112">Exposes methods that provide information about a connection in RemoteApp and Desktop Connection, and adds the ability to retrieve or set a claims token.</span></span>

</dd> <dt>

[<span data-ttu-id="5df7b-113">**Iworkspaceclikotext**</span><span class="sxs-lookup"><span data-stu-id="5df7b-113">**IWorkspaceClientExt**</span></span>](/windows/desktop/api/Workspaceruntimeclientext/nn-workspaceruntimeclientext-iworkspaceclientext)
</dt> <dd>

<span data-ttu-id="5df7b-114">Macht Methoden verfügbar, mit denen die Common Language Runtime einen benutzerdefinierten Client in RemoteApp-und Desktopverbindung trennen kann.</span><span class="sxs-lookup"><span data-stu-id="5df7b-114">Exposes methods that allow the runtime to disconnect a custom client in RemoteApp and Desktop Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="5df7b-115">**Iworkspaceregistration**</span><span class="sxs-lookup"><span data-stu-id="5df7b-115">**IWorkspaceRegistration**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspaceregistration)
</dt> <dd>

<span data-ttu-id="5df7b-116">Macht Methoden verfügbar, mit denen in RemoteApp-und Desktopverbindung Verweise auf benutzerdefinierte Clients hinzugefügt und entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="5df7b-116">Exposes methods that add and remove references to custom clients in RemoteApp and Desktop Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="5df7b-117">**IWorkspaceRegistration2**</span><span class="sxs-lookup"><span data-stu-id="5df7b-117">**IWorkspaceRegistration2**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspaceregistration2)
</dt> <dd>

<span data-ttu-id="5df7b-118">Macht Methoden verfügbar, mit denen in RemoteApp-und Desktopverbindung Verweise auf benutzerdefinierte Clients hinzugefügt und entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="5df7b-118">Exposes methods that add and remove references to custom clients in RemoteApp and Desktop Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="5df7b-119">**Iworkspacereportmessage**</span><span class="sxs-lookup"><span data-stu-id="5df7b-119">**IWorkspaceReportMessage**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacereportmessage)
</dt> <dd>

<span data-ttu-id="5df7b-120">Macht Methoden verfügbar, die die Behandlung von Fehlermeldungen für Remote Arbeitsbereiche unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5df7b-120">Exposes methods that support error message handling for remote workspaces.</span></span>

</dd> <dt>

[<span data-ttu-id="5df7b-121">**Iworkspacerestyperegistry**</span><span class="sxs-lookup"><span data-stu-id="5df7b-121">**IWorkspaceResTypeRegistry**</span></span>](/windows/desktop/api/Workspaceax/nn-workspaceax-iworkspacerestyperegistry)
</dt> <dd>

<span data-ttu-id="5df7b-122">Macht Methoden verfügbar, mit denen ein Plug-in Dateinamen Erweiterungen von Drittanbietern in RemoteApp-und Desktopverbindung Laufzeit verwalten kann.</span><span class="sxs-lookup"><span data-stu-id="5df7b-122">Exposes methods that allow a plug-in to manage third-party file name extensions in RemoteApp and Desktop Connection runtime.</span></span>

</dd> <dt>

[<span data-ttu-id="5df7b-123">**Iworkspacescriptable**</span><span class="sxs-lookup"><span data-stu-id="5df7b-123">**IWorkspaceScriptable**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable)
</dt> <dd>

<span data-ttu-id="5df7b-124">Macht Methoden verfügbar, die RemoteApp-und Desktopverbindung Anmelde Informationen und Verbindungen verwalten.</span><span class="sxs-lookup"><span data-stu-id="5df7b-124">Exposes methods that manage RemoteApp and Desktop Connection credentials and connections.</span></span>

</dd> <dt>

[<span data-ttu-id="5df7b-125">**IWorkspaceScriptable2**</span><span class="sxs-lookup"><span data-stu-id="5df7b-125">**IWorkspaceScriptable2**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable2)
</dt> <dd>

<span data-ttu-id="5df7b-126">Macht Methoden verfügbar, die RemoteApp-und Desktopverbindung Anmelde Informationen und Verbindungen verwalten.</span><span class="sxs-lookup"><span data-stu-id="5df7b-126">Exposes methods that manage RemoteApp and Desktop Connection credentials and connections.</span></span>

</dd> <dt>

[<span data-ttu-id="5df7b-127">**IWorkspaceScriptable3**</span><span class="sxs-lookup"><span data-stu-id="5df7b-127">**IWorkspaceScriptable3**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable3)
</dt> <dd>

<span data-ttu-id="5df7b-128">Macht Methoden verfügbar, die RemoteApp-und Desktopverbindung Anmelde Informationen und Verbindungen verwalten.</span><span class="sxs-lookup"><span data-stu-id="5df7b-128">Exposes methods that manage RemoteApp and Desktop Connection credentials and connections.</span></span>

</dd> </dl>

 

 




