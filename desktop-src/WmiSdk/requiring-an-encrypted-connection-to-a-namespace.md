---
description: Sie können anfordern, dass Client Skripts und-Anwendungen eine verschlüsselte Verbindung für die Authentifizierung herstellen, indem Sie den "Requirements sencryption"-Qualifizierer der MOF-Datei (Managed Object Format) hinzufügen, die den Namespace erstellt.
ms.assetid: 07b225a2-3834-4879-beae-f5b9180d112f
ms.tgt_platform: multiple
title: Eine verschlüsselte Verbindung mit einem Namespace ist erforderlich.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e42415c0f714f99a51d6a1a0ee1a0b22f398b1b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360848"
---
# <a name="requiring-an-encrypted-connection-to-a-namespace"></a><span data-ttu-id="bf984-103">Eine verschlüsselte Verbindung mit einem Namespace ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bf984-103">Requiring an Encrypted Connection to a Namespace</span></span>

<span data-ttu-id="bf984-104">Sie können anfordern, dass Client Skripts und-Anwendungen eine verschlüsselte Verbindung für die Authentifizierung herstellen, indem Sie den "Requirements **sencryption** "-Qualifizierer der MOF-Datei (Managed Object Format) hinzufügen, die den Namespace erstellt.</span><span class="sxs-lookup"><span data-stu-id="bf984-104">You can require that client scripts and applications establish an encrypted connection for authentication by adding the **RequiresEncryption** qualifier to the Managed Object Format (MOF) .mof file that creates the namespace.</span></span>


<span data-ttu-id="bf984-105">Eine verschlüsselte Verbindung mit einem WMI-Namespace gibt die **\_ \_ \_ \_ Pkt- \_ Datenschutzebene** (oder **PKTPRIVACY** in einem Skript) der RPC-C-authn für die Authentifizierung an.</span><span class="sxs-lookup"><span data-stu-id="bf984-105">An encrypted connection to a WMI namespace specifies **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** (or **PktPrivacy** in a script) for authentication.</span></span> <span data-ttu-id="bf984-106">Der **"** Requirements"-Qualifizierer bewirkt, dass WMI eingehende Datenanforderungen ablehnt, es sei denn, Sie verwenden explizit verschlüsselte Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="bf984-106">The **RequiresEncryption** qualifier causes WMI to reject any incoming data requests unless they explicitly use encrypted authentication.</span></span> <span data-ttu-id="bf984-107">Weitere Informationen finden Sie unter [Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von VBScript](setting-the-default-process-security-level-using-vbscript.md) oder [Festlegen der Authentifizierung mithilfe von C++](setting-authentication-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="bf984-107">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md) or [Setting Authentication Using C++](setting-authentication-using-c-.md).</span></span>

<span data-ttu-id="bf984-108">Sie können auch einen vorhandenen Namespace ändern, indem Sie dieses Attribut hinzufügen und die MOF-Datei dann erneut kompilieren.</span><span class="sxs-lookup"><span data-stu-id="bf984-108">You can also modify an existing namespace by adding this attribute and then compile the MOF file again.</span></span> <span data-ttu-id="bf984-109">"Requirements- **cryption** " wird in [*MOF*](gloss-m.md) mit der Namespace-Präprozessoranweisung " [pragma](pragma-namespace.md) " verwendet.</span><span class="sxs-lookup"><span data-stu-id="bf984-109">**RequiresEncryption** is used in [*MOF*](gloss-m.md) with the [pragma namespace](pragma-namespace.md) preprocessor instruction.</span></span>

<span data-ttu-id="bf984-110">Im folgenden Verfahren wird der-Namespace so festgelegt, dass eine verschlüsselte Verbindung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="bf984-110">The following procedure sets the namespace to require an encrypted connection.</span></span>

<span data-ttu-id="bf984-111">**So legen Sie die erforderliche Verschlüsselung fest**</span><span class="sxs-lookup"><span data-stu-id="bf984-111">**To set required encryption**</span></span>

1.  <span data-ttu-id="bf984-112">Erstellen Sie eine Managed Object Format Datei (MOF), oder ändern Sie die vorhandene MOF-Datei, die den Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="bf984-112">Create a Managed Object Format (MOF) file or modify your existing MOF file that defines the namespace.</span></span>

    <span data-ttu-id="bf984-113">Das folgende Codebeispiel zeigt, wie der Namespace, der geändert wird, der Stamm *\\ MyNamespace* und die Datei den Namen *MyNamespace \_ Security. MOF* hat.</span><span class="sxs-lookup"><span data-stu-id="bf984-113">The following code example shows the namespace that will be modified is *root\\MyNamespace* and the file is named *MyNamespace\_security.mof*.</span></span> <span data-ttu-id="bf984-114">"Requirements **sencryption** " weist einen booleschen Datentyp auf, sodass er auf " **true** " oder " **false**" festgelegt werden muss.</span><span class="sxs-lookup"><span data-stu-id="bf984-114">**RequiresEncryption** has a Boolean datatype so it must be set to **True** or **False**.</span></span>

    ```mof
    #pragma namespace("\\\\.\\Root\\MyNamespace") 

    [RequiresEncryption(TRUE)] 
    instance of __systemSecurity { };
    ```

    

2.  <span data-ttu-id="bf984-115">Führen Sie [**mofcomp.exe**](mofcomp.md) aus, um die MOF-Datei zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="bf984-115">Run [**mofcomp.exe**](mofcomp.md) to compile the MOF file.</span></span>

    <span data-ttu-id="bf984-116">**c: " \\ mynamespace" " \_ Security. mof"**</span><span class="sxs-lookup"><span data-stu-id="bf984-116">**c:\\mofcomp MyNamespace\_security.mof**</span></span>

    <span data-ttu-id="bf984-117">Verwenden Sie in C++ die [**imuf Compiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) -Methoden.</span><span class="sxs-lookup"><span data-stu-id="bf984-117">In C++, use the [**IMoFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) methods.</span></span>

<span data-ttu-id="bf984-118">WMI lehnt einen Client ab, der die Standard Authentifizierungs Ebene verwendet, da DCOM die Sicherheit auf die Ebene aushandiert, die für den Svchost-Prozess erforderlich ist, in dem der WMI-Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bf984-118">WMI rejects a client that uses the default authentication level because DCOM negotiates the security to the level required by the SVCHOST process in which the WMI service is running.</span></span> <span data-ttu-id="bf984-119">Weitere Informationen zu Dienst Hosts finden Sie unter [Anbieter Hosting und-Sicherheit](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="bf984-119">For more information about service hosts, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span> <span data-ttu-id="bf984-120">Weitere Informationen zum Festlegen von Authentifizierungs Ebenen beim Herstellen einer Verbindung mit WMI-Namespaces finden Sie unter [Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von C++](setting-the-default-process-security-level-using-c-.md), [Festlegen der Authentifizierung mithilfe von C++](setting-authentication-using-c-.md)oder [Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="bf984-120">For more information about setting authentication levels when connecting to WMI namespaces, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md), [Setting Authentication Using C++](setting-authentication-using-c-.md), or [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

<span data-ttu-id="bf984-121">Beim Zurückgeben von Daten in einer asynchronen Rückruf Verbindung gibt WMI die Meldung "Zugriff verweigert" an den anfordernden Computer zurück.</span><span class="sxs-lookup"><span data-stu-id="bf984-121">When returning data on an asynchronous callback connection, WMI returns an access denied message to the requesting computer.</span></span> <span data-ttu-id="bf984-122">WMI erstellt auch einen Protokolleintrag im NT-Ereignisprotokoll des Computers mit dem verschlüsselten Namespace, der besagt, dass keine sichere Verbindung mit dem Client hergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="bf984-122">WMI also makes a log entry in the NT Event Log of the computer with the encrypted namespace stating that a secure connection cannot be established to the client.</span></span>

<span data-ttu-id="bf984-123">Ab Windows Vista ist die Datei "wbemcore. log" nicht mehr vorhanden.</span><span class="sxs-lookup"><span data-stu-id="bf984-123">Starting with Windows Vista, the WbemCore.log file no longer exists.</span></span> <span data-ttu-id="bf984-124">Sie können das NT-Ereignisprotokoll auf Einträge überprüfen, die auf abgelehnte eingehende Datenanforderungen an Namespaces hindeuten, die eine Verschlüsselung erfordern.</span><span class="sxs-lookup"><span data-stu-id="bf984-124">You can check the NT Event Log for entries indicating rejected inbound data requests to namespaces that require encryption.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf984-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bf984-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf984-126">Festlegen von namepace-Sicherheits Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="bf984-126">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="bf984-127">**Wbemauthenticationlevelerum**</span><span class="sxs-lookup"><span data-stu-id="bf984-127">**WbemAuthenticationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[<span data-ttu-id="bf984-128">Sichern einer Remote-WMI-Verbindung</span><span class="sxs-lookup"><span data-stu-id="bf984-128">Securing a Remote WMI Connection</span></span>](securing-a-remote-wmi-connection.md)
</dt> </dl>

 

 



