---
title: Iwmpcdromburn-Bezeichnung (Eigenschaft)
description: Die Label-Eigenschaft ruft die Zeichenfolge der CD-Volumebezeichnung ab
ms.assetid: 46e7741c-59c5-46d8-b9ca-09892d907cd7
keywords:
- Label-Eigenschaften Fenster Media Player
- Label-Eigenschaft, Windows Media Player, iwmpcdromburn-Schnittstelle
- Iwmpcdromburn Interface, Windows Media Player, Bezeichnung (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPCdromBurn.label
- IWMPCdromBurn.get_label
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05da344f1148de7e79cb605135964c6ab8225ac0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372128"
---
# <a name="iwmpcdromburnlabel-property"></a><span data-ttu-id="34f20-106">Iwmpcdromburn:: Label-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="34f20-106">IWMPCdromBurn::label property</span></span>

<span data-ttu-id="34f20-107">Die *Label* -Eigenschaft ruft die Zeichenfolge der CD-Volumebezeichnung ab</span><span class="sxs-lookup"><span data-stu-id="34f20-107">The *label* property gets the CD volume label string.</span></span>

<span data-ttu-id="34f20-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="34f20-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="34f20-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="34f20-109">Syntax</span></span>


```CSharp
public System.String label {get;}
```


```VB

Public ReadOnly Property label As System.String
```





## <a name="property-value"></a><span data-ttu-id="34f20-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="34f20-110">Property value</span></span>

<span data-ttu-id="34f20-111">Eine **System. String** , die die Zeichenfolge der Volumebezeichnung ist.</span><span class="sxs-lookup"><span data-stu-id="34f20-111">A **System.String** that is the volume label string.</span></span>

## <a name="remarks"></a><span data-ttu-id="34f20-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="34f20-112">Remarks</span></span>

<span data-ttu-id="34f20-113">Aufgrund der Art und Weise, wie CD-Bezeichnungen gespeichert werden, ist die Bezeichnung der CD möglicherweise kürzer als die Länge der angegebenen volumezeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="34f20-113">Due to the way CD labels are stored, the label of the CD may be shorter than the length of the specified volume label string.</span></span> <span data-ttu-id="34f20-114">Wenn die Zeichenfolge länger als die maximale Länge einer CD-Bezeichnung ist, wird der Text abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="34f20-114">If the string is longer than the maximum length of a CD label, the text will be truncated.</span></span>

## <a name="requirements"></a><span data-ttu-id="34f20-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34f20-115">Requirements</span></span>



| <span data-ttu-id="34f20-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="34f20-116">Requirement</span></span> | <span data-ttu-id="34f20-117">Wert</span><span class="sxs-lookup"><span data-stu-id="34f20-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34f20-118">Version</span><span class="sxs-lookup"><span data-stu-id="34f20-118">Version</span></span><br/>   | <span data-ttu-id="34f20-119">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="34f20-119">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="34f20-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="34f20-120">Namespace</span></span><br/> | <span data-ttu-id="34f20-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="34f20-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="34f20-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="34f20-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="34f20-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="34f20-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34f20-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34f20-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34f20-125">**Iwmpcdromburn-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="34f20-125">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





