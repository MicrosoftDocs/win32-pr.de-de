---
title: uuid-Attribut
description: Das \ UUID \ Interface-Attribut kennzeichnet einen universellen eindeutigen Bezeichner (UUID), der der-Schnittstelle zugewiesen ist und von anderen Schnittstellen unterschieden wird.
ms.assetid: 72cf12f5-49cd-440d-9665-73211509d050
keywords:
- uuid-Attribut-Mittel l
topic_type:
- apiref
api_name:
- uuid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5688bafe8343bdc1ab508a4e65984cc15c88b124
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718534"
---
# <a name="uuid-attribute"></a><span data-ttu-id="c5fb2-104">uuid-Attribut</span><span class="sxs-lookup"><span data-stu-id="c5fb2-104">uuid attribute</span></span>

<span data-ttu-id="c5fb2-105">Das **\[ UUID \]** Interface-Attribut kennzeichnet einen universellen eindeutigen Bezeichner (UUID), der der-Schnittstelle zugewiesen ist und von anderen Schnittstellen unterschieden wird.</span><span class="sxs-lookup"><span data-stu-id="c5fb2-105">The **\[uuid\]** interface attribute designates a universally unique identifier (UUID) that is assigned to the interface and that distinguishes it from other interfaces.</span></span>

``` syntax
uuid (string-uuid) 
uuid ("string-uuid")
```

## <a name="parameters"></a><span data-ttu-id="c5fb2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5fb2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5fb2-107">*Zeichenfolge-UUID*</span><span class="sxs-lookup"><span data-stu-id="c5fb2-107">*string-uuid*</span></span> 
</dt> <dd>

<span data-ttu-id="c5fb2-108">Gibt eine Zeichenfolge an, die aus 8 hexadezimalen Ziffern gefolgt von einem Bindestrich und dann drei Gruppen von vier hexadezimalen Ziffern gefolgt von einem Bindestrich und dann 12 hexadezimal Ziffern besteht.</span><span class="sxs-lookup"><span data-stu-id="c5fb2-108">Specifies a string consisting of 8 hexadecimal digits followed by a hyphen, then three groups of 4 hexadecimal digits each followed by a hyphen, then 12 hexadecimal digits.</span></span> <span data-ttu-id="c5fb2-109">Sie können die UUID-Zeichenfolge in Anführungszeichen einschließen, es sei denn, Sie verwenden den Mittel l-Compilerschalter [**/OSF**](-osf.md).</span><span class="sxs-lookup"><span data-stu-id="c5fb2-109">You can enclose the UUID string in quotes, except when you use the MIDL compiler switch [**/osf**](-osf.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c5fb2-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c5fb2-110">Remarks</span></span>

<span data-ttu-id="c5fb2-111">Die Lauf Zeit Bibliothek verwendet die von dem **\[ UUID \]** -Attribut Festlegung-Schnittstellen-UUID, um die Kommunikation zwischen Client-und Server Anwendungen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c5fb2-111">The run-time library uses the interface UUID that the **\[uuid\]** attribute designates to help establish communication between the client and server applications.</span></span> <span data-ttu-id="c5fb2-112">Das **\[ UUID \]** -Attribut kann in der Liste der Schnittstellen Attribute entweder für eine RPC-Schnittstelle oder eine COM-Schnittstelle angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c5fb2-112">The **\[uuid\]** attribute can appear in the interface attribute list for either an RPC interface or a COM interface.</span></span>

<span data-ttu-id="c5fb2-113">Für eine RPC-Schnittstelle muss die Liste der Schnittstellen Attribute entweder das **\[ \] UUID** -Attribut oder das **\[** [**lokale**](local.md) **\]** Attribut enthalten, und das von Ihnen gewählte muss genau einmal erfolgen.</span><span class="sxs-lookup"><span data-stu-id="c5fb2-113">For an RPC interface, the interface attribute list must include either the **\[uuid\]** attribute or the **\[**[**local**](local.md)**\]** attribute, and the one you choose must occur exactly once.</span></span> <span data-ttu-id="c5fb2-114">Wenn die Liste das **\[ UUID \]** -Attribut enthält, kann Sie auch das **\[** [**Versions**](version.md) **\]** Attribut enthalten.</span><span class="sxs-lookup"><span data-stu-id="c5fb2-114">If the list includes the **\[uuid\]** attribute, it can also include the **\[**[**version**](version.md)**\]** attribute.</span></span>

<span data-ttu-id="c5fb2-115">Für eine COM-Schnittstelle (identifiziert durch das **\[** [**Objekt**](object.md) **\]** Schnittstellen Attribut) muss die Schnittstellen Attribut Liste das **\[ UUID \]** -Attribut enthalten, aber es kann nicht das **\[ Versions \]** Attribut enthalten.</span><span class="sxs-lookup"><span data-stu-id="c5fb2-115">For a COM interface (identified by the **\[**[**object**](object.md)**\]** interface attribute), the interface attribute list must include the **\[uuid\]** attribute, but it cannot include the **\[version\]** attribute.</span></span> <span data-ttu-id="c5fb2-116">Die Liste für eine COM-Schnittstelle kann das **\[ lokale \]** Attribut enthalten, auch wenn das **\[ UUID \]** -Attribut vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c5fb2-116">The list for a COM interface can include the **\[local\]** attribute even though the **\[uuid\]** attribute is present.</span></span>

<span data-ttu-id="c5fb2-117">Microsoft RPC unterstützt eine Erweiterung der DCE-IDL, die es ermöglicht, dass die UUID in doppelte Anführungszeichen ("" "") eingeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="c5fb2-117">Microsoft RPC supports an extension to DCE IDL that allows the UUID to be enclosed in double quotation marks ("" "").</span></span> <span data-ttu-id="c5fb2-118">Das Formular in Anführungszeichen wird für C-Compiler-Präprozessoren benötigt, die UUID-Nummern als Gleit Komma Zahlen interpretieren.</span><span class="sxs-lookup"><span data-stu-id="c5fb2-118">The quoted form is needed for C-compiler preprocessors that interpret UUID numbers as floating-point numbers.</span></span>

<span data-ttu-id="c5fb2-119">Alle UUID-Werte sollten Computer generiert werden, um Eindeutigkeit sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="c5fb2-119">All UUID values should be computer-generated to guarantee uniqueness.</span></span> <span data-ttu-id="c5fb2-120">Verwenden Sie das Hilfsprogramm uuidgen, um eindeutige UUID-Werte zu generieren.</span><span class="sxs-lookup"><span data-stu-id="c5fb2-120">Use the Uuidgen utility to generate unique UUID values.</span></span>

<span data-ttu-id="c5fb2-121">Die UUID und die Versionsnummern der-Schnittstelle werden verwendet, um zu bestimmen, ob der Client an den Server gebunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="c5fb2-121">The UUID and version numbers of the interface are used to determine whether the client can bind to the server.</span></span> <span data-ttu-id="c5fb2-122">Damit der Client an den Server gebunden wird, muss die in den Client-und Server Schnittstellen angegebene UUID identisch sein.</span><span class="sxs-lookup"><span data-stu-id="c5fb2-122">For the client to bind to the server, the UUID specified in the client and server interfaces must be the same.</span></span>

<span data-ttu-id="c5fb2-123">Beachten Sie, dass eine Schnittstelle ohne Attribute in eine Basis-IDL-Datei importiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="c5fb2-123">Note that an interface without attributes can be imported into a base IDL file.</span></span> <span data-ttu-id="c5fb2-124">Allerdings darf die-Schnittstelle nur Datentypen ohne Prozeduren enthalten.</span><span class="sxs-lookup"><span data-stu-id="c5fb2-124">However, the interface must contain only datatypes with no procedures.</span></span> <span data-ttu-id="c5fb2-125">Wenn auch eine Prozedur in der Schnittstelle enthalten ist, muss ein lokales Attribut oder ein uuid-Attribut angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c5fb2-125">If even one procedure is contained in the interface, a local or UUID attribute must be specified.</span></span>

## <a name="examples"></a><span data-ttu-id="c5fb2-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c5fb2-126">Examples</span></span>

``` syntax
uuid(6B29FC40-CA47-1067-B31D-00DD010662DA) 
 
uuid("6B29FC40-CA47-1067-B31D-00DD010662DA")
```

## <a name="see-also"></a><span data-ttu-id="c5fb2-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c5fb2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5fb2-128">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="c5fb2-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="c5fb2-129">**berfläche**</span><span class="sxs-lookup"><span data-stu-id="c5fb2-129">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="c5fb2-130">**nah**</span><span class="sxs-lookup"><span data-stu-id="c5fb2-130">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="c5fb2-131">**Objekt (object)**</span><span class="sxs-lookup"><span data-stu-id="c5fb2-131">**object**</span></span>](object.md)
</dt> <dt>

[<span data-ttu-id="c5fb2-132">**/osf**</span><span class="sxs-lookup"><span data-stu-id="c5fb2-132">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="c5fb2-133">**version**</span><span class="sxs-lookup"><span data-stu-id="c5fb2-133">**version**</span></span>](version.md)
</dt> </dl>

 

 




