---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: 06fd0284-5af9-409a-8748-c0b40e0fa317
title: T (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fada27e903c465f9b5e0342fca481e5161b699c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362342"
---
# <a name="t-windows-installer"></a><span data-ttu-id="5279c-103">T (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="5279c-103">T (Windows Installer)</span></span>

<span data-ttu-id="5279c-104">[a](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) T [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="5279c-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) T [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="5279c-105"><span id="_msi_transaction_processing_gly"></span><span id="_MSI_TRANSACTION_PROCESSING_GLY"></span>**Transaktionsverarbeitung**</span><span class="sxs-lookup"><span data-stu-id="5279c-105"><span id="_msi_transaction_processing_gly"></span><span id="_MSI_TRANSACTION_PROCESSING_GLY"></span>**transaction processing**</span></span>
</dt> <dd>

<span data-ttu-id="5279c-106">Mindestens ein Vorgang, der als einzelner unteilbarer gesamter Vorgang (Transaktion) verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="5279c-106">One or more operations processed together as a single indivisible whole called a transaction.</span></span> <span data-ttu-id="5279c-107">Alle konstituierenden Vorgänge müssen erfolgreich sein, damit die Transaktion erfolgreich ausgeführt werden kann. andernfalls werden alle Vorgänge in den ursprünglichen Zustand zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="5279c-107">All the constituent operations must succeed for the transaction to succeed, otherwise all the operations are rolled back to the original state.</span></span>

</dd> <dt>

<span data-ttu-id="5279c-108"><span id="_msi_transform_gly"></span><span id="_MSI_TRANSFORM_GLY"></span>**Sin**</span><span class="sxs-lookup"><span data-stu-id="5279c-108"><span id="_msi_transform_gly"></span><span id="_MSI_TRANSFORM_GLY"></span>**transform**</span></span>
</dt> <dd>

<span data-ttu-id="5279c-109">Vorlage der Unterschiede zwischen zwei [*Installer-Datenbanken*](i-gly.md) , die angewendet werden können, um ähnliche Änderungen in anderen Datenbanken zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5279c-109">Template of the differences between two [*installer databases*](i-gly.md) that can be applied to produce similar changes in other databases.</span></span> <span data-ttu-id="5279c-110">Beispielsweise kann eine Lokalisierungs Transformation verwendet werden, um die Sprache einer Anwendung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="5279c-110">For example, a localization transform can be used to change the language of an application.</span></span> <span data-ttu-id="5279c-111">Weitere Informationen finden Sie unter Zusammenführungen [und Transformationen](merges-and-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="5279c-111">For more information, see [Merges and Transforms](merges-and-transforms.md).</span></span>

</dd> <dt>

<span data-ttu-id="5279c-112"><span id="_msi_transform_error_condition_flags_gly"></span><span id="_MSI_TRANSFORM_ERROR_CONDITION_FLAGS_GLY"></span>**Transformations fehlerbedingungs-Flags**</span><span class="sxs-lookup"><span data-stu-id="5279c-112"><span id="_msi_transform_error_condition_flags_gly"></span><span id="_MSI_TRANSFORM_ERROR_CONDITION_FLAGS_GLY"></span>**transform error condition flags**</span></span>
</dt> <dd>

<span data-ttu-id="5279c-113">Ein Satz von Eigenschaften, die zum Markieren der Fehlerbedingungen einer [*Transformation*](/windows)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5279c-113">Set of properties used to flag the error conditions of a [*transform*](/windows).</span></span> <span data-ttu-id="5279c-114">Weitere Informationen finden Sie unter [**msikreatetransformsummaryinfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span><span class="sxs-lookup"><span data-stu-id="5279c-114">For more information, see [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span></span>

</dd> <dt>

<span data-ttu-id="5279c-115"><span id="_msi_transform_validation_flags_gly"></span><span id="_MSI_TRANSFORM_VALIDATION_FLAGS_GLY"></span>**Transformations-Validierungs Flags**</span><span class="sxs-lookup"><span data-stu-id="5279c-115"><span id="_msi_transform_validation_flags_gly"></span><span id="_MSI_TRANSFORM_VALIDATION_FLAGS_GLY"></span>**transform validation flags**</span></span>
</dt> <dd>

<span data-ttu-id="5279c-116">Ein Satz von Eigenschaften, mit denen überprüft wird, ob die [*Transformation*](/windows) auf die Datenbank angewendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5279c-116">Set of properties used to verify that the [*transform*](/windows) can be applied to the database.</span></span> <span data-ttu-id="5279c-117">Eine Liste dieser Eigenschaften finden Sie unter [**msikreatetransformsummaryinfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span><span class="sxs-lookup"><span data-stu-id="5279c-117">For a list of these properties, see [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span></span>

</dd> </dl>

 

 
