---
title: /Ms_union Schalter
description: Der/MS- \_ Union-Switch steuert die NDR-Ausrichtung von nicht gekapselten Unions. Hinweis Dieses Attribut wird aus Gründen der Abwärtskompatibilität bereitgestellt.
ms.assetid: 683d1498-6419-4600-ad5b-c0b6ea44a8e1
keywords:
- /Ms_union-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /ms_union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 968618af5c2bb5b32ec14b293225bc09c2997aa5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857548"
---
# <a name="ms_union-switch"></a><span data-ttu-id="a58e9-104">/MS \_ Union-Switch</span><span class="sxs-lookup"><span data-stu-id="a58e9-104">/ms\_union switch</span></span>

<span data-ttu-id="a58e9-105">Der **/MS- \_ Union** -Switch steuert die NDR-Ausrichtung von nicht gekapselten Unions.</span><span class="sxs-lookup"><span data-stu-id="a58e9-105">The **/ms\_union** switch controls the NDR alignment of nonencapsulated unions.</span></span>

> [!Note]  
> <span data-ttu-id="a58e9-106">Dieses Attribut wird aus Gründen der Abwärtskompatibilität bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="a58e9-106">This attribute is provided for backwards compatibility.</span></span> <span data-ttu-id="a58e9-107">Es wird nicht empfohlen, in einer neuen-Schnittstelle zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a58e9-107">It is not recommended for use in a new interface.</span></span>

 

``` syntax
midl /ms_union
```

## <a name="switch-options"></a><span data-ttu-id="a58e9-108">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="a58e9-108">Switch Options</span></span>

<span data-ttu-id="a58e9-109">Dieser Switch hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="a58e9-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="a58e9-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a58e9-110">Remarks</span></span>

<span data-ttu-id="a58e9-111">Der mittlerer l-Compiler spiegelt das Verhalten des OSF-DCE-IDL-Compilers für nicht gekapselte Unions wider.</span><span class="sxs-lookup"><span data-stu-id="a58e9-111">The MIDL compiler mirrors the behavior of the OSF-DCE IDL compiler for nonencapsulated unions.</span></span> <span data-ttu-id="a58e9-112">Da jedoch frühere Versionen des Mittel l-Compilers dies nicht getan haben, bietet der **/MS \_ Union** -Switch Kompatibilität mit Schnittstellen, die auf früheren Versionen des Mittel l-Compilers erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="a58e9-112">However, because earlier versions of the MIDL compiler did not do so, the **/ms\_union** switch provides compatibility with interfaces built on previous versions of the MIDL compiler.</span></span>

<span data-ttu-id="a58e9-113">Die MS \_ -Union-Funktion kann als Befehls Zeilenschalter (**/MS \_ Union**), als idl-Schnittstellen Attribut oder als IDL-Type-Attribut verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a58e9-113">The ms\_union feature can be used as a command-line switch (**/ms\_union**), an IDL interface attribute, or as an IDL-type attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="a58e9-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a58e9-114">Examples</span></span>

<span data-ttu-id="a58e9-115">**Mittel l/MS \_ Union file. idl**</span><span class="sxs-lookup"><span data-stu-id="a58e9-115">**midl /ms\_union file.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="a58e9-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a58e9-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a58e9-117">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="a58e9-117">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="a58e9-118">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="a58e9-118">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> </dl>

 

 




