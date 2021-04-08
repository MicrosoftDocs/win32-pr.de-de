---
description: Autoren von Installationspaketen können angeben, dass das Installationsprogramm die freigegebenen Dateien (häufig freigegebene DLLs) einer Anwendung in den Ordner der Anwendung und nicht in einen freigegebenen Speicherort kopiert.
ms.assetid: eb5f7088-30e0-4644-813a-c93e6f56ccbf
title: Isolierte Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f29f614dfd819e093c5729a9a97a076247d281d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750120"
---
# <a name="isolated-components"></a><span data-ttu-id="28686-103">Isolierte Komponenten</span><span class="sxs-lookup"><span data-stu-id="28686-103">Isolated Components</span></span>

<span data-ttu-id="28686-104">Autoren von Installationspaketen können angeben, dass das Installationsprogramm die freigegebenen Dateien (häufig freigegebene DLLs) einer Anwendung in den Ordner der Anwendung und nicht in einen freigegebenen Speicherort kopiert.</span><span class="sxs-lookup"><span data-stu-id="28686-104">Authors of installation packages can specify that the installer copy the shared files (commonly shared DLLs) of an application into that application's folder rather than to a shared location.</span></span> <span data-ttu-id="28686-105">Dieser private Satz von Dateien (DLLs) wird dann nur von der Anwendung verwendet.</span><span class="sxs-lookup"><span data-stu-id="28686-105">This private set of files (DLLs) are then used only by the application.</span></span> <span data-ttu-id="28686-106">Wenn Sie die Anwendung auf diese Weise mit den freigegebenen Komponenten isolieren, haben Sie folgende Vorteile:</span><span class="sxs-lookup"><span data-stu-id="28686-106">Isolating the application together with its shared components in this manner has the following advantages:</span></span>

-   <span data-ttu-id="28686-107">Die Anwendung verwendet immer die Versionen der freigegebenen Dateien, mit denen Sie bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="28686-107">The application always uses the versions of the shared files with which it was deployed.</span></span>
-   <span data-ttu-id="28686-108">Beim Installieren der Anwendung werden andere Versionen der freigegebenen Dateien von anderen Anwendungen nicht überschrieben.</span><span class="sxs-lookup"><span data-stu-id="28686-108">Installing the application does not overwrite other versions of the shared files by other applications.</span></span>
-   <span data-ttu-id="28686-109">Bei nachfolgenden Installationen anderer Anwendungen, die unterschiedliche Versionen der freigegebenen Dateien verwenden, können die von dieser Anwendung verwendeten Dateien nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="28686-109">Subsequent installations of other applications using different versions of the shared files cannot overwrite the files used by this application.</span></span>

<span data-ttu-id="28686-110">Da die aktuelle Implementierung von com einen einzelnen vollständigen Pfad in der Registrierung für jedes CLSID/Kontext-paar beibehält, zwingt Sie alle Anwendungen, dieselbe Version einer freigegebenen DLL zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="28686-110">Because the current implementation of COM keeps a single full path in the registry for each CLSID/Context pair, it forces all applications to use the same version of a shared DLL.</span></span> <span data-ttu-id="28686-111">Damit eine Anwendung eine private Kopie eines COM-Servers beibehalten kann, prüft das System Lade Modul in Windows 2000, ob ein vorhanden ist. Lokale Datei im Ordner der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="28686-111">To enable an application to keep a private copy of a COM server, the system loader in Windows 2000 checks for the presence of a .LOCAL file in the application's folder.</span></span> <span data-ttu-id="28686-112">, Wenn das System Lade Modul eine erkennt. Lokale Datei ändert Ihre Suchlogik so, dass DLLs bevorzugt werden, die sich im selben Ordner wie die Anwendung befinden.</span><span class="sxs-lookup"><span data-stu-id="28686-112">If the system loader detects a .LOCAL file, it alters its search logic to prefer DLLs located in the same folder as the application.</span></span>

<span data-ttu-id="28686-113">Wenn Windows Installer die [isolatecomponents-Aktion](isolatecomponents-action.md) ausführt, kopieren Sie die Dateien der Komponente (in der Regel eine freigegebene DLL), die in der frei \_ gegebenen Komponenten Spalte der [isolatedcomponent-Tabelle](isolatedcomponent-table.md) angegeben ist, in denselben Ordner wie die Komponente (in der Regel eine exe-Datei), die in der Spalte Komponenten Anwendung angegeben ist \_ .</span><span class="sxs-lookup"><span data-stu-id="28686-113">When Windows Installer runs the [IsolateComponents action](isolatecomponents-action.md) they copy the files of the component (commonly a shared DLL) specified in the Component\_Shared column of the [IsolatedComponent table](isolatedcomponent-table.md) into the same folder as the component (commonly an .exe file) specified in the Component\_Application column.</span></span> <span data-ttu-id="28686-114">Das Installationsprogramm erstellt eine Datei in diesem Verzeichnis, eine Länge von 0 (null) Bytes, wobei der kurze Dateiname der Schlüsseldatei für die Komponenten \_ Anwendung (in der Regel der Name ist identisch mit der exe-Datei der Anwendung) ist, der angefügt wird. Nah.</span><span class="sxs-lookup"><span data-stu-id="28686-114">The installer creates a file in this directory, zero bytes in length, having the short file name of the key file for Component\_Application (typically the name is the same as the application's .exe) appended with .LOCAL.</span></span> <span data-ttu-id="28686-115">Das Installationsprogramm verwendet die Registrierung für die Komponente am freigegebenen Speicherort und schreibt keine Registrierungsinformationen für die Kopie der Komponente am privaten Speicherort.</span><span class="sxs-lookup"><span data-stu-id="28686-115">The installer uses the registration for the component in its shared location and does not write any registration information for the copy of the component in the private location.</span></span>

<span data-ttu-id="28686-116">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="28686-116">For more information, see:</span></span>

-   [<span data-ttu-id="28686-117">Installation isolierter Komponenten</span><span class="sxs-lookup"><span data-stu-id="28686-117">Installation of Isolated Components</span></span>](installation-of-isolated-components.md)
-   [<span data-ttu-id="28686-118">Neuinstallation isolierter Komponenten</span><span class="sxs-lookup"><span data-stu-id="28686-118">Reinstallation of Isolated Components</span></span>](reinstallation-of-isolated-components.md)
-   [<span data-ttu-id="28686-119">Entfernen isolierter Komponenten</span><span class="sxs-lookup"><span data-stu-id="28686-119">Removal of Isolated Components</span></span>](removal-of-isolated-components.md)
-   [<span data-ttu-id="28686-120">Verwenden isolierter Komponenten</span><span class="sxs-lookup"><span data-stu-id="28686-120">Using Isolated Components</span></span>](using-isolated-components.md)

 

 



