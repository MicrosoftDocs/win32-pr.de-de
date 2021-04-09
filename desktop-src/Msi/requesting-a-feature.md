---
description: Es gibt mehrere Funktionen, die von einer Anwendung aufgerufen werden müssen, um Features anzufordern.
ms.assetid: 5253c6f0-316f-4f24-b0c0-951db8d16745
title: Anfordern einer Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e5261aac69ad2dd604a072e4b02e3bcde76a2e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042496"
---
# <a name="requesting-a-feature"></a><span data-ttu-id="e2294-103">Anfordern einer Funktion</span><span class="sxs-lookup"><span data-stu-id="e2294-103">Requesting a Feature</span></span>

<span data-ttu-id="e2294-104">Es gibt mehrere Funktionen, die von einer Anwendung aufgerufen werden müssen, um Features anzufordern.</span><span class="sxs-lookup"><span data-stu-id="e2294-104">There are several functions an application must call to request features.</span></span> <span data-ttu-id="e2294-105">Bevor eine Funktion angefordert wird, muss die Anwendung sicherstellen, dass die Funktion installiert ist.</span><span class="sxs-lookup"><span data-stu-id="e2294-105">Before requesting a feature, the application must ensure that the feature is installed.</span></span> <span data-ttu-id="e2294-106">Wenn die Anwendung [**msiusefeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) aufruft, bevor die Anwendung auf eine Funktion zugreift, kann die Anwendung die zurückgegebenen Informationen verwenden, um nutzungsmetriken beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="e2294-106">If the application calls [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) before the application accesses a feature, the application can use the information returned to maintain usage metrics.</span></span>

<span data-ttu-id="e2294-107">**So fordern Sie eine Funktion an**</span><span class="sxs-lookup"><span data-stu-id="e2294-107">**To request a feature**</span></span>

1.  <span data-ttu-id="e2294-108">Wenn Sie die Verfügbarkeit eines Features ohne Erhöhung der Verwendungs Anzahl ermitteln möchten, können Sie die [**msienüberfeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) -oder [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) -Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="e2294-108">Call the [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) or the [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) function if you want to determine the availability of a feature without incrementing the usage count.</span></span>
2.  <span data-ttu-id="e2294-109">Geben Sie an, dass die Anwendung eine Funktion verwenden soll, indem Sie die [**msiusefeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e2294-109">Indicate your application's intent to use a feature by calling the [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) function.</span></span>
3.  <span data-ttu-id="e2294-110">Bestimmen Sie die Speicherorte durch Aufrufen der [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="e2294-110">Determine file locations by calling the [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) function.</span></span>
4.  <span data-ttu-id="e2294-111">Konfigurieren Sie die Funktion, indem Sie die Funktion [**msikonfigurirefeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e2294-111">Configure the feature by calling the [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) function.</span></span>
5.  <span data-ttu-id="e2294-112">Rufen Sie nutzungsmetriken ab, die Ihre Anwendung verwenden kann, indem Sie die [**msigetfeatureusage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e2294-112">Obtain usage metrics that your application can use by calling the [**MsiGetFeatureUsage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea) function.</span></span>

<span data-ttu-id="e2294-113">Das folgende Diagramm veranschaulicht das Funktions Anforderungsmodell.</span><span class="sxs-lookup"><span data-stu-id="e2294-113">The following diagram illustrates the feature request model.</span></span>

![<span data-ttu-id="e2294-114">Funktions Anforderungsmodell.</span><span class="sxs-lookup"><span data-stu-id="e2294-114">feature request model.</span></span> ](images/over2.png)

 

 



