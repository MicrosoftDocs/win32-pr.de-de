---
title: /robust-Schalter
description: Der/robust-Schalter weist den Mittelwert Compiler an, zusätzliche Fehler Überprüfungs Informationen zu generieren, die von der NDR-Engine zur Ausführung von Integritätsprüfungen zur Laufzeit verwendet werden.
ms.assetid: 7a858600-ea06-4396-9a1b-240d646e8c7d
keywords:
- /robust-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /robust
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 974f9530006c03a041d9d444c41f9c5ca01569c0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857239"
---
# <a name="robust-switch"></a><span data-ttu-id="038c8-104">/robust-Schalter</span><span class="sxs-lookup"><span data-stu-id="038c8-104">/robust switch</span></span>

<span data-ttu-id="038c8-105">Der **/robust** -Schalter weist den Mittelwert Compiler an, zusätzliche Fehler Überprüfungs Informationen zu generieren, die von der NDR-Engine zur Ausführung von Integritätsprüfungen zur Laufzeit verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="038c8-105">The **/robust** switch tells the MIDL compiler to generate additional error-checking information, which the NDR engine uses to perform integrity checks at run time.</span></span>

``` syntax
midl /robust {/Oicf | /Oif }
```

## <a name="switch-options"></a><span data-ttu-id="038c8-106">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="038c8-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="038c8-107">*/Oicf*</span><span class="sxs-lookup"><span data-stu-id="038c8-107">*/Oicf*</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="038c8-108">*/OIF*</span><span class="sxs-lookup"><span data-stu-id="038c8-108">*/Oif*</span></span> 
</dt> <dd>

<span data-ttu-id="038c8-109">Diese Switches sind in ihrer Funktionalität identisch.</span><span class="sxs-lookup"><span data-stu-id="038c8-109">These switches are identical in their functionality.</span></span> <span data-ttu-id="038c8-110">Sie geben die coschess-Proxy Methode für das Marshalling an und verwenden schnelle Format Zeichenfolgen, um die Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="038c8-110">They specify the codeless proxy method of marshaling and use fast format strings for improved performance.</span></span> <span data-ttu-id="038c8-111">Siehe/ [**Oi**](-oi.md).</span><span class="sxs-lookup"><span data-stu-id="038c8-111">See / [**Oi**](-oi.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="038c8-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="038c8-112">Remarks</span></span>

<span data-ttu-id="038c8-113">Durch die Verwendung des **/robust** -Schalters werden zusätzliche Informationen generiert, mit denen die Engine für die Netzwerkdaten Darstellung die Lauf Zeit Fehlerüberprüfung für korrelierte Argumente in dynamischen Arrays, Unions und in [**out**](out-idl.md) -Schnittstellen Zeigern in DCOM-Anwendungen ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="038c8-113">Using the **/robust** switch generates additional information that allows the Network Data Representation (NDR) engine to perform run-time error checking on correlated arguments in dynamic arrays, unions, and in [**out**](out-idl.md) interface pointers in DCOM applications.</span></span> <span data-ttu-id="038c8-114">Der **/robust** -Schalter ist nur unter Windows 2000 und neueren Versionen von Windows verfügbar.</span><span class="sxs-lookup"><span data-stu-id="038c8-114">The **/robust** switch is only available under WindowsÂ 2000 and later versions of Windows.</span></span>

<span data-ttu-id="038c8-115">Bei einem korrelierten Argument handelt es sich um ein Argument, das eines der Attribute verwendet, mit denen die Größe eines Datenobjekts zur Laufzeit bestimmt werden kann: [**size \_ ist**](size-is.md), [**length \_ ist**](length-is.md), [**First \_ is**](first-is.md), [**Last \_ is**](last-is.md), [**Max \_ is**](max-is.md), [**Switch \_ is**](switch-is.md)und [**IID \_ ist**](iid-is.md).</span><span class="sxs-lookup"><span data-stu-id="038c8-115">A correlated argument is an argument that uses any of the attributes that allow the size of a data object to be determined at run time: [**size\_is**](size-is.md), [**length\_is**](length-is.md), [**first\_is**](first-is.md), [**last\_is**](last-is.md), [**max\_is**](max-is.md), [**switch\_is**](switch-is.md), and [**iid\_is**](iid-is.md).</span></span> <span data-ttu-id="038c8-116">In Übereinstimmung mit der OSF-DCE-Spezifikation für die Wire-Darstellung wird dieses korrelierte Argument an zwei unterschiedlichen Stellen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="038c8-116">In accordance with the OSF-DCE specification for the wire representation, this correlated argument appears in two different places.</span></span> <span data-ttu-id="038c8-117">Nehmen wir beispielsweise an, eine typische Verwendung der **Größe \_ ist** "Attribute":</span><span class="sxs-lookup"><span data-stu-id="038c8-117">For example, consider a typical usage of the **size\_is** attribute:</span></span>

``` syntax
HRESULT Func1([in] long Size, 
              [in, size_is(Size)]BAR_TYPE *pBarType);
```

<span data-ttu-id="038c8-118">In diesem Beispiel übergibt der Client einen Long-Wert, der die Größe eines Blocks von Balken \_ Typen (in Bezug auf die Anzahl der Balken \_ Typen Elemente) und einen Zeiger auf den eigentlichen Block von Balken \_ Typen angibt.</span><span class="sxs-lookup"><span data-stu-id="038c8-118">In this example, the client passes a long that specifies the size of a block of BAR\_TYPEs (in terms of number of BAR\_TYPES elements), and a pointer to the actual block of BAR\_TYPEs.</span></span> <span data-ttu-id="038c8-119">Das Größen Argument korreliert mit dem pbartype-Argument.</span><span class="sxs-lookup"><span data-stu-id="038c8-119">The Size argument correlates with the pBarType argument.</span></span> <span data-ttu-id="038c8-120">In Übereinstimmung mit der OSF-DCE-Spezifikation wird das size-Argument zweimal im Netzwerk dargestellt – zuerst als sich selbst und dann mit dem Array von Bar- \_ Element-Elementen, die das pbartype-Argument darstellen.</span><span class="sxs-lookup"><span data-stu-id="038c8-120">In accordance with the OSF-DCE specification, the Size argument is represented twice on the wire—first as itself and then with the array of BAR\_TYPE elements that represent the pBarType argument.</span></span> <span data-ttu-id="038c8-121">Jedes Argument wird gemäß seiner eigenen Wire-Darstellung unabhängig voneinander gemarshallt.</span><span class="sxs-lookup"><span data-stu-id="038c8-121">Each argument is unmarshaled independently, according to its own wire representation.</span></span> <span data-ttu-id="038c8-122">Normalerweise haben das Größen Argument und seine Kopie, das zum Darstellen eines Teils des anderen Arguments verwendet wird, dieselben Werte.</span><span class="sxs-lookup"><span data-stu-id="038c8-122">Normally, the Size argument and its copy, which is used to represent part of the other argument, have the same values.</span></span> <span data-ttu-id="038c8-123">Wenn das Größen Argument jedoch beschädigt wird (z. b. wenn der Block mit den Balken \_ Typen größer ist als der zugeordnete Wert), reagiert die Serveranwendung möglicherweise nicht mehr, da Sie den Wert des Size-Arguments verwendet, um eingehende Daten zu messen.</span><span class="sxs-lookup"><span data-stu-id="038c8-123">However, if the Size argument becomes corrupted (for example, when the block of BAR\_TYPES is larger than what was allocated), the server application may stop responding, because it uses the value of the Size argument to measure incoming data.</span></span>

<span data-ttu-id="038c8-124">Der **/robust** -Schalter ist erforderlich, um eine gültige Bereichs Überprüfung mit dem [**Range**](range.md) -Attribut zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="038c8-124">The **/robust** switch is required to implement valid range checking with the [**range**](range.md) attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="038c8-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="038c8-125">Examples</span></span>

<span data-ttu-id="038c8-126">**Mittel l/robust/Oicf filename. idl**</span><span class="sxs-lookup"><span data-stu-id="038c8-126">**midl /robust /Oicf filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="038c8-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="038c8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="038c8-128">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="038c8-128">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="038c8-129">**/Oi**</span><span class="sxs-lookup"><span data-stu-id="038c8-129">**/Oi**</span></span>](-oi.md)
</dt> <dt>

[<span data-ttu-id="038c8-130">**Bereich**</span><span class="sxs-lookup"><span data-stu-id="038c8-130">**range**</span></span>](range.md)
</dt> </dl>

 

 




