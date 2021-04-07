---
title: /OSF-Schalter
description: Der Schalter/OSF erzwingt eine strikte Kompatibilität mit OSF-DCE.
ms.assetid: d94228fa-24af-43d7-9596-cf3a14690e0b
keywords:
- /OSF-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /osf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2936401d59bb8c2c2bcfdcffce27ba9ed978d506
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038875"
---
# <a name="osf-switch"></a><span data-ttu-id="82982-104">/OSF-Schalter</span><span class="sxs-lookup"><span data-stu-id="82982-104">/osf switch</span></span>

<span data-ttu-id="82982-105">Der Schalter **/OSF** erzwingt eine strikte Kompatibilität mit OSF-DCE.</span><span class="sxs-lookup"><span data-stu-id="82982-105">The **/osf** switch forces strict compatibility with OSF DCE.</span></span>

``` syntax
midl /osf
```

## <a name="switch-options"></a><span data-ttu-id="82982-106">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="82982-106">Switch Options</span></span>

<span data-ttu-id="82982-107">Dieser Switch hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="82982-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="82982-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82982-108">Remarks</span></span>

<span data-ttu-id="82982-109">Verwenden Sie diesen Switch, wenn Ihre Anwendung aus Gründen der Portabilität eine strikte Kompatibilität mit OSF-DCE erfordert.</span><span class="sxs-lookup"><span data-stu-id="82982-109">Use this switch if your application requires strict compatibility with OSF DCE for portability reasons.</span></span>

<span data-ttu-id="82982-110">Im **/OSF** -Modus wird das RPCSS-Paket automatisch aktiviert, wenn Sie vollständige Zeiger verwenden, die Argumente eine Speicher Belegung erfordern oder wenn Sie das Attribut " [**\_ zuordnen**](enable-allocate.md) " verwenden.</span><span class="sxs-lookup"><span data-stu-id="82982-110">In **/osf** mode, the RpcSs package is automatically enabled when you use full pointers, the arguments require memory allocation, or when you use the [**enable\_allocate**](enable-allocate.md) attribute.</span></span> <span data-ttu-id="82982-111">Dies bedeutet, dass Sie in Ihrer Client-und Serveranwendung nicht die [**\_ Benutzer \_ Freihand**](/windows/desktop/Rpc/the-midl-user-free-function) -Funktionen für [**mittlere \_ Benutzer \_**](/windows/desktop/Rpc/the-midl-user-allocate-function) Zuordnungen und mittellose Benutzer angeben müssen.</span><span class="sxs-lookup"><span data-stu-id="82982-111">This means that you do not have to supply the [**midl\_user\_allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function) and [**midl\_user\_free**](/windows/desktop/Rpc/the-midl-user-free-function) functions in your client and server application.</span></span>

<span data-ttu-id="82982-112">Die folgenden von Microsoft erweiterten Features sind nicht verfügbar, wenn Sie mit dem **/OSF** -Schalter kompilieren:</span><span class="sxs-lookup"><span data-stu-id="82982-112">The following Microsoft-extended features are not available when you compile with the **/osf** switch:</span></span>

-   <span data-ttu-id="82982-113">Abstrakte Deklaratoren (unbenannte Parameter) in der IDL-Datei.</span><span class="sxs-lookup"><span data-stu-id="82982-113">Abstract declarators (unnamed parameters) in the IDL file.</span></span>
-   <span data-ttu-id="82982-114">Schnittstellendefinitionen für COM-Objekte.</span><span class="sxs-lookup"><span data-stu-id="82982-114">Interface definitions for COM objects.</span></span>
-   <span data-ttu-id="82982-115">Schnittstellennamen mit mehr als 17 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="82982-115">Interface names with more than 17 characters.</span></span>
-   <span data-ttu-id="82982-116">Nur-Mittel-Attribute, z. b. [**Wire \_ Marshal**](wire-marshal.md), [**User \_ Marshal**](user-marshal.md)und die Export der Typbibliothek-Erweiterungen (ODL).</span><span class="sxs-lookup"><span data-stu-id="82982-116">MIDL-only attributes, such as [**wire\_marshal**](wire-marshal.md), [**user\_marshal**](user-marshal.md), and the typelib (ODL)extensions.</span></span>
-   <span data-ttu-id="82982-117">Verwenden von ACF-Schlüsselwörtern in einer IDL-Datei (die Option "Mittel l **/App \_ config** ").</span><span class="sxs-lookup"><span data-stu-id="82982-117">Using ACF keywords in an IDL file (the MIDL **/app\_config** option).</span></span>
-   <span data-ttu-id="82982-118">Statische Rückruf Funktionen auf dem Client.</span><span class="sxs-lookup"><span data-stu-id="82982-118">Static callback functions on the client.</span></span>
-   <span data-ttu-id="82982-119">Das [**Async**](async.md) -Attribut.</span><span class="sxs-lookup"><span data-stu-id="82982-119">The [**async**](async.md) attribute.</span></span>
-   <span data-ttu-id="82982-120">[**cpp- \_ Anführungs**](cpp-quote.md) Zeichen und **\# pragma-Mittell- \_ Echo**.</span><span class="sxs-lookup"><span data-stu-id="82982-120">[**cpp\_quote**](cpp-quote.md) and **\#pragma midl\_echo**.</span></span>
-   <span data-ttu-id="82982-121">[**WCHAR \_ t**](wchar-t.md) -breit Zeichen Typen,-Konstanten und-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="82982-121">[**wchar\_t**](wchar-t.md) wide-character types, constants, and strings.</span></span>
-   <span data-ttu-id="82982-122">[](enum.md) enumerationsinitialisierung (Sparse-Enumeratoren).</span><span class="sxs-lookup"><span data-stu-id="82982-122">[**enum**](enum.md) initialization (sparse enumerators).</span></span>
-   <span data-ttu-id="82982-123">Spezifikation für die [**out**](out-idl.md)-only-Größe.</span><span class="sxs-lookup"><span data-stu-id="82982-123">[**out**](out-idl.md)-only size specification.</span></span>
-   <span data-ttu-id="82982-124">Arrays mit gemischter Groß-und Größenanpassung.</span><span class="sxs-lookup"><span data-stu-id="82982-124">Mixed sized-pointers and sized arrays.</span></span>
-   <span data-ttu-id="82982-125">Ausdrücke, die für Größen-und diskriminatorspezifiatoren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="82982-125">Expressions used for size and discriminator specifiers.</span></span>
-   <span data-ttu-id="82982-126">Explizite handle-Parameter an einer beliebigen Position in der Argumentliste.</span><span class="sxs-lookup"><span data-stu-id="82982-126">Explicit handle parameters in any position in the argument list.</span></span> <span data-ttu-id="82982-127">Im **/OSF** -Modus sucht der mittlerer l-Compiler nach einem expliziten Bindungs Handle als ersten Parameter.</span><span class="sxs-lookup"><span data-stu-id="82982-127">In **/osf** mode, the MIDL compiler looks for an explicit binding handle as the first parameter.</span></span> <span data-ttu-id="82982-128">Wenn der erste Parameter kein Bindungs Handle und mindestens ein Kontext Handle angegeben ist, wird das äußerste Kontext Handle als Bindungs Handle verwendet.</span><span class="sxs-lookup"><span data-stu-id="82982-128">When the first parameter is not a binding handle and one or more context handles are specified, the leftmost context handle is used as the binding handle.</span></span> <span data-ttu-id="82982-129">Wenn der erste Parameter kein Handle ist und keine Kontext Handles vorhanden sind, verwendet die Prozedur die implizite Bindung mithilfe des [**impliziten \_ Handles**](implicit-handle.md) oder [**automatischen \_ Handles**](auto-handle.md)des ACF-Attributs.</span><span class="sxs-lookup"><span data-stu-id="82982-129">When the first parameter is not a handle and there are no context handles, the procedure uses implicit binding using the ACF attribute [**implicit\_handle**](implicit-handle.md) or [**auto\_handle**](auto-handle.md).</span></span>
-   <span data-ttu-id="82982-130">Vererbung von Zeiger Attributen.</span><span class="sxs-lookup"><span data-stu-id="82982-130">Pointer-attribute type inheritance.</span></span> <span data-ttu-id="82982-131">Die OSF-DCE lässt keine nicht attributierten Zeiger zu.</span><span class="sxs-lookup"><span data-stu-id="82982-131">OSF DCE does not allow unattributed pointers.</span></span> <span data-ttu-id="82982-132">Daher muss jede IDL-Datei im **/OSF** -Modus Attribute für Ihre Zeiger definieren.</span><span class="sxs-lookup"><span data-stu-id="82982-132">Therefore, in **/osf** mode each IDL file must define attributes for its pointers.</span></span> <span data-ttu-id="82982-133">Wenn ein Zeiger über kein explizites Attribut verfügt, muss die IDL-Datei eine [**Zeiger \_ Standard**](pointer-default.md) Spezifikation aufweisen, um den Zeigertyp festzulegen.</span><span class="sxs-lookup"><span data-stu-id="82982-133">If any pointer does not have an explicit attribute, the IDL file must have a [**pointer\_default**](pointer-default.md) specification to set the pointer type.</span></span>
-   <span data-ttu-id="82982-134">Mehrere Schnittstellen in einer IDL-Datei.</span><span class="sxs-lookup"><span data-stu-id="82982-134">Multiple interfaces in an IDL file.</span></span>
-   <span data-ttu-id="82982-135">Definitionen außerhalb des Schnittstellen Blocks.</span><span class="sxs-lookup"><span data-stu-id="82982-135">Definitions outside of the interface block.</span></span>
-   <span data-ttu-id="82982-136">Typqualifizierer wie " **Far** " und " **StdCall"**.</span><span class="sxs-lookup"><span data-stu-id="82982-136">Type qualifiers such as **far** and **stdcall**.</span></span>
-   <span data-ttu-id="82982-137">Weglassen von direktionalen Attributen.</span><span class="sxs-lookup"><span data-stu-id="82982-137">Omitting directional attributes.</span></span>

<span data-ttu-id="82982-138">Die folgenden C/C++-Spracherweiterungen sind nicht verfügbar, wenn Sie die Kompilierung mit dem **/OSF** -Schalter durchlaufen:</span><span class="sxs-lookup"><span data-stu-id="82982-138">The following C/C++ language extensions are not available when you compile with the **/osf** switch:</span></span>

-   <span data-ttu-id="82982-139">Bitfelder in Strukturen und Unions.</span><span class="sxs-lookup"><span data-stu-id="82982-139">Bit fields in structures and unions.</span></span>
-   <span data-ttu-id="82982-140">Einzeilige Kommentare sind durch zwei Schrägstriche (//) getrennt.</span><span class="sxs-lookup"><span data-stu-id="82982-140">Single line comments delimited with two slash characters (//).</span></span>
-   <span data-ttu-id="82982-141">Externe Deklarationen.</span><span class="sxs-lookup"><span data-stu-id="82982-141">External declarations.</span></span>
-   <span data-ttu-id="82982-142">Prozeduren mit Ellipsen in der Parameterliste.</span><span class="sxs-lookup"><span data-stu-id="82982-142">Procedures with ellipses in the parameter list.</span></span>
-   <span data-ttu-id="82982-143">Geben Sie [**int**](int.md)ein.</span><span class="sxs-lookup"><span data-stu-id="82982-143">Type [**int**](int.md).</span></span>
-   <span data-ttu-id="82982-144">Geben **Sie \* void** ein (außer mit dem [**Kontext \_ handle**](context-handle.md) -Attribut).</span><span class="sxs-lookup"><span data-stu-id="82982-144">Type **void \*** (except with the [**context\_handle**](context-handle.md) attribute).</span></span>
-   <span data-ttu-id="82982-145">Typqualifizierer, einschließlich des Formulars mit dem ANSI-konforme Präfix, enthalten zwei Unterstriche: **\_ \_ cdecl**, **cdecl**, [**const**](const.md), **const**, **\_ \_ Export**, **Export**, **\_ \_ weit**, **weit**, **\_ \_ loadds**, **loadds**, **\_ \_ near**, **near**, **\_ \_ Pascal**, **Pascal**, **\_ \_ StdCall,** **StdCall,** **\_ \_ volatile** und **volatile**.</span><span class="sxs-lookup"><span data-stu-id="82982-145">Type qualifiers, including the form with the ANSI-conformant prefix, contain two underscore characters: **\_\_cdecl**, **cdecl**, [**const**](const.md), **const**, **\_\_export**, **export**, **\_\_far**, **far**, **\_\_loadds**, **loadds**, **\_\_near**, **near**, **\_\_pascal**, **pascal**, **\_\_stdcall**, **stdcall**, **\_\_volatile**, and **volatile**.</span></span>
-   <span data-ttu-id="82982-146">Eine beliebige \# [**pragma**](pragma.md) -Warnung oder ein **\# pragma** -Kommentar.</span><span class="sxs-lookup"><span data-stu-id="82982-146">Any \# [**pragma**](pragma.md) warning or **\#pragma** comment.</span></span>
-   <span data-ttu-id="82982-147">Typserialisierung.</span><span class="sxs-lookup"><span data-stu-id="82982-147">Type serialization.</span></span>
-   <span data-ttu-id="82982-148">Der [**\_ \_ int3264**](--int3264.md) -Datentyp.</span><span class="sxs-lookup"><span data-stu-id="82982-148">The [**\_\_int3264**](--int3264.md) data type.</span></span>
-   <span data-ttu-id="82982-149">Der [**/Protocol**](-protocol.md) -Switch und die ndr64-Übertragungs Syntax.</span><span class="sxs-lookup"><span data-stu-id="82982-149">The [**/protocol**](-protocol.md) switch, and ndr64 transfer syntax.</span></span>

## <a name="examples"></a><span data-ttu-id="82982-150">Beispiele</span><span class="sxs-lookup"><span data-stu-id="82982-150">Examples</span></span>

<span data-ttu-id="82982-151">**Mittel l/OSF Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="82982-151">**midl /osf filename.idl**</span></span>

<span data-ttu-id="82982-152">**Mittel l/OSF/APP \_ Konfigurations Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="82982-152">**midl /osf /app\_config filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="82982-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82982-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82982-154">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="82982-154">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="82982-155">**/APP- \_ Konfiguration**</span><span class="sxs-lookup"><span data-stu-id="82982-155">**/app\_config**</span></span>](-app-config.md)
</dt> <dt>

[<span data-ttu-id="82982-156">**/MS \_ ext**</span><span class="sxs-lookup"><span data-stu-id="82982-156">**/ms\_ext**</span></span>](-ms-ext.md)
</dt> <dt>

[<span data-ttu-id="82982-157">RPCSS-Speicher Verwaltungspaket</span><span class="sxs-lookup"><span data-stu-id="82982-157">Rpcss Memory Management Package</span></span>](/windows/desktop/Rpc/rpcss-memory-management-package)
</dt> </dl>

 

 