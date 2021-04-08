---
description: Die Richtlinie für die automatische Anmeldung (automatische Anmeldung) bestimmt, wann WinHTTP die Standard Anmelde Informationen in eine Anforderung an den Server aufnehmen kann.
ms.assetid: 4ED8B6BC-E52D-4DE9-A9AE-1FDF61A978A9
title: Winhttpautologonlevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7760faa94e24b7fe5b33717c504b03e4de42c0aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866052"
---
# <a name="winhttpautologonlevel"></a><span data-ttu-id="b6a72-103">Winhttpautologonlevel</span><span class="sxs-lookup"><span data-stu-id="b6a72-103">WinHttpAutoLogonLevel</span></span>

<span data-ttu-id="b6a72-104">Die Richtlinie für die automatische Anmeldung (automatische Anmeldung) bestimmt, wann *WinHTTP* die Standard Anmelde Informationen in eine Anforderung an den Server aufnehmen kann.</span><span class="sxs-lookup"><span data-stu-id="b6a72-104">The automatic logon (auto-logon) policy determines when it is acceptable for *WinHTTP* to include the default credentials in a request to the server.</span></span>

<span data-ttu-id="b6a72-105">Sie können diesen Wert auf " **L** " festlegen, wenn die **WinHTTP-Authentifizierungs \_ Stufe " \_ \_ \_ niedrig**" auf " **M** " festgelegt ist, auf "M" für **WinHTTP- \_ Autologon- \_ Sicherheits \_ \_** Stufe "Mittel" festgelegt ist und auf " **H** " für die **\_ \_ \_ \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="b6a72-105">You can set this value to **L** for **WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_LOW**, set to **M** for **WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM**, and set to **H** for **WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_HIGH**.</span></span> <span data-ttu-id="b6a72-106">Die Standard Ebene ist **WinHTTP \_ Autologon \_ Security \_ Level \_ Medium**.</span><span class="sxs-lookup"><span data-stu-id="b6a72-106">The default level is **WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM**.</span></span> <span data-ttu-id="b6a72-107">Weitere Informationen zur Richtlinie für die automatische Anmeldung finden Sie im Abschnitt zur [Authentifizierung in WinHTTP](../winhttp/authentication-in-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="b6a72-107">For more information about automatic logon policy, see the section for [Authentication in WinHTTP](../winhttp/authentication-in-winhttp.md).</span></span>

<span data-ttu-id="b6a72-108">**Windows 8 und Windows Server 2012:** Diese Richtlinie erfordert, dass Windows Installer unter Windows 8 oder Windows Server 2012 ausgeführt wird und in allen früheren Versionen von Windows nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="b6a72-108">**Windows 8 and Windows Server 2012:** This policy requires Windows Installer running on the Windows 8 or Windows Server 2012 and is unavailable on all earlier versions of Windows.</span></span>

## <a name="registry-key"></a><span data-ttu-id="b6a72-109">Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="b6a72-109">Registry Key</span></span>

<span data-ttu-id="b6a72-110">**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="b6a72-110">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="b6a72-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b6a72-111">Data Type</span></span>

<span data-ttu-id="b6a72-112">**REG- \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="b6a72-112">**REG\_SZ**</span></span>

 

 
