---
title: /Oi-Schalter
description: Die Schalter/Oi und/OIC leiten den Mittel l-Compiler an die Verwendung einer vollständig interpretierten Marshallingmethode. Der/Oicf-Schalter bietet weitere Leistungsverbesserungen.
ms.assetid: cf597a45-410f-4098-850b-240c6ebce23b
keywords:
- /Oi-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /Oi
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1671b16640d3f3214f10138e50a2ac08b6114674
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104208868"
---
# <a name="oi-switch"></a><span data-ttu-id="bdc58-105">/Oi-Schalter</span><span class="sxs-lookup"><span data-stu-id="bdc58-105">/Oi switch</span></span>

<span data-ttu-id="bdc58-106">Die Schalter **/Oi** und **/OIC** leiten den Mittel l-Compiler an die Verwendung einer vollständig interpretierten Marshallingmethode.</span><span class="sxs-lookup"><span data-stu-id="bdc58-106">The **/Oi** and **/Oic** switches direct the MIDL compiler to use a fully-interpreted marshaling method.</span></span> <span data-ttu-id="bdc58-107">Der **/Oicf** -Schalter bietet weitere Leistungsverbesserungen.</span><span class="sxs-lookup"><span data-stu-id="bdc58-107">The **/Oicf** switch provides additional performance enhancements.</span></span>

``` syntax
midl /{Oi | Oic | Oif | Oicf}
```

## <a name="switch-options"></a><span data-ttu-id="bdc58-108">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="bdc58-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="bdc58-109">*Zählen*</span><span class="sxs-lookup"><span data-stu-id="bdc58-109">*Oi*</span></span> 
</dt> <dd>

<span data-ttu-id="bdc58-110">Gibt die vollständig interpretierte Methode zum Marshalling von Stub-Code an, der zwischen Client und Server übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="bdc58-110">Specifies the fully-interpreted method for marshaling stub code passed between client and server.</span></span>

> [!Note]  
> <span data-ttu-id="bdc58-111">Dieser Schalter ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="bdc58-111">This switch is obsolete.</span></span> <span data-ttu-id="bdc58-112">Es wird empfohlen, dass der Schalter **/Oicf** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bdc58-112">It is recommended that the **/Oicf** switch be used in its place.</span></span>

 

</dd> <dt>

<span data-ttu-id="bdc58-113">*OIC*</span><span class="sxs-lookup"><span data-stu-id="bdc58-113">*Oic*</span></span> 
</dt> <dd>

<span data-ttu-id="bdc58-114">Gibt die ohne Code-Proxy Methode für das Marshalling an, das alle Features von **/Oi** bereitstellt und außerdem die Größe des Client-Stub-Codes für Objekt Schnittstellen weiter reduziert.</span><span class="sxs-lookup"><span data-stu-id="bdc58-114">Specifies the codeless proxy method of marshaling that provides all the features of **/Oi** and also further reduces the size of the client stub code for object interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="bdc58-115">Dieser Schalter ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="bdc58-115">This switch is obsolete.</span></span> <span data-ttu-id="bdc58-116">Es wird empfohlen, dass der Schalter **/Oicf** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bdc58-116">It is recommended that the **/Oicf** switch be used in its place.</span></span>

 

</dd> <dt>

<span data-ttu-id="bdc58-117">*OIF oder Oicf*</span><span class="sxs-lookup"><span data-stu-id="bdc58-117">*Oif or Oicf*</span></span> 
</dt> <dd>

<span data-ttu-id="bdc58-118">Gibt die coschess-Proxy Methode für das Marshalling an, das alle von **/Oi** und **/OIC** bereitgestellten Features umfasst, aber einen neuen Interpreter (schnelle Format Zeichenfolgen) verwendet, der eine bessere Leistung als **/Oi** oder **/OIC** bietet.</span><span class="sxs-lookup"><span data-stu-id="bdc58-118">Specifies the codeless proxy method of marshaling that includes all the features provided by **/Oi** and **/Oic** but uses a new interpreter (fast format strings) that provides better performance than **/Oi** or **/Oic**.</span></span> <span data-ttu-id="bdc58-119">Dieser Switch umfasst aktuelle RPC-Erweiterungen und wird für moderne RPC-Szenarien empfohlen.</span><span class="sxs-lookup"><span data-stu-id="bdc58-119">This switch includes recent RPC enhancements and is recommended for modern RPC scenarios.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bdc58-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bdc58-120">Remarks</span></span>

<span data-ttu-id="bdc58-121">Beachten Sie die Einschränkungen in Bezug auf die unterstützenden Plattformen.</span><span class="sxs-lookup"><span data-stu-id="bdc58-121">Please note the restrictions related to supporting platforms.</span></span>

<span data-ttu-id="bdc58-122">Der Compiler für die Mittel l 3,0 bietet zwei Methoden zum Mars Hallen von Code: vollständig interpretiert ( **/Oi**, **/OIC** und **/Oicf**) und gemischter Modus ( [**/OS**](-os.md)).</span><span class="sxs-lookup"><span data-stu-id="bdc58-122">The MIDL 3.0 compiler provides two methods for marshaling code: fully-interpreted ( **/Oi**, **/Oic** and **/Oicf**) and mixed-mode ( [**/Os**](-os.md)).</span></span> <span data-ttu-id="bdc58-123">Beginnend mit der basl-Version 6.0.359 generiert der Mittelwert Compiler standardmäßig **/Oicf**- [**/robust**](-robust.md) -stubwerte.</span><span class="sxs-lookup"><span data-stu-id="bdc58-123">Starting with MIDL version 6.0.359, the MIDL compiler generates **/Oicf** Â  [**/robust**](-robust.md) stubs by default.</span></span> <span data-ttu-id="bdc58-124">Einige sprach Features werden in einigen Modi nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bdc58-124">Some language features are not supported in some modes.</span></span> <span data-ttu-id="bdc58-125">In diesem Fall wechselt der Compiler automatisch in den entsprechenden Modus und gibt eine Warnung aus.</span><span class="sxs-lookup"><span data-stu-id="bdc58-125">In this case, the compiler automatically switches to the appropriate mode and issues a warning.</span></span>

<span data-ttu-id="bdc58-126">Wenn die Leistung von Bedeutung ist, kann die Methode mit gemischtem Modus ( [**/OS**](-os.md)) die beste Methode sein.</span><span class="sxs-lookup"><span data-stu-id="bdc58-126">If performance is a concern, the mixed-mode ( [**/Os**](-os.md)) method can be the best approach.</span></span> <span data-ttu-id="bdc58-127">In diesem Modus wählt der Compiler, dass einige Parameter in den generierten stubflächen Inline gemarshallt werden.</span><span class="sxs-lookup"><span data-stu-id="bdc58-127">In this mode, the compiler chooses to marshal some parameters inline in the generated stubs.</span></span> <span data-ttu-id="bdc58-128">Dies führt zwar zu einer größeren stubgröße, bietet jedoch eine höhere Leistung.</span><span class="sxs-lookup"><span data-stu-id="bdc58-128">While this results in larger stub size, it offers increased performance.</span></span>

<span data-ttu-id="bdc58-129">Die vollständig interpretierte Methode Marshalls Daten vollständig offline.</span><span class="sxs-lookup"><span data-stu-id="bdc58-129">The fully-interpreted method marshals data completely offline.</span></span> <span data-ttu-id="bdc58-130">Dadurch wird die Größe des stubcodes beträchtlich reduziert, dies führt jedoch zu einer geringeren Leistung.</span><span class="sxs-lookup"><span data-stu-id="bdc58-130">This considerably reduces the size of the stub code, but results in decreased performance.</span></span> <span data-ttu-id="bdc58-131">Außerdem gibt es bei der voll interpretierten Methode eine Beschränkung von 16 Parametern für jede Prozedur.</span><span class="sxs-lookup"><span data-stu-id="bdc58-131">Also, with the fully-interpreted method, there is a limit of 16 parameters for each procedure.</span></span> <span data-ttu-id="bdc58-132">Jede Prozedur, die mehr als 16 Parameter enthält, wird automatisch im [**/OS**](-os.md) -Modus verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="bdc58-132">Any procedure containing more than 16 parameters will automatically be processed in [**/Os**](-os.md) mode.</span></span> <span data-ttu-id="bdc58-133">Unter den interpretierten Modi bietet **/Oicf** die beste Leistung, und **/Oi** bietet die beste Abwärtskompatibilität.</span><span class="sxs-lookup"><span data-stu-id="bdc58-133">Among the interpreted modes, **/Oicf** offers the best performance and **/Oi** offers the best backward compatibility.</span></span>

<span data-ttu-id="bdc58-134">Möglicherweise möchten Sie die **/OIF** -Option verwenden, wenn Ihre Anwendung in der Mitte 3,0 eingeführte Mittel l-Funktionen verwendet, wie z \[ . b. das [**Wire \_ Marshal**](wire-marshal.md) \] -Attribut und das \[ [**User \_ Marshal**](user-marshal.md) - \] Attribut.</span><span class="sxs-lookup"><span data-stu-id="bdc58-134">You may want to use the **/Oif** option if your application uses MIDL features that were introduced with MIDL 3.0, such as the \[[**wire\_marshal**](wire-marshal.md)\] and \[[**user\_marshal**](user-marshal.md)\] attributes.</span></span> <span data-ttu-id="bdc58-135">Wenn Ihre Anwendung [Pipes](/windows/desktop/Rpc/pipes) verwendet, müssen Sie die **/OIF** -Option verwenden. Wenn Sie einen anderen Modus angeben, wechselt der Mittell-Compiler zu **/OIF**.</span><span class="sxs-lookup"><span data-stu-id="bdc58-135">If your application uses [pipes](/windows/desktop/Rpc/pipes) you must use the **/Oif** option; if you specify another mode, the MIDL compiler will switch to **/Oif**.</span></span>

<span data-ttu-id="bdc58-136">Zum Optimieren der Art und Weise, in der der Stubcode gemarshallt wird, bietet Microsoft RPC ein ACF- \[ [**Optimierungs**](optimize.md) \] Attribut.</span><span class="sxs-lookup"><span data-stu-id="bdc58-136">To fine-tune the way your stub code is marshaled, Microsoft RPC provides an ACF \[[**optimize**](optimize.md)\] attribute.</span></span> <span data-ttu-id="bdc58-137">Dieses Attribut wird als Schnittstellen Attribut oder Vorgangs Attribut verwendet, um den marshallingmodus für einzelne Schnittstellen oder für einzelne Vorgänge auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="bdc58-137">This attribute is used as an interface attribute or operation attribute to select the marshaling mode for individual interfaces or for individual operations.</span></span>

### <a name="calling-conventions"></a><span data-ttu-id="bdc58-138">Aufrufkonventionen</span><span class="sxs-lookup"><span data-stu-id="bdc58-138">Calling Conventions</span></span>

<span data-ttu-id="bdc58-139">Vom Mittel l-Compiler in der interpretierten Methode mithilfe der **/Oi**-, **/OIC**-oder **/OIF** -Switches generierte Stub müssen während der C-Kompilierung entweder als stdcall-oder als cdecl-Prozedur kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="bdc58-139">Stubs generated by the MIDL compiler in the interpreted method using the **/Oi**, **/Oic**, or **/Oif** switches must be compiled as either a stdcall or a cdecl procedure during the C compilation.</span></span> <span data-ttu-id="bdc58-140">Eine Pascal-oder Fastcall-Aufruf Konvention funktioniert nicht.</span><span class="sxs-lookup"><span data-stu-id="bdc58-140">A PASCAL or Fastcall calling convention will not work.</span></span> <span data-ttu-id="bdc58-141">Außerdem muss der Stub des Servers als stdcallkompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="bdc58-141">Additionally, the server stub must be compiled as stdcall.</span></span>

## <a name="examples"></a><span data-ttu-id="bdc58-142">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bdc58-142">Examples</span></span>

<span data-ttu-id="bdc58-143">**Mittel l/Oi Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="bdc58-143">**midl /Oi filename.idl**</span></span>

<span data-ttu-id="bdc58-144">**Mittel l/OIC Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="bdc58-144">**midl /Oic filename.idl**</span></span>

<span data-ttu-id="bdc58-145">**Mittel l/OIF Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="bdc58-145">**midl /Oif filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="bdc58-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bdc58-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdc58-147">**/robust**</span><span class="sxs-lookup"><span data-stu-id="bdc58-147">**/robust**</span></span>](-robust.md)
</dt> <dt>

[<span data-ttu-id="bdc58-148">**/No \_ robust**</span><span class="sxs-lookup"><span data-stu-id="bdc58-148">**/no\_robust**</span></span>](-no-robust.md)
</dt> <dt>

[<span data-ttu-id="bdc58-149">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="bdc58-149">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="bdc58-150">**/OS**</span><span class="sxs-lookup"><span data-stu-id="bdc58-150">**/Os**</span></span>](-os.md)
</dt> <dt>

[<span data-ttu-id="bdc58-151">**optimiert**</span><span class="sxs-lookup"><span data-stu-id="bdc58-151">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="bdc58-152">**/No \_ Format \_ Opt**</span><span class="sxs-lookup"><span data-stu-id="bdc58-152">**/no\_format\_opt**</span></span>](-no-format-opt.md)
</dt> </dl>

 

 