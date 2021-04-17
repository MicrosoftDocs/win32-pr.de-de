---
title: Iremotedesktopclient-Methoden
description: Die iremotedesktopclient-Schnittstelle stellt die folgenden Methoden zur Verfügung.
ms.assetid: CE2BC8B5-ED33-451C-87E0-32192BF41334
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da56cc283eec90176fc476517517783744d71caf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390550"
---
# <a name="iremotedesktopclient-methods"></a><span data-ttu-id="3abf9-103">Iremotedesktopclient-Methoden</span><span class="sxs-lookup"><span data-stu-id="3abf9-103">IRemoteDesktopClient methods</span></span>

<span data-ttu-id="3abf9-104">Die [**iremotedesktopclient**](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclient) -Schnittstelle stellt die folgenden Methoden zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="3abf9-104">The [**IRemoteDesktopClient**](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclient) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3abf9-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="3abf9-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="3abf9-106">**AttachEvent-Methode**</span><span class="sxs-lookup"><span data-stu-id="3abf9-106">**attachEvent method**</span></span>](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-attachevent)
</dt> <dd>

<span data-ttu-id="3abf9-107">Fügt einem Ereignis einen Ereignishandler an.</span><span class="sxs-lookup"><span data-stu-id="3abf9-107">Attaches an event handler to an event.</span></span>

</dd> <dt>

[<span data-ttu-id="3abf9-108">**Connect-Methode**</span><span class="sxs-lookup"><span data-stu-id="3abf9-108">**Connect method**</span></span>](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-connect)
</dt> <dd>

<span data-ttu-id="3abf9-109">Initiiert eine Verbindung mit den Eigenschaften, die derzeit auf dem Client Steuerelement für die Remotedesktopprotokoll (RDP)-app-Container festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="3abf9-109">Initiates a connection by using the properties currently set on the Remote Desktop Protocol (RDP) app container client control.</span></span>

</dd> <dt>

[<span data-ttu-id="3abf9-110">**Delta esaved-Anmelde Informationen-Methode**</span><span class="sxs-lookup"><span data-stu-id="3abf9-110">**DeleteSavedCredentials method**</span></span>](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-deletesavedcredentials)
</dt> <dd>

<span data-ttu-id="3abf9-111">Löscht gespeicherte Anmelde Informationen für den angegebenen Remote Computer.</span><span class="sxs-lookup"><span data-stu-id="3abf9-111">Deletes saved credentials for the specified remote computer.</span></span>

</dd> <dt>

[<span data-ttu-id="3abf9-112">**DetachEvent-Methode**</span><span class="sxs-lookup"><span data-stu-id="3abf9-112">**detachEvent method**</span></span>](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-detachevent)
</dt> <dd>

<span data-ttu-id="3abf9-113">Trennt einen Ereignishandler von einem Ereignis.</span><span class="sxs-lookup"><span data-stu-id="3abf9-113">Detaches an event handler from an event.</span></span>

</dd> <dt>

[<span data-ttu-id="3abf9-114">**Disconnect-Methode**</span><span class="sxs-lookup"><span data-stu-id="3abf9-114">**Disconnect method**</span></span>](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-disconnect)
</dt> <dd>

<span data-ttu-id="3abf9-115">Trennt die aktive Verbindung.</span><span class="sxs-lookup"><span data-stu-id="3abf9-115">Disconnects the active connection.</span></span>

</dd> <dt>

[<span data-ttu-id="3abf9-116">**Reconnect-Methode**</span><span class="sxs-lookup"><span data-stu-id="3abf9-116">**Reconnect method**</span></span>](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-reconnect)
</dt> <dd>

<span data-ttu-id="3abf9-117">Initiiert eine automatische erneute Verbindung Remotedesktopprotokoll des Client Steuer Elements (RDP)-app-Container, um die Sitzung an die neue Breite und Höhe anzupassen.</span><span class="sxs-lookup"><span data-stu-id="3abf9-117">Initiates an automatic reconnection of the Remote Desktop Protocol (RDP) app container client control to fit the session to the new width and height.</span></span>

</dd> <dt>

[<span data-ttu-id="3abf9-118">**Updatesessiondisplaysettings-Methode**</span><span class="sxs-lookup"><span data-stu-id="3abf9-118">**UpdateSessionDisplaySettings method**</span></span>](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-updatesessiondisplaysettings)
</dt> <dd>

<span data-ttu-id="3abf9-119">Aktualisiert die breiten-und Höheneinstellungen für das Client Steuerelement für die Remotedesktopprotokoll (RDP)-app-Container.</span><span class="sxs-lookup"><span data-stu-id="3abf9-119">Updates the width and height settings for the Remote Desktop Protocol (RDP) app container client control.</span></span>

</dd> </dl>

 

 