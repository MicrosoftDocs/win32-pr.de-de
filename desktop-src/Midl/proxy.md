---
title: Proxy Attribut
description: Das Attribut \ Proxy \ verhindert, dass die Automatisierung als Proxy-/stubhandler für eine duale Schnittstelle registriert wird.
ms.assetid: 88e59938-83c9-436a-931c-f4396fdcf653
keywords:
- Proxy Attribut-Mittel l
topic_type:
- apiref
api_name:
- proxy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa8c9d305b7f51a012ae26d7b1a76d2e3011fd7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472757"
---
# <a name="proxy-attribute"></a><span data-ttu-id="a9389-104">Proxy Attribut</span><span class="sxs-lookup"><span data-stu-id="a9389-104">proxy attribute</span></span>

<span data-ttu-id="a9389-105">Das **\[ Proxy \]** Attribut verhindert, dass die Automatisierung als Proxy-/Stub-Handler für eine duale Schnittstelle registriert wird.</span><span class="sxs-lookup"><span data-stu-id="a9389-105">The **\[proxy\]** attribute prevents Automation from registering as a proxy/stub handler for a dual interface.</span></span>

``` syntax
[ 
    proxy, 
    uuid(string-uuid <>)
    [ , interface-attribute-list <>] 
] 
interface interface-name <> : base-interface <>
{
    ...
}
```

## <a name="parameters"></a><span data-ttu-id="a9389-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9389-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9389-107">*Zeichenfolge-UUID*</span><span class="sxs-lookup"><span data-stu-id="a9389-107">*string-uuid*</span></span> 
</dt> <dd>

<span data-ttu-id="a9389-108">Gibt eine Zeichenfolge an, die aus 8 hexadezimalen Ziffern gefolgt von einem Bindestrich und dann drei Gruppen von vier hexadezimalen Ziffern gefolgt von einem Bindestrich und dann 12 hexadezimal Ziffern besteht.</span><span class="sxs-lookup"><span data-stu-id="a9389-108">Specifies a string consisting of 8 hexadecimal digits followed by a hyphen, then three groups of 4 hexadecimal digits each followed by a hyphen, then 12 hexadecimal digits.</span></span> <span data-ttu-id="a9389-109">Sie können die UUID-Zeichenfolge in Anführungszeichen einschließen, es sei denn, Sie verwenden den Mittel l-Compilerschalter [**/OSF**](-osf.md).</span><span class="sxs-lookup"><span data-stu-id="a9389-109">You can enclose the UUID string in quotes, except when you use the MIDL compiler switch [**/osf**](-osf.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9389-110">*Interface-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="a9389-110">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a9389-111">Gibt eine Liste von 0 (null) oder mehr IDL-Attributen an, die auf die gesamte Schnittstelle angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="a9389-111">Specifies a list of zero or more IDL attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="a9389-112">Wenn zwei oder mehr Schnittstellen Attribute vorhanden sind, müssen diese durch Kommas getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="a9389-112">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="a9389-113">*Schnittstellen Name*</span><span class="sxs-lookup"><span data-stu-id="a9389-113">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a9389-114">Der Name der Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a9389-114">Name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="a9389-115">*Basisschnittstelle*</span><span class="sxs-lookup"><span data-stu-id="a9389-115">*base-interface*</span></span> 
</dt> <dd>

<span data-ttu-id="a9389-116">Gibt den Namen einer Schnittstelle an, von der diese abgeleitete Schnittstelle Member-Funktionen, Statuscodes und Schnittstellen Attribute erbt.</span><span class="sxs-lookup"><span data-stu-id="a9389-116">Specifies the name of an interface from which this derived interface inherits member functions, status codes, and interface attributes.</span></span> <span data-ttu-id="a9389-117">Die abgeleitete Schnittstelle erbt keine Typdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="a9389-117">The derived interface does not inherit type definitions.</span></span> <span data-ttu-id="a9389-118">Verwenden Sie hierzu das Schlüsselwort [**Import**](import.md) , um die IDL-Datei der Basisschnittstelle zu importieren.</span><span class="sxs-lookup"><span data-stu-id="a9389-118">To do this, use the [**import**](import.md) keyword to import the IDL file of the base interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a9389-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9389-119">Remarks</span></span>

<span data-ttu-id="a9389-120">Durch die Verwendung des \[ **Proxy** \] Attributs für eine duale Schnittstelle wird verhindert, dass der TLB generierte stubfunktionen übernimmt.</span><span class="sxs-lookup"><span data-stu-id="a9389-120">Using the \[ **proxy**\] attribute for a dual interface prevents the TLB from taking over generated stubs.</span></span> <span data-ttu-id="a9389-121">Wenn dieses Attribut angegeben wird, sollte die Registrierung des Export der Typbibliothek-Proxys nicht aufgehoben werden, wenn die Registrierung des Export der Typbibliothek aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="a9389-121">If this attribute is specified, the typelib proxy should not be unregistered when the typelib is unregistered.</span></span>

### <a name="flags"></a><span data-ttu-id="a9389-122">Flags</span><span class="sxs-lookup"><span data-stu-id="a9389-122">Flags</span></span>

<dl> <dt>

<span data-ttu-id="a9389-123"><span id="TYPEFLAG_PROXY"></span><span id="typeflag_proxy"></span>TYPEFLAG- \_ Proxy</span><span class="sxs-lookup"><span data-stu-id="a9389-123"><span id="TYPEFLAG_PROXY"></span><span id="typeflag_proxy"></span>TYPEFLAG\_PROXY</span></span>
</dt> <dd>

<span data-ttu-id="a9389-124">Schnittstellen können mit dem TYPEFLAG \_ -ProxyFlag gekennzeichnet werden, um anzugeben, dass Sie eine Proxy-/Stub-Dynamic Link Library verwenden werden.</span><span class="sxs-lookup"><span data-stu-id="a9389-124">Interfaces can be marked with the TYPEFLAG\_PROXY flag to indicate they will be using a proxy/stub dynamic link library.</span></span> <span data-ttu-id="a9389-125">Dieses Flag gibt an, dass die Registrierung des Export der Typbibliothek-Proxys nicht aufgehoben werden soll, wenn die Registrierung der Typbibliothek aufgehoben</span><span class="sxs-lookup"><span data-stu-id="a9389-125">This flag specifies the typelib proxy should not be unregistered when the typelib is unregistered.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="a9389-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9389-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9389-127">**Erstellen einer Typbibliothek mit "Mittel l"**</span><span class="sxs-lookup"><span data-stu-id="a9389-127">**Generating a Type Library with MIDL**</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="a9389-128">**Ales**</span><span class="sxs-lookup"><span data-stu-id="a9389-128">**dual**</span></span>](dual.md)
</dt> <dt>

[<span data-ttu-id="a9389-129">**FUNCFLAGS**</span><span class="sxs-lookup"><span data-stu-id="a9389-129">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 