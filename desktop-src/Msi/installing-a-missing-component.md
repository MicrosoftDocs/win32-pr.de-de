---
description: Sie können den Windows Installer verwenden, um fehlende Komponenten oder Dateien zu erkennen, und dann Features neu installieren, die die fehlenden Komponenten enthalten.
ms.assetid: b197c9d0-fcc2-4ca7-a870-e1af82343455
title: Installieren einer fehlenden Komponente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9bbfd38517e850a7f4e83c9c84075d92fea2290
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357514"
---
# <a name="installing-a-missing-component"></a><span data-ttu-id="1ad9e-103">Installieren einer fehlenden Komponente</span><span class="sxs-lookup"><span data-stu-id="1ad9e-103">Installing a Missing Component</span></span>

<span data-ttu-id="1ad9e-104">Sie können den Windows Installer verwenden, um fehlende Komponenten oder Dateien zu erkennen, und dann Features neu installieren, die die fehlenden Komponenten enthalten.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-104">You can use the Windows Installer to detect missing components or files, and then reinstall features that contain the missing components.</span></span> <span data-ttu-id="1ad9e-105">Da das Installationsprogramm Features und keine Komponenten installiert, muss es zuerst aufgelöst werden, zu welcher Komponente eine fehlende Datei gehört, und dann die Funktion installieren, die die Komponente enthält.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-105">Because the Installer installs features and not components, it must first resolve to which component a missing file belongs, and then install the feature that contains the component.</span></span> <span data-ttu-id="1ad9e-106">Wenn mehr als eine Funktion mit der Komponente verknüpft ist, installiert das Installationsprogramm die Funktion, die den geringsten Speicherplatz benötigt.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-106">If more than one feature is linked to the component, the Installer installs the feature that requires the least disk space.</span></span>

<span data-ttu-id="1ad9e-107">Wenn Sie [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)aufrufen, können Sie überprüfen, ob die Schlüsseldatei einer Komponente vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-107">If you call [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha), you can verify that the key file of a component is present.</span></span> <span data-ttu-id="1ad9e-108">Es ist jedoch weiterhin möglich, dass andere Dateien, die der Komponente angehören, fehlen.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-108">However, it is still possible that other files belonging to the component are missing.</span></span> <span data-ttu-id="1ad9e-109">In diesem Szenario wird [**msiinstallmissingfile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-109">In that scenario, call [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea).</span></span> <span data-ttu-id="1ad9e-110">Der Installer löst dann eine Auflösung zu der Komponente aus, zu der die Datei gehört, und installiert das Feature, das mit der Komponente verknüpft ist, für die der geringste Speicherplatz erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-110">The Installer then resolves to which component the file belongs, and installs the feature that is linked to the component that requires the least disk space.</span></span>

<span data-ttu-id="1ad9e-111">Wenn die [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) -Funktion unerwartet ausfällt, müssen Sie fehlende Komponenten installieren.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-111">If the [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) function unexpectedly fails, you must install any missing components.</span></span>

<span data-ttu-id="1ad9e-112">Im folgenden Verfahren wird gezeigt, wie Sie fehlende Komponenten installieren.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-112">The following procedure shows you how to install missing components.</span></span>

<span data-ttu-id="1ad9e-113">**So erkennen und installieren Sie eine fehlende Komponente**</span><span class="sxs-lookup"><span data-stu-id="1ad9e-113">**To detect and install a missing component**</span></span>

1.  <span data-ttu-id="1ad9e-114">[**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) aufrufen, um zu überprüfen, ob die Schlüsseldatei einer Komponente vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-114">Call [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) to verify that the key file of a component is present.</span></span> <span data-ttu-id="1ad9e-115">Auch wenn die Schlüsseldatei der Komponente vorhanden ist, ist es weiterhin möglich, dass andere Dateien, die der Komponente angehören, fehlen.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-115">However, even if the key file of the component is present, it is still possible that other files belonging to the component are missing.</span></span>
2.  <span data-ttu-id="1ad9e-116">Wenn die Funktion, die der Komponente zugeordnet ist, unbekannt ist, wird die Funktion [**msiinstallmissingcomponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-116">Call the [**MsiInstallMissingComponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta) function if the feature associated with the component is unknown.</span></span>
3.  <span data-ttu-id="1ad9e-117">Wenn die Funktion bekannt ist, die der Komponente zugeordnet ist, wird die Funktion [**msikonfigurirefeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) oder [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-117">Call the [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) or [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta) function if the feature associated with the component is known.</span></span>
4.  <span data-ttu-id="1ad9e-118">[**Msiinstallmissingfile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea) wird aufgerufen, wenn eine Anwendung nicht in der Lage ist, eine Datei zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-118">Call [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea) if an application is unable to open a file.</span></span>

 

 



