---
title: Vererbung von Pointer-Attribute Typen
description: Gemäß der DCE-Spezifikation muss jede IDL-Dateiattribute für Ihre Zeiger definieren.
ms.assetid: ab8821ce-d52a-42bf-aa5e-582bb24adf93
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 182b7d46774484a9520424fd82bcff2d7103aa3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390833"
---
# <a name="pointer-attribute-type-inheritance"></a><span data-ttu-id="cd753-103">Vererbung von Pointer-Attribute Typen</span><span class="sxs-lookup"><span data-stu-id="cd753-103">Pointer-Attribute Type Inheritance</span></span>

<span data-ttu-id="cd753-104">Gemäß der DCE-Spezifikation muss jede IDL-Dateiattribute für Ihre Zeiger definieren.</span><span class="sxs-lookup"><span data-stu-id="cd753-104">According to the DCE specification, each IDL file must define attributes for its pointers.</span></span> <span data-ttu-id="cd753-105">Wenn ein explizites Attribut keinem Zeiger zugewiesen ist, verwendet der Zeiger den Wert, der vom \[ [Zeiger \_ default](/windows/desktop/Midl/pointer-default) - \] Schlüsselwort angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cd753-105">If an explicit attribute is not assigned to a pointer, the pointer uses the value specified by the \[ [pointer\_default](/windows/desktop/Midl/pointer-default)\] keyword.</span></span> <span data-ttu-id="cd753-106">Einige DCE-Implementierungen lassen keine nicht attributierten Zeiger zu.</span><span class="sxs-lookup"><span data-stu-id="cd753-106">Some DCE implementations do not allow unattributed pointers.</span></span> <span data-ttu-id="cd753-107">Wenn ein Zeiger kein explizites Attribut hat, muss die IDL-Datei eine **\[ Zeiger \_ Standard \]** Spezifikation aufweisen, damit das Zeiger Attribut festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="cd753-107">If a pointer does not have an explicit attribute, the IDL file must have a **\[pointer\_default\]** specification so that the pointer attribute can be set.</span></span>

<span data-ttu-id="cd753-108">Im Standardmodus (Microsoft-Extensions) können Sie das-Attribut eines Zeigers in der IDL-Datei angeben, die die definierende IDL-Datei importiert.</span><span class="sxs-lookup"><span data-stu-id="cd753-108">In default (Microsoft-extensions) mode, you can specify a pointer's attribute in the IDL file that imports the defining IDL file.</span></span> <span data-ttu-id="cd753-109">In einer IDL-Datei definierte Zeiger können Attribute erben, die in anderen IDL-Dateien angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="cd753-109">Pointers defined in one IDL file can inherit attributes that are specified in other IDL files.</span></span> <span data-ttu-id="cd753-110">Außerdem können IDL-Dateien im Standardmodus nicht attributierte Zeiger enthalten.</span><span class="sxs-lookup"><span data-stu-id="cd753-110">Also, in default mode, IDL files can include unattributed pointers.</span></span> <span data-ttu-id="cd753-111">Wenn weder die Basis-noch die importierten IDL-Dateien ein Zeiger Attribut oder einen Zeiger auf den **\[ \_ Standard \]** Wert angeben, werden nicht attributierte Zeiger als eindeutige Zeiger interpretiert.</span><span class="sxs-lookup"><span data-stu-id="cd753-111">If neither the base nor the imported IDL files specify a pointer attribute or **\[pointer\_default\]**, unattributed pointers are interpreted as unique pointers.</span></span>

<span data-ttu-id="cd753-112">Der mittlerer l-Compiler weist Zeiger Attribute mithilfe der folgenden Prioritätsregeln (1 ist am höchsten) Zeiger Attributen zu.</span><span class="sxs-lookup"><span data-stu-id="cd753-112">The MIDL compiler assigns pointer attributes to pointers using the following priority rules (1 is highest).</span></span>



| <span data-ttu-id="cd753-113">Priorität</span><span class="sxs-lookup"><span data-stu-id="cd753-113">Priority</span></span> | <span data-ttu-id="cd753-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cd753-114">Description</span></span>                                                                                                                |
|----------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd753-115">1</span><span class="sxs-lookup"><span data-stu-id="cd753-115">1</span></span>        | <span data-ttu-id="cd753-116">Explizite Zeiger Attribute werden auf den Zeiger an der Definition oder der Verwendungs Website angewendet.</span><span class="sxs-lookup"><span data-stu-id="cd753-116">Explicit pointer attributes are applied to the pointer at the definition or use site.</span></span>                                      |
| <span data-ttu-id="cd753-117">2</span><span class="sxs-lookup"><span data-stu-id="cd753-117">2</span></span>        | <span data-ttu-id="cd753-118">Der Standardwert ist das **\[ Zeiger- \_ Standard \]** Attribut in der IDL-Datei, die den Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="cd753-118">The default is the **\[pointer\_default\]** attribute in the IDL file that defines the type.</span></span>                               |
| <span data-ttu-id="cd753-119">3</span><span class="sxs-lookup"><span data-stu-id="cd753-119">3</span></span>        | <span data-ttu-id="cd753-120">Der Standardwert ist das **\[ Zeiger- \_ Standard \]** Attribut in der IDL-Datei, die den Typ importiert.</span><span class="sxs-lookup"><span data-stu-id="cd753-120">The default is the **\[pointer\_default\]** attribute in the IDL file that imports the type.</span></span>                               |
| <span data-ttu-id="cd753-121">4</span><span class="sxs-lookup"><span data-stu-id="cd753-121">4</span></span>        | <span data-ttu-id="cd753-122">Der Standardwert ist \[ [ptr](/windows/desktop/Midl/ptr) \] im DCE-Kompatibilitätsmodus oder \[ [](/windows/desktop/Midl/unique) \] im Microsoft-Erweiterungs Modus eindeutig.</span><span class="sxs-lookup"><span data-stu-id="cd753-122">The default is \[ [ptr](/windows/desktop/Midl/ptr)\] in DCE-compatibility mode, or \[ [unique](/windows/desktop/Midl/unique)\] in Microsoft-extensions mode.</span></span> |



 

 

 