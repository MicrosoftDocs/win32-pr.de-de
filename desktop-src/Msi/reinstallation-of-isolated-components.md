---
description: Windows Installer führt während der erneuten Installation einer Anwendung die folgenden Aktionen aus, wenn das Paket isolierte Komponenten enthält. In der Regel \_ handelt es sich bei der gemeinsam genutzten Komponente um eine DLL, die von Komponenten \_ Anwendungen und anderen ausführbaren Client Dateien gemeinsam genutzt wird
ms.assetid: 65909b47-dc09-4e9a-920a-9cb3f55b2e67
title: Neuinstallation isolierter Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ad1c7fb53eb09e96882209f7738e95be9b4a64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864828"
---
# <a name="reinstallation-of-isolated-components"></a><span data-ttu-id="01930-104">Neuinstallation isolierter Komponenten</span><span class="sxs-lookup"><span data-stu-id="01930-104">Reinstallation of Isolated Components</span></span>

<span data-ttu-id="01930-105">Windows Installer führt während der erneuten Installation einer Anwendung die folgenden Aktionen aus, wenn das Paket isolierte Komponenten enthält.</span><span class="sxs-lookup"><span data-stu-id="01930-105">Windows Installer performs the following actions during reinstallation of an application when the package contains isolated components.</span></span> <span data-ttu-id="01930-106">In der Regel \_ handelt es sich bei der gemeinsam genutzten Komponente um eine DLL, die von Komponenten \_ Anwendungen und anderen ausführbaren Client Dateien gemeinsam genutzt wird</span><span class="sxs-lookup"><span data-stu-id="01930-106">Typically, Component\_Shared is a DLL that is shared by Component\_Application and other client executables.</span></span>

## <a name="reinstallation"></a><span data-ttu-id="01930-107">Neuinstallation</span><span class="sxs-lookup"><span data-stu-id="01930-107">Reinstallation</span></span>

-   <span data-ttu-id="01930-108">Installieren Sie die Dateien der-Komponente, die \_ im selben Ordner wie die Komponenten Anwendung freigegeben \_ werden, neu, wenn die Komponenten \_ Anwendung ebenfalls neu installiert wird.</span><span class="sxs-lookup"><span data-stu-id="01930-108">Reinstall of the files of Component\_Shared into the same folder as Component\_Application only if Component\_Application is also being reinstalled.</span></span>
-   <span data-ttu-id="01930-109">Erhöhen Sie nicht die Client Liste der freigegebenen Komponenten, \_ und erhöhen Sie die Anzahl der SHAREDDLL nicht.</span><span class="sxs-lookup"><span data-stu-id="01930-109">Do not increment the client list of Component\_Shared and do not increment the SharedDLL count.</span></span>
-   <span data-ttu-id="01930-110">Erstellen Sie die 0-Byte-Datei mit dem kurzen Dateinamen der Schlüsseldatei der Komponenten \_ Anwendung neu.</span><span class="sxs-lookup"><span data-stu-id="01930-110">Recreate the zero-byte file with the short file name of the key file of Component\_Application.</span></span> <span data-ttu-id="01930-111">Diese Datei muss sich im selben Ordner wie \_ die Komponenten Anwendung befinden und die Erweiterung aufweisen. Nah.</span><span class="sxs-lookup"><span data-stu-id="01930-111">This file must be located in the same folder as Component\_Application and have the extension .LOCAL.</span></span>
-   <span data-ttu-id="01930-112">Installieren Sie wie gewohnt alle Ressourcen der Komponenten \_ Anwendung neu.</span><span class="sxs-lookup"><span data-stu-id="01930-112">Reinstall all of the resources of Component\_Application as usual.</span></span>

<span data-ttu-id="01930-113">Wenn SHAREDDLL refcount für die frei \_ gegebene Komponente größer als 1 ist, oder wenn andere Produkte in der Client Liste der freigegebenen Komponenten verbleiben \_ :</span><span class="sxs-lookup"><span data-stu-id="01930-113">If the SharedDLL refcount for Component\_Shared is more than 1, or if other products remain on the client list of Component\_Shared:</span></span>

-   <span data-ttu-id="01930-114">Installieren Sie keine Dateien erneut an den freigegebenen Speicherort der frei \_ gegebenen Komponente.</span><span class="sxs-lookup"><span data-stu-id="01930-114">Reinstall no files to the shared location of Component\_Shared.</span></span>

<span data-ttu-id="01930-115">Wenn SHAREDDLL refcount für die frei \_ gegebene Komponente 1 ist, oder wenn keine anderen verbleibenden Clients der Komponente frei \_ gegeben sind:</span><span class="sxs-lookup"><span data-stu-id="01930-115">If the SharedDLL refcount for Component\_Shared equals 1, or if there are no other remaining clients of Component\_Shared:</span></span>

-   <span data-ttu-id="01930-116">Installieren Sie die Dateien der an \_ den freigegebenen Speicherort freigegebenen Komponenten mithilfe der Regeln für die [Datei Versions](file-versioning-rules.md)Verwaltung neu.</span><span class="sxs-lookup"><span data-stu-id="01930-116">Reinstall of the files of Component\_Shared into the shared location using the [File Versioning Rules](file-versioning-rules.md).</span></span>
-   <span data-ttu-id="01930-117">Alle Neuinstallations Aktionen für freigegebene Komponenten verarbeiten \_ .</span><span class="sxs-lookup"><span data-stu-id="01930-117">Process all reinstall actions for Component\_Shared.</span></span>
-   <span data-ttu-id="01930-118">Wenn die \_ freigegebene Komponente eine COM-Komponente ist, registrieren Sie den vollständigen com-Pfad, sodass der Installer \[ $Component \] und den \[ \# filekey- \] Punkt auf den freigegebenen Speicherort der freigegebenen Komponente verweist \_ .</span><span class="sxs-lookup"><span data-stu-id="01930-118">If Component\_Shared is a COM component, register the full COM path such that the installer syntaxes \[$Component\] and \[\#FileKey\] point to the shared location of Component\_Shared.</span></span>

 

 



