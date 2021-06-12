---
description: Erfahren Sie mehr über Windows Installer Konzepte, die mit dem Buchstaben T beginnen, z. B. Transaktionsverarbeitung und Transformation.
ms.assetid: 06fd0284-5af9-409a-8748-c0b40e0fa317
title: T (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e9489455f880ba558e5a9f8584be19718823035
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011263"
---
# <a name="t-windows-installer"></a><span data-ttu-id="9c4dd-103">T (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="9c4dd-103">T (Windows Installer)</span></span>

<span data-ttu-id="9c4dd-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) T [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="9c4dd-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) T [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="9c4dd-105"><span id="_msi_transaction_processing_gly"></span><span id="_MSI_TRANSACTION_PROCESSING_GLY"></span>**Transaktionsverarbeitung**</span><span class="sxs-lookup"><span data-stu-id="9c4dd-105"><span id="_msi_transaction_processing_gly"></span><span id="_MSI_TRANSACTION_PROCESSING_GLY"></span>**transaction processing**</span></span>
</dt> <dd>

<span data-ttu-id="9c4dd-106">Mindestens ein Vorgang, der zusammen als einzelnes unteilbares Ganzes verarbeitet wird, wird als Transaktion bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9c4dd-106">One or more operations processed together as a single indivisible whole called a transaction.</span></span> <span data-ttu-id="9c4dd-107">Alle konstituierenden Vorgänge müssen erfolgreich ausgeführt werden, damit die Transaktion erfolgreich ist. Andernfalls wird für alle Vorgänge ein Rollback auf den ursprünglichen Zustand ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9c4dd-107">All the constituent operations must succeed for the transaction to succeed, otherwise all the operations are rolled back to the original state.</span></span>

</dd> <dt>

<span data-ttu-id="9c4dd-108"><span id="_msi_transform_gly"></span><span id="_MSI_TRANSFORM_GLY"></span>**Verwandeln**</span><span class="sxs-lookup"><span data-stu-id="9c4dd-108"><span id="_msi_transform_gly"></span><span id="_MSI_TRANSFORM_GLY"></span>**transform**</span></span>
</dt> <dd>

<span data-ttu-id="9c4dd-109">Vorlage der Unterschiede zwischen zwei [*Installer-Datenbanken,*](i-gly.md) die angewendet werden können, um ähnliche Änderungen in anderen Datenbanken zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="9c4dd-109">Template of the differences between two [*installer databases*](i-gly.md) that can be applied to produce similar changes in other databases.</span></span> <span data-ttu-id="9c4dd-110">Beispielsweise kann eine Lokalisierungstransformation verwendet werden, um die Sprache einer Anwendung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="9c4dd-110">For example, a localization transform can be used to change the language of an application.</span></span> <span data-ttu-id="9c4dd-111">Weitere Informationen finden Sie unter [Zusammenführungen und Transformationen.](merges-and-transforms.md)</span><span class="sxs-lookup"><span data-stu-id="9c4dd-111">For more information, see [Merges and Transforms](merges-and-transforms.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c4dd-112"><span id="_msi_transform_error_condition_flags_gly"></span><span id="_MSI_TRANSFORM_ERROR_CONDITION_FLAGS_GLY"></span>**Transformieren von Fehlerbedingungsflags**</span><span class="sxs-lookup"><span data-stu-id="9c4dd-112"><span id="_msi_transform_error_condition_flags_gly"></span><span id="_MSI_TRANSFORM_ERROR_CONDITION_FLAGS_GLY"></span>**transform error condition flags**</span></span>
</dt> <dd>

<span data-ttu-id="9c4dd-113">Satz von Eigenschaften, die zum Kennzeichnen der Fehlerbedingungen einer [*Transformation*](/windows)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9c4dd-113">Set of properties used to flag the error conditions of a [*transform*](/windows).</span></span> <span data-ttu-id="9c4dd-114">Weitere Informationen finden Sie unter [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span><span class="sxs-lookup"><span data-stu-id="9c4dd-114">For more information, see [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span></span>

</dd> <dt>

<span data-ttu-id="9c4dd-115"><span id="_msi_transform_validation_flags_gly"></span><span id="_MSI_TRANSFORM_VALIDATION_FLAGS_GLY"></span>**Transformieren von Validierungsflags**</span><span class="sxs-lookup"><span data-stu-id="9c4dd-115"><span id="_msi_transform_validation_flags_gly"></span><span id="_MSI_TRANSFORM_VALIDATION_FLAGS_GLY"></span>**transform validation flags**</span></span>
</dt> <dd>

<span data-ttu-id="9c4dd-116">Satz von Eigenschaften, mit denen überprüft wird, ob die [*Transformation*](/windows) auf die Datenbank angewendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9c4dd-116">Set of properties used to verify that the [*transform*](/windows) can be applied to the database.</span></span> <span data-ttu-id="9c4dd-117">Eine Liste dieser Eigenschaften finden Sie unter [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span><span class="sxs-lookup"><span data-stu-id="9c4dd-117">For a list of these properties, see [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span></span>

</dd> </dl>

 

 
