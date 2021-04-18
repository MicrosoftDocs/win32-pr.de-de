---
title: Sitzungs Konstanten
description: Die Sitzungs Konstanten in der \_ \_ wsmansessionflags-Enumeration geben die Authentifizierung und andere Informationen für die Aufrufe WSMAN. anatesession oder iwsman-Befehle an, die eine Verbindung mit einem Remote Computer herstellen.
ms.assetid: 5df52696-ac2c-42b7-8b0f-99a27b58575b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8417289a218203dbdaee288ff03096d894f4bd4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338160"
---
# <a name="session-constants"></a><span data-ttu-id="a794c-103">Sitzungs Konstanten</span><span class="sxs-lookup"><span data-stu-id="a794c-103">Session Constants</span></span>

<span data-ttu-id="a794c-104">Die Sitzungs Konstanten in der **\_ \_ wsmansessionflags** -Enumeration geben die Authentifizierung und andere Informationen für die Aufrufe [**WSMAN. foratesession**](wsman-createsession.md) oder [**iwsman:: foratesession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) an, die eine Verbindung mit einem Remote Computer herstellen.</span><span class="sxs-lookup"><span data-stu-id="a794c-104">The session constants in the **\_\_WSManSessionFlags** enumeration specify authentication and other information for [**WSMan.CreateSession**](wsman-createsession.md) or [**IWSMan::CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) calls that connect to a remote computer.</span></span> <span data-ttu-id="a794c-105">Diese Konstanten sind auch eng mit den **WinRM** -Befehlszeilen Tool-Switches verknüpft.</span><span class="sxs-lookup"><span data-stu-id="a794c-105">These constants are also closely related to **Winrm** command-line tool switches.</span></span>

## <a name="using-session-constants"></a><span data-ttu-id="a794c-106">Verwenden von Sitzungs Konstanten</span><span class="sxs-lookup"><span data-stu-id="a794c-106">Using Session Constants</span></span>

<span data-ttu-id="a794c-107">Sie können die Sitzungsflags für den Aufrufen von [**WSMAN. kreatesession**](wsman-createsession.md) auf zwei verschiedene Arten festlegen.</span><span class="sxs-lookup"><span data-stu-id="a794c-107">You can set the Session flags for the call to [**WSMan.CreateSession**](wsman-createsession.md) in two different ways.</span></span> <span data-ttu-id="a794c-108">Eine ist kürzer und einfacher.</span><span class="sxs-lookup"><span data-stu-id="a794c-108">One is shorter and simpler.</span></span> <span data-ttu-id="a794c-109">Die längere Methode, wie im folgenden Beispiel gezeigt, besteht darin, den Wert des Flags zu suchen, das Sie verwenden möchten, und eine Konstante in Ihrem Skript mit diesem Wert zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a794c-109">The longer way, as is shown in the following example, is to locate the value of the flag you want to use and create a constant in your script with that value.</span></span> <span data-ttu-id="a794c-110">Anschließend wird die Konstante verwendet, um den Wert des *IFlags* -Parameters festzulegen.</span><span class="sxs-lookup"><span data-stu-id="a794c-110">Then the constant is used to set the value of the *iFlags* parameter.</span></span>

``` syntax
Const SessionFlagUseNegotiate = 131072
Const SessionFlagCredUserNamePassword = 4096
iFlags = SessionFlagUseNegotiate Or SessionFlagCredUserNamePassword
```

<span data-ttu-id="a794c-111">Die empfohlene Vorgehensweise, wie im folgenden Beispiel gezeigt, ist die Verwendung der [**WSMAN**](wsman.md) -Objektmethode, die mit dem-Flag verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="a794c-111">The recommended way, as shown in the following example, is to use the [**WSMan**](wsman.md) object method associated with the flag.</span></span>

``` syntax
iFlags = Wsman.SessionFlagUseNegotiate Or Wsman.SessionFlagCredUserNamePassword
```

<dl> <dt>

<span data-ttu-id="a794c-112"><span id="Authentication_Constants"></span><span id="authentication_constants"></span><span id="AUTHENTICATION_CONSTANTS"></span>[**Authentifizierungs Konstanten**](authentication-constants.md)</span><span class="sxs-lookup"><span data-stu-id="a794c-112"><span id="Authentication_Constants"></span><span id="authentication_constants"></span><span id="AUTHENTICATION_CONSTANTS"></span>[**Authentication Constants**](authentication-constants.md)</span></span>
</dt> <dd>

<span data-ttu-id="a794c-113">Geben Sie die Authentifizierungsmethode und die Vorgehensweise zum Behandeln von Zertifikat Servern an.</span><span class="sxs-lookup"><span data-stu-id="a794c-113">Specify the authentication method and how to handle certificate servers.</span></span>

</dd> <dt>

<span data-ttu-id="a794c-114"><span id="Other_Session_Constants"></span><span id="other_session_constants"></span><span id="OTHER_SESSION_CONSTANTS"></span>[**Andere Sitzungs Konstanten**](other-session-constants.md)</span><span class="sxs-lookup"><span data-stu-id="a794c-114"><span id="Other_Session_Constants"></span><span id="other_session_constants"></span><span id="OTHER_SESSION_CONSTANTS"></span>[**Other Session Constants**](other-session-constants.md)</span></span>
</dt> <dd>

<span data-ttu-id="a794c-115">Geben Sie den Port für Codierung, Verschlüsselung und Dienst Prinzipal Name an.</span><span class="sxs-lookup"><span data-stu-id="a794c-115">Specify the encoding, encryption, and service principal name port.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="a794c-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a794c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a794c-117">WinRM-Konstanten und-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="a794c-117">WinRM Constants and Enumerations</span></span>](winrm-constants-and-enumerations.md)
</dt> <dt>

[<span data-ttu-id="a794c-118">**WSMAN. kreatesession**</span><span class="sxs-lookup"><span data-stu-id="a794c-118">**WSMan.CreateSession**</span></span>](wsman-createsession.md)
</dt> <dt>

[<span data-ttu-id="a794c-119">Authentifizierung für Remote Verbindungen</span><span class="sxs-lookup"><span data-stu-id="a794c-119">Authentication for Remote Connections</span></span>](authentication-for-remote-connections.md)
</dt> </dl>

 

 




