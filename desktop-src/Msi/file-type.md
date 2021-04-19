---
description: Der Dateityp des semantischen Typs ist einer der Schlüssel Format Typen. Dieser Typ besteht aus einem Fremdschlüssel in der vom Benutzer bereitgestellten Dateitabelle.
ms.assetid: cbcaa016-879e-48c2-93c6-b0e91e1eb9ed
title: Dateityp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36b47e76f4a910b336c749a4f0d5001c8568cead
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364096"
---
# <a name="file-type"></a><span data-ttu-id="a1be7-104">Dateityp</span><span class="sxs-lookup"><span data-stu-id="a1be7-104">File Type</span></span>

<span data-ttu-id="a1be7-105">Der Dateityp des [semantischen Typs](semantic-types.md) ist einer der [Schlüssel Format Typen](key-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="a1be7-105">The File Type of [semantic type](semantic-types.md) is one of the [Key Format Types](key-format-types.md).</span></span> <span data-ttu-id="a1be7-106">Dieser Typ besteht aus einem Fremdschlüssel in der vom Benutzer bereitgestellten [Dateitabelle](file-table.md) .</span><span class="sxs-lookup"><span data-stu-id="a1be7-106">This type consists of a foreign key into the [File table](file-table.md) provided by the user.</span></span>

<span data-ttu-id="a1be7-107">Der Dateityp kann mit den folgenden Arten von ContextData verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a1be7-107">The File type may be used with the following kinds of ContextData.</span></span>

<span data-ttu-id="a1be7-108">**Assemblycontext ContextData**</span><span class="sxs-lookup"><span data-stu-id="a1be7-108">**AssemblyContext ContextData**</span></span>

<span data-ttu-id="a1be7-109">Dieser Typ kann verwendet werden, um es Benutzern zu ermöglichen, Fremdschlüssel für Win32-oder Common Language Runtime Assemblys zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="a1be7-109">This type may be used to enable users to configure foreign keys to Win32 or common language runtime assemblies.</span></span> <span data-ttu-id="a1be7-110">Das Merge-Tool muss einen Windows Installer [Bezeichner](identifier.md) für Elemente dieses Typs in die Vorlage in der Spalte Wert der [Tabelle ModuleSubstitution](modulesubstitution-table.md)ersetzen.</span><span class="sxs-lookup"><span data-stu-id="a1be7-110">The merge tool must substitute a Windows Installer [Identifier](identifier.md) for items of this type into the template in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span> <span data-ttu-id="a1be7-111">Mergemod.dll erzwingt dies nicht, und es liegt an dem Merge-Tool, sicherzustellen, dass der Benutzer einen gültigen Schlüssel für die Dateitabelle bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="a1be7-111">Mergemod.dll does not enforce this and it is up to the merge tool to ensure that the user provides a valid key into the File table.</span></span>

<span data-ttu-id="a1be7-112">NULL ist ein gültiger Wert für diesen Typ, es sei denn, der msmconfigitemnonable-Wert ist im Feld Attribute der [Tabelle ModuleConfiguration](moduleconfiguration-table.md)enthalten.</span><span class="sxs-lookup"><span data-stu-id="a1be7-112">Null is a valid value for this type unless the msmConfigItemNonNullable has been included in the Attributes field of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

 

 



