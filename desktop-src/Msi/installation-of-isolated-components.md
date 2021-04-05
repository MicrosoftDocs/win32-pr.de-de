---
description: Windows Installer führt die folgenden Aktionen während der Installation einer Anwendung aus, wenn das Paket isolierte Komponenten enthält. In der Regel \_ handelt es sich bei der gemeinsam genutzten Komponente um eine DLL, die von Komponenten \_ Anwendungen und anderen ausführbaren Client Dateien gemeinsam genutzt wird
ms.assetid: fbc5dd86-5d38-4ce8-ab38-03c84cc77e80
title: Installation isolierter Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c1b9a7e21c212474701409e887d0afd5517774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753768"
---
# <a name="installation-of-isolated-components"></a><span data-ttu-id="70d41-104">Installation isolierter Komponenten</span><span class="sxs-lookup"><span data-stu-id="70d41-104">Installation of Isolated Components</span></span>

<span data-ttu-id="70d41-105">Windows Installer führt die folgenden Aktionen während der Installation einer Anwendung aus, wenn das Paket isolierte Komponenten enthält.</span><span class="sxs-lookup"><span data-stu-id="70d41-105">Windows Installer performs the following actions during installation of an application when the package contains isolated components.</span></span> <span data-ttu-id="70d41-106">In der Regel \_ handelt es sich bei der gemeinsam genutzten Komponente um eine DLL, die von Komponenten \_ Anwendungen und anderen ausführbaren Client Dateien gemeinsam genutzt wird</span><span class="sxs-lookup"><span data-stu-id="70d41-106">Typically, Component\_Shared is a DLL that is shared by Component\_Application and other client executables.</span></span>

## <a name="installation"></a><span data-ttu-id="70d41-107">Installation</span><span class="sxs-lookup"><span data-stu-id="70d41-107">Installation</span></span>

-   <span data-ttu-id="70d41-108">Kopieren Sie die Dateien der frei \_ gegebenen Komponente in denselben Ordner wie die Komponenten \_ Anwendung, wenn auch die Komponenten \_ Anwendung installiert wird.</span><span class="sxs-lookup"><span data-stu-id="70d41-108">Copy the files of Component\_Shared into the same folder as Component\_Application only if Component\_Application is also being installed.</span></span>
-   <span data-ttu-id="70d41-109">Erstellen Sie eine 0-Byte-Datei mit dem kurzen Dateinamen der Schlüsseldatei der Komponenten \_ Anwendung.</span><span class="sxs-lookup"><span data-stu-id="70d41-109">Create a zero-byte file with the short file name of the key file of Component\_Application.</span></span> <span data-ttu-id="70d41-110">Suchen Sie diese Datei im selben Ordner wie die Komponenten \_ Anwendung.</span><span class="sxs-lookup"><span data-stu-id="70d41-110">Locate this file in the same folder as Component\_Application.</span></span> <span data-ttu-id="70d41-111">Fügen Sie die Erweiterung an. Lokal mit diesem Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="70d41-111">Append the extension .LOCAL to this file name.</span></span>
-   <span data-ttu-id="70d41-112">Erhöhen Sie SHAREDDLL refcount, wenn das msidbcomponentattributesshareddllrefcount-Bit in der Attribute-Spalte der [Komponenten Tabelle](component-table.md)festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="70d41-112">Increment the SharedDLL refcount if the msidbComponentAttributesSharedDllRefCount bit is set in the Attributes column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="70d41-113">Registrieren \_ Sie die Komponenten Anwendung als Client der \_ gemeinsam genutzten Komponente, und registrieren Sie einen Schlüssel Pfad, der auf den freigegebenen Speicherort der freigegebenen Komponente verweist \_ .</span><span class="sxs-lookup"><span data-stu-id="70d41-113">Register Component\_Application as a client of Component\_Shared and register a key path pointing to the shared location of Component\_Shared.</span></span>
-   <span data-ttu-id="70d41-114">Installieren Sie alle Ressourcen der Komponenten \_ Anwendung wie gewohnt.</span><span class="sxs-lookup"><span data-stu-id="70d41-114">Install all of the resources of Component\_Application as usual.</span></span>

<span data-ttu-id="70d41-115">Wenn \_ die freigegebene Komponente oder die zugehörige Schlüsseldatei bereits auf dem Computer installiert ist, kopieren Sie keine Dateien an den freigegebenen Speicherort der freigegebenen Komponente \_ .</span><span class="sxs-lookup"><span data-stu-id="70d41-115">If Component\_Shared or its key file is already installed on the computer do not copy files to the shared location of Component\_Shared.</span></span>

<span data-ttu-id="70d41-116">Wenn \_ die freigegebene Komponente oder die zugehörige Schlüsseldatei noch nicht auf dem Computer installiert ist:</span><span class="sxs-lookup"><span data-stu-id="70d41-116">If Component\_Shared or its key file is not yet installed on the computer:</span></span>

-   <span data-ttu-id="70d41-117">Kopieren Sie die Dateien der frei \_ gegebenen Komponente in den freigegebenen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="70d41-117">Copy the files of Component\_Shared to the shared location.</span></span>
-   <span data-ttu-id="70d41-118">Alle Installations Aktionen für freigegebene Komponenten verarbeiten \_ .</span><span class="sxs-lookup"><span data-stu-id="70d41-118">Process all install actions for Component\_Shared.</span></span>
-   <span data-ttu-id="70d41-119">Wenn die \_ freigegebene Komponente eine COM-Komponente ist, registrieren Sie den vollständigen com-Pfad so, dass die Syntax \[ $Component \] und \[ \# File Key \] auf den freigegebenen Speicherort der freigegebenen Komponente verweisen \_ .</span><span class="sxs-lookup"><span data-stu-id="70d41-119">If Component\_Shared is a COM component, register the full COM path such that the syntax \[$Component\] and \[\#FileKey\] point to the shared location of Component\_Shared.</span></span>

 

 



