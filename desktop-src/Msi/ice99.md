---
description: ICE99 überprüft, ob kein in der Verzeichnis Tabelle eingegebener Eigenschaftsname einen Namen dupliziert, der für die öffentliche oder private Verwendung des Windows Installer reserviert ist.
ms.assetid: a7657c14-6542-4a7b-a8f7-727b109cfc39
title: ICE99
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7d70aeaf6480e45db5b47f76434f93e49adf317
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757039"
---
# <a name="ice99"></a><span data-ttu-id="9c9c1-103">ICE99</span><span class="sxs-lookup"><span data-stu-id="9c9c1-103">ICE99</span></span>

<span data-ttu-id="9c9c1-104">ICE99 überprüft, ob kein in der [Verzeichnis](directory-table.md) Tabelle eingegebener Eigenschaftsname einen Namen dupliziert, der für die öffentliche oder private Verwendung des Windows Installer reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="9c9c1-104">ICE99 verifies that no property name entered in the [Directory](directory-table.md) table duplicates a name reserved for the public or private use of the Windows Installer.</span></span>

## <a name="result"></a><span data-ttu-id="9c9c1-105">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="9c9c1-105">Result</span></span>

<span data-ttu-id="9c9c1-106">ICE99 gibt den folgenden Fehler aus.</span><span class="sxs-lookup"><span data-stu-id="9c9c1-106">ICE99 posts the following error.</span></span>



| <span data-ttu-id="9c9c1-107">ICE99-Fehler</span><span class="sxs-lookup"><span data-stu-id="9c9c1-107">ICE99 error</span></span>                                                                                                      | <span data-ttu-id="9c9c1-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9c9c1-108">Description</span></span>                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c9c1-109">Der Verzeichnisname: \[ 1 \] ist mit einer der öffentlichen MSI-Eigenschaften identisch und kann zu unvorhersehbaren Nebeneffekten führen.</span><span class="sxs-lookup"><span data-stu-id="9c9c1-109">The directory name: \[1\] is the same as one of the MSI Public Properties and can cause unforeseen side effects.</span></span> | <span data-ttu-id="9c9c1-110">Der Wert in der Spalte Verzeichnis der [Verzeichnis](directory-table.md) Tabelle dupliziert einen Eigenschaftsnamen, der vom Windows Installer reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="9c9c1-110">The value in the Directory column of the [Directory](directory-table.md) table duplicates a property name reserved by the Windows Installer.</span></span> |



 

## <a name="example"></a><span data-ttu-id="9c9c1-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9c9c1-111">Example</span></span>

<span data-ttu-id="9c9c1-112">ICE99 meldet den folgenden Fehler für das Beispiel:</span><span class="sxs-lookup"><span data-stu-id="9c9c1-112">ICE99 reports the following error for the example:</span></span>

``` syntax
CustomActionData is the same as one of the MSI Public Properties and can cause unforeseen side effects.
```

<span data-ttu-id="9c9c1-113">[Verzeichnis](directory-table.md) (teilweise)</span><span class="sxs-lookup"><span data-stu-id="9c9c1-113">[Directory](directory-table.md) (partial)</span></span>



| <span data-ttu-id="9c9c1-114">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="9c9c1-114">Directory</span></span>        | <span data-ttu-id="9c9c1-115">Über \_ geordnetes Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="9c9c1-115">Directory\_Parent</span></span> | <span data-ttu-id="9c9c1-116">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="9c9c1-116">DefaultDir</span></span> |
|------------------|-------------------|------------|
| <span data-ttu-id="9c9c1-117">Customaktiondata</span><span class="sxs-lookup"><span data-stu-id="9c9c1-117">CustomActionData</span></span> |                   |            |



 

<span data-ttu-id="9c9c1-118">Um diese Warnung zu beheben, sollten Sie den Namen von "customaktiondata" ändern.</span><span class="sxs-lookup"><span data-stu-id="9c9c1-118">To correct this warning you should change the name of CustomActionData.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c9c1-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9c9c1-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c9c1-120">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="9c9c1-120">ICE Reference</span></span>](ice-reference.md)
</dt> <dt>

[<span data-ttu-id="9c9c1-121">Verzeichnis Tabelle</span><span class="sxs-lookup"><span data-stu-id="9c9c1-121">Directory Table</span></span>](directory-table.md)
</dt> <dt>

[<span data-ttu-id="9c9c1-122">Wird in Windows Installer 3,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9c9c1-122">Not Supported in Windows Installer 3.0 and earlier</span></span>](not-supported-in-windows-installer-version-3-0.md)
</dt> </dl>

 

 



