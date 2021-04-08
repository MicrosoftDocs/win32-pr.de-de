---
title: WinRM-Konstanten und-Enumerationen
description: Windows-Remoteverwaltung verfügt über Bitflags, die zum Erstellen von Sitzungen und Enumerationen sowie für Zugriffs Typen und die Authentifizierung auf einem Proxy Server verwendet werden.
ms.assetid: 17e59245-26a3-4383-a741-4a09f3cfcec6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0789d440ff0f88cc037e0dc9e544ca559c1af5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037265"
---
# <a name="winrm-constants-and-enumerations"></a><span data-ttu-id="ab7ac-103">WinRM-Konstanten und-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="ab7ac-103">WinRM Constants and Enumerations</span></span>

<span data-ttu-id="ab7ac-104">Windows-Remoteverwaltung verfügt über Bitflags, die zum Erstellen von Sitzungen und Enumerationen sowie für Zugriffs Typen und die Authentifizierung auf einem Proxy Server verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab7ac-104">Windows Remote Management has bit flags used in creating sessions and enumerations, and for access types and authentication to a proxy server.</span></span> <span data-ttu-id="ab7ac-105">In der folgenden Liste sind die verschiedenen Bitflags aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="ab7ac-105">The following list lists the different bit flags.</span></span>

<dl> <dt>

<span data-ttu-id="ab7ac-106"><span id="Session_Constants"></span><span id="session_constants"></span><span id="SESSION_CONSTANTS"></span>[Sitzungs Konstanten](session-constants.md)</span><span class="sxs-lookup"><span data-stu-id="ab7ac-106"><span id="Session_Constants"></span><span id="session_constants"></span><span id="SESSION_CONSTANTS"></span>[Session Constants](session-constants.md)</span></span>
</dt> <dd>

<span data-ttu-id="ab7ac-107">Flags, die im *Flags* -Parameter der [**WSMAN. kreatesession**](wsman-createsession.md) -Methode oder der [**iwsman:: | atesession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) -Methode verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab7ac-107">Flags used in *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) or [**IWSMan::CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) methods.</span></span>

</dd> <dt>

<span data-ttu-id="ab7ac-108"><span id="Enumeration_Constants"></span><span id="enumeration_constants"></span><span id="ENUMERATION_CONSTANTS"></span>[**Enumerationskonstanten**](enumeration-constants.md)</span><span class="sxs-lookup"><span data-stu-id="ab7ac-108"><span id="Enumeration_Constants"></span><span id="enumeration_constants"></span><span id="ENUMERATION_CONSTANTS"></span>[**Enumeration Constants**](enumeration-constants.md)</span></span>
</dt> <dd>

<span data-ttu-id="ab7ac-109">Flags, die im *Flags* -Parameter des Aufrufes [**Session. Enumerate**](session-enumerate.md) oder [**iwsmansession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab7ac-109">Flags used in *flags* parameter of call to [**Session.Enumerate**](session-enumerate.md) or [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span></span>

</dd> <dt>

<span data-ttu-id="ab7ac-110"><span id="WSManProxyAuthenticationFlags"></span><span id="wsmanproxyauthenticationflags"></span><span id="WSMANPROXYAUTHENTICATIONFLAGS"></span>[**Wsmanproxyauthenticationflags**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyauthenticationflags)</span><span class="sxs-lookup"><span data-stu-id="ab7ac-110"><span id="WSManProxyAuthenticationFlags"></span><span id="wsmanproxyauthenticationflags"></span><span id="WSMANPROXYAUTHENTICATIONFLAGS"></span>[**WSManProxyAuthenticationFlags**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyauthenticationflags)</span></span>
</dt> <dd>

<span data-ttu-id="ab7ac-111">Flags, die im *authenticationmechanism* -Parameter des Aufrufes [**IWSManConnectionOptionsEx2:: SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab7ac-111">Flags used in *authenticationMechanism* parameter of call to [**IWSManConnectionOptionsEx2::SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy).</span></span>

</dd> <dt>

<span data-ttu-id="ab7ac-112"><span id="WSManProxyAccessTypeFlags"></span><span id="wsmanproxyaccesstypeflags"></span><span id="WSMANPROXYACCESSTYPEFLAGS"></span>[**Wsmanproxyaccesstypflags**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyaccesstypeflags)</span><span class="sxs-lookup"><span data-stu-id="ab7ac-112"><span id="WSManProxyAccessTypeFlags"></span><span id="wsmanproxyaccesstypeflags"></span><span id="WSMANPROXYACCESSTYPEFLAGS"></span>[**WSManProxyAccessTypeFlags**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyaccesstypeflags)</span></span>
</dt> <dd>

<span data-ttu-id="ab7ac-113">Flags, die im *accessType* -Parameter des Aufrufes [**IWSManConnectionOptionsEx2:: SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab7ac-113">Flags used in *accessType* parameter of call to [**IWSManConnectionOptionsEx2::SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy).</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="ab7ac-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ab7ac-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab7ac-115">Windows-Remoteverwaltung Referenz</span><span class="sxs-lookup"><span data-stu-id="ab7ac-115">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> <dt>

[<span data-ttu-id="ab7ac-116">**WSMAN. kreatesession**</span><span class="sxs-lookup"><span data-stu-id="ab7ac-116">**WSMan.CreateSession**</span></span>](wsman-createsession.md)
</dt> <dt>

[<span data-ttu-id="ab7ac-117">**Iwsman:: kreatesession**</span><span class="sxs-lookup"><span data-stu-id="ab7ac-117">**IWSMan::CreateSession**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession)
</dt> <dt>

[<span data-ttu-id="ab7ac-118">**IWSManConnectionOptionsEx2:: SetProxy**</span><span class="sxs-lookup"><span data-stu-id="ab7ac-118">**IWSManConnectionOptionsEx2::SetProxy**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy)
</dt> </dl>

 

 




