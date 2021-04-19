---
description: Beschreibt die WMI-SNMP-Anbieter Fehler 1051 bis 1060.
ms.assetid: 789cc5b6-e3ef-4f66-8dec-6970d6df1fe9
ms.tgt_platform: multiple
title: Fehler 1051 bis 1060
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 170eddf3126a40f929aa36899259b731fa244941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352446"
---
# <a name="errors-1051-through-1060"></a><span data-ttu-id="9b0fd-103">Fehler 1051 bis 1060</span><span class="sxs-lookup"><span data-stu-id="9b0fd-103">Errors 1051 through 1060</span></span>

<span data-ttu-id="9b0fd-104">Beschreibt die WMI-SNMP-Anbieter Fehler 1051 bis 1060.</span><span class="sxs-lookup"><span data-stu-id="9b0fd-104">Describes WMI SNMP provider errors 1051 through 1060.</span></span>

[<span data-ttu-id="9b0fd-105">Schwerwiegender Fehler 1051</span><span class="sxs-lookup"><span data-stu-id="9b0fd-105">Fatal Error 1051</span></span>](#fatal-error-1051)

[<span data-ttu-id="9b0fd-106">Schwerwiegender Fehler 1054</span><span class="sxs-lookup"><span data-stu-id="9b0fd-106">Fatal Error 1054</span></span>](#fatal-error-1054)

[<span data-ttu-id="9b0fd-107">Schwerwiegender Fehler 1055</span><span class="sxs-lookup"><span data-stu-id="9b0fd-107">Fatal Error 1055</span></span>](#fatal-error-1055)

## <a name="fatal-error-1051"></a><span data-ttu-id="9b0fd-108">Schwerwiegender Fehler 1051</span><span class="sxs-lookup"><span data-stu-id="9b0fd-108">Fatal Error 1051</span></span>

<dl> <dt>

<span data-ttu-id="9b0fd-109"><span id="_1051__Fatal_____fileName___line____Ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__fatal_____filename___line____ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__FATAL_____FILENAME___LINE____AMBIGUOUS_REFERENCE_TO_SYMBOL__IDENTIFIER__"></span>**<1051, schwerwiegender>: " <fileName> : <line \#>: mehrdeutiger Verweis auf Symbol <identifier> "**</span><span class="sxs-lookup"><span data-stu-id="9b0fd-109"><span id="_1051__Fatal_____fileName___line____Ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__fatal_____filename___line____ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__FATAL_____FILENAME___LINE____AMBIGUOUS_REFERENCE_TO_SYMBOL__IDENTIFIER__"></span>**<1051, Fatal>: "<fileName>:<line\#>: Ambiguous reference to symbol <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="9b0fd-110">Der Code für die Modul Semantik der Importe ist spezifisch für weder SNMPv1 noch SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="9b0fd-110">IMPORTS section module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="9b0fd-111">Jeder Objekt Deskriptor, der einem Objekt in einer Internet Standard-MIB entspricht, muss eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="9b0fd-111">Each object descriptor corresponding to an object in an Internet Standard MIB must be unique.</span></span> <span data-ttu-id="9b0fd-112">Da Enterprise-MIBs allgemeine Objekt Deskriptoren haben können, müssen solche Deskriptoren, die aus zwei Modulen importiert werden, im MIB-Modul mithilfe der Notation "Module. Descriptor" eindeutig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9b0fd-112">Since enterprise MIBs can have common object descriptors, such descriptors imported from two modules must be used unambiguously in the MIB module by using the notation "module.descriptor."</span></span>

</dd> </dl>

## <a name="fatal-error-1054"></a><span data-ttu-id="9b0fd-113">Schwerwiegender Fehler 1054</span><span class="sxs-lookup"><span data-stu-id="9b0fd-113">Fatal Error 1054</span></span>

<dl> <dt>

<span data-ttu-id="9b0fd-114"><span id="_1054__Fatal_____fileName___line_____identifier__in_INDEX_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__fatal_____filename___line_____identifier__in_index_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__FATAL_____FILENAME___LINE_____IDENTIFIER__IN_INDEX_CLAUSE_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1054, schwerwiegender>: " <fileName> : <line \#>: <identifier> in einer Index Klausel wird nicht in einen der zulässigen Typen aufgelöst."**</span><span class="sxs-lookup"><span data-stu-id="9b0fd-114"><span id="_1054__Fatal_____fileName___line_____identifier__in_INDEX_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__fatal_____filename___line_____identifier__in_index_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__FATAL_____FILENAME___LINE_____IDENTIFIER__IN_INDEX_CLAUSE_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1054, Fatal>: "<fileName>:<line\#>: <identifier> in INDEX clause does not resolve to one of the allowed types"**</span></span>
</dt> <dd>

<span data-ttu-id="9b0fd-115">Semantik Fehler des **Objekttyp-** Makro Aufruf Moduls.</span><span class="sxs-lookup"><span data-stu-id="9b0fd-115">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="9b0fd-116">Der Typ eines Objekts in der Index Klausel oder ein beliebiger Typ, der in der Index-Klausel angegeben ist, muss in einen skalaren Typ aufgelöst werden, d. h. eine nicht-Sequenz oder eine nicht-Sequenz vom Typ.</span><span class="sxs-lookup"><span data-stu-id="9b0fd-116">The type of an object in the INDEX clause, or any type specified in the INDEX clause, must resolve to a scalar type, that is, a non-SEQUENCE or non-SEQUENCE OF type.</span></span> <span data-ttu-id="9b0fd-117">Jeder in der Index-Klausel angegebene Typ muss ebenfalls in einen dieser Typen aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="9b0fd-117">Any type specified in the INDEX clause must also resolve to one of these.</span></span>

<span data-ttu-id="9b0fd-118">Dieser Fehler kann entweder in SNMPv1 oder SNMPv2C auftreten.</span><span class="sxs-lookup"><span data-stu-id="9b0fd-118">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1055"></a><span data-ttu-id="9b0fd-119">Schwerwiegender Fehler 1055</span><span class="sxs-lookup"><span data-stu-id="9b0fd-119">Fatal Error 1055</span></span>

<dl> <dt>

<span data-ttu-id="9b0fd-120"><span id="_1055__Fatal____fileName___line____SYNTAX_of_INDEX_OBJECT-TYPE__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__fatal____filename___line____syntax_of_index_object-type__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__FATAL____FILENAME___LINE____SYNTAX_OF_INDEX_OBJECT-TYPE__IDENTIFIER___DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1055, schwerwiegender>: " <fileName> : <line \#>: Syntax des Index Objekt Typs <identifier> wird nicht in einen der zulässigen Typen aufgelöst"**</span><span class="sxs-lookup"><span data-stu-id="9b0fd-120"><span id="_1055__Fatal____fileName___line____SYNTAX_of_INDEX_OBJECT-TYPE__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__fatal____filename___line____syntax_of_index_object-type__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__FATAL____FILENAME___LINE____SYNTAX_OF_INDEX_OBJECT-TYPE__IDENTIFIER___DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1055, Fatal>:"<fileName>:<line\#>: SYNTAX of INDEX OBJECT-TYPE <identifier>, does not resolve to one of the allowed types"**</span></span>
</dt> <dd>

<span data-ttu-id="9b0fd-121">Semantik Fehler des **Objekttyp-** Makro Aufruf Moduls.</span><span class="sxs-lookup"><span data-stu-id="9b0fd-121">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="9b0fd-122">Der Typ eines Objekts in der Index Klausel oder ein beliebiger Typ, der in der Index-Klausel angegeben ist, muss in einen skalaren Typ aufgelöst werden, d. h. eine nicht-Sequenz oder eine nicht-Sequenz vom Typ.</span><span class="sxs-lookup"><span data-stu-id="9b0fd-122">The type of an object in the INDEX clause, or any type specified in the INDEX clause, must resolve to a scalar type, that is, a non-SEQUENCE or non-SEQUENCE OF type.</span></span>

<span data-ttu-id="9b0fd-123">Dieser Fehler kann entweder in SNMPv1 oder SNMPv2C auftreten.</span><span class="sxs-lookup"><span data-stu-id="9b0fd-123">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

 

 



