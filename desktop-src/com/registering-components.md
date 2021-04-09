---
title: Registrieren von Komponenten
description: Registrieren von Komponenten
ms.assetid: d7fd231b-17ec-42ad-9144-df7ed5ffb17b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d683ae419466d62d764283cfa8706981de402a9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039647"
---
# <a name="registering-components"></a><span data-ttu-id="269e6-103">Registrieren von Komponenten</span><span class="sxs-lookup"><span data-stu-id="269e6-103">Registering Components</span></span>

<span data-ttu-id="269e6-104">Wenn die folgenden Anwendungs Typen installiert sind, müssen die Installationsinformationen der Registrierung hinzugefügt werden, in der Regel über ein Setup Programm:</span><span class="sxs-lookup"><span data-stu-id="269e6-104">When the following types of applications are installed, installation information must be added to the registry, usually through a setup program:</span></span>

-   <span data-ttu-id="269e6-105">Server Anwendungen</span><span class="sxs-lookup"><span data-stu-id="269e6-105">Server applications</span></span>
-   <span data-ttu-id="269e6-106">Container-/Server-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="269e6-106">Container/server applications</span></span>
-   <span data-ttu-id="269e6-107">Container Anwendungen, die das Verknüpfen mit eingebetteten Objekten ermöglichen</span><span class="sxs-lookup"><span data-stu-id="269e6-107">Container applications that allow linking to embedded objects</span></span>

<span data-ttu-id="269e6-108">Registrieren Sie für alle drei Instanzen com library (dll)-Informationen und anwendungsspezifische Informationen.</span><span class="sxs-lookup"><span data-stu-id="269e6-108">For all three instances, register COM library (DLL) information and application-specific information.</span></span>

<span data-ttu-id="269e6-109">Die dll registriert die Informationen für alle Ihre Komponenten, indem Sie [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) und [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver)exportiert.</span><span class="sxs-lookup"><span data-stu-id="269e6-109">The DLL registers the information for all its components by exporting [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver).</span></span> <span data-ttu-id="269e6-110">Verwenden Sie die folgenden Funktionen, um eine Komponente zu registrieren und die Registrierung aufzuheben:</span><span class="sxs-lookup"><span data-stu-id="269e6-110">Use the following functions to register and unregister a component:</span></span>

-   [<span data-ttu-id="269e6-111">**Fehler bei RegOpenKeyEx**</span><span class="sxs-lookup"><span data-stu-id="269e6-111">**RegOpenKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regopenkeyexa)
-   [<span data-ttu-id="269e6-112">**Regkreatekeyex**</span><span class="sxs-lookup"><span data-stu-id="269e6-112">**RegCreateKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa)
-   [<span data-ttu-id="269e6-113">**Fehler bei RegSetValueEx**</span><span class="sxs-lookup"><span data-stu-id="269e6-113">**RegSetValueEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regsetvalueexa)
-   [<span data-ttu-id="269e6-114">**Regenum keyex**</span><span class="sxs-lookup"><span data-stu-id="269e6-114">**RegEnumKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regenumkeyexa)
-   [<span data-ttu-id="269e6-115">**Regdeletekey**</span><span class="sxs-lookup"><span data-stu-id="269e6-115">**RegDeleteKey**</span></span>](/windows/desktop/api/winreg/nf-winreg-regdeletekeya)
-   [<span data-ttu-id="269e6-116">**Fehler bei RegCloseKey**</span><span class="sxs-lookup"><span data-stu-id="269e6-116">**RegCloseKey**</span></span>](/windows/desktop/api/winreg/nf-winreg-regclosekey)

## <a name="related-topics"></a><span data-ttu-id="269e6-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="269e6-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="269e6-118">Registrieren von com-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="269e6-118">Registering COM Applications</span></span>](registering-com-applications.md)
</dt> </dl>

 

 