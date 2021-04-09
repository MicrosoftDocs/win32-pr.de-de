---
title: IDL-Dateien
description: IDL-Dateien
ms.assetid: 94a6752d-fcf3-47ce-ac3f-be1d1c9768e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bc9a736bf9b9a77ec1cb655fb5c76e9e1c0d27e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103858498"
---
# <a name="idl-files"></a><span data-ttu-id="9e7dc-103">IDL-Dateien</span><span class="sxs-lookup"><span data-stu-id="9e7dc-103">IDL Files</span></span>

<span data-ttu-id="9e7dc-104">Com verwendet die Microsoft Interface Definition Language (mittlere), um COM-Objekte zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="9e7dc-104">COM uses the Microsoft Interface Definition Language (MIDL) to describe COM objects.</span></span> <span data-ttu-id="9e7dc-105">"Mittel l" ist eine Erweiterung der IDL für verteilte Computerumgebungen, die von der Open Software Foundation definiert wurden, die zum Definieren von Schnittstellen für Remote Prozedur Aufrufe in herkömmlichen Client-/Server-Anwendungen entwickelt wurde.</span><span class="sxs-lookup"><span data-stu-id="9e7dc-105">MIDL is an extension of the IDL for distributed computing environments defined by the Open Software Foundation, which was developed to define interfaces for remote procedure calls in traditional client/server applications.</span></span> <span data-ttu-id="9e7dc-106">Die Mittel l enthält die meisten Attribute und Anweisungen der Object Definition Language (ODL), der ursprünglich zum Generieren von Typbibliotheken für OLE-Automatisierung verwendeten Sprache.</span><span class="sxs-lookup"><span data-stu-id="9e7dc-106">MIDL includes most of the attributes and statements of Object Definition Language (ODL), the language originally used to generate type libraries for OLE Automation.</span></span>

<span data-ttu-id="9e7dc-107">In C++ und Java erstellt ein Entwickler, der ein COM-Objekt erstellt, eine IDL-Datei, die vom-compilercompiler verarbeitet wird, um eine Typbibliothek oder Header-und Proxy Dateien zu erstellen, oder beides.</span><span class="sxs-lookup"><span data-stu-id="9e7dc-107">In C++ and Java, a developer building a COM object creates an IDL file that the MIDL compiler then processes to create a type library or header and proxy files, or both.</span></span> <span data-ttu-id="9e7dc-108">Eine *Typbibliothek* ist eine Binärdatei, die das COM-Objekt oder die COM-Schnittstellen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="9e7dc-108">A *type library* is a binary file that describes the COM object or COM interfaces, or both.</span></span> <span data-ttu-id="9e7dc-109">Eine Typbibliothek ist die kompilierte Version der IDL-Datei.</span><span class="sxs-lookup"><span data-stu-id="9e7dc-109">A type library is the compiled version of the IDL file.</span></span> <span data-ttu-id="9e7dc-110">Typbibliotheken unterstützen jedoch nur ODL-Semantik.</span><span class="sxs-lookup"><span data-stu-id="9e7dc-110">However, type libraries support ODL semantics only.</span></span> <span data-ttu-id="9e7dc-111">Vor allem können Sie nicht alle Informationen aus einer IDL-Datei darstellen, die sich auf IDL-Attribute wie " \[ [**\_ size**](/windows/desktop/Midl/size-is)" bezieht \] .</span><span class="sxs-lookup"><span data-stu-id="9e7dc-111">In particular, they cannot represent all the information from an IDL file related to IDL attributes like \[[**size\_is**](/windows/desktop/Midl/size-is)\].</span></span> <span data-ttu-id="9e7dc-112">Sie müssen Proxy Dateien für IDL-Dateien erstellen und verwenden, die von Informations Verlusten in der Typbibliothek betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="9e7dc-112">You need to create and use proxy files for IDL files affected by information loss in the type library.</span></span>

<span data-ttu-id="9e7dc-113">In Visual Basic erstellt ein Entwickler, der ein COM-Objekt erstellt, keine IDL-Datei.</span><span class="sxs-lookup"><span data-stu-id="9e7dc-113">In Visual Basic, a developer creating a COM object does not create an IDL file.</span></span> <span data-ttu-id="9e7dc-114">Stattdessen sammelt Visual Basic Informationen mithilfe von Klassen-und Projekteigenschaften und erstellt die Typbibliothek direkt.</span><span class="sxs-lookup"><span data-stu-id="9e7dc-114">Instead, Visual Basic gathers information using class and project properties and directly creates the type library.</span></span>

 

 