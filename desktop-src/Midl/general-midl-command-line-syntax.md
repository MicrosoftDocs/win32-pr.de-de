---
title: Allgemeine Syntax der Mittell-Befehlszeile
description: Der mittlerer l-Compiler verarbeitet eine IDL-Datei und eine optionale Anwendungs Konfigurationsdatei (ACF), um einen Satz von Ausgabedateien zu generieren.
ms.assetid: 1906b374-d0d1-4ec8-9a00-c5228b4c29ca
keywords:
- Befehlszeilen Referenz-Mittell, allgemeine Syntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14baa145c7be03467a24bd4298cf2f502d93b6ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856844"
---
# <a name="general-midl-command-line-syntax"></a><span data-ttu-id="eef22-104">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="eef22-104">General MIDL Command-line Syntax</span></span>

<span data-ttu-id="eef22-105">Der mittlerer l-Compiler verarbeitet eine IDL-Datei und eine optionale Anwendungs Konfigurationsdatei (ACF), um einen Satz von Ausgabedateien zu generieren.</span><span class="sxs-lookup"><span data-stu-id="eef22-105">The MIDL compiler processes an IDL file and an optional application configuration file (ACF) to generate a set of output files.</span></span> <span data-ttu-id="eef22-106">Die in der Schnittstellen Attribut Liste der IDL-Datei angegebenen Attribute bestimmen, ob der Compiler Quelldateien für eine RPC-Schnittstelle oder für eine benutzerdefinierte OLE-Schnittstelle generiert.</span><span class="sxs-lookup"><span data-stu-id="eef22-106">The attributes specified in the IDL file's interface attribute list determine whether the compiler generates source files for an RPC interface or for a custom OLE interface.</span></span>

## <a name="switch-options"></a><span data-ttu-id="eef22-107">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="eef22-107">Switch Options</span></span>

``` syntax
     midl [command-line-switch [switch-options]] filename
    
```

<dl> <dt>

<span data-ttu-id="eef22-108"><span id="command-line-switch"></span><span id="COMMAND-LINE-SWITCH"></span>*Befehls Zeilenschalter*</span><span class="sxs-lookup"><span data-stu-id="eef22-108"><span id="command-line-switch"></span><span id="COMMAND-LINE-SWITCH"></span>*command-line-switch*</span></span>
</dt> <dd>

<span data-ttu-id="eef22-109">Gibt Befehls Zeilenschalter für Mittel-Compiler an.</span><span class="sxs-lookup"><span data-stu-id="eef22-109">Specifies MIDL compiler command-line switches.</span></span> <span data-ttu-id="eef22-110">Switches können in beliebiger Reihenfolge angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="eef22-110">Switches can appear in any sequence.</span></span>

</dd> <dt>

<span data-ttu-id="eef22-111"><span id="switch-options"></span><span id="SWITCH-OPTIONS"></span>*Switch-Optionen*</span><span class="sxs-lookup"><span data-stu-id="eef22-111"><span id="switch-options"></span><span id="SWITCH-OPTIONS"></span>*switch-options*</span></span>
</dt> <dd>

<span data-ttu-id="eef22-112">Gibt die jedem Switch zugeordneten Optionen an.</span><span class="sxs-lookup"><span data-stu-id="eef22-112">Specifies options associated with each switch.</span></span> <span data-ttu-id="eef22-113">Gültige Optionen werden im Verweis Eintrag für jeden Mittelpunkt-Compilerschalter beschrieben.</span><span class="sxs-lookup"><span data-stu-id="eef22-113">Valid options are described in the reference entry for each MIDL compiler switch.</span></span>

</dd> <dt>

<span data-ttu-id="eef22-114"><span id="filename"></span><span id="FILENAME"></span>*Einfügen*</span><span class="sxs-lookup"><span data-stu-id="eef22-114"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="eef22-115">Gibt den Namen der IDL-Datei an.</span><span class="sxs-lookup"><span data-stu-id="eef22-115">Specifies the name of the IDL file.</span></span> <span data-ttu-id="eef22-116">Diese Datei weist in der Regel die Erweiterung. idl auf, Sie kann jedoch auch einen anderen Wert oder keinen enthalten.</span><span class="sxs-lookup"><span data-stu-id="eef22-116">This file usually has the extension .idl, but it can have another or none.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eef22-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eef22-117">Remarks</span></span>

<span data-ttu-id="eef22-118">In den folgenden Listen sind die Standardnamen der Dateien aufgeführt, die für eine IDL-Datei namens. IDL generiert werden.</span><span class="sxs-lookup"><span data-stu-id="eef22-118">The following lists show the default names of the files generated for an IDL file named Name.idl.</span></span> <span data-ttu-id="eef22-119">Sie können Befehls Zeilenschalter verwenden, um diese Standardnamen zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="eef22-119">You can use command-line switches to override these default names.</span></span> <span data-ttu-id="eef22-120">Beachten Sie, dass der Name der IDL-Datei eine andere Erweiterung als IDL oder keine Erweiterung aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="eef22-120">Note that the name of the IDL file can have an extension other than .idl, or no extension at all.</span></span>

<span data-ttu-id="eef22-121">Standardmäßig generiert der Compiler die folgenden Dateien für eine [RPC-Schnittstelle](files-generated-for-an-rpc-interface.md), wenn die Schnittstellen Attribut Liste das [**Objekt**](object.md) oder das [**lokale**](local.md) Attribut nicht enthält.</span><span class="sxs-lookup"><span data-stu-id="eef22-121">By default (that is, if the interface attribute list does not contain the [**object**](object.md) or [**local**](local.md) attribute), the compiler generates the following files for an [RPC interface](files-generated-for-an-rpc-interface.md):</span></span>

-   <span data-ttu-id="eef22-122">Client-Stub (Name \_ c. c)</span><span class="sxs-lookup"><span data-stu-id="eef22-122">Client stub (name\_c.c)</span></span>
-   <span data-ttu-id="eef22-123">Server-Stub (Name \_ s. c)</span><span class="sxs-lookup"><span data-stu-id="eef22-123">Server stub (name\_s.c)</span></span>
-   <span data-ttu-id="eef22-124">Header Datei (Name. h)</span><span class="sxs-lookup"><span data-stu-id="eef22-124">Header file (name.h)</span></span>

<span data-ttu-id="eef22-125">Wenn das [**Objekt**](object.md) Attribut in der Liste der Schnittstellen Attribute angezeigt wird, generiert der Compiler die folgenden Dateien für eine COM-Schnittstelle:</span><span class="sxs-lookup"><span data-stu-id="eef22-125">When the [**object**](object.md) attribute appears in the interface attribute list, the compiler generates the following files for a COM interface:</span></span>

-   <span data-ttu-id="eef22-126">Schnittstellen Proxy Datei (Name \_ p. c)</span><span class="sxs-lookup"><span data-stu-id="eef22-126">Interface proxy file (name\_p.c)</span></span>
-   <span data-ttu-id="eef22-127">Schnittstellen Header Datei (Name. h)</span><span class="sxs-lookup"><span data-stu-id="eef22-127">Interface header file (name.h)</span></span>
-   <span data-ttu-id="eef22-128">Interface UUID-Datei (Name \_ I. c)</span><span class="sxs-lookup"><span data-stu-id="eef22-128">Interface UUID file (name\_I.c)</span></span>

<span data-ttu-id="eef22-129">Wenn das [**lokale**](local.md) Attribut in der Liste der Schnittstellen Attribute angezeigt wird, generiert der Compiler nur die Schnittstellen Header Datei namens. h.</span><span class="sxs-lookup"><span data-stu-id="eef22-129">When the [**local**](local.md) attribute appears in the interface attribute list, the compiler generates only the interface header file, Name.h.</span></span>

<span data-ttu-id="eef22-130">Der von Microsoft RPC bereitgestellte mittlerer l-Compiler ruft den C-Präprozessor nach Bedarf auf, um die IDL-Datei zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="eef22-130">The MIDL compiler provided with Microsoft RPC invokes the C preprocessor as needed to process the IDL file.</span></span> <span data-ttu-id="eef22-131">Der C-Compiler wird nicht automatisch aufgerufen, um generierte Dateien zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="eef22-131">It does not automatically invoke the C compiler to compile generated files.</span></span>

> [!Note]  
> <span data-ttu-id="eef22-132">Der mit Microsoft RPC bereitgestellte mittlerer l-Compiler verwendet eine andere Befehlszeilen Syntax als der DCE-IDL-Compiler.</span><span class="sxs-lookup"><span data-stu-id="eef22-132">The MIDL compiler provided with Microsoft RPC uses a different command-line syntax than the DCE IDL compiler.</span></span>

 

<span data-ttu-id="eef22-133">Der-Compilerschalter [**/env**](-env.md), [**/Server**](-server.md), [**/sstub**](-sstub.md)und [**/out**](-out.md) wirkt sich auf die Server-Stub-Datei aus.</span><span class="sxs-lookup"><span data-stu-id="eef22-133">The MIDL compiler switches [**/env**](-env.md), [**/server**](-server.md), [**/sstub**](-sstub.md), and [**/out**](-out.md) affect the server stub file.</span></span>

<span data-ttu-id="eef22-134">Beginnend mit der 6.0.359-Mittell-Version ist die standardmäßige Befehlszeilenoption für den-Mittell-Compiler [**/Oicf**](-oi.md)- [**/robust**](-robust.md).</span><span class="sxs-lookup"><span data-stu-id="eef22-134">Starting with MIDL version 6.0.359, the default command line option for the MIDL compiler is [**/Oicf**](-oi.md)Â  [**/robust**](-robust.md).</span></span> <span data-ttu-id="eef22-135">Um/robust zu deaktivieren, geben Sie die [**/No \_ robust**](-no-robust.md) -Option an.</span><span class="sxs-lookup"><span data-stu-id="eef22-135">To disable /robust, specify the [**/no\_robust**](-no-robust.md) option.</span></span>

## <a name="the-header-file"></a><span data-ttu-id="eef22-136">Die Header Datei</span><span class="sxs-lookup"><span data-stu-id="eef22-136">The Header File</span></span>

<span data-ttu-id="eef22-137">Die Header Datei enthält Definitionen aller in der IDL-Datei deklarierten Datentypen und Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="eef22-137">The header file contains definitions of all the data types and operations declared in the IDL file.</span></span> <span data-ttu-id="eef22-138">Die Header Datei muss von allen Anwendungsmodulen eingeschlossen werden, die die definierten Vorgänge aufzurufen, die definierten Vorgänge implementieren oder die definierten Typen bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="eef22-138">The header file must be included by all application modules that call the defined operations, implement the defined operations, or manipulate the defined types.</span></span>

<span data-ttu-id="eef22-139">Die Mittel-Compilerschalter [**/Header**](-header.md) und [**/out**](-out.md) wirken sich auf die Header Datei aus.</span><span class="sxs-lookup"><span data-stu-id="eef22-139">The MIDL compiler switches [**/header**](-header.md) and [**/out**](-out.md) affect the header file.</span></span>

 

 




