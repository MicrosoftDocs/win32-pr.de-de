---
description: Die ganzzahligen Format Typen konfigurierbarer Daten können entweder in Text-oder ganzzahligen Datenbankfeldern verwendet werden. Das msmconfigitemnonable-Attribut ist in diesem Datenformat implizit und muss nicht festgelegt werden. NULL ist nie ein gültiger Wert für diesen Typ.
ms.assetid: 63fb9c0d-e7f1-4c1d-bb83-2833c5fff18d
title: Ganzzahlige Format Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 184ef6380f25474a9e2ad07be7a4eb6d00706aee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757033"
---
# <a name="integer-format-types"></a><span data-ttu-id="1569c-105">Ganzzahlige Format Typen</span><span class="sxs-lookup"><span data-stu-id="1569c-105">Integer Format Types</span></span>

<span data-ttu-id="1569c-106">Die ganzzahligen Format Typen konfigurierbarer Daten können entweder in Text-oder ganzzahligen Datenbankfeldern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1569c-106">The Integer Format Types of configurable data may be used in either text or integer database fields.</span></span> <span data-ttu-id="1569c-107">Das msmconfigitemnonable-Attribut ist in diesem Datenformat implizit und muss nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1569c-107">The msmConfigItemNonNullable attribute is implicit in this data format and does not need to be set.</span></span> <span data-ttu-id="1569c-108">NULL ist nie ein gültiger Wert für diesen Typ.</span><span class="sxs-lookup"><span data-stu-id="1569c-108">Null is never a valid value for this type.</span></span>

<span data-ttu-id="1569c-109">Der folgende ganzzahlige Formattyp ist vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1569c-109">The following Integer Format type exists.</span></span>

[<span data-ttu-id="1569c-110">Beliebiger Integer-Typ</span><span class="sxs-lookup"><span data-stu-id="1569c-110">Arbitrary Integer Type</span></span>](arbitrary-integer-type.md)

<span data-ttu-id="1569c-111">Konfigurierbare Elemente des ganzzahligen Formattyps werden in Text-oder ganzzahligen Spalten verwendet und können im Allgemeinen durch eine beliebige positive oder negative ganze Zahl ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="1569c-111">Configurable items of the Integer Format Type are used in either text or integer columns and in general could be replaced by any positive or negative integer.</span></span> <span data-ttu-id="1569c-112">Bestimmte konfigurierbare Elemente können jedoch auch über charakteristische Semantik Einschränkungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="1569c-112">However, particular configurable items may also have characteristic semantic restrictions.</span></span> <span data-ttu-id="1569c-113">Beispielsweise weist ein bestimmtes konfigurierbares Element, das eine ganze Zahl zwischen 0 und 100 sein muss, eine zusätzliche semantische Einschränkung auf.</span><span class="sxs-lookup"><span data-stu-id="1569c-113">For example, a particular configurable item required to be an integer between 0 and 100 has and additional semantic restriction.</span></span> <span data-ttu-id="1569c-114">Solche Einschränkungen werden von Mergemod.dll nicht erzwungen. Daher sollten Modul Autoren darauf vorbereitet sein, jede beliebige Zeichenfolge zu verarbeiten, die den angegebenen ganzzahligen Formattyp erfüllt.</span><span class="sxs-lookup"><span data-stu-id="1569c-114">Such restrictions are not enforced by Mergemod.dll and therefore module authors should be prepared to handle any string that satisfies the specified Integer Format type.</span></span>

 

 



