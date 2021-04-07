---
title: Schnittstellen Definitionsdatei (IDL)
description: Gemäß der Konvention wird die Datei, die Schnittstellen-und Typbibliotheks Definitionen enthält, als IDL-Datei und die Dateinamenerweiterung. idl bezeichnet.
ms.assetid: 4df87df8-3206-4845-b5ab-d77ea443b9e3
keywords:
- Schnittstellen-Mittell, IDL-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 950daa2c1841f6e4b3f015f14e373804fcd34b80
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725432"
---
# <a name="interface-definition-idl-file"></a><span data-ttu-id="65b15-104">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="65b15-104">Interface Definition (IDL) File</span></span>

<span data-ttu-id="65b15-105">Gemäß der Konvention wird die Datei, die Schnittstellen-und Typbibliotheks Definitionen enthält, als IDL-Datei und die Dateinamenerweiterung. idl bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="65b15-105">By convention, the file that contains interface and type library definitions is called an IDL file, and has an .idl file name extension.</span></span> <span data-ttu-id="65b15-106">Tatsächlich analysiert der mittlerer l-Compiler unabhängig von seiner Erweiterung eine Schnittstellen Definitionsdatei.</span><span class="sxs-lookup"><span data-stu-id="65b15-106">In reality, the MIDL compiler will parse an interface definition file regardless of its extension.</span></span> <span data-ttu-id="65b15-107">Eine Schnittstelle wird durch die Schlüsselwort [**Schnittstelle**](interface.md)identifiziert.</span><span class="sxs-lookup"><span data-stu-id="65b15-107">An interface is identified by the keyword [**interface**](interface.md).</span></span>

<span data-ttu-id="65b15-108">Jede Schnittstelle besteht aus einem Header und einem Text.</span><span class="sxs-lookup"><span data-stu-id="65b15-108">Each interface consists of a header and a body.</span></span> <span data-ttu-id="65b15-109">Der Schnittstellen Header enthält Attribute, die auf die gesamte Schnittstelle angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="65b15-109">The interface header contains attributes that apply to the entire interface.</span></span> <span data-ttu-id="65b15-110">Der Text der-Schnittstelle enthält die restlichen Schnittstellendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="65b15-110">The body of the interface contains the remaining interface definitions.</span></span> <span data-ttu-id="65b15-111">Eine Übersicht über Schnittstellen und IDL-Dateien finden Sie in [der IDL-Datei (Interface Definition Language)](/windows/desktop/Rpc/the-interface-definition-language-idl-file).</span><span class="sxs-lookup"><span data-stu-id="65b15-111">For an overview of interfaces and IDL files, see [The Interface Definition Language (IDL) File](/windows/desktop/Rpc/the-interface-definition-language-idl-file).</span></span> <span data-ttu-id="65b15-112">Eine Zusammenfassung der Attribute, die in einem Schnittstellen Header verwendet werden können, finden Sie unter [IDL-Attribute](idl-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="65b15-112">For a summary of attributes that can be used in an interface header, see [IDL Attributes](idl-attributes.md).</span></span>

 

 