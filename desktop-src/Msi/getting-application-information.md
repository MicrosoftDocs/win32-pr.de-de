---
description: Die Produktdatenbank enthält Informationen zu einem Produkt. Weitere Informationen zum Abrufen von Produktinformationen mit Enumerationsfunktionen finden Sie unter Initialisieren einer Anwendung.
ms.assetid: 528c915c-296c-4620-8105-0b5d543e56a5
title: Anwendungsinformationen werden erhalten.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2dce842f057efb65b6d0db3ad0407a19bf08435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959269"
---
# <a name="getting-application-information"></a><span data-ttu-id="e2006-104">Anwendungsinformationen werden erhalten.</span><span class="sxs-lookup"><span data-stu-id="e2006-104">Getting Application Information</span></span>

<span data-ttu-id="e2006-105">Die Produktdatenbank enthält Informationen zu einem Produkt.</span><span class="sxs-lookup"><span data-stu-id="e2006-105">The product database contains information about a product.</span></span> <span data-ttu-id="e2006-106">Weitere Informationen zum Abrufen von Produktinformationen mit Enumerationsfunktionen finden Sie unter [Initialisieren einer Anwendung](initializing-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="e2006-106">For more information on obtaining product information with enumeration functions, see [Initializing an Application](initializing-an-application.md).</span></span>

<span data-ttu-id="e2006-107">**So erhalten Sie Produktinformationen**</span><span class="sxs-lookup"><span data-stu-id="e2006-107">**To get product information**</span></span>

1.  <span data-ttu-id="e2006-108">Überprüfen Sie, ob ein Produkt installiert ist, indem Sie die [**msiqueryproductstate**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e2006-108">Verify that a product is installed by calling the [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea) function.</span></span>
2.  <span data-ttu-id="e2006-109">Öffnen Sie die Datenbank, und rufen Sie ein Handle dafür ab, indem Sie die [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e2006-109">Open the database and obtain a handle to it by calling the [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) function.</span></span>

    <span data-ttu-id="e2006-110">Wenn die Datenbank in einem Installationspaket enthalten ist, müssen Sie die Funktion [**msiopenpackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea) aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="e2006-110">If the database is contained in an installation package, call the [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea) function.</span></span>

3.  <span data-ttu-id="e2006-111">Verwenden Sie das offene Handle zum Abrufen von Produkteigenschaften mit der [**msigetproductproperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya) -Funktion und zum Abrufen beschreibender Funktions Informationen mit der [**msigetfeatureinfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="e2006-111">Use the open handle to obtain product properties with the [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya) function, and to obtain descriptive feature information with the [**MsiGetFeatureInfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa) function.</span></span>

    <span data-ttu-id="e2006-112">Wenn Sie Produktinformationen mithilfe des Produktcodes abrufen möchten, anstatt das geöffnete Daten Bank Handle zu verwenden, rufen Sie die [**msigetproductinfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa) -Funktion anstelle von " [**msigetproductproperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya)" auf.</span><span class="sxs-lookup"><span data-stu-id="e2006-112">If you want to obtain product information using the product code, rather than using the open database handle, call the [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa) function instead of [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya).</span></span>

4.  <span data-ttu-id="e2006-113">Schließen Sie ein geöffnetes Installations handle, indem Sie die [**msiclosehandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e2006-113">Close an open installation handle by calling the [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle) function.</span></span>

    <span data-ttu-id="e2006-114">Die [**msicloseallhandles**](/windows/desktop/api/Msi/nf-msi-msicloseallhandles) -Funktion ist eine Diagnosefunktion und sollte nicht verwendet werden, um die zu öffnenden Handles zu schließen.</span><span class="sxs-lookup"><span data-stu-id="e2006-114">The [**MsiCloseAllHandles**](/windows/desktop/api/Msi/nf-msi-msicloseallhandles) function is a diagnostic function and should not be used to close handles you know to be open.</span></span> <span data-ttu-id="e2006-115">Es ist zulässig, die **msicloseallhandles** -Funktion aufzurufen, wenn die Anwendung geschlossen wird, um sicherzustellen, dass alle Handles geschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="e2006-115">It is acceptable to call the **MsiCloseAllHandles** function when the application closes to ensure that all handles have been closed.</span></span>

 

 



