---
description: Beim Zugriff auf einen Windows-Verwaltungsinstrumentation (WMI)-Server mit einem Skript können Sie zwischen NT LAN Manager (NTLM)-oder Kerberos-Authentifizierungs Protokollen wählen.
ms.assetid: db2dc750-bfdd-4f6c-859b-e104814f0800
ms.tgt_platform: multiple
title: Festlegen des Authentifizierungs Dienstanbieter mithilfe von VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bd2cf444560aac7ebce96b52d9abaa528bdcaa76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353971"
---
# <a name="setting-the-authentication-service-using-vbscript"></a><span data-ttu-id="26007-103">Festlegen des Authentifizierungs Dienstanbieter mithilfe von VBScript</span><span class="sxs-lookup"><span data-stu-id="26007-103">Setting the Authentication Service Using VBScript</span></span>

<span data-ttu-id="26007-104">Beim Zugriff auf einen Windows-Verwaltungsinstrumentation (WMI)-Server mit einem Skript können Sie zwischen NT LAN Manager (NTLM)-oder Kerberos-Authentifizierungs Protokollen wählen.</span><span class="sxs-lookup"><span data-stu-id="26007-104">When accessing a Windows Management Instrumentation (WMI) server with a script, you can choose between NT LAN Manager (NTLM) or Kerberos authentication protocols.</span></span> <span data-ttu-id="26007-105">Die Angabe von Kerberos ist nicht erforderlich, außer bei der Verwendung der Delegierung.</span><span class="sxs-lookup"><span data-stu-id="26007-105">Specifying Kerberos is not required except when using delegation.</span></span> <span data-ttu-id="26007-106">Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit einer dritten Computer Delegierung](connecting-to-a-3rd-computer-delegation.md).</span><span class="sxs-lookup"><span data-stu-id="26007-106">For more information, see [Connecting to a 3rd Computer-Delegation](connecting-to-a-3rd-computer-delegation.md).</span></span>

<span data-ttu-id="26007-107">Da sich die Betriebssystemversionen von dem verwendeten Authentifizierungsdienst unterscheiden, wird empfohlen, beim Herstellen einer Verbindung mit einem Remote System keinen Wert für das Feld "Authority" anzugeben.</span><span class="sxs-lookup"><span data-stu-id="26007-107">Because operating system versions differ in which authentication service they use, it is recommended that you do not specify a value for the authority field when connecting to a remote system.</span></span> <span data-ttu-id="26007-108">Verwenden Sie stattdessen das Betriebssystem und die verteilte Version von Component Object Model (DCOM), um NTLM oder Kerberos auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="26007-108">Instead, allow the operating system and distributed version of Component Object Model (DCOM) to select NTLM or Kerberos.</span></span> <span data-ttu-id="26007-109">Wenn ein Authentifizierungsdienst angegeben wird, ist für die Syntax der Server Prinzipal Name erforderlich. Dies ist der Name des Ziel Computers anstelle des Domänen Controllers.</span><span class="sxs-lookup"><span data-stu-id="26007-109">If an authentication service is specified, the syntax requires the server principal name, which is the name of the target computer rather than the domain controller.</span></span>

<span data-ttu-id="26007-110">Sie können den Authority-Parameter nur mit Verbindungen mit Remote-WMI-Servern verwenden.</span><span class="sxs-lookup"><span data-stu-id="26007-110">You can use the authority parameter only with connections to remote WMI servers.</span></span> <span data-ttu-id="26007-111">Beim Verbindungsversuch tritt ein Fehler auf, wenn Sie versuchen, Autorisierungs Ebenen als Teil eines Monikers oder durch einen Aufruf von " [**Swap-Locator. ConnectServer**](swbemlocator-connectserver.md) " für eine lokale Verbindung festzulegen.</span><span class="sxs-lookup"><span data-stu-id="26007-111">The connection attempt fails if you attempt to set authorization levels as part of a moniker or with a call to [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) for a local connection.</span></span>

<span data-ttu-id="26007-112">Führen Sie das folgende Verfahren aus, um den Authentifizierungsdienst anzugeben, den Sie im Parameter " *stranauthority* " der Methode " [**Swap. ConnectServer**](swbemlocator-connectserver.md) " oder der [Monikerzeichenfolge](constructing-a-moniker-string.md) verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="26007-112">Perform the following procedure to specify the authentication service that you want to use in the *strAuthority* parameter of the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method or the [moniker](constructing-a-moniker-string.md) string connection.</span></span>

<span data-ttu-id="26007-113">**So geben Sie die NTLM-oder Kerberos-Authentifizierung mit der Skript-API für WMI an**</span><span class="sxs-lookup"><span data-stu-id="26007-113">**To specify NTLM or Kerberos authentication with the Scripting API for WMI**</span></span>

1.  <span data-ttu-id="26007-114">Wenn der Parameter " *stranauthority* " mit der Zeichenfolge "Kerberos:" beginnt, geht WMI davon aus, dass die Zeichenfolge auf einen Kerberos-Prinzipal Namen verweist und die Kerberos-Authentifizierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="26007-114">If the *strAuthority* parameter begins with the string "kerberos:", WMI assumes the string refers to a Kerberos principal name and Kerberos authentication is used.</span></span> <span data-ttu-id="26007-115">Wenn der Parameter " *strauauthority* " mit der Zeichenfolge "ntlmdomain:" beginnt, verwendet WMI stattdessen die NTLM-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="26007-115">If the *strAuthority* parameter begins with the string "ntlmdomain:", WMI uses NTLM authentication instead.</span></span>
2.  <span data-ttu-id="26007-116">Alternativ können Sie den Authority-Teil eines Monikers verwenden, um den Authentifizierungstyp anzugeben, der zum Herstellen der Verbindung mit WMI verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="26007-116">Alternately, You can use the authority part of a moniker to specify the type of authentication used to connect to WMI.</span></span> <span data-ttu-id="26007-117">Wenn Sie die Kerberos-Authentifizierung verwenden möchten, wenn Sie einen Moniker verwenden, schließen Sie die Zeichenfolge "Authority = Kerberos:" gefolgt vom Prinzipal Namen ein.</span><span class="sxs-lookup"><span data-stu-id="26007-117">To use Kerberos authentication when using a moniker include the string, "authority=kerberos:" followed by the principal name.</span></span> <span data-ttu-id="26007-118">Um die NTLM-Authentifizierung zu verwenden, schließen Sie die Zeichenfolge "Authority = ntlmdomain:" gefolgt vom NTLM-Domänen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="26007-118">To use NTLM authentication, include the string, "authority=ntlmdomain:" followed by the NTLM domain name.</span></span>

    <span data-ttu-id="26007-119">Das folgende Beispiel zeigt einen Moniker, der die Kerberos-Authentifizierung mit dem Prinzipal "mydomain \\ Server" anfordert.</span><span class="sxs-lookup"><span data-stu-id="26007-119">The following example shows you a moniker that requests Kerberos authentication using the principal "mydomain\\server".</span></span>

    ```VB
    winmgmts:{impersonationLevel=delegate, _
            authority=kerberos:mydomain\server} _
            !//myserver/root/default:__cimomidentification=@
    ```

    

    <span data-ttu-id="26007-120">Im Gegensatz dazu zeigt das folgende Beispiel einen Moniker, der die NTLM-Authentifizierung mithilfe der Domäne "mydomain" anfordert.</span><span class="sxs-lookup"><span data-stu-id="26007-120">In contrast, the following example shows you a moniker that requests NTLM authentication using the domain "mydomain".</span></span>

    ```VB
    winmgmts:{impersonationLevel=impersonate, _
            authority=ntlmdomain:mydomain} _
            !//myserver/root/default:__cimomidentification=@
    ```

    

 

 



