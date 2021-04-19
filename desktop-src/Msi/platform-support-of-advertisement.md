---
description: Der Windows Installer unterstützt Ankündigungen von Anwendungen und Features.
ms.assetid: 9e5158bc-4877-49d1-9bb9-4dd17abb444d
title: Platt Form Unterstützung für Ankündigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48016241998473a5bb5ae8ecff05a14fd702f8be
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106355729"
---
# <a name="platform-support-of-advertisement"></a><span data-ttu-id="1a13b-103">Platt Form Unterstützung für Ankündigungen</span><span class="sxs-lookup"><span data-stu-id="1a13b-103">Platform Support of Advertisement</span></span>

<span data-ttu-id="1a13b-104">Der Windows Installer unterstützt Ankündigungen von Anwendungen und Features.</span><span class="sxs-lookup"><span data-stu-id="1a13b-104">The Windows Installer supports advertisement of applications and features.</span></span>

<span data-ttu-id="1a13b-105">Die folgenden Ankündigungs Funktionen sind unter Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003, Windows XP und Windows 2000 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1a13b-105">The following advertisement capabilities are available on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003, Windows XP, and Windows 2000.</span></span>

-   <span data-ttu-id="1a13b-106">Tastenkombinationen und deren Symbole.</span><span class="sxs-lookup"><span data-stu-id="1a13b-106">Shortcuts and their icons.</span></span>

-   <span data-ttu-id="1a13b-107">Erweiterungen und ihre Symbole, die in der [ProgID-Tabelle](progid-table.md)angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="1a13b-107">Extensions and their icons specified in the [ProgId Table](progid-table.md).</span></span>

-   <span data-ttu-id="1a13b-108">Shell-und Befehls Verben, die unterhalb des ProgID-Schlüssels registriert sind</span><span class="sxs-lookup"><span data-stu-id="1a13b-108">Shell and command Verbs registered underneath the ProgId key.</span></span>

-   <span data-ttu-id="1a13b-109">CLSID-Kontexte und InprocHandler.</span><span class="sxs-lookup"><span data-stu-id="1a13b-109">CLSID contexts and InProcHandler.</span></span>

-   <span data-ttu-id="1a13b-110">Die Installation von on-Demand über OLE ist nur Programm gesteuert über [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) (C/C++) und **CreateObject-Funktion (Visual Basic)** oder **GetObject-Funktion (Visual Basic)** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1a13b-110">Install-On-Demand through OLE is only available programmatically through [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) (C/C++), and **CreateObject Function (Visual Basic)** or **GetObject Function (Visual Basic)**.</span></span>

> [!Note]
> <span data-ttu-id="1a13b-111">Die AppID-und TypeLib-Informationen werden nur geschrieben, wenn eine angekündigte Komponente installiert ist.</span><span class="sxs-lookup"><span data-stu-id="1a13b-111">AppId and Typelib information is only written when an advertised component is installed.</span></span>
> 
> <span data-ttu-id="1a13b-112">Zur Unterstützung von Dateinamen Erweiterungen muss die Anwendung von einem Administrator mit Gruppenrichtlinie Active Directory veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="1a13b-112">To support file name extensions, the application must be published to Active Directory by an administrator using Group Policy.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a13b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1a13b-113">Remarks</span></span>

<span data-ttu-id="1a13b-114">Die Installation des Produkts erfordert möglicherweise keinen Neustart, aber alle angekündigten Verknüpfungen funktionieren erst, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="1a13b-114">The installation of the product may not require a restart, but any advertised shortcuts do not work until the machine is restarted.</span></span> <span data-ttu-id="1a13b-115">Die angekündigten Verknüpfungen für nachfolgende Installationen funktionieren ohne Neustart.</span><span class="sxs-lookup"><span data-stu-id="1a13b-115">The advertised shortcuts of subsequent installations work without a restart.</span></span>

<span data-ttu-id="1a13b-116">Um sicherzustellen, dass angekündigte Verknüpfungen ordnungsgemäß funktionieren, sollte der Paket Ersteller am Ende der Installation einen erzwungenen Neustart planen.</span><span class="sxs-lookup"><span data-stu-id="1a13b-116">To ensure that advertised shortcuts work correctly, the package author should schedule a forced restart at the end of the installation.</span></span>

<span data-ttu-id="1a13b-117">Um unnötige Neustarts des Systems zu vermeiden, planen Sie einen Neustart so, dass er nur ausgeführt wird, wenn keine Version des Windows Installer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="1a13b-117">To avoid unnecessary restarts of the system, schedule a restart to run only if no version of the Windows Installer is installed.</span></span>

<span data-ttu-id="1a13b-118">Bedingte Anweisungen können die [**shelladvtsupport**](shelladvtsupport.md) -Eigenschaft und die [**Version9X**](version9x.md) -Eigenschaft überprüfen.</span><span class="sxs-lookup"><span data-stu-id="1a13b-118">Conditional statements can check the [**ShellAdvtSupport**](shelladvtsupport.md) property and [**Version9X**](version9x.md) property.</span></span> <span data-ttu-id="1a13b-119">Weitere Informationen zum Planen eines bedingten erzwungenen Neustarts finden Sie unter [System Neustarts](system-reboots.md) und [Verwenden von Eigenschaften in Bedingungs Anweisungen](using-properties-in-conditional-statements.md).</span><span class="sxs-lookup"><span data-stu-id="1a13b-119">For more information about scheduling a conditional forced restarts, see [System Reboots](system-reboots.md) and [Using Properties in Conditional Statements](using-properties-in-conditional-statements.md).</span></span>

 

 
