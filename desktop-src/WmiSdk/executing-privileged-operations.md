---
description: Für privilegierte Vorgänge sind Sicherheits Privilegien erforderlich, z. b. SeLoadDriverPrivilege (wbemprivilegeloaddriver in den Scripting API-Konstanten), eine Berechtigung, die für ein Konto aktiviert werden muss, das einen Gerätetreiber lädt.
ms.assetid: 11bb8723-f329-4083-8219-2256ce44a5e3
ms.tgt_platform: multiple
title: Ausführen privilegierter Vorgänge
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 37abba9d774025825611e311f08414b50e660f65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348916"
---
# <a name="executing-privileged-operations"></a><span data-ttu-id="087e6-103">Ausführen privilegierter Vorgänge</span><span class="sxs-lookup"><span data-stu-id="087e6-103">Executing Privileged Operations</span></span>

<span data-ttu-id="087e6-104">Für privilegierte Vorgänge sind Sicherheits Privilegien erforderlich, z. **b. SeLoadDriverPrivilege** (**wbemprivilegeloaddriver** in den [Scripting API-Konstanten](scripting-api-constants.md)), eine Berechtigung, die für ein Konto aktiviert werden muss, das einen Gerätetreiber lädt.</span><span class="sxs-lookup"><span data-stu-id="087e6-104">Privileged operations require security privileges such as **SeLoadDriverPrivilege** (**wbemPrivilegeLoadDriver** in the [Scripting API Constants](scripting-api-constants.md)), a privilege that must be enabled for an account that is loading a device driver.</span></span> <span data-ttu-id="087e6-105">Sie können einem Administrator oder Benutzer über WMI keine Berechtigungen hinzufügen. Sie können nur Berechtigungen aktivieren, die das Konto bereits besitzt.</span><span class="sxs-lookup"><span data-stu-id="087e6-105">You cannot add privileges to an administrator or user through WMI, you can only enable privileges that the account already has.</span></span> <span data-ttu-id="087e6-106">Eine Liste der Berechtigungen finden Sie unter [**Berechtigungs \_ Konstanten**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="087e6-106">For a list of privileges, see [**Privilege\_Constants**](privilege-constants.md).</span></span>

<span data-ttu-id="087e6-107">Standardmäßig kann ein lokaler Benutzer auf einem Computer statische Daten aus dem [*WMI-Repository*](gloss-w.md)lesen, in Instanzen, die von Anbietern bereitgestellt werden, schreiben und Anbieter Methoden ausführen, es sei denn, der Anbieter erzwingt besondere, eigene Sicherheitsanforderungen.</span><span class="sxs-lookup"><span data-stu-id="087e6-107">By default, a local user on a computer can read static data from the [*WMI repository*](gloss-w.md), write to instances supplied by providers, and execute provider methods, unless the provider enforces special security requirements of its own.</span></span> <span data-ttu-id="087e6-108">Nur Administratoren können [eine Verbindung mit einem Remote Computer herstellen](connecting-to-wmi-on-a-remote-computer.md), Sicherheits Deskriptoren ändern oder statische WMI-Repository-Daten wie z. b. eine WMI-Klassendefinition ändern.</span><span class="sxs-lookup"><span data-stu-id="087e6-108">Only administrators can [connect to a remote computer](connecting-to-wmi-on-a-remote-computer.md), change security descriptors, or change static WMI repository data, such as a WMI class definition.</span></span> <span data-ttu-id="087e6-109">Alle Berechtigungen sind für eine Remote Verbindung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="087e6-109">All privileges are enabled for a remote connection.</span></span> <span data-ttu-id="087e6-110">Weitere Informationen finden Sie unter [Sichern einer Remote-WMI-Verbindung](securing-a-remote-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="087e6-110">For more information, see [Securing a Remote WMI Connection](securing-a-remote-wmi-connection.md).</span></span>

<span data-ttu-id="087e6-111">Die Berechtigungs Konstanten für C++ unterscheiden sich von denen, die von Automatisierungs Sprachen wie z. b. Visual Basic verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="087e6-111">The privilege constants for C++ differ from those that are used by automation languages such as Visual Basic.</span></span> <span data-ttu-id="087e6-112">Skripts müssen den Wert der Konstante anstelle des Namens verwenden.</span><span class="sxs-lookup"><span data-stu-id="087e6-112">Scripts must use the value of the constant rather than the name.</span></span> <span data-ttu-id="087e6-113">Weitere Informationen finden Sie unter [Ausführen von privilegierten Vorgängen mithilfe von C++](executing-privileged-operations-using-c-.md) oder [Ausführen privilegierter Vorgänge mithilfe von VBScript](executing-privileged-operations-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="087e6-113">For more information, see [Executing Privileged Operations Using C++](executing-privileged-operations-using-c-.md) or [Executing Privileged Operations Using VBScript](executing-privileged-operations-using-vbscript.md).</span></span>

<span data-ttu-id="087e6-114">Eine häufige Ursache für Zugriffs Verweigerungs Fehler bei der Verwendung von WMI ist das Fehlen einer aktivierten Berechtigung für Vorgänge, z. b. das Abrufen aller Instanzen von [**Win32 \_ nteventlogfile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="087e6-114">A common cause of access denied errors when using WMI is the lack of an enabled privilege for operations, such as getting all instances of [**Win32\_NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)).</span></span> <span data-ttu-id="087e6-115">Wenn Sie die **sesecurity** -Berechtigung nicht aktivieren, können Sie nicht auf die Sicherheitsprotokoll Datei zugreifen.</span><span class="sxs-lookup"><span data-stu-id="087e6-115">Without enabling the **SeSecurity** privilege, you cannot access the Security log file.</span></span>

<span data-ttu-id="087e6-116">Im folgenden VBScript-Codebeispiel wird gezeigt, wie die **sesecurity** -Berechtigung in der Monikerzeichenfolge festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="087e6-116">The following VBScript code example shows how to set the **SeSecurity** privilege in the moniker string.</span></span> <span data-ttu-id="087e6-117">Bei Verwendung im Moniker löscht der Berechtigungs Name in Klammern den ursprünglichen "SE".</span><span class="sxs-lookup"><span data-stu-id="087e6-117">When used in the moniker, the privilege name in parentheses drops the initial "Se".</span></span> <span data-ttu-id="087e6-118">Weitere Informationen finden Sie unter [Erstellen einer Monikerzeichenfolge](constructing-a-moniker-string.md).</span><span class="sxs-lookup"><span data-stu-id="087e6-118">For more information, see [Constructing a Moniker String](constructing-a-moniker-string.md).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate,(Security)}!\\" _
    & strComputer & "\root\cimv2")
Set colFiles = objWMIService.ExecQuery _
    ("Select * from Win32_NTEventLogFile " _
    & "Where LogFileName='Security'")
For Each LogFile in colFiles
Wscript.Echo LogFile.NumberOfRecords
Next
```



## <a name="related-topics"></a><span data-ttu-id="087e6-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="087e6-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="087e6-120">**Berechtigungs Konstanten**</span><span class="sxs-lookup"><span data-stu-id="087e6-120">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> </dl>

 

 
